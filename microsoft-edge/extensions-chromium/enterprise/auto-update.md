---
description: Saiba mais sobre atualizações automáticas para extensões no Microsoft Edge
title: Atualizar extensões automaticamente no Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desenvolvimento de extensões, extensões de navegador, complementos, partner center, desenvolvedor
ms.openlocfilehash: 74d7b61c8eca1155b545b7e81627a652bf336e66
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483069"
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
# <a name="automatically-update-extensions-in-microsoft-edge"></a><span data-ttu-id="51335-104">Atualizar extensões automaticamente no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="51335-104">Automatically update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="51335-105">Quando você definir sua extensão para atualizar automaticamente, sua extensão compartilhará os seguintes benefícios com o Microsoft Edge quando definida para atualização automática.</span><span class="sxs-lookup"><span data-stu-id="51335-105">When you set your extension to automatically update, your extension shares the following benefits with Microsoft Edge when set to automatically update.</span></span>  

*   <span data-ttu-id="51335-106">Incorporar correções de segurança e bug.</span><span class="sxs-lookup"><span data-stu-id="51335-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="51335-107">Adicione novos recursos ou aprimoramentos de desempenho.</span><span class="sxs-lookup"><span data-stu-id="51335-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="51335-108">Melhorar a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="51335-108">Improve the user interface.</span></span>  

<span data-ttu-id="51335-109">Anteriormente, extensões baseadas em não armazenamento eram suportadas.</span><span class="sxs-lookup"><span data-stu-id="51335-109">Previously, non-store based extensions were supported.</span></span>  <span data-ttu-id="51335-110">Além disso, você atualizou os binários nativos e a extensão ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="51335-110">Also, you updated the native binaries and the extension at the same time.</span></span>  

<span data-ttu-id="51335-111">Agora, o armazenamento de Complementos do Microsoft Edge hospeda suas extensões e você atualiza sua extensão usando o mesmo mecanismo que o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="51335-111">Now, the Microsoft Edge Add-ons store hosts your extensions and you update your extension using the same mechanism as Microsoft Edge.</span></span>  <span data-ttu-id="51335-112">Você não controla o mecanismo de atualização.</span><span class="sxs-lookup"><span data-stu-id="51335-112">You don't control the update mechanism.</span></span>  <span data-ttu-id="51335-113">Tenha cuidado ao atualizar extensões que têm uma dependência de binários nativos.</span><span class="sxs-lookup"><span data-stu-id="51335-113">Be careful when you update extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="51335-114">Este artigo não se aplica às extensões que você publica usando o [painel do Partner Center.][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]</span><span class="sxs-lookup"><span data-stu-id="51335-114">This article does not apply to extensions that you publish using the [Partner Center][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] dashboard.</span></span>  <span data-ttu-id="51335-115">Você pode usar o painel para liberar versões atualizadas para seus usuários e para o armazenamento de Complementos do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="51335-115">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="51335-116">Para obter mais informações, navegue [até Atualizar ou remova sua extensão][ExtensionsPublishUpdateExtension].</span><span class="sxs-lookup"><span data-stu-id="51335-116">For more information, navigate to [Update or remove your extension][ExtensionsPublishUpdateExtension].</span></span>  

## <a name="overview"></a><span data-ttu-id="51335-117">Visão geral</span><span class="sxs-lookup"><span data-stu-id="51335-117">Overview</span></span>  

<span data-ttu-id="51335-118">A cada poucas horas, o Microsoft Edge verifica se cada extensão instalada ou aplicativo tem uma URL de atualização.</span><span class="sxs-lookup"><span data-stu-id="51335-118">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="51335-119">Para especificar uma URL de atualização para sua extensão, use `update_url` o campo no manifesto.</span><span class="sxs-lookup"><span data-stu-id="51335-119">To specify an update URL for your extension, use the `update_url` field in the manifest.</span></span>  <span data-ttu-id="51335-120">O `update_url` campo no manifesto aponta para um local para concluir uma verificação de atualização.</span><span class="sxs-lookup"><span data-stu-id="51335-120">The `update_url` field in the manifest points to a location to complete an update check.</span></span>  <span data-ttu-id="51335-121">Para cada `update_url` , ele envia solicitações para arquivos XML de manifesto atualizados.</span><span class="sxs-lookup"><span data-stu-id="51335-121">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="51335-122">Se o arquivo XML do manifesto de atualização listar uma versão mais recente do que a instalada, o Microsoft Edge baixará e instalará a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="51335-122">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="51335-123">O mesmo processo funciona para atualizações manuais, onde o novo arquivo deve ser assinado com a mesma chave privada da `.crx` versão instalada no momento.</span><span class="sxs-lookup"><span data-stu-id="51335-123">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="51335-124">Para manter a privacidade do usuário, o Microsoft Edge não envia nenhum headers com solicitações de manifesto de atualização automática e ignora quaisquer headers nas respostas a `Cookie` `Set-Cookie` essas solicitações.</span><span class="sxs-lookup"><span data-stu-id="51335-124">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="51335-125">Atualizar URL</span><span class="sxs-lookup"><span data-stu-id="51335-125">Update URL</span></span>  

