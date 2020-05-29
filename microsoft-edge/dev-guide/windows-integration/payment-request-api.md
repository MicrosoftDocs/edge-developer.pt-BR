---
description: Saiba como a solicitação de pagamento APIenables o Microsoft Edge para atuar como intermediário entre comerciantes, consumidores e métodos de pagamento do consumidor armazenados na nuvem.
title: Guia de desenvolvimento-API de solicitação de pagamento
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: 75c596570a222336a4ba0c371acb8770f97804ee
ms.sourcegitcommit: e690bb4d1cb9e73c93b468c9f55d91ea6fb6c654
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/10/2020
ms.locfileid: "10562544"
---
# <span data-ttu-id="c4dbb-104">API de solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-104">Payment Request API</span></span>

<span data-ttu-id="c4dbb-105">As vendas de comércio eletrônico continuam crescendo em um ritmo rápido.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-105">E-commerce sales continue growing at a rapid pace.</span></span> <span data-ttu-id="c4dbb-106">De acordo com o [eMarketer](https://www.emarketer.com/), por 2018, as vendas digitais são previstas para aumentar em 23% dos níveis medidos em 2013.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-106">According to [eMarketer](https://www.emarketer.com/), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="c4dbb-107">Embora os consumidores e as empresas aproveitem a praticidade das vendas de comércio eletrônico, ainda restam desafios.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-107">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="c4dbb-108">Hoje, cada proprietário de site de comércio eletrônico precisa investir tempo para desenvolver fluxos de check-out e regras de validação de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-108">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="c4dbb-109">Os consumidores precisam navegar por fluxos de check-out diferentes e digitar novamente as informações de pagamento e remessa em todos os sites onde elas fazem compras.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-109">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="c4dbb-110">Isso pode ser demorado e frustrante para os consumidores, que levam a uma taxa alta de abandono do carrinho de compras e das vendas reduzidas para comerciantes.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-110">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span> <span data-ttu-id="c4dbb-111">Os comerciantes [estimarem](http://baymard.com/lists/cart-abandonment-rate) entre 60% e 70% dos carrinhos de compras são abandonados.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-111">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>      

<span data-ttu-id="c4dbb-112">A [API de solicitação de pagamento](https://w3.org/TR/payment-request/) padroniza o processo de check-out do pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-112">The [Payment Request API](https://w3.org/TR/payment-request/) standardizes the payment checkout process.</span></span> <span data-ttu-id="c4dbb-113">Essa API requer menos personalização para desenvolvedores da Web e fornece uma experiência mais rápida, consistente e, portanto, menos confusa para os consumidores.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-113">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="c4dbb-114">Como os consumidores podem selecionar instrumentos de pagamento e enviar endereços da conta da Microsoft, eles são necessários para inserir menos dados para concluir as compras, o que reduz o tempo e a entrada de dados necessários para concluir um pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-114">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>   

<span data-ttu-id="c4dbb-115">A [API de solicitação de pagamento](https://w3.org/TR/payment-request/) é um padrão aberto e de navegador cruzado que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento (por exemplo, cartões de crédito) que os consumidores armazenaram na nuvem.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-115">The [Payment Request API](https://w3.org/TR/payment-request/) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods (e.g. credit cards) that consumers have stored in the cloud.</span></span> 
  
<span data-ttu-id="c4dbb-116">Em resumo, ao usar a [API de solicitação de pagamento](https://w3.org/TR/payment-request/), os clientes fazem compras em sites de comerciante normalmente.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-116">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request/), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="c4dbb-117">Quando estiver pronto para pagar, o website de comerciante chamará a API de **solicitação de pagamento** para criar uma **solicitação de pagamento** e passar as informações de pagamento relevantes (por exemplo, os métodos de pagamento, o valor de compra, a moeda, etc.) para o navegador.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-117">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information (e.g. supported payment methods, purchase amount, currency, etc.) to the browser.</span></span>

![Construção de solicitação de pagamento](./../media/payment_request_construct.png)

<span data-ttu-id="c4dbb-119">O navegador autentica o usuário, permite que o usuário selecione um método de pagamento com suporte no arquivo e processa os detalhes de pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-119">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span> <span data-ttu-id="c4dbb-120">Em seguida, o navegador envia os detalhes das informações de pagamento de volta para o website de comerciante, para que o comerciante possa concluir o pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-120">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="c4dbb-121">Além de receber informações de pagamento, o comerciante também pode optar por receber informações de remessa como parte da **solicitação de pagamento**.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-121">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

![Construção de resposta de pagamento](./../media/payment_response_construct.png)

<span data-ttu-id="c4dbb-123">Para ver a API de solicitação de pagamento em ação, além de ter uma visão geral de como usá-la, confira este vídeo.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-123">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> <span data-ttu-id="c4dbb-124">A API de solicitação de pagamento tem suporte no Microsoft Edge Build 14992 +.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-124">The Payment Request API is supported in Microsoft Edge build 14992+.</span></span>


## <span data-ttu-id="c4dbb-125">Criando uma solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-125">Creating a Payment Request</span></span> 
<span data-ttu-id="c4dbb-126">Páginas da Web crie uma **solicitação de pagamento** geralmente quando o usuário iniciar um processo de pagamento clicando no botão "comprar".</span><span class="sxs-lookup"><span data-stu-id="c4dbb-126">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="c4dbb-127">O **Payment Request** [Construtor](https://msdn.microsoft.com/library/mt790440) de solicitação de pagamento inclui methodData, detalhes e opções.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-127">The **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) includes methodData, details, and options.</span></span> 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

<span data-ttu-id="c4dbb-128">O [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro contém uma lista dos métodos de pagamento e redes aceitas pelo site e qualquer dado específico do método de pagamento associado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-128">The [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span> <span data-ttu-id="c4dbb-129">No Microsoft Edge, essa lista é correspondida com os métodos de pagamento com suporte que o comprador salvou na conta da Microsoft e resulta na lista "pagar com" na experiência do usuário do pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-129">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>

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

<span data-ttu-id="c4dbb-131">O [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro contém informações que o comerciante deseja transmitir para o cliente sobre a transação.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-131">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="c4dbb-132">Isso inclui itens de resumo do pedido, como total, imposto, valor da entrega e outros itens de nível resumido que afetam o valor do pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-132">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span> <span data-ttu-id="c4dbb-133">Esses itens não devem ser pedidos de linha.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-133">These are not intended to be order line items.</span></span> 
  
<span data-ttu-id="c4dbb-134">O [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro também é usado para definir as opções de envio disponíveis para o cliente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-134">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="c4dbb-135">Mais detalhes estão incluídos na seção de **pagamento** com a seção remessa abaixo.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-135">More details are included in the **Payment Request** with Shipping section below.</span></span> 

<span data-ttu-id="c4dbb-136">Cada [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) linha inclui um rótulo para a moeda e o valor.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-136">Each [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="c4dbb-137">A **solicitação de pagamento** não calcula a soma ou o total desses valores.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-137">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="c4dbb-138">É responsabilidade do website do comerciante para garantir que os itens de linha toquem total corretamente.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-138">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>   


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

<span data-ttu-id="c4dbb-140">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)não oferece suporte a reembolsos; portanto, os valores sempre devem ser positivos; itens de lista individuais podem ser negativos, como descontos.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-140">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span> 

<span data-ttu-id="c4dbb-141">O navegador renderizará os rótulos conforme você os define e renderizará automaticamente a formatação de moeda correta com base na localidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-141">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span> <span data-ttu-id="c4dbb-142">Observe que os rótulos devem ser renderizados no mesmo idioma do seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-142">Note that the labels should be rendered in the same language as your content.</span></span> 

<span data-ttu-id="c4dbb-143">O [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro define os dados que a página da Web deseja retornar da **solicitação de pagamento**.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-143">The [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span> <span data-ttu-id="c4dbb-144">Isso também define os dados que precisam ser coletados, incluindo se a remessa, o endereço de email e/ou o número de telefone são necessários.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-144">This also defines the data that needs to be collected, including if shipping, email address, and/or phone number are required.</span></span>

![Lista suspensa de endereços de email](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## <span data-ttu-id="c4dbb-146">Mostrando a solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-146">Showing the Payment Request</span></span>

<span data-ttu-id="c4dbb-147">O [`show()`](https://msdn.microsoft.com/library/mt790448) método é chamado pela página da Web para permitir que o usuário interaja com a interface do usuário para **solicitação de pagamento** .</span><span class="sxs-lookup"><span data-stu-id="c4dbb-147">The [`show()`](https://msdn.microsoft.com/library/mt790448) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="c4dbb-148">O [`show()`](https://msdn.microsoft.com/library/mt790448) método retorna uma promessa que será resolvida quando o usuário autorizar a solicitação de pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-148">The [`show()`](https://msdn.microsoft.com/library/mt790448) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Confirmar e pagar detalhes](./../media/pay_screen_default.png)

## <span data-ttu-id="c4dbb-150">Anular uma solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-150">Aborting a Payment Request</span></span>
 
<span data-ttu-id="c4dbb-151">O [`abort()`](https://msdn.microsoft.com/library/mt790437) método pode ser chamado pela página da Web a qualquer momento após o [`show()`](https://msdn.microsoft.com/library/mt790448) método ser chamado, até o ponto em que a promessa está resolvida.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-151">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method can be called by the web page any time after the [`show()`](https://msdn.microsoft.com/library/mt790448) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="c4dbb-152">O [`abort()`](https://msdn.microsoft.com/library/mt790437) método fará com que o navegador anule a **solicitação de pagamento** e feche a interface do usuário da **solicitação de pagamento** .</span><span class="sxs-lookup"><span data-stu-id="c4dbb-152">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="c4dbb-153">Por exemplo, uma página da Web pode optar por anular se o usuário não concluiu a transação na quantidade de tempo necessária.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-153">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>

```js
payment.abort();
``` 

## <span data-ttu-id="c4dbb-154">Resposta de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-154">Payment Response</span></span>
<span data-ttu-id="c4dbb-155">Quando o cliente aprova a **solicitação de pagamento**, uma **resposta de pagamento** é retornada ao site.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-155">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span> <span data-ttu-id="c4dbb-156">A **resposta de pagamento** inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c4dbb-156">The **Payment Response** includes the following:</span></span> 

 <span data-ttu-id="c4dbb-157">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c4dbb-157">Property</span></span>      | <span data-ttu-id="c4dbb-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4dbb-158">Description</span></span> | <span data-ttu-id="c4dbb-159">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c4dbb-159">Required</span></span> | <span data-ttu-id="c4dbb-160">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="c4dbb-160">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | <span data-ttu-id="c4dbb-161">A ID do método de pagamento selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="c4dbb-161">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="c4dbb-162">Y</span><span class="sxs-lookup"><span data-stu-id="c4dbb-162">Y</span></span> | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | <span data-ttu-id="c4dbb-163">Um objeto JSON que inclui todos os dados que o comerciante exige para processar a transação usando o método de pagamento selecionado ou um token de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-163">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="c4dbb-164">Y</span><span class="sxs-lookup"><span data-stu-id="c4dbb-164">Y</span></span> | <span data-ttu-id="c4dbb-165">[Cartão básico](https://go.microsoft.com/fwlink/?linkid=834965) Dicionário: titularname; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="c4dbb-165">[Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | <span data-ttu-id="c4dbb-166">O endereço de remessa selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="c4dbb-166">The shipping address selected by the user</span></span>  |  <span data-ttu-id="c4dbb-167">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-167">Optional.</span></span> <span data-ttu-id="c4dbb-168">Obrigatório quando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="c4dbb-168">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | <span data-ttu-id="c4dbb-169">Dicionário de endereços: país; endereçamento; mente York dependentLocality; CEP sortingCode; languageCode; porte correspondente telefone</span><span class="sxs-lookup"><span data-stu-id="c4dbb-169">Address dictionary: country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | <span data-ttu-id="c4dbb-170">A ID da opção de remessa selecionada</span><span class="sxs-lookup"><span data-stu-id="c4dbb-170">The ID for the selected shipping option</span></span> | <span data-ttu-id="c4dbb-171">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-171">Optional.</span></span> <span data-ttu-id="c4dbb-172">Obrigatório quando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="c4dbb-172">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="c4dbb-173">O nome fornecido pelo usuário</span><span class="sxs-lookup"><span data-stu-id="c4dbb-173">The name provided by the user</span></span>  | <span data-ttu-id="c4dbb-174">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-174">Optional.</span></span> <span data-ttu-id="c4dbb-175">Obrigatório quando [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="c4dbb-175">Required when [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="c4dbb-176">O endereço de email selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="c4dbb-176">The email address selected by the user</span></span> | <span data-ttu-id="c4dbb-177">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-177">Optional.</span></span> <span data-ttu-id="c4dbb-178">Obrigatório quando [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="c4dbb-178">Required when [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="c4dbb-179">O número de telefone selecionado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="c4dbb-179">The phone number selected by the user</span></span> | <span data-ttu-id="c4dbb-180">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-180">Optional.</span></span> <span data-ttu-id="c4dbb-181">Obrigatório quando [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="c4dbb-181">Required when [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |

<span data-ttu-id="c4dbb-182">O [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) objeto JSON na **resposta de pagamento** conterá os dados de pagamento exigidos pelo comerciante para processar um pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-182">The [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span> <span data-ttu-id="c4dbb-183">Em sua forma mais simples, a resposta será um payload de [cartão básico](https://go.microsoft.com/fwlink/?linkid=834965) contendo detalhes do cartão de pagamento de texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-183">In its simplest form, the response will be a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) payload containing cleartext payment card details.</span></span> <span data-ttu-id="c4dbb-184">Quando comerciantes têm arranjos com parceiros adicionais de gateway/processador para fornecer suporte a pagamentos, o comerciante pode exigir uma carga que o processador pode manipular.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-184">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span> <span data-ttu-id="c4dbb-185">Eles podem assumir a forma de um token de processador/gateway ou um instrumento de pagamento criptografado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-185">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span> <span data-ttu-id="c4dbb-186">Esses métodos de pagamento estão fora do escopo deste documento e serão abordados na documentação específica do processador.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-186">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span> <span data-ttu-id="c4dbb-187">Além disso, para receber uma resposta [básica de cartão](https://go.microsoft.com/fwlink/?linkid=834965) , não há necessidade de integração adicional à Microsoft para o desenvolvedor, diferentemente de outros métodos de pagamento específicos do processador/gateway que podem exigir a chave de criptografia ou a autorização de solicitação (OAuth).</span><span class="sxs-lookup"><span data-stu-id="c4dbb-187">Additionally, to receive a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization (oauth).</span></span> 

<span data-ttu-id="c4dbb-188">Durante o recebimento da **resposta de pagamento**, o website envia as informações de pagamento para o processador de pagamento.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-188">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="c4dbb-189">O navegador exibirá uma página Spinner enquanto o pagamento estiver sendo processado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-189">The browser will display a spinner page while the payment is being processed.</span></span>

![A página exibida quando o pagamento está sendo processado](./../media/loading_screen.png)

<span data-ttu-id="c4dbb-191">Depois que o pagamento for concluído, a página da Web chamará o [`complete()`](https://msdn.microsoft.com/library/mt790642) método e passará um valor de **sucesso** ou **falhará**.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-191">Once the payment is complete, the web page calls the [`complete()`](https://msdn.microsoft.com/library/mt790642) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="c4dbb-192">O [`complete()`](https://msdn.microsoft.com/library/mt790642) método informa ao navegador que a compra foi concluída e a tela de interface do usuário de terminação apropriada deve ser mostrada dependendo do valor de **sucesso** ou **falha**.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-192">The [`complete()`](https://msdn.microsoft.com/library/mt790642) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span> 

![<span data-ttu-id="c4dbb-193">A interface do usuário é exibida quando a compra tiver sido bem-sucedida ](./../media/response_payment-request_complete.png)
![ a interface do usuário exibida quando a compra falhar</span><span class="sxs-lookup"><span data-stu-id="c4dbb-193">The UI displayed when the purchase succeeded](./../media/response_payment-request_complete.png)
![The UI displayed when the purchase failed</span></span>](./../media/response_payment-request_failure.png)

## <span data-ttu-id="c4dbb-194">Solicitação de pagamento com remessa</span><span class="sxs-lookup"><span data-stu-id="c4dbb-194">Payment Request with Shipping</span></span>

### <span data-ttu-id="c4dbb-195">Endereço para entrega</span><span class="sxs-lookup"><span data-stu-id="c4dbb-195">Shipping Address</span></span>

<span data-ttu-id="c4dbb-196">Para vendas que exijam a remessa de bens físicos, é preciso um endereço de entrega.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-196">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="c4dbb-197">Para incluir um endereço de remessa, defina `requestShipping = True` o [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro da solicitação.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-197">To include a shipping address, set `requestShipping = True` in the [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter of the request.</span></span>   

<span data-ttu-id="c4dbb-198">Quando o usuário selecionar ou atualizar o endereço de entrega, o [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) evento será executado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-198">When the user selects or updates the shipping address, the [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) event will run.</span></span>  <span data-ttu-id="c4dbb-199">O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá validar o endereço, recalcular os custos de remessa e os impostos e atualizar [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) para refletir os custos e as opções de remessa disponíveis para o endereço selecionado (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="c4dbb-199">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to reflect the changed costs and shipping options available for the address selected (if applicable).</span></span> 

### <span data-ttu-id="c4dbb-200">Opções de envio</span><span class="sxs-lookup"><span data-stu-id="c4dbb-200">Shipping Options</span></span> 

<span data-ttu-id="c4dbb-201">As opções de envio podem ser apresentadas ao cliente adicionando- [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) se ao [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-201">Shipping options can be presented to the customer by adding [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="c4dbb-202">Um padrão pode ser estabelecido por meio da configuração de `selected = True` uma das opções de envio.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-202">A default can be established by setting `selected = True` for one of the shipping options.</span></span> 
 
<span data-ttu-id="c4dbb-203">Quando o usuário seleciona ou atualiza as remessas, o [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) evento será executado.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-203">When the user selects or updates the shippingOptions, the [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) event will run.</span></span>  <span data-ttu-id="c4dbb-204">O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá atualizar o [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro com o valor de remessa correto.</span><span class="sxs-lookup"><span data-stu-id="c4dbb-204">The website, using an event listener, will be aware of the change and can update the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter with the correct shipping amount.</span></span>   

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

## <span data-ttu-id="c4dbb-205">Referência da API</span><span class="sxs-lookup"><span data-stu-id="c4dbb-205">API Reference</span></span>
[<span data-ttu-id="c4dbb-206">API de solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-206">Payment Request API</span></span>](https://msdn.microsoft.com/library/mt790447)

## <span data-ttu-id="c4dbb-207">Especificada</span><span class="sxs-lookup"><span data-stu-id="c4dbb-207">Specification</span></span>
[<span data-ttu-id="c4dbb-208">API de solicitação de pagamento</span><span class="sxs-lookup"><span data-stu-id="c4dbb-208">Payment Request API</span></span>](https://w3.org/TR/payment-request/)
