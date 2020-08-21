---
description: Saiba como a solicitação de pagamento APIenables o Microsoft Edge para atuar como intermediário entre comerciantes, consumidores e métodos de pagamento do consumidor armazenados na nuvem.
title: API de solicitação de pagamento-guia de desenvolvimento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 338940ab6f7e6bb04c6d5a8cc6ff0a198e7afbcc
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941849"
---
# <span data-ttu-id="5c040-104">API de solicitação de pagamento (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="5c040-104">Payment Request API (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="5c040-105">Este artigo descreve o fluxo de trabalho com suporte na [versão herdada do Microsoft Edge][MicrosoftSupport44533505].</span><span class="sxs-lookup"><span data-stu-id="5c040-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="5c040-106">O Microsoft Edge \ (Chromium \) dá suporte à API de solicitação de pagamento com uma implementação diferente com base no projeto Chromium.</span><span class="sxs-lookup"><span data-stu-id="5c040-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="5c040-107">As vendas de comércio eletrônico continuam crescendo em um ritmo rápido.</span><span class="sxs-lookup"><span data-stu-id="5c040-107">E-commerce sales continue growing at a rapid pace.</span></span>  <span data-ttu-id="5c040-108">De acordo com o [eMarketer](https://www.emarketer.com), por 2018, as vendas digitais são previstas para aumentar em 23% dos níveis medidos em 2013.</span><span class="sxs-lookup"><span data-stu-id="5c040-108">According to [eMarketer](https://www.emarketer.com), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="5c040-109">Embora os consumidores e as empresas aproveitem a praticidade das vendas de comércio eletrônico, ainda restam desafios.</span><span class="sxs-lookup"><span data-stu-id="5c040-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="5c040-110">Hoje, cada proprietário de site de comércio eletrônico precisa investir tempo para desenvolver fluxos de check-out e regras de validação de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="5c040-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="5c040-111">Os consumidores precisam navegar por fluxos de check-out diferentes e digitar novamente as informações de pagamento e remessa em todos os sites onde elas fazem compras.</span><span class="sxs-lookup"><span data-stu-id="5c040-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="5c040-112">Isso pode ser demorado e frustrante para os consumidores, que levam a uma taxa alta de abandono do carrinho de compras e das vendas reduzidas para comerciantes.</span><span class="sxs-lookup"><span data-stu-id="5c040-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span>  <span data-ttu-id="5c040-113">Os comerciantes [estimarem](http://baymard.com/lists/cart-abandonment-rate) entre 60% e 70% dos carrinhos de compras são abandonados.</span><span class="sxs-lookup"><span data-stu-id="5c040-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>  

