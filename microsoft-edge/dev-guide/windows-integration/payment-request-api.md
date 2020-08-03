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
# API de solicitação de pagamento (EdgeHTML)

> [!NOTE]
> Este artigo descreve o fluxo de trabalho com suporte na [versão herdada do Microsoft Edge][MicrosoftSupport44533505].  O Microsoft Edge \ (Chromium \) dá suporte à API de solicitação de pagamento com uma implementação diferente com base no projeto Chromium.  

As vendas de comércio eletrônico continuam crescendo em um ritmo rápido. De acordo com o [eMarketer](https://www.emarketer.com/), por 2018, as vendas digitais são previstas para aumentar em 23% dos níveis medidos em 2013.  Embora os consumidores e as empresas aproveitem a praticidade das vendas de comércio eletrônico, ainda restam desafios.  Hoje, cada proprietário de site de comércio eletrônico precisa investir tempo para desenvolver fluxos de check-out e regras de validação de alta qualidade.  Os consumidores precisam navegar por fluxos de check-out diferentes e digitar novamente as informações de pagamento e remessa em todos os sites onde elas fazem compras.  Isso pode ser demorado e frustrante para os consumidores, que levam a uma taxa alta de abandono do carrinho de compras e das vendas reduzidas para comerciantes. Os comerciantes [estimarem](http://baymard.com/lists/cart-abandonment-rate) entre 60% e 70% dos carrinhos de compras são abandonados.      

A [API de solicitação de pagamento](https://w3.org/TR/payment-request/) padroniza o processo de check-out do pagamento. Essa API requer menos personalização para desenvolvedores da Web e fornece uma experiência mais rápida, consistente e, portanto, menos confusa para os consumidores.  Como os consumidores podem selecionar instrumentos de pagamento e enviar endereços da conta da Microsoft, eles são necessários para inserir menos dados para concluir as compras, o que reduz o tempo e a entrada de dados necessários para concluir um pagamento.   

A [API de solicitação de pagamento](https://w3.org/TR/payment-request/) é um padrão aberto e de navegador cruzado que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento (por exemplo, cartões de crédito) que os consumidores armazenaram na nuvem. 
  
Em resumo, ao usar a [API de solicitação de pagamento](https://w3.org/TR/payment-request/), os clientes fazem compras em sites de comerciante normalmente.  Quando estiver pronto para pagar, o website de comerciante chamará a API de **solicitação de pagamento** para criar uma **solicitação de pagamento** e passar as informações de pagamento relevantes (por exemplo, os métodos de pagamento, o valor de compra, a moeda, etc.) para o navegador.

![Construção de solicitação de pagamento](./../media/payment_request_construct.png)

O navegador autentica o usuário, permite que o usuário selecione um método de pagamento com suporte no arquivo e processa os detalhes de pagamento. Em seguida, o navegador envia os detalhes das informações de pagamento de volta para o website de comerciante, para que o comerciante possa concluir o pagamento.  Além de receber informações de pagamento, o comerciante também pode optar por receber informações de remessa como parte da **solicitação de pagamento**.  

![Construção de resposta de pagamento](./../media/payment_response_construct.png)

Para ver a API de solicitação de pagamento em ação, além de ter uma visão geral de como usá-la, confira este vídeo.

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> A API de solicitação de pagamento tem suporte no Microsoft Edge Build 14992 +.


## Criando uma solicitação de pagamento 
Páginas da Web crie uma **solicitação de pagamento** geralmente quando o usuário iniciar um processo de pagamento clicando no botão "comprar".  O **Payment Request** [Construtor](https://msdn.microsoft.com/library/mt790440) de solicitação de pagamento inclui methodData, detalhes e opções. 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

O [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro contém uma lista dos métodos de pagamento e redes aceitas pelo site e qualquer dado específico do método de pagamento associado. No Microsoft Edge, essa lista é correspondida com os métodos de pagamento com suporte que o comprador salvou na conta da Microsoft e resulta na lista "pagar com" na experiência do usuário do pagamento.

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

O [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro contém informações que o comerciante deseja transmitir para o cliente sobre a transação.  Isso inclui itens de resumo do pedido, como total, imposto, valor da entrega e outros itens de nível resumido que afetam o valor do pagamento. Esses itens não devem ser pedidos de linha. 
  
O [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro também é usado para definir as opções de envio disponíveis para o cliente quando necessário.  Mais detalhes estão incluídos na seção de **pagamento** com a seção remessa abaixo. 

Cada [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) linha inclui um rótulo para a moeda e o valor.  

> [!NOTE]
> A **solicitação de pagamento** não calcula a soma ou o total desses valores.  É responsabilidade do website do comerciante para garantir que os itens de linha toquem total corretamente.   


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

[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)não oferece suporte a reembolsos; portanto, os valores sempre devem ser positivos; itens de lista individuais podem ser negativos, como descontos. 

O navegador renderizará os rótulos conforme você os define e renderizará automaticamente a formatação de moeda correta com base na localidade do cliente. Observe que os rótulos devem ser renderizados no mesmo idioma do seu conteúdo. 

O [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro define os dados que a página da Web deseja retornar da **solicitação de pagamento**. Isso também define os dados que precisam ser coletados, incluindo se a remessa, o endereço de email e/ou o número de telefone são necessários.

![Lista suspensa de endereços de email](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## Mostrando a solicitação de pagamento

O [`show()`](https://msdn.microsoft.com/library/mt790448) método é chamado pela página da Web para permitir que o usuário interaja com a interface do usuário para **solicitação de pagamento** .  O [`show()`](https://msdn.microsoft.com/library/mt790448) método retorna uma promessa que será resolvida quando o usuário autorizar a solicitação de pagamento.  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Confirmar e pagar detalhes](./../media/pay_screen_default.png)

## Anular uma solicitação de pagamento
 
O [`abort()`](https://msdn.microsoft.com/library/mt790437) método pode ser chamado pela página da Web a qualquer momento após o [`show()`](https://msdn.microsoft.com/library/mt790448) método ser chamado, até o ponto em que a promessa está resolvida.  O [`abort()`](https://msdn.microsoft.com/library/mt790437) método fará com que o navegador anule a **solicitação de pagamento** e feche a interface do usuário da **solicitação de pagamento** .  Por exemplo, uma página da Web pode optar por anular se o usuário não concluiu a transação na quantidade de tempo necessária.

```js
payment.abort();
``` 

## Resposta de pagamento
Quando o cliente aprova a **solicitação de pagamento**, uma **resposta de pagamento** é retornada ao site. A **resposta de pagamento** inclui o seguinte: 

 Propriedade      | Descrição | Obrigatório | Informações adicionais
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | A ID do método de pagamento selecionado pelo usuário | Y | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | Um objeto JSON que inclui todos os dados que o comerciante exige para processar a transação usando o método de pagamento selecionado ou um token de pagamento | Y | [Cartão básico](https://go.microsoft.com/fwlink/?linkid=834965) Dicionário: titularname; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | O endereço de remessa selecionado pelo usuário  |  Opcional. Obrigatório quando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**  | Dicionário de endereços: país; endereçamento; mente York dependentLocality; CEP sortingCode; languageCode; porte correspondente telefone |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | A ID da opção de remessa selecionada | Opcional. Obrigatório quando [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | O nome fornecido pelo usuário  | Opcional. Obrigatório quando [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro** | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | O endereço de email selecionado pelo usuário | Opcional. Obrigatório quando [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro**  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | O número de telefone selecionado pelo usuário | Opcional. Obrigatório quando [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) é **verdadeiro** | |

O [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) objeto JSON na **resposta de pagamento** conterá os dados de pagamento exigidos pelo comerciante para processar um pagamento. Em sua forma mais simples, a resposta será um payload de [cartão básico](https://go.microsoft.com/fwlink/?linkid=834965) contendo detalhes do cartão de pagamento de texto não criptografado. Quando comerciantes têm arranjos com parceiros adicionais de gateway/processador para fornecer suporte a pagamentos, o comerciante pode exigir uma carga que o processador pode manipular. Eles podem assumir a forma de um token de processador/gateway ou um instrumento de pagamento criptografado. Esses métodos de pagamento estão fora do escopo deste documento e serão abordados na documentação específica do processador. Além disso, para receber uma resposta [básica de cartão](https://go.microsoft.com/fwlink/?linkid=834965) , não há necessidade de integração adicional à Microsoft para o desenvolvedor, diferentemente de outros métodos de pagamento específicos do processador/gateway que podem exigir a chave de criptografia ou a autorização de solicitação (OAuth). 

Durante o recebimento da **resposta de pagamento**, o website envia as informações de pagamento para o processador de pagamento.  O navegador exibirá uma página Spinner enquanto o pagamento estiver sendo processado.

![A página exibida quando o pagamento está sendo processado](./../media/loading_screen.png)

Depois que o pagamento for concluído, a página da Web chamará o [`complete()`](https://msdn.microsoft.com/library/mt790642) método e passará um valor de **sucesso** ou **falhará**.  O [`complete()`](https://msdn.microsoft.com/library/mt790642) método informa ao navegador que a compra foi concluída e a tela de interface do usuário de terminação apropriada deve ser mostrada dependendo do valor de **sucesso** ou **falha**. 

![A interface do usuário é exibida quando a compra tiver sido bem-sucedida ](./../media/response_payment-request_complete.png)
![ a interface do usuário exibida quando a compra falhar](./../media/response_payment-request_failure.png)

## Solicitação de pagamento com remessa

### Endereço para entrega

Para vendas que exijam a remessa de bens físicos, é preciso um endereço de entrega.  Para incluir um endereço de remessa, defina `requestShipping = True` o [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro da solicitação.   

Quando o usuário selecionar ou atualizar o endereço de entrega, o [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) evento será executado.  O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá validar o endereço, recalcular os custos de remessa e os impostos e atualizar [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) para refletir os custos e as opções de remessa disponíveis para o endereço selecionado (se aplicável). 

### Opções de envio 

As opções de envio podem ser apresentadas ao cliente adicionando- [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) se ao [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro.  Um padrão pode ser estabelecido por meio da configuração de `selected = True` uma das opções de envio. 
 
Quando o usuário seleciona ou atualiza as remessas, o [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) evento será executado.  O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá atualizar o [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parâmetro com o valor de remessa correto.   

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

## Referência da API
[API da Solicitação de Pagamento](https://msdn.microsoft.com/library/mt790447)

## Especificada
[API da Solicitação de Pagamento](https://w3.org/TR/payment-request/)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "O que é o Microsoft Edge herdado?"  
