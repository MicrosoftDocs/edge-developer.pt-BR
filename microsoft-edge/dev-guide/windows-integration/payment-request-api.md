---
description: Saiba como a solicitação de pagamento APIenables o Microsoft Edge para atuar como intermediário entre comerciantes, consumidores e métodos de pagamento do consumidor armazenados na nuvem.
title: Guia de desenvolvimento-API de solicitação de pagamento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: b082e311dcbe5cff3101f084e7ff2c145e6e83df
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902861"
---
# <span data-ttu-id="ab3ec-104">API de solicitação de pagamento (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="ab3ec-104">Payment Request API (EdgeHTML)</span></span>

> [!NOTE]
> <span data-ttu-id="ab3ec-105">Este artigo descreve o fluxo de trabalho com suporte na [versão herdada do Microsoft Edge][MicrosoftSupport44533505].</span><span class="sxs-lookup"><span data-stu-id="ab3ec-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="ab3ec-106">O Microsoft Edge \ (Chromium \) dá suporte à API de solicitação de pagamento com uma implementação diferente com base no projeto Chromium.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="ab3ec-107">As vendas de comércio eletrônico continuam crescendo em um ritmo rápido.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-107">E-commerce sales continue growing at a rapid pace.</span></span> <span data-ttu-id="ab3ec-108">De acordo com o [eMarketer](https://www.emarketer.com/), por 2018, as vendas digitais são previstas para aumentar em 23% dos níveis medidos em 2013.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-108">According to [eMarketer](https://www.emarketer.com/), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="ab3ec-109">Embora os consumidores e as empresas aproveitem a praticidade das vendas de comércio eletrônico, ainda restam desafios.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="ab3ec-110">Hoje, cada proprietário de site de comércio eletrônico precisa investir tempo para desenvolver fluxos de check-out e regras de validação de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="ab3ec-111">Os consumidores precisam navegar por fluxos de check-out diferentes e digitar novamente as informações de pagamento e remessa em todos os sites onde elas fazem compras.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="ab3ec-112">Isso pode ser demorado e frustrante para os consumidores, que levam a uma taxa alta de abandono do carrinho de compras e das vendas reduzidas para comerciantes.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span> <span data-ttu-id="ab3ec-113">Os comerciantes [estimarem](http://baymard.com/lists/cart-abandonment-rate) entre 60% e 70% dos carrinhos de compras são abandonados.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>      

<span data-ttu-id="ab3ec-114">A [API de solicitação de pagamento](https://w3.org/TR/payment-request/) padroniza o processo de check-out do pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-114">The [Payment Request API](https://w3.org/TR/payment-request/) standardizes the payment checkout process.</span></span> <span data-ttu-id="ab3ec-115">Essa API requer menos personalização para desenvolvedores da Web e fornece uma experiência mais rápida, consistente e, portanto, menos confusa para os consumidores.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="ab3ec-116">Como os consumidores podem selecionar instrumentos de pagamento e enviar endereços da conta da Microsoft, eles são necessários para inserir menos dados para concluir as compras, o que reduz o tempo e a entrada de dados necessários para concluir um pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>   

<span data-ttu-id="ab3ec-117">A [API de solicitação de pagamento](https://w3.org/TR/payment-request/) é um padrão aberto e de navegador cruzado que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento (por exemplo, cartões de crédito) que os consumidores armazenaram na nuvem.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-117">The [Payment Request API](https://w3.org/TR/payment-request/) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods (e.g. credit cards) that consumers have stored in the cloud.</span></span> 
  
<span data-ttu-id="ab3ec-118">Em resumo, ao usar a [API de solicitação de pagamento](https://w3.org/TR/payment-request/), os clientes fazem compras em sites de comerciante normalmente.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request/), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="ab3ec-119">Quando estiver pronto para pagar, o website de comerciante chamará a API de **solicitação de pagamento** para criar uma **solicitação de pagamento** e passar as informações de pagamento relevantes (por exemplo, os métodos de pagamento, o valor de compra, a moeda, etc.) para o navegador.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information (e.g. supported payment methods, purchase amount, currency, etc.) to the browser.</span></span>

![Construção de solicitação de pagamento](./../media/payment_request_construct.png)

<span data-ttu-id="ab3ec-121">O navegador autentica o usuário, permite que o usuário selecione um método de pagamento com suporte no arquivo e processa os detalhes de pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-121">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span> <span data-ttu-id="ab3ec-122">Em seguida, o navegador envia os detalhes das informações de pagamento de volta para o website de comerciante, para que o comerciante possa concluir o pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-122">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="ab3ec-123">Além de receber informações de pagamento, o comerciante também pode optar por receber informações de remessa como parte da **solicitação de pagamento**.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-123">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

![Construção de resposta de pagamento](./../media/payment_response_construct.png)

<span data-ttu-id="ab3ec-125">Para ver a API de solicitação de pagamento em ação, além de ter uma visão geral de como usá-la, confira este vídeo.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-125">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> <span data-ttu-id="ab3ec-126">A API de solicitação de pagamento tem suporte no Microsoft Edge Build 14992 +.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-126">The Payment Request API is supported in Microsoft Edge build 14992+.</span></span>


## <span data-ttu-id="ab3ec-127">Criando uma solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-127">Creating a Payment Request</span></span> 
<span data-ttu-id="ab3ec-128">Páginas da Web crie uma **solicitação de pagamento** geralmente quando o usuário iniciar um processo de pagamento clicando no botão "comprar".</span><span class="sxs-lookup"><span data-stu-id="ab3ec-128">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="ab3ec-129">O **Payment Request** [Construtor](https://msdn.microsoft.com/library/mt790440) de solicitação de pagamento inclui methodData, detalhes e opções.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-129">The **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) includes methodData, details, and options.</span></span> 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

<span data-ttu-id="ab3ec-130">O [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro contém uma lista dos métodos de pagamento e redes aceitas pelo site e qualquer dado específico do método de pagamento associado.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-130">The [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span> <span data-ttu-id="ab3ec-131">No Microsoft Edge, essa lista é correspondida com os métodos de pagamento com suporte que o comprador salvou na conta da Microsoft e resulta na lista "pagar com" na experiência do usuário do pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-131">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>

![A lista "pagar com" na experiência de usuário da Microsoft carteira](./../media/pay_with.png)

```js
var supportedInstruments = [{
    supportedMethods: ['basic-card'],
    data: {
        supportedNetworks: ['visa', 'mastercard', 'amex'],
        supportedTypes: ['credit'] 
    }         
}]; 
```

<span data-ttu-id="ab3ec-133">O [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro contém informações que o comerciante deseja transmitir para o cliente sobre a transação.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-133">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="ab3ec-134">Isso inclui itens de resumo do pedido, como total, imposto, valor da entrega e outros itens de nível resumido que afetam o valor do pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-134">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span> <span data-ttu-id="ab3ec-135">Esses itens não devem ser pedidos de linha.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-135">These are not intended to be order line items.</span></span> 
  
<span data-ttu-id="ab3ec-136">O [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro também é usado para definir as opções de envio disponíveis para o cliente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-136">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="ab3ec-137">Mais detalhes estão incluídos na seção de **pagamento** com a seção remessa abaixo.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-137">More details are included in the **Payment Request** with Shipping section below.</span></span> 

<span data-ttu-id="ab3ec-138">Cada [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) linha inclui um rótulo para a moeda e o valor.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-138">Each [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="ab3ec-139">A **solicitação de pagamento** não calcula a soma ou o total desses valores.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-139">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="ab3ec-140">É responsabilidade do website do comerciante para garantir que os itens de linha toquem total corretamente.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-140">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>   


![Detalhes de subtotal, remessa, impostos e total](./../media/show_details.png)

```js
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

<span data-ttu-id="ab3ec-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)não oferece suporte a reembolsos; portanto, os valores sempre devem ser positivos; itens de lista individuais podem ser negativos, como descontos.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span> 

<span data-ttu-id="ab3ec-143">O navegador renderizará os rótulos conforme você os define e renderizará automaticamente a formatação de moeda correta com base na localidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-143">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span> <span data-ttu-id="ab3ec-144">Observe que os rótulos devem ser renderizados no mesmo idioma do seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-144">Note that the labels should be rendered in the same language as your content.</span></span> 

<span data-ttu-id="ab3ec-145">O [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro define os dados que a página da Web deseja retornar da **solicitação de pagamento**.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-145">The [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span> <span data-ttu-id="ab3ec-146">Isso também define os dados que precisam ser coletados, incluindo se a remessa, o endereço de email e/ou o número de telefone são necessários.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-146">This also defines the data that needs to be collected, including if shipping, email address, and/or phone number are required.</span></span>

![Lista suspensa de endereços de email](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## <span data-ttu-id="ab3ec-148">Mostrando a solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-148">Showing the Payment Request</span></span>

<span data-ttu-id="ab3ec-149">O [`show()`](https://msdn.microsoft.com/library/mt790448) método é chamado pela página da Web para permitir que o usuário interaja com a interface do usuário para **solicitação de pagamento** .</span><span class="sxs-lookup"><span data-stu-id="ab3ec-149">The [`show()`](https://msdn.microsoft.com/library/mt790448) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="ab3ec-150">O [`show()`](https://msdn.microsoft.com/library/mt790448) método retorna uma promessa que será resolvida quando o usuário autorizar a solicitação de pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-150">The [`show()`](https://msdn.microsoft.com/library/mt790448) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Confirmar e pagar detalhes](./../media/pay_screen_default.png)

## <span data-ttu-id="ab3ec-152">Anular uma solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-152">Aborting a Payment Request</span></span>
 
<span data-ttu-id="ab3ec-153">O [`abort()`](https://msdn.microsoft.com/library/mt790437) método pode ser chamado pela página da Web a qualquer momento após o [`show()`](https://msdn.microsoft.com/library/mt790448) método ser chamado, até o ponto em que a promessa está resolvida.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-153">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method can be called by the web page any time after the [`show()`](https://msdn.microsoft.com/library/mt790448) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="ab3ec-154">O [`abort()`](https://msdn.microsoft.com/library/mt790437) método fará com que o navegador anule a **solicitação de pagamento** e feche a interface do usuário da **solicitação de pagamento** .</span><span class="sxs-lookup"><span data-stu-id="ab3ec-154">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="ab3ec-155">Por exemplo, uma página da Web pode optar por anular se o usuário não concluiu a transação na quantidade de tempo necessária.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-155">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>

```js
payment.abort();
``` 

## <span data-ttu-id="ab3ec-156">Resposta de pagamento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-156">Payment Response</span></span>
<span data-ttu-id="ab3ec-157">Quando o cliente aprova a **solicitação de pagamento**, uma **resposta de pagamento** é retornada ao site.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-157">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span> <span data-ttu-id="ab3ec-158">A **resposta de pagamento** inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ab3ec-158">The **Payment Response** includes the following:</span></span> 

 <span data-ttu-id="ab3ec-159">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ab3ec-159">Property</span></span>      | <span data-ttu-id="ab3ec-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab3ec-160">Description</span></span> | <span data-ttu-id="ab3ec-161">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ab3ec-161">Required</span></span> | <span data-ttu-id="ab3ec-162">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="ab3ec-162">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | <span data-ttu-id="ab3ec-163">A ID do método de pagamento selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="ab3ec-163">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="ab3ec-164">Y</span><span class="sxs-lookup"><span data-stu-id="ab3ec-164">Y</span></span> | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | <span data-ttu-id="ab3ec-165">Um objeto JSON que inclui todos os dados que o comerciante exige para processar a transação usando o método de pagamento selecionado ou um token de pagamento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-165">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="ab3ec-166">Y</span><span class="sxs-lookup"><span data-stu-id="ab3ec-166">Y</span></span> | <span data-ttu-id="ab3ec-167">[Cartão básico](https://go.microsoft.com/fwlink/?linkid=834965) Dicionário: titularname; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="ab3ec-167">[Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | <span data-ttu-id="ab3ec-168">O endereço de remessa selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="ab3ec-168">The shipping address selected by the user</span></span>  |  <span data-ttu-id="ab3ec-169">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-169">Optional.</span></span> <span data-ttu-id="ab3ec-170">Obrigatório quando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="ab3ec-170">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | <span data-ttu-id="ab3ec-171">Dicionário de endereços: país; endereçamento; mente York dependentLocality; CEP sortingCode; languageCode; porte correspondente telefone</span><span class="sxs-lookup"><span data-stu-id="ab3ec-171">Address dictionary: country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | <span data-ttu-id="ab3ec-172">A ID da opção de remessa selecionada</span><span class="sxs-lookup"><span data-stu-id="ab3ec-172">The ID for the selected shipping option</span></span> | <span data-ttu-id="ab3ec-173">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-173">Optional.</span></span> <span data-ttu-id="ab3ec-174">Obrigatório quando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="ab3ec-174">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="ab3ec-175">O nome fornecido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="ab3ec-175">The name provided by the user</span></span>  | <span data-ttu-id="ab3ec-176">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-176">Optional.</span></span> <span data-ttu-id="ab3ec-177">Obrigatório quando [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="ab3ec-177">Required when [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="ab3ec-178">O endereço de email selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="ab3ec-178">The email address selected by the user</span></span> | <span data-ttu-id="ab3ec-179">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-179">Optional.</span></span> <span data-ttu-id="ab3ec-180">Obrigatório quando [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="ab3ec-180">Required when [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="ab3ec-181">O número de telefone selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="ab3ec-181">The phone number selected by the user</span></span> | <span data-ttu-id="ab3ec-182">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-182">Optional.</span></span> <span data-ttu-id="ab3ec-183">Obrigatório quando [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="ab3ec-183">Required when [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |

<span data-ttu-id="ab3ec-184">O [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) objeto JSON na **resposta de pagamento** conterá os dados de pagamento exigidos pelo comerciante para processar um pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-184">The [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span> <span data-ttu-id="ab3ec-185">Em sua forma mais simples, a resposta será um payload de [cartão básico](https://go.microsoft.com/fwlink/?linkid=834965) contendo detalhes do cartão de pagamento de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-185">In its simplest form, the response will be a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) payload containing cleartext payment card details.</span></span> <span data-ttu-id="ab3ec-186">Quando comerciantes têm arranjos com parceiros adicionais de gateway/processador para fornecer suporte a pagamentos, o comerciante pode exigir uma carga que o processador pode manipular.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-186">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span> <span data-ttu-id="ab3ec-187">Eles podem assumir a forma de um token de processador/gateway ou um instrumento de pagamento criptografado.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-187">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span> <span data-ttu-id="ab3ec-188">Esses métodos de pagamento estão fora do escopo deste documento e serão abordados na documentação específica do processador.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-188">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span> <span data-ttu-id="ab3ec-189">Além disso, para receber uma resposta [básica de cartão](https://go.microsoft.com/fwlink/?linkid=834965) , não há necessidade de integração adicional à Microsoft para o desenvolvedor, diferentemente de outros métodos de pagamento específicos do processador/gateway que podem exigir a chave de criptografia ou a autorização de solicitação (OAuth).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-189">Additionally, to receive a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization (oauth).</span></span> 

<span data-ttu-id="ab3ec-190">Durante o recebimento da **resposta de pagamento**, o website envia as informações de pagamento para o processador de pagamento.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-190">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="ab3ec-191">O navegador exibirá uma página Spinner enquanto o pagamento estiver sendo processado.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-191">The browser will display a spinner page while the payment is being processed.</span></span>

![A página exibida quando o pagamento está sendo processado](./../media/loading_screen.png)

<span data-ttu-id="ab3ec-193">Depois que o pagamento for concluído, a página da Web chamará o [`complete()`](https://msdn.microsoft.com/library/mt790642) método e passará um valor de **sucesso** ou **falhará**.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-193">Once the payment is complete, the web page calls the [`complete()`](https://msdn.microsoft.com/library/mt790642) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="ab3ec-194">O [`complete()`](https://msdn.microsoft.com/library/mt790642) método informa ao navegador que a compra foi concluída e a tela de interface do usuário de terminação apropriada deve ser mostrada dependendo do valor de **sucesso** ou **falha**.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-194">The [`complete()`](https://msdn.microsoft.com/library/mt790642) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span> 

![<span data-ttu-id="ab3ec-195">A interface do usuário é exibida quando a compra tiver sido bem-sucedida ](./../media/response_payment-request_complete.png)
![ a interface do usuário exibida quando a compra falhar</span><span class="sxs-lookup"><span data-stu-id="ab3ec-195">The UI displayed when the purchase succeeded](./../media/response_payment-request_complete.png)
![The UI displayed when the purchase failed</span></span>](./../media/response_payment-request_failure.png)

## <span data-ttu-id="ab3ec-196">Solicitação de pagamento com remessa</span><span class="sxs-lookup"><span data-stu-id="ab3ec-196">Payment Request with Shipping</span></span>

### <span data-ttu-id="ab3ec-197">Endereço para entrega</span><span class="sxs-lookup"><span data-stu-id="ab3ec-197">Shipping Address</span></span>

<span data-ttu-id="ab3ec-198">Para vendas que exijam a remessa de bens físicos, é preciso um endereço de entrega.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-198">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="ab3ec-199">Para incluir um endereço de remessa, defina `requestShipping = True` o [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro da solicitação.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-199">To include a shipping address, set `requestShipping = True` in the [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter of the request.</span></span>   

<span data-ttu-id="ab3ec-200">Quando o usuário selecionar ou atualizar o endereço de entrega, o [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) evento será executado.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-200">When the user selects or updates the shipping address, the [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) event will run.</span></span>  <span data-ttu-id="ab3ec-201">O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá validar o endereço, recalcular os custos de remessa e os impostos e atualizar [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) para refletir os custos e as opções de remessa disponíveis para o endereço selecionado (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="ab3ec-201">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to reflect the changed costs and shipping options available for the address selected (if applicable).</span></span> 

### <span data-ttu-id="ab3ec-202">Opções de envio</span><span class="sxs-lookup"><span data-stu-id="ab3ec-202">Shipping Options</span></span> 

<span data-ttu-id="ab3ec-203">As opções de envio podem ser apresentadas ao cliente adicionando- [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) se ao [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-203">Shipping options can be presented to the customer by adding [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="ab3ec-204">Um padrão pode ser estabelecido por meio da configuração de `selected = True` uma das opções de envio.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-204">A default can be established by setting `selected = True` for one of the shipping options.</span></span> 
 
<span data-ttu-id="ab3ec-205">Quando o usuário seleciona ou atualiza as remessas, o [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) evento será executado.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-205">When the user selects or updates the shippingOptions, the [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) event will run.</span></span>  <span data-ttu-id="ab3ec-206">O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá atualizar o [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro com o valor de remessa correto.</span><span class="sxs-lookup"><span data-stu-id="ab3ec-206">The website, using an event listener, will be aware of the change and can update the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter with the correct shipping amount.</span></span>   

```js
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

## <span data-ttu-id="ab3ec-207">Referência da API</span><span class="sxs-lookup"><span data-stu-id="ab3ec-207">API Reference</span></span>
[<span data-ttu-id="ab3ec-208">API da Solicitação de Pagamento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-208">Payment Request API</span></span>](https://msdn.microsoft.com/library/mt790447)

## <span data-ttu-id="ab3ec-209">Especificada</span><span class="sxs-lookup"><span data-stu-id="ab3ec-209">Specification</span></span>
[<span data-ttu-id="ab3ec-210">API da Solicitação de Pagamento</span><span class="sxs-lookup"><span data-stu-id="ab3ec-210">Payment Request API</span></span>](https://w3.org/TR/payment-request/)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "O que é o Microsoft Edge herdado?"  
