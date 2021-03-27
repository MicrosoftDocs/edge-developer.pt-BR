---
description: Saiba mais sobre atualizações automáticas para extensões no Microsoft Edge
title: Extensões de atualização automática no Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 0f3f140cd3a2a079cd09f4d61e46a420342e15e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461483"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="auto-update-extensions-in-microsoft-edge"></a>Extensões de atualização automática no Microsoft Edge  

A atualização automática de extensões compartilha alguns dos mesmos benefícios que a atualização automática do Microsoft Edge:   

*   Incorporar correções de segurança e bug.  
*   Adicione novos recursos ou aprimoramentos de desempenho.  
*   Melhorar a interface do usuário.  

Anteriormente, quando eram suportadas extensões baseadas em não armazenamento, era possível atualizar os binários nativos e a extensão ao mesmo tempo.  Agora, essas extensões são hospedadas no armazenamento de Complementos do Microsoft Edge e as atualizações são feitas usando o mesmo mecanismo que o Microsoft Edge usa, que você não pode controlar.  Você deve ter cuidado ao atualizar extensões que têm uma dependência de binários nativos.  

> [!NOTE]
> Este tópico não se aplica a extensões publicadas usando o [painel do Partner Center.][MicrosoftPartnerCenter]  Você pode usar o painel para liberar versões atualizadas para seus usuários e para o armazenamento de Complementos do Microsoft Edge.

## <a name="overview"></a>Visão geral  

A cada poucas horas, o Microsoft Edge verifica se cada extensão instalada ou aplicativo tem uma URL de atualização.  As extensões podem especificar uma URL de atualização usando o campo no manifesto, que aponta para `update_url` um local para executar uma verificação de atualização.  Para cada `update_url` , ele envia solicitações para arquivos XML de manifesto atualizados.  Se o arquivo XML do manifesto de atualização listar uma versão mais recente do que a instalada, o Microsoft Edge baixará e instalará a versão mais recente.  O mesmo processo funciona para atualizações manuais, onde o novo arquivo deve ser assinado com a mesma chave privada da `.crx` versão instalada no momento.  

> [!NOTE]
> Para manter a privacidade do usuário, o Microsoft Edge não envia nenhum headers com solicitações de manifesto de atualização automática e ignora quaisquer headers nas respostas a `Cookie` `Set-Cookie` essas solicitações.  

## <a name="update-url"></a>Atualizar URL  

Se você hospedar sua própria extensão ou aplicativo, deverá adicionar o `update_url` campo ao seu `manifest.json` arquivo.  Revise o trecho de código a seguir para ver um exemplo do `update_url` .  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a>Manifesto atualizado  

O manifesto atualizado retornado pelo servidor deve ser um documento XML.  Revise o seguinte trecho de código para ver um exemplo do arquivo XML do manifesto atualizado.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

A tabela a seguir descreve atributos do arquivo XML de manifesto atualizado.  

| Atributo | Detalhes | 
|:--- |:--- |  
| `appid` | A ID da extensão é gerada com base em um hash da chave pública.  Para encontrar a ID de uma extensão, abra o Microsoft Edge e navegue até `edge://extensions` . |  
| `codebase` | Uma URL para o `.crx` arquivo. |  
| `version` | Esse valor de atributo é usado pelo Microsoft Edge para determinar se ele deve baixar o `.crx` arquivo especificado por `codebase` .  Ele deve corresponder ao valor `version` de no arquivo do `manifest.json` `.crx` arquivo. |  

O arquivo XML do manifesto de atualização pode conter informações sobre várias extensões incluindo vários elementos.  

## <a name="testing"></a>Testes  

A frequência de verificação de atualização padrão é de várias horas.  Para forçar uma atualização, navegue até `edge://extensions` e escolha o botão Atualizar **extensões agora.**  

## <a name="advanced-usage-request-parameters"></a>Uso avançado: parâmetros de solicitação  

O mecanismo básico de atualização automática é tão fácil quanto soltar um arquivo XML estático em qualquer servidor Web, como o Apache, e atualizar o arquivo XML à medida que você libera novas versões de suas extensões.  

Você pode aproveitar o fato de que os parâmetros são adicionados à solicitação de manifesto de atualização que indicam a ID de extensão e a versão. Você pode usar a mesma URL de atualização para todas as suas extensões em vez de um arquivo XML estático.  Para usar a mesma URL de atualização para todas as suas extensões, aponte para uma URL que executa código dinâmico do lado do servidor para testar esses parâmetros.  

O exemplo a seguir demonstra o formato dos parâmetros de solicitação da URL de atualização: `?x={extension_data}` .

Neste exemplo, é uma cadeia de caracteres codificada por `{extension_data}` URL que usa o seguinte formato: `id={id}&v={version}` .

Por exemplo, as duas extensões a seguir apontam para a mesma URL de `http://contoso.com/extension_updates.php` atualização.  

*  Extensão 1 - ID: "aaaaaaaaaaa" Versão: "1.1"
*  Extensão 2 - ID: "bbbbbbbb" Versão: "0,4"


A seguir estão as solicitações para atualizar cada extensão.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

Você também pode listar várias extensões em uma única solicitação para cada URL de atualização exclusiva.  O exemplo a seguir mescla as solicitações anteriores em uma única solicitação.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

Se você enviar uma única solicitação e o número de extensões instaladas que usam a mesma URL de atualização for muito longo, a atualização verificará mais `GET` solicitações.  Uma `GET` URL de solicitação é muito longa se for aproximadamente 2.000 caracteres.  

> [!NOTE]
> No futuro, uma única `POST` solicitação pode substituir várias `GET` solicitações.  A `POST` solicitação pode conter os parâmetros de solicitação no `POST` corpo.  

## <a name="advanced-usage-minimum-browser-version"></a>Uso avançado: versão mínima do navegador  

À medida que novas APIs são lançados para o sistema de extensões do Microsoft Edge, você pode lançar uma versão atualizada de sua extensão ou aplicativo que só funciona com versões mais recentes do Microsoft Edge.  Quando o Microsoft Edge é atualizado automaticamente, pode levar alguns dias até que a maioria dos usuários atualize essa nova versão.  Para garantir que uma atualização específica se aplique apenas às versões do Microsoft Edge que são atuais ou mais recentes do que uma versão específica, adicione o `prodversionmin` atributo no manifesto de atualização.  No trecho de código a seguir, o valor do atributo especifica que o aplicativo atualiza automaticamente para a versão somente quando o usuário está executando o `prodversionmin` Microsoft Edge ou mais `3.0.193.0` `2.0` `3.0.193.0` recente.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].  
> A página original é encontrada [aqui](https://developer.chrome.com/docs/apps/autoupdate/).  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
