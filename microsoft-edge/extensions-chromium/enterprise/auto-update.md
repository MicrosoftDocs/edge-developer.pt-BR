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
# <a name="auto-update-extensions-in-microsoft-edge"></a><span data-ttu-id="9792b-104">Extensões de atualização automática no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9792b-104">Auto-update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="9792b-105">A atualização automática de extensões compartilha alguns dos mesmos benefícios que a atualização automática do Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="9792b-105">Automatically updating extensions share some of the same benefits as automatically updating Microsoft Edge:</span></span>   

*   <span data-ttu-id="9792b-106">Incorporar correções de segurança e bug.</span><span class="sxs-lookup"><span data-stu-id="9792b-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="9792b-107">Adicione novos recursos ou aprimoramentos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="9792b-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="9792b-108">Melhorar a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="9792b-108">Improve the user interface.</span></span>  

<span data-ttu-id="9792b-109">Anteriormente, quando eram suportadas extensões baseadas em não armazenamento, era possível atualizar os binários nativos e a extensão ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9792b-109">Previously when non-store based extensions were supported, it was possible to update the native binaries and the extension at the same time.</span></span>  <span data-ttu-id="9792b-110">Agora, essas extensões são hospedadas no armazenamento de Complementos do Microsoft Edge e as atualizações são feitas usando o mesmo mecanismo que o Microsoft Edge usa, que você não pode controlar.</span><span class="sxs-lookup"><span data-stu-id="9792b-110">Now, those extensions are hosted in the Microsoft Edge Add-ons store and updates are made using the same mechanism that Microsoft Edge uses, which you can't control.</span></span>  <span data-ttu-id="9792b-111">Você deve ter cuidado ao atualizar extensões que têm uma dependência de binários nativos.</span><span class="sxs-lookup"><span data-stu-id="9792b-111">You should be careful when updating extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="9792b-112">Este tópico não se aplica a extensões publicadas usando o [painel do Partner Center.][MicrosoftPartnerCenter]</span><span class="sxs-lookup"><span data-stu-id="9792b-112">This topic does not apply to extensions published using the [Partner Center][MicrosoftPartnerCenter] dashboard.</span></span>  <span data-ttu-id="9792b-113">Você pode usar o painel para liberar versões atualizadas para seus usuários e para o armazenamento de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9792b-113">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>

## <a name="overview"></a><span data-ttu-id="9792b-114">Visão geral</span><span class="sxs-lookup"><span data-stu-id="9792b-114">Overview</span></span>  

<span data-ttu-id="9792b-115">A cada poucas horas, o Microsoft Edge verifica se cada extensão instalada ou aplicativo tem uma URL de atualização.</span><span class="sxs-lookup"><span data-stu-id="9792b-115">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="9792b-116">As extensões podem especificar uma URL de atualização usando o campo no manifesto, que aponta para `update_url` um local para executar uma verificação de atualização.</span><span class="sxs-lookup"><span data-stu-id="9792b-116">Extensions can specify an update URL using the `update_url` field in the manifest, which points to a location to perform an update check.</span></span>  <span data-ttu-id="9792b-117">Para cada `update_url` , ele envia solicitações para arquivos XML de manifesto atualizados.</span><span class="sxs-lookup"><span data-stu-id="9792b-117">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="9792b-118">Se o arquivo XML do manifesto de atualização listar uma versão mais recente do que a instalada, o Microsoft Edge baixará e instalará a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="9792b-118">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="9792b-119">O mesmo processo funciona para atualizações manuais, onde o novo arquivo deve ser assinado com a mesma chave privada da `.crx` versão instalada no momento.</span><span class="sxs-lookup"><span data-stu-id="9792b-119">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="9792b-120">Para manter a privacidade do usuário, o Microsoft Edge não envia nenhum headers com solicitações de manifesto de atualização automática e ignora quaisquer headers nas respostas a `Cookie` `Set-Cookie` essas solicitações.</span><span class="sxs-lookup"><span data-stu-id="9792b-120">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="9792b-121">Atualizar URL</span><span class="sxs-lookup"><span data-stu-id="9792b-121">Update URL</span></span>  