<span data-ttu-id="51335-126">Se você hospedar sua própria extensão ou aplicativo, deverá adicionar o `update_url` campo ao seu `manifest.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="51335-126">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="51335-127">Revise o trecho de código a seguir para ver um exemplo do `update_url` .</span><span class="sxs-lookup"><span data-stu-id="51335-127">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="51335-128">Manifesto atualizado</span><span class="sxs-lookup"><span data-stu-id="51335-128">Updated manifest</span></span>  

<span data-ttu-id="51335-129">O manifesto atualizado retornado pelo servidor deve ser um documento XML.</span><span class="sxs-lookup"><span data-stu-id="51335-129">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="51335-130">Revise o seguinte trecho de código para ver um exemplo do arquivo XML do manifesto atualizado.</span><span class="sxs-lookup"><span data-stu-id="51335-130">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="51335-131">A tabela a seguir descreve atributos do arquivo XML de manifesto atualizado.</span><span class="sxs-lookup"><span data-stu-id="51335-131">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="51335-132">Atributo</span><span class="sxs-lookup"><span data-stu-id="51335-132">Attribute</span></span> | <span data-ttu-id="51335-133">Detalhes</span><span class="sxs-lookup"><span data-stu-id="51335-133">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="51335-134">A ID da extensão é gerada com base em um hash da chave pública.</span><span class="sxs-lookup"><span data-stu-id="51335-134">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="51335-135">Para encontrar a ID de uma extensão, abra o Microsoft Edge e navegue até `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="51335-135">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="51335-136">Uma URL para o `.crx` arquivo.</span><span class="sxs-lookup"><span data-stu-id="51335-136">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="51335-137">Esse valor de atributo é usado pelo Microsoft Edge para determinar se ele deve baixar o `.crx` arquivo especificado por `codebase` .</span><span class="sxs-lookup"><span data-stu-id="51335-137">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="51335-138">Ele deve corresponder ao valor `version` de no arquivo do `manifest.json` `.crx` arquivo.</span><span class="sxs-lookup"><span data-stu-id="51335-138">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="51335-139">O arquivo XML do manifesto de atualização pode conter informações sobre várias extensões incluindo vários elementos.</span><span class="sxs-lookup"><span data-stu-id="51335-139">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="51335-140">Testes</span><span class="sxs-lookup"><span data-stu-id="51335-140">Testing</span></span>  

<span data-ttu-id="51335-141">A frequência de verificação de atualização padrão é de várias horas.</span><span class="sxs-lookup"><span data-stu-id="51335-141">The default update check frequency is several hours.</span></span>  <span data-ttu-id="51335-142">Para forçar uma atualização, navegue até `edge://extensions` e escolha o botão Atualizar **extensões agora.**</span><span class="sxs-lookup"><span data-stu-id="51335-142">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="51335-143">Uso avançado: parâmetros de solicitação</span><span class="sxs-lookup"><span data-stu-id="51335-143">Advanced usage: request parameters</span></span>  

<span data-ttu-id="51335-144">O mecanismo básico é simples.</span><span class="sxs-lookup"><span data-stu-id="51335-144">The basic mechanism is simple.</span></span>  <span data-ttu-id="51335-145">Para atualizar automaticamente sua extensão, conclua as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="51335-145">To automatically update your extension, complete the following actions.</span></span>  

1.  <span data-ttu-id="51335-146">Carregue seu arquivo XML estático em seu servidor Web, como o Apache.</span><span class="sxs-lookup"><span data-stu-id="51335-146">Upload your static XML file on your web server, such as Apache.</span></span>  
1.  <span data-ttu-id="51335-147">Atualize o arquivo XML à medida que você lança novas versões de suas extensões.</span><span class="sxs-lookup"><span data-stu-id="51335-147">Update the XML file as you release new versions of your extensions.</span></span>  
    
<span data-ttu-id="51335-148">Aproveite o fato de que alguns parâmetros adicionados à solicitação de manifesto de atualização indicam a extensão `ID` e `version` .</span><span class="sxs-lookup"><span data-stu-id="51335-148">Take advantage of the fact that some parameters added to the update manifest request indicate the extension `ID` and `version`.</span></span>  <span data-ttu-id="51335-149">Você pode usar o mesmo `update URL` para todas as suas extensões em vez de um arquivo XML estático.</span><span class="sxs-lookup"><span data-stu-id="51335-149">You may use the same `update URL` for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="51335-150">Para usar o mesmo para todas as extensões, aponte para uma URL que executa código dinâmico do lado do `update URL` servidor para testar os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="51335-150">To use the same `update URL` for all your extensions, point to a URL that runs dynamic server-side code to test the parameters.</span></span>  

<span data-ttu-id="51335-151">O exemplo a seguir demonstra o formato dos parâmetros de solicitação da URL de atualização.</span><span class="sxs-lookup"><span data-stu-id="51335-151">The following example demonstrates the format of the request parameters of update URL.</span></span>  