<span data-ttu-id="5c040-114">A [API de solicitação de pagamento](https://w3.org/TR/payment-request) padroniza o processo de check-out do pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-114">The [Payment Request API](https://w3.org/TR/payment-request) standardizes the payment checkout process.</span></span>  <span data-ttu-id="5c040-115">Essa API requer menos personalização para desenvolvedores da Web e fornece uma experiência mais rápida, consistente e, portanto, menos confusa para os consumidores.</span><span class="sxs-lookup"><span data-stu-id="5c040-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="5c040-116">Como os consumidores podem selecionar instrumentos de pagamento e enviar endereços da conta da Microsoft, eles são necessários para inserir menos dados para concluir as compras, o que reduz o tempo e a entrada de dados necessários para concluir um pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>  

<span data-ttu-id="5c040-117">A [API de solicitação de pagamento](https://w3.org/TR/payment-request) é um padrão de navegador cruzado aberto que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento \ (como cartões de crédito \) que os consumidores armazenaram na nuvem.</span><span class="sxs-lookup"><span data-stu-id="5c040-117">The [Payment Request API](https://w3.org/TR/payment-request) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  
  
<span data-ttu-id="5c040-118">Em resumo, ao usar a [API de solicitação de pagamento](https://w3.org/TR/payment-request), os clientes fazem compras em sites de comerciante normalmente.</span><span class="sxs-lookup"><span data-stu-id="5c040-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="5c040-119">Quando estiver pronto para pagar, o website de comerciante chama a API de **solicitação de pagamento** para criar uma **solicitação de pagamento** e passa as informações de pagamento relevantes \ (como métodos de pagamento com suporte, valor de compra, moeda e assim por diante \) para o navegador.</span><span class="sxs-lookup"><span data-stu-id="5c040-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information \(such as supported payment methods, purchase amount, currency, and so on\) to the browser.</span></span>  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Construção de solicitação de pagamento" lightbox="../media/payment_request_construct.png":::
   <span data-ttu-id="5c040-121">Construção de solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-121">Payment request construct</span></span>  
:::image-end:::  

<span data-ttu-id="5c040-122">O navegador autentica o usuário, permite que o usuário selecione um método de pagamento com suporte no arquivo e processa os detalhes de pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-122">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span>  <span data-ttu-id="5c040-123">Em seguida, o navegador envia os detalhes das informações de pagamento de volta para o website de comerciante, para que o comerciante possa concluir o pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-123">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="5c040-124">Além de receber informações de pagamento, o comerciante também pode optar por receber informações de remessa como parte da **solicitação de pagamento**.</span><span class="sxs-lookup"><span data-stu-id="5c040-124">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Construção de resposta de pagamento" lightbox="../media/payment_response_construct.png":::
   <span data-ttu-id="5c040-126">Construção de resposta de pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-126">Payment response construct</span></span>  
:::image-end:::  

<span data-ttu-id="5c040-127">Para ver a API de solicitação de pagamento em ação, além de ter uma visão geral de como usá-la, confira este vídeo.</span><span class="sxs-lookup"><span data-stu-id="5c040-127">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> <span data-ttu-id="5c040-128">A API de solicitação de pagamento tem suporte no Microsoft Edge Build 14992 ou mais recente.</span><span class="sxs-lookup"><span data-stu-id="5c040-128">The Payment Request API is supported in Microsoft Edge build 14992 or newer.</span></span>  

## <span data-ttu-id="5c040-129">Criando uma solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-129">Creating a Payment Request</span></span>  

<span data-ttu-id="5c040-130">Páginas da Web crie uma **solicitação de pagamento** geralmente quando o usuário iniciar um processo de pagamento clicando no botão "comprar".</span><span class="sxs-lookup"><span data-stu-id="5c040-130">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="5c040-131">O **Payment Request** [Construtor](/previous-versions/mt790440(v=vs.85)) de solicitação de pagamento inclui methodData, detalhes e opções.</span><span class="sxs-lookup"><span data-stu-id="5c040-131">The **Payment Request** [constructor](/previous-versions/mt790440(v=vs.85)) includes methodData, details, and options.</span></span>  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

<span data-ttu-id="5c040-132">O parâmetro [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contém uma lista dos métodos de pagamento e redes aceitas pelo site e qualquer dado específico de método de pagamento associado.</span><span class="sxs-lookup"><span data-stu-id="5c040-132">The [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span>  <span data-ttu-id="5c040-133">No Microsoft Edge, essa lista é correspondida com os métodos de pagamento com suporte que o comprador salvou na conta da Microsoft e resulta na lista "pagar com" na experiência do usuário do pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-133">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="A lista pagar com na experiência do usuário de bolso da Microsoft" lightbox="../media/pay_with.png":::
         <span data-ttu-id="5c040-135">A lista **pagar com** na experiência do usuário de bolso da Microsoft</span><span class="sxs-lookup"><span data-stu-id="5c040-135">The **pay with** list in the Microsoft Wallet user experience</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var supportedInstruments = [{
          supportedMethods: ['basic-card'],
          data: {
              supportedNetworks: ['visa', 'mastercard', 'amex'],
              supportedTypes: ['credit'] 
          }         
      }]; 
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5c040-136">O parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contém informações que o comerciante deseja transmitir para o cliente sobre a transação.</span><span class="sxs-lookup"><span data-stu-id="5c040-136">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="5c040-137">Isso inclui itens de resumo do pedido, como total, imposto, valor da entrega e outros itens de nível resumido que afetam o valor do pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-137">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span>  <span data-ttu-id="5c040-138">Esses itens não devem ser pedidos de linha.</span><span class="sxs-lookup"><span data-stu-id="5c040-138">These are not intended to be order line items.</span></span>  
  
<span data-ttu-id="5c040-139">O parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) também é usado para definir as opções de envio disponíveis para o cliente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="5c040-139">The [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="5c040-140">Mais detalhes estão incluídos na seção de **pagamento** com a seção remessa abaixo.</span><span class="sxs-lookup"><span data-stu-id="5c040-140">More details are included in the **Payment Request** with Shipping section below.</span></span>  

<span data-ttu-id="5c040-141">Cada linha de [detalhe](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) inclui um rótulo para a moeda e o valor.</span><span class="sxs-lookup"><span data-stu-id="5c040-141">Each [detail](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="5c040-142">A **solicitação de pagamento** não calcula a soma ou o total desses valores.</span><span class="sxs-lookup"><span data-stu-id="5c040-142">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="5c040-143">É responsabilidade do website do comerciante para garantir que os itens de linha toquem total corretamente.</span><span class="sxs-lookup"><span data-stu-id="5c040-143">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Detalhes de subtotal, remessa, impostos e total" lightbox="../media/show_details.png":::
         <span data-ttu-id="5c040-145">Detalhes de subtotal, remessa, impostos e total</span><span class="sxs-lookup"><span data-stu-id="5c040-145">Subtotal, shipping, taxes, and total details</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var details = {
          total: {
              label: 'Total (USD)',
              amount: {currency: 'USD', value: '193.98'}
          },
          displayItems: [{
                  label: 'Subtotal',
                  amount: {currency: 'USD', value: '174.99'}
              }, {
                  label: 'Taxes',
                  amount: {currency: "USD", value: '18.99'}
          }],
      };  
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5c040-146">O [PaymentRequest](/previous-versions/mt790440(v=vs.85)) não dá suporte a reembolsos; portanto, os valores sempre devem ser positivos; itens de lista individuais podem ser negativos, como descontos.</span><span class="sxs-lookup"><span data-stu-id="5c040-146">[PaymentRequest](/previous-versions/mt790440(v=vs.85)) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span>  

<span data-ttu-id="5c040-147">O navegador renderizará os rótulos conforme você os define e renderizará automaticamente a formatação de moeda correta com base na localidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="5c040-147">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span>  <span data-ttu-id="5c040-148">Observe que os rótulos devem ser renderizados no mesmo idioma do seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5c040-148">Note that the labels should be rendered in the same language as your content.</span></span>  

<span data-ttu-id="5c040-149">O parâmetro [Options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) define os dados que a página da Web deseja retornar da **solicitação de pagamento**.</span><span class="sxs-lookup"><span data-stu-id="5c040-149">The [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span>  <span data-ttu-id="5c040-150">Isso também define os dados que precisam ser coletados, incluindo se a remessa, o endereço de email, o número de telefone ou todos forem necessários.</span><span class="sxs-lookup"><span data-stu-id="5c040-150">This also defines the data that needs to be collected, including if shipping, email address, phone number or all are required.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Lista suspensa de endereços de email" lightbox="../media/email_snippet.png":::
         <span data-ttu-id="5c040-152">Lista suspensa de endereços de email</span><span class="sxs-lookup"><span data-stu-id="5c040-152">Email address dropdown</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      var options =
          {
              requestPayerEmail: true
          }; 
      ```  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="5c040-153">Mostrando a solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-153">Showing the Payment Request</span></span>  

<span data-ttu-id="5c040-154">O método [show ()](/previous-versions/mt790448(v=vs.85)) é chamado pela página da Web para permitir que o usuário interaja com a interface do usuário de **solicitação de pagamento** .</span><span class="sxs-lookup"><span data-stu-id="5c040-154">The [show()](/previous-versions/mt790448(v=vs.85)) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="5c040-155">O método [show ()](/previous-versions/mt790448(v=vs.85)) retorna uma promessa que será resolvida quando o usuário autorizar a solicitação de pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-155">The [show()](/previous-versions/mt790448(v=vs.85)) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Confirmar e pagar detalhes" lightbox="../media/pay_screen_default.png":::
         <span data-ttu-id="5c040-157">Confirmar e pagar detalhes</span><span class="sxs-lookup"><span data-stu-id="5c040-157">Confirm and pay details</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      ```javascript
      paymentRequest.show().then(paymentInstrumentResponse => {
          paymentInstrumentResponse.complete('success').then().catch(error => {
              handlePaymentRequestError(error); 
      });
      ```  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="5c040-158">Anular uma solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-158">Aborting a Payment Request</span></span>  
 
<span data-ttu-id="5c040-159">O método [Abort ()](/previous-versions/mt790437(v=vs.85)) pode ser chamado pela página da Web a qualquer momento após o método [show ()](/previous-versions/mt790448(v=vs.85)) ser chamado, até o ponto em que a promessa está resolvida.</span><span class="sxs-lookup"><span data-stu-id="5c040-159">The [abort()](/previous-versions/mt790437(v=vs.85)) method can be called by the web page any time after the [show()](/previous-versions/mt790448(v=vs.85)) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="5c040-160">O método [Abort ()](/previous-versions/mt790437(v=vs.85)) fará com que o navegador anule a **solicitação de pagamento** e feche a interface do usuário da **solicitação de pagamento** .</span><span class="sxs-lookup"><span data-stu-id="5c040-160">The [abort()](/previous-versions/mt790437(v=vs.85)) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="5c040-161">Por exemplo, uma página da Web pode optar por anular se o usuário não concluiu a transação na quantidade de tempo necessária.</span><span class="sxs-lookup"><span data-stu-id="5c040-161">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>  

```javascript
payment.abort();
```  

## <span data-ttu-id="5c040-162">Resposta de pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-162">Payment Response</span></span>  
<span data-ttu-id="5c040-163">Quando o cliente aprova a **solicitação de pagamento**, uma **resposta de pagamento** é retornada ao site.</span><span class="sxs-lookup"><span data-stu-id="5c040-163">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span>  <span data-ttu-id="5c040-164">A **resposta de pagamento** inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5c040-164">The **Payment Response** includes the following:</span></span>  

 <span data-ttu-id="5c040-165">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5c040-165">Property</span></span>      | <span data-ttu-id="5c040-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c040-166">Description</span></span> | <span data-ttu-id="5c040-167">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5c040-167">Required</span></span> | <span data-ttu-id="5c040-168">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="5c040-168">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[<span data-ttu-id="5c040-169">methodName</span><span class="sxs-lookup"><span data-stu-id="5c040-169">methodName</span></span>](/previous-versions/mt790656(v=vs.85)) | <span data-ttu-id="5c040-170">A ID do método de pagamento selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5c040-170">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="5c040-171">Y</span><span class="sxs-lookup"><span data-stu-id="5c040-171">Y</span></span> | |   
[<span data-ttu-id="5c040-172">details</span><span class="sxs-lookup"><span data-stu-id="5c040-172">details</span></span>](/previous-versions/mt790655(v=vs.85)) | <span data-ttu-id="5c040-173">Um objeto JSON que inclui todos os dados que o comerciante exige para processar a transação usando o método de pagamento selecionado ou um token de pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-173">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="5c040-174">Y</span><span class="sxs-lookup"><span data-stu-id="5c040-174">Y</span></span> | <span data-ttu-id="5c040-175">[Cartão básico](https://w3c.github.io/payment-method-basic-card) Dicionário: titularname; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="5c040-175">[Basic Card](https://w3c.github.io/payment-method-basic-card) Dictionary:  cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> |   
[<span data-ttu-id="5c040-176">shippingAddress</span><span class="sxs-lookup"><span data-stu-id="5c040-176">shippingAddress</span></span>](/previous-versions/mt790445(v=vs.85)) | <span data-ttu-id="5c040-177">O endereço de remessa selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5c040-177">The shipping address selected by the user</span></span>  |  <span data-ttu-id="5c040-178">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5c040-178">Optional.</span></span>  <span data-ttu-id="5c040-179">Obrigatório quando o [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é</span><span class="sxs-lookup"><span data-stu-id="5c040-179">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | <span data-ttu-id="5c040-180">Dicionário de endereços: país; endereçamento; mente York dependentLocality; CEP sortingCode; languageCode; porte correspondente telefone</span><span class="sxs-lookup"><span data-stu-id="5c040-180">Address dictionary:  country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |  
[<span data-ttu-id="5c040-181">shippingOption</span><span class="sxs-lookup"><span data-stu-id="5c040-181">shippingOption</span></span>](/previous-versions/mt790446(v=vs.85)) | <span data-ttu-id="5c040-182">A ID da opção de remessa selecionada</span><span class="sxs-lookup"><span data-stu-id="5c040-182">The ID for the selected shipping option</span></span> | <span data-ttu-id="5c040-183">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5c040-183">Optional.</span></span>  <span data-ttu-id="5c040-184">Obrigatório quando o [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é</span><span class="sxs-lookup"><span data-stu-id="5c040-184">Required when [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |   
[<span data-ttu-id="5c040-185">sacador</span><span class="sxs-lookup"><span data-stu-id="5c040-185">payerName</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="5c040-186">O nome fornecido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5c040-186">The name provided by the user</span></span>  | <span data-ttu-id="5c040-187">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5c040-187">Optional.</span></span>  <span data-ttu-id="5c040-188">Obrigatório quando o [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é</span><span class="sxs-lookup"><span data-stu-id="5c040-188">Required when [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  
[<span data-ttu-id="5c040-189">payerEmail</span><span class="sxs-lookup"><span data-stu-id="5c040-189">payerEmail</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="5c040-190">O endereço de email selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5c040-190">The email address selected by the user</span></span> | <span data-ttu-id="5c040-191">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5c040-191">Optional.</span></span>  <span data-ttu-id="5c040-192">Obrigatório quando o [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é</span><span class="sxs-lookup"><span data-stu-id="5c040-192">Required when [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True`  | |  
[<span data-ttu-id="5c040-193">PayerPhone</span><span class="sxs-lookup"><span data-stu-id="5c040-193">PayerPhone</span></span>](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | <span data-ttu-id="5c040-194">O número de telefone selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="5c040-194">The phone number selected by the user</span></span> | <span data-ttu-id="5c040-195">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5c040-195">Optional.</span></span>  <span data-ttu-id="5c040-196">Obrigatório quando o [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é</span><span class="sxs-lookup"><span data-stu-id="5c040-196">Required when [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) is</span></span> `True` | |  

<span data-ttu-id="5c040-197">O objeto JSON de [detalhes](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) na **resposta de pagamento** conterá os dados de pagamento exigidos pelo comerciante para processar um pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-197">The [details](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span>  <span data-ttu-id="5c040-198">Em sua forma mais simples, a resposta será um payload de [cartão básico](https://w3c.github.io/payment-method-basic-card) contendo detalhes do cartão de pagamento de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="5c040-198">In its simplest form, the response will be a [Basic Card](https://w3c.github.io/payment-method-basic-card) payload containing cleartext payment card details.</span></span>  <span data-ttu-id="5c040-199">Quando comerciantes têm arranjos com parceiros adicionais de gateway/processador para fornecer suporte a pagamentos, o comerciante pode exigir uma carga que o processador pode manipular.</span><span class="sxs-lookup"><span data-stu-id="5c040-199">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span>  <span data-ttu-id="5c040-200">Eles podem assumir a forma de um token de processador/gateway ou um instrumento de pagamento criptografado.</span><span class="sxs-lookup"><span data-stu-id="5c040-200">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span>  <span data-ttu-id="5c040-201">Esses métodos de pagamento estão fora do escopo deste documento e serão abordados na documentação específica do processador.</span><span class="sxs-lookup"><span data-stu-id="5c040-201">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span>  <span data-ttu-id="5c040-202">Além disso, para receber uma resposta [básica de cartão](https://w3c.github.io/payment-method-basic-card) , nenhuma integração adicional à Microsoft é necessária para o desenvolvedor, diferentemente de outros métodos de pagamento específicos do processador/gateway que podem exigir a chave de criptografia ou a autorização de solicitação \ (OAuth \).</span><span class="sxs-lookup"><span data-stu-id="5c040-202">Additionally, to receive a [Basic Card](https://w3c.github.io/payment-method-basic-card) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization \(oAuth\).</span></span>  

<span data-ttu-id="5c040-203">Durante o recebimento da **resposta de pagamento**, o website envia as informações de pagamento para o processador de pagamento.</span><span class="sxs-lookup"><span data-stu-id="5c040-203">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="5c040-204">O navegador exibirá uma página Spinner enquanto o pagamento estiver sendo processado.</span><span class="sxs-lookup"><span data-stu-id="5c040-204">The browser will display a spinner page while the payment is being processed.</span></span>  

:::image type="complex" source="../media/loading_screen.png" alt-text="A página exibida quando o pagamento está sendo processado" lightbox="../media/loading_screen.png":::
   <span data-ttu-id="5c040-206">A página exibida quando o pagamento está sendo processado</span><span class="sxs-lookup"><span data-stu-id="5c040-206">The page displayed when the payment is being processed</span></span>  
:::image-end:::  

<span data-ttu-id="5c040-207">Depois que o pagamento for concluído, a página da Web chamará o método [Complete ()](/previous-versions/mt790642(v=vs.85)) e passará um valor de **êxito** ou **falhará**.</span><span class="sxs-lookup"><span data-stu-id="5c040-207">Once the payment is complete, the web page calls the [complete()](/previous-versions/mt790642(v=vs.85)) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="5c040-208">O método [Complete ()](/previous-versions/mt790642(v=vs.85)) informa ao navegador que a compra foi concluída e a tela de interface do usuário de terminação apropriada deve ser mostrada dependendo do valor de **êxito** ou **falha**.</span><span class="sxs-lookup"><span data-stu-id="5c040-208">The [complete()](/previous-versions/mt790642(v=vs.85)) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="A interface do usuário é exibida quando a compra é bem-sucedida" lightbox="../media/response_payment-request_complete.png":::
         <span data-ttu-id="5c040-210">A interface do usuário é exibida quando a compra é bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="5c040-210">The UI displayed when the purchase succeeded</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="A interface do usuário exibida quando a compra falhou" lightbox="../media/response_payment-request_failure.png":::
         <span data-ttu-id="5c040-212">A interface do usuário exibida quando a compra falhou</span><span class="sxs-lookup"><span data-stu-id="5c040-212">The UI displayed when the purchase failed</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="5c040-213">Solicitação de pagamento com remessa</span><span class="sxs-lookup"><span data-stu-id="5c040-213">Payment Request with Shipping</span></span>  

### <span data-ttu-id="5c040-214">Endereço para entrega</span><span class="sxs-lookup"><span data-stu-id="5c040-214">Shipping Address</span></span>  

<span data-ttu-id="5c040-215">Para vendas que exijam a remessa de bens físicos, é preciso um endereço de entrega.</span><span class="sxs-lookup"><span data-stu-id="5c040-215">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="5c040-216">Para incluir um endereço de remessa, defina `requestShipping = True` o parâmetro de [Opções](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) da solicitação.</span><span class="sxs-lookup"><span data-stu-id="5c040-216">To include a shipping address, set `requestShipping = True` in the [options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter of the request.</span></span>  

<span data-ttu-id="5c040-217">Quando o usuário selecionar ou atualizar o endereço de remessa, o evento [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) será executado.</span><span class="sxs-lookup"><span data-stu-id="5c040-217">When the user selects or updates the shipping address, the [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) event will run.</span></span>  <span data-ttu-id="5c040-218">O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá validar o endereço, recalcular os custos e impostos da remessa e atualizar as [remeteroptions](/previous-versions/mt790440(v=vs.85)) para refletir os custos alterados e as opções de envio disponíveis para o endereço selecionado \ (se aplicável \).</span><span class="sxs-lookup"><span data-stu-id="5c040-218">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [shippingOptions](/previous-versions/mt790440(v=vs.85)) to reflect the changed costs and shipping options available for the address selected \(if applicable\).</span></span>  

### <span data-ttu-id="5c040-219">Opções de envio</span><span class="sxs-lookup"><span data-stu-id="5c040-219">Shipping Options</span></span>  

<span data-ttu-id="5c040-220">As opções de envio podem ser apresentadas ao cliente adicionando [shippingoptions](/previous-versions/mt790440(v=vs.85)) ao parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) .</span><span class="sxs-lookup"><span data-stu-id="5c040-220">Shipping options can be presented to the customer by adding [shippingOptions](/previous-versions/mt790440(v=vs.85)) to the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="5c040-221">Um padrão pode ser estabelecido por meio da configuração de `selected = True` uma das opções de envio.</span><span class="sxs-lookup"><span data-stu-id="5c040-221">A default can be established by setting `selected = True` for one of the shipping options.</span></span>  
 
<span data-ttu-id="5c040-222">Quando o usuário seleciona ou atualiza as remessas, o evento [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) será executado.</span><span class="sxs-lookup"><span data-stu-id="5c040-222">When the user selects or updates the shippingOptions, the [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) event will run.</span></span>  <span data-ttu-id="5c040-223">O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá atualizar o parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) com o valor de remessa correto.</span><span class="sxs-lookup"><span data-stu-id="5c040-223">The website, using an event listener, will be aware of the change and can update the [details](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) parameter with the correct shipping amount.</span></span>  

```javascript
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
```  

## <span data-ttu-id="5c040-224">Referência da API</span><span class="sxs-lookup"><span data-stu-id="5c040-224">API Reference</span></span>  

[<span data-ttu-id="5c040-225">API da Solicitação de Pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-225">Payment Request API</span></span>](/previous-versions/mt790447(v=vs.85))  

## <span data-ttu-id="5c040-226">Especificada</span><span class="sxs-lookup"><span data-stu-id="5c040-226">Specification</span></span>
[<span data-ttu-id="5c040-227">API da Solicitação de Pagamento</span><span class="sxs-lookup"><span data-stu-id="5c040-227">Payment Request API</span></span>](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "O que é o Microsoft Edge herdado?"  