<span data-ttu-id="9792b-122">Se você hospedar sua própria extensão ou aplicativo, deverá adicionar o `update_url` campo ao seu `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="9792b-122">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="9792b-123">Revise o trecho de código a seguir para ver um exemplo do `update_url` .</span><span class="sxs-lookup"><span data-stu-id="9792b-123">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="9792b-124">Manifesto atualizado</span><span class="sxs-lookup"><span data-stu-id="9792b-124">Updated manifest</span></span>  

<span data-ttu-id="9792b-125">O manifesto atualizado retornado pelo servidor deve ser um documento XML.</span><span class="sxs-lookup"><span data-stu-id="9792b-125">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="9792b-126">Revise o seguinte trecho de código para ver um exemplo do arquivo XML do manifesto atualizado.</span><span class="sxs-lookup"><span data-stu-id="9792b-126">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="9792b-127">A tabela a seguir descreve atributos do arquivo XML de manifesto atualizado.</span><span class="sxs-lookup"><span data-stu-id="9792b-127">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="9792b-128">Atributo</span><span class="sxs-lookup"><span data-stu-id="9792b-128">Attribute</span></span> | <span data-ttu-id="9792b-129">Detalhes</span><span class="sxs-lookup"><span data-stu-id="9792b-129">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="9792b-130">A ID da extensão é gerada com base em um hash da chave pública.</span><span class="sxs-lookup"><span data-stu-id="9792b-130">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="9792b-131">Para encontrar a ID de uma extensão, abra o Microsoft Edge e navegue até `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="9792b-131">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="9792b-132">Uma URL para o `.crx` arquivo.</span><span class="sxs-lookup"><span data-stu-id="9792b-132">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="9792b-133">Esse valor de atributo é usado pelo Microsoft Edge para determinar se ele deve baixar o `.crx` arquivo especificado por `codebase` .</span><span class="sxs-lookup"><span data-stu-id="9792b-133">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="9792b-134">Ele deve corresponder ao valor `version` de no arquivo do `manifest.json` `.crx` arquivo.</span><span class="sxs-lookup"><span data-stu-id="9792b-134">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="9792b-135">O arquivo XML do manifesto de atualização pode conter informações sobre várias extensões incluindo vários elementos.</span><span class="sxs-lookup"><span data-stu-id="9792b-135">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="9792b-136">Testes</span><span class="sxs-lookup"><span data-stu-id="9792b-136">Testing</span></span>  

<span data-ttu-id="9792b-137">A frequência de verificação de atualização padrão é de várias horas.</span><span class="sxs-lookup"><span data-stu-id="9792b-137">The default update check frequency is several hours.</span></span>  <span data-ttu-id="9792b-138">Para forçar uma atualização, navegue até `edge://extensions` e escolha o botão Atualizar **extensões agora.**</span><span class="sxs-lookup"><span data-stu-id="9792b-138">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="9792b-139">Uso avançado: parâmetros de solicitação</span><span class="sxs-lookup"><span data-stu-id="9792b-139">Advanced usage: request parameters</span></span>  

<span data-ttu-id="9792b-140">O mecanismo básico de atualização automática é tão fácil quanto soltar um arquivo XML estático em qualquer servidor Web, como o Apache, e atualizar o arquivo XML à medida que você libera novas versões de suas extensões.</span><span class="sxs-lookup"><span data-stu-id="9792b-140">The basic auto-update mechanism is as easy as dropping a static XML file onto any web server such as Apache, and updating the XML file as you release new versions of your extensions.</span></span>  

<span data-ttu-id="9792b-141">Você pode aproveitar o fato de que os parâmetros são adicionados à solicitação de manifesto de atualização que indicam a ID de extensão e a versão.</span><span class="sxs-lookup"><span data-stu-id="9792b-141">You may take advantage of the fact that parameters are added to the update manifest request that indicate the extension ID and version.</span></span> <span data-ttu-id="9792b-142">Você pode usar a mesma URL de atualização para todas as suas extensões em vez de um arquivo XML estático.</span><span class="sxs-lookup"><span data-stu-id="9792b-142">You can use the same update URL for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="9792b-143">Para usar a mesma URL de atualização para todas as suas extensões, aponte para uma URL que executa código dinâmico do lado do servidor para testar esses parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9792b-143">To use the same update URL for all your extensions, point to a URL that runs dynamic server-side code to test these parameters.</span></span>  