```url
?x={extension_data}
```  

<span data-ttu-id="51335-152">Neste exemplo, `{extension_data}` é uma cadeia de caracteres codificada por URL que usa o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="51335-152">In this example, `{extension_data}` is a URL-encoded string that uses the following format.</span></span>  

```url
id={id}&v={version}
```  

<span data-ttu-id="51335-153">Por exemplo, as duas extensões a seguir apontam para a mesma URL de `http://contoso.com/extension_updates.php` atualização.</span><span class="sxs-lookup"><span data-stu-id="51335-153">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*   <span data-ttu-id="51335-154">Extensão 1</span><span class="sxs-lookup"><span data-stu-id="51335-154">Extension 1</span></span>  
    *   <span data-ttu-id="51335-155">ID:</span><span class="sxs-lookup"><span data-stu-id="51335-155">ID:</span></span> `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
    *   <span data-ttu-id="51335-156">URL de atualização:</span><span class="sxs-lookup"><span data-stu-id="51335-156">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="51335-157">Versão:</span><span class="sxs-lookup"><span data-stu-id="51335-157">Version:</span></span> `1.1`  
*   <span data-ttu-id="51335-158">Extensão 2</span><span class="sxs-lookup"><span data-stu-id="51335-158">Extension 2</span></span>  
    *   <span data-ttu-id="51335-159">ID:</span><span class="sxs-lookup"><span data-stu-id="51335-159">ID:</span></span> `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb`  
    *   <span data-ttu-id="51335-160">URL de atualização:</span><span class="sxs-lookup"><span data-stu-id="51335-160">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="51335-161">Versão:</span><span class="sxs-lookup"><span data-stu-id="51335-161">Version:</span></span> `0.4`  


<span data-ttu-id="51335-162">A seguir estão as solicitações para atualizar cada extensão.</span><span class="sxs-lookup"><span data-stu-id="51335-162">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="51335-163">Você também pode listar várias extensões em uma única solicitação para cada URL de atualização exclusiva.</span><span class="sxs-lookup"><span data-stu-id="51335-163">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="51335-164">O exemplo a seguir mescla as solicitações anteriores em uma única solicitação.</span><span class="sxs-lookup"><span data-stu-id="51335-164">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="51335-165">Se você enviar uma única solicitação e o número de extensões instaladas que usam a mesma URL de atualização for muito longo, a atualização verificará mais `GET` solicitações.</span><span class="sxs-lookup"><span data-stu-id="51335-165">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="51335-166">Uma `GET` URL de solicitação é muito longa se for aproximadamente 2.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="51335-166">A `GET` request URL is too long if it's approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="51335-167">No futuro, uma única `POST` solicitação pode substituir várias `GET` solicitações.</span><span class="sxs-lookup"><span data-stu-id="51335-167">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="51335-168">A `POST` solicitação pode conter os parâmetros de solicitação no `POST` corpo.</span><span class="sxs-lookup"><span data-stu-id="51335-168">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="51335-169">Uso avançado: versão mínima do navegador</span><span class="sxs-lookup"><span data-stu-id="51335-169">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="51335-170">À medida que novas APIs são lançados para o sistema de extensões do Microsoft Edge, você pode lançar uma versão atualizada de sua extensão ou aplicativo que só funciona com versões mais recentes do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="51335-170">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="51335-171">Quando o Microsoft Edge é atualizado automaticamente, pode levar alguns dias até que a maioria dos usuários atualize essa nova versão.</span><span class="sxs-lookup"><span data-stu-id="51335-171">When Microsoft Edge is automatically updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="51335-172">Para garantir que uma atualização específica se aplique apenas às versões do Microsoft Edge que são atuais ou mais recentes do que uma versão específica, adicione o `prodversionmin` atributo no manifesto de atualização.</span><span class="sxs-lookup"><span data-stu-id="51335-172">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="51335-173">No trecho de código a seguir, o valor do atributo especifica que seu aplicativo foi atualizado automaticamente para a versão somente quando o usuário estiver executando o `prodversionmin` Microsoft Edge ou mais `3.0.193.0` `2.0` `3.0.193.0` recente.</span><span class="sxs-lookup"><span data-stu-id="51335-173">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app automatically updated to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[ExtensionsPublishUpdateExtension]: ../publish/update-extension.md "Atualizar ou remover a extensão | Microsoft Docs"  

[MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Partner Center"  

> [!NOTE]
> <span data-ttu-id="51335-176">Partes desta página são modificações baseadas no trabalho criado e [compartilhado pelo Google][GoogleSitePolicies] e usadas de acordo com os termos descritos na [Licença Pública Creative Commons Atribuição 4.0 Internacional][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51335-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="51335-177">A página original é encontrada [aqui](https://developer.chrome.com/docs/apps/autoupdate).</span><span class="sxs-lookup"><span data-stu-id="51335-177">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate).</span></span>  

[![Licença Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="51335-179">Esse trabalho é licenciado sob uma [Licença Attribution 4.0 International da Creative Commons][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51335-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