<span data-ttu-id="9792b-144">O exemplo a seguir demonstra o formato dos parâmetros de solicitação da URL de atualização: `?x={extension_data}` .</span><span class="sxs-lookup"><span data-stu-id="9792b-144">The following example demonstrates the format of the request parameters of update URL: `?x={extension_data}`.</span></span>

<span data-ttu-id="9792b-145">Neste exemplo, é uma cadeia de caracteres codificada por `{extension_data}` URL que usa o seguinte formato: `id={id}&v={version}` .</span><span class="sxs-lookup"><span data-stu-id="9792b-145">In this example, `{extension_data}` is a URL-encoded string that uses the following format: `id={id}&v={version}`.</span></span>

<span data-ttu-id="9792b-146">Por exemplo, as duas extensões a seguir apontam para a mesma URL de `http://contoso.com/extension_updates.php` atualização.</span><span class="sxs-lookup"><span data-stu-id="9792b-146">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*  <span data-ttu-id="9792b-147">Extensão 1 - ID: "aaaaaaaaaaa" Versão: "1.1"</span><span class="sxs-lookup"><span data-stu-id="9792b-147">Extension 1 - ID: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa" Version: "1.1"</span></span>
*  <span data-ttu-id="9792b-148">Extensão 2 - ID: "bbbbbbbb" Versão: "0,4"</span><span class="sxs-lookup"><span data-stu-id="9792b-148">Extension 2 - ID: "bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb" Version: "0.4"</span></span>


<span data-ttu-id="9792b-149">A seguir estão as solicitações para atualizar cada extensão.</span><span class="sxs-lookup"><span data-stu-id="9792b-149">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="9792b-150">Você também pode listar várias extensões em uma única solicitação para cada URL de atualização exclusiva.</span><span class="sxs-lookup"><span data-stu-id="9792b-150">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="9792b-151">O exemplo a seguir mescla as solicitações anteriores em uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="9792b-151">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="9792b-152">Se você enviar uma única solicitação e o número de extensões instaladas que usam a mesma URL de atualização for muito longo, a atualização verificará mais `GET` solicitações.</span><span class="sxs-lookup"><span data-stu-id="9792b-152">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="9792b-153">Uma `GET` URL de solicitação é muito longa se for aproximadamente 2.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="9792b-153">A `GET` request URL is too long if it is approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="9792b-154">No futuro, uma única `POST` solicitação pode substituir várias `GET` solicitações.</span><span class="sxs-lookup"><span data-stu-id="9792b-154">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="9792b-155">A `POST` solicitação pode conter os parâmetros de solicitação no `POST` corpo.</span><span class="sxs-lookup"><span data-stu-id="9792b-155">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="9792b-156">Uso avançado: versão mínima do navegador</span><span class="sxs-lookup"><span data-stu-id="9792b-156">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="9792b-157">À medida que novas APIs são lançados para o sistema de extensões do Microsoft Edge, você pode lançar uma versão atualizada de sua extensão ou aplicativo que só funciona com versões mais recentes do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9792b-157">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="9792b-158">Quando o Microsoft Edge é atualizado automaticamente, pode levar alguns dias até que a maioria dos usuários atualize essa nova versão.</span><span class="sxs-lookup"><span data-stu-id="9792b-158">When Microsoft Edge is auto-updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="9792b-159">Para garantir que uma atualização específica se aplique apenas às versões do Microsoft Edge que são atuais ou mais recentes do que uma versão específica, adicione o `prodversionmin` atributo no manifesto de atualização.</span><span class="sxs-lookup"><span data-stu-id="9792b-159">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="9792b-160">No trecho de código a seguir, o valor do atributo especifica que o aplicativo atualiza automaticamente para a versão somente quando o usuário está executando o `prodversionmin` Microsoft Edge ou mais `3.0.193.0` `2.0` `3.0.193.0` recente.</span><span class="sxs-lookup"><span data-stu-id="9792b-160">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app auto-updates to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

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
> <span data-ttu-id="9792b-162">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9792b-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9792b-163">A página original é encontrada [aqui](https://developer.chrome.com/docs/apps/autoupdate/).</span><span class="sxs-lookup"><span data-stu-id="9792b-163">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate/).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9792b-165">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9792b-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
