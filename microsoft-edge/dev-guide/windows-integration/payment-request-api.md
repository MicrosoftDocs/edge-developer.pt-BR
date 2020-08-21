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
# API de solicitação de pagamento (EdgeHTML)  

> [!NOTE]
> Este artigo descreve o fluxo de trabalho com suporte na [versão herdada do Microsoft Edge][MicrosoftSupport44533505].  O Microsoft Edge \ (Chromium \) dá suporte à API de solicitação de pagamento com uma implementação diferente com base no projeto Chromium.  

As vendas de comércio eletrônico continuam crescendo em um ritmo rápido.  De acordo com o [eMarketer](https://www.emarketer.com), por 2018, as vendas digitais são previstas para aumentar em 23% dos níveis medidos em 2013.  Embora os consumidores e as empresas aproveitem a praticidade das vendas de comércio eletrônico, ainda restam desafios.  Hoje, cada proprietário de site de comércio eletrônico precisa investir tempo para desenvolver fluxos de check-out e regras de validação de alta qualidade.  Os consumidores precisam navegar por fluxos de check-out diferentes e digitar novamente as informações de pagamento e remessa em todos os sites onde elas fazem compras.  Isso pode ser demorado e frustrante para os consumidores, que levam a uma taxa alta de abandono do carrinho de compras e das vendas reduzidas para comerciantes.  Os comerciantes [estimarem](http://baymard.com/lists/cart-abandonment-rate) entre 60% e 70% dos carrinhos de compras são abandonados.  

A [API de solicitação de pagamento](https://w3.org/TR/payment-request) padroniza o processo de check-out do pagamento.  Essa API requer menos personalização para desenvolvedores da Web e fornece uma experiência mais rápida, consistente e, portanto, menos confusa para os consumidores.  Como os consumidores podem selecionar instrumentos de pagamento e enviar endereços da conta da Microsoft, eles são necessários para inserir menos dados para concluir as compras, o que reduz o tempo e a entrada de dados necessários para concluir um pagamento.  

A [API de solicitação de pagamento](https://w3.org/TR/payment-request) é um padrão de navegador cruzado aberto que permite que os navegadores atuem como intermediários entre comerciantes, consumidores e métodos de pagamento \ (como cartões de crédito \) que os consumidores armazenaram na nuvem.  
  
Em resumo, ao usar a [API de solicitação de pagamento](https://w3.org/TR/payment-request), os clientes fazem compras em sites de comerciante normalmente.  Quando estiver pronto para pagar, o website de comerciante chama a API de **solicitação de pagamento** para criar uma **solicitação de pagamento** e passa as informações de pagamento relevantes \ (como métodos de pagamento com suporte, valor de compra, moeda e assim por diante \) para o navegador.  

:::image type="complex" source="../media/payment_request_construct.png" alt-text="Construção de solicitação de pagamento" lightbox="../media/payment_request_construct.png":::
   Construção de solicitação de pagamento  
:::image-end:::  

O navegador autentica o usuário, permite que o usuário selecione um método de pagamento com suporte no arquivo e processa os detalhes de pagamento.  Em seguida, o navegador envia os detalhes das informações de pagamento de volta para o website de comerciante, para que o comerciante possa concluir o pagamento.  Além de receber informações de pagamento, o comerciante também pode optar por receber informações de remessa como parte da **solicitação de pagamento**.  

:::image type="complex" source="../media/payment_response_construct.png" alt-text="Construção de resposta de pagamento" lightbox="../media/payment_response_construct.png":::
   Construção de resposta de pagamento  
:::image-end:::  

Para ver a API de solicitação de pagamento em ação, além de ter uma visão geral de como usá-la, confira este vídeo.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]  

> [!NOTE]
> A API de solicitação de pagamento tem suporte no Microsoft Edge Build 14992 ou mais recente.  

## Criando uma solicitação de pagamento  

Páginas da Web crie uma **solicitação de pagamento** geralmente quando o usuário iniciar um processo de pagamento clicando no botão "comprar".  O **Payment Request** [Construtor](/previous-versions/mt790440(v=vs.85)) de solicitação de pagamento inclui methodData, detalhes e opções.  

```javascript
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```  

O parâmetro [methodData](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contém uma lista dos métodos de pagamento e redes aceitas pelo site e qualquer dado específico de método de pagamento associado.  No Microsoft Edge, essa lista é correspondida com os métodos de pagamento com suporte que o comprador salvou na conta da Microsoft e resulta na lista "pagar com" na experiência do usuário do pagamento.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_with.png" alt-text="A lista pagar com na experiência do usuário de bolso da Microsoft" lightbox="../media/pay_with.png":::
         A lista **pagar com** na experiência do usuário de bolso da Microsoft  
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

O parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) contém informações que o comerciante deseja transmitir para o cliente sobre a transação.  Isso inclui itens de resumo do pedido, como total, imposto, valor da entrega e outros itens de nível resumido que afetam o valor do pagamento.  Esses itens não devem ser pedidos de linha.  
  
O parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) também é usado para definir as opções de envio disponíveis para o cliente quando necessário.  Mais detalhes estão incluídos na seção de **pagamento** com a seção remessa abaixo.  

Cada linha de [detalhe](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) inclui um rótulo para a moeda e o valor.  

> [!NOTE]
> A **solicitação de pagamento** não calcula a soma ou o total desses valores.  É responsabilidade do website do comerciante para garantir que os itens de linha toquem total corretamente.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/show_details.png" alt-text="Detalhes de subtotal, remessa, impostos e total" lightbox="../media/show_details.png":::
         Detalhes de subtotal, remessa, impostos e total  
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

O [PaymentRequest](/previous-versions/mt790440(v=vs.85)) não dá suporte a reembolsos; portanto, os valores sempre devem ser positivos; itens de lista individuais podem ser negativos, como descontos.  

O navegador renderizará os rótulos conforme você os define e renderizará automaticamente a formatação de moeda correta com base na localidade do cliente.  Observe que os rótulos devem ser renderizados no mesmo idioma do seu conteúdo.  

O parâmetro [Options](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) define os dados que a página da Web deseja retornar da **solicitação de pagamento**.  Isso também define os dados que precisam ser coletados, incluindo se a remessa, o endereço de email, o número de telefone ou todos forem necessários.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/email_snippet.png" alt-text="Lista suspensa de endereços de email" lightbox="../media/email_snippet.png":::
         Lista suspensa de endereços de email  
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

## Mostrando a solicitação de pagamento  

O método [show ()](/previous-versions/mt790448(v=vs.85)) é chamado pela página da Web para permitir que o usuário interaja com a interface do usuário de **solicitação de pagamento** .  O método [show ()](/previous-versions/mt790448(v=vs.85)) retorna uma promessa que será resolvida quando o usuário autorizar a solicitação de pagamento.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/pay_screen_default.png" alt-text="Confirmar e pagar detalhes" lightbox="../media/pay_screen_default.png":::
         Confirmar e pagar detalhes  
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

## Anular uma solicitação de pagamento  
 
O método [Abort ()](/previous-versions/mt790437(v=vs.85)) pode ser chamado pela página da Web a qualquer momento após o método [show ()](/previous-versions/mt790448(v=vs.85)) ser chamado, até o ponto em que a promessa está resolvida.  O método [Abort ()](/previous-versions/mt790437(v=vs.85)) fará com que o navegador anule a **solicitação de pagamento** e feche a interface do usuário da **solicitação de pagamento** .  Por exemplo, uma página da Web pode optar por anular se o usuário não concluiu a transação na quantidade de tempo necessária.  

```javascript
payment.abort();
```  

## Resposta de pagamento  
Quando o cliente aprova a **solicitação de pagamento**, uma **resposta de pagamento** é retornada ao site.  A **resposta de pagamento** inclui o seguinte:  

 Propriedade      | Descrição | Obrigatório | Informações adicionais
|---------------|-----------------|-------|-----------------|
[methodName](/previous-versions/mt790656(v=vs.85)) | A ID do método de pagamento selecionado pelo usuário | Y | |   
[details](/previous-versions/mt790655(v=vs.85)) | Um objeto JSON que inclui todos os dados que o comerciante exige para processar a transação usando o método de pagamento selecionado ou um token de pagamento | Y | [Cartão básico](https://w3c.github.io/payment-method-basic-card) Dicionário: titularname; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress; |   
[shippingAddress](/previous-versions/mt790445(v=vs.85)) | O endereço de remessa selecionado pelo usuário  |  Opcional.  Obrigatório quando o [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é `True`  | Dicionário de endereços: país; endereçamento; mente York dependentLocality; CEP sortingCode; languageCode; porte correspondente telefone |  
[shippingOption](/previous-versions/mt790446(v=vs.85)) | A ID da opção de remessa selecionada | Opcional.  Obrigatório quando o [requestShipping](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é `True`  | |   
[sacador](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | O nome fornecido pelo usuário  | Opcional.  Obrigatório quando o [requestPayerName](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é `True` | |  
[payerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | O endereço de email selecionado pelo usuário | Opcional.  Obrigatório quando o [requestPayerEmail](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é `True`  | |  
[PayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) | O número de telefone selecionado pelo usuário | Opcional.  Obrigatório quando o [requestPayerPhone](/previous-versions/mt790440(v=vs.85)#PaymentOptions) é `True` | |  

O objeto JSON de [detalhes](/previous-versions/mt790655(v=vs.85)#PaymentRequest_params) na **resposta de pagamento** conterá os dados de pagamento exigidos pelo comerciante para processar um pagamento.  Em sua forma mais simples, a resposta será um payload de [cartão básico](https://w3c.github.io/payment-method-basic-card) contendo detalhes do cartão de pagamento de texto não criptografado.  Quando comerciantes têm arranjos com parceiros adicionais de gateway/processador para fornecer suporte a pagamentos, o comerciante pode exigir uma carga que o processador pode manipular.  Eles podem assumir a forma de um token de processador/gateway ou um instrumento de pagamento criptografado.  Esses métodos de pagamento estão fora do escopo deste documento e serão abordados na documentação específica do processador.  Além disso, para receber uma resposta [básica de cartão](https://w3c.github.io/payment-method-basic-card) , nenhuma integração adicional à Microsoft é necessária para o desenvolvedor, diferentemente de outros métodos de pagamento específicos do processador/gateway que podem exigir a chave de criptografia ou a autorização de solicitação \ (OAuth \).  

Durante o recebimento da **resposta de pagamento**, o website envia as informações de pagamento para o processador de pagamento.  O navegador exibirá uma página Spinner enquanto o pagamento estiver sendo processado.  

:::image type="complex" source="../media/loading_screen.png" alt-text="A página exibida quando o pagamento está sendo processado" lightbox="../media/loading_screen.png":::
   A página exibida quando o pagamento está sendo processado  
:::image-end:::  

Depois que o pagamento for concluído, a página da Web chamará o método [Complete ()](/previous-versions/mt790642(v=vs.85)) e passará um valor de **êxito** ou **falhará**.  O método [Complete ()](/previous-versions/mt790642(v=vs.85)) informa ao navegador que a compra foi concluída e a tela de interface do usuário de terminação apropriada deve ser mostrada dependendo do valor de **êxito** ou **falha**.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_complete.png" alt-text="A interface do usuário é exibida quando a compra é bem-sucedida" lightbox="../media/response_payment-request_complete.png":::
         A interface do usuário é exibida quando a compra é bem-sucedida  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/response_payment-request_failure.png" alt-text="A interface do usuário exibida quando a compra falhou" lightbox="../media/response_payment-request_failure.png":::
         A interface do usuário exibida quando a compra falhou  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Solicitação de pagamento com remessa  

### Endereço para entrega  

Para vendas que exijam a remessa de bens físicos, é preciso um endereço de entrega.  Para incluir um endereço de remessa, defina `requestShipping = True` o parâmetro de [Opções](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) da solicitação.  

Quando o usuário selecionar ou atualizar o endereço de remessa, o evento [onshippingaddresschange](/previous-versions/mt790442(v=vs.85)) será executado.  O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá validar o endereço, recalcular os custos e impostos da remessa e atualizar as [remeteroptions](/previous-versions/mt790440(v=vs.85)) para refletir os custos alterados e as opções de envio disponíveis para o endereço selecionado \ (se aplicável \).  

### Opções de envio  

As opções de envio podem ser apresentadas ao cliente adicionando [shippingoptions](/previous-versions/mt790440(v=vs.85)) ao parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) .  Um padrão pode ser estabelecido por meio da configuração de `selected = True` uma das opções de envio.  
 
Quando o usuário seleciona ou atualiza as remessas, o evento [onshippingoptionchange](/previous-versions/mt790436(v=vs.85)) será executado.  O site, usando um ouvinte de eventos, será informado sobre a alteração e poderá atualizar o parâmetro [detalhes](/previous-versions/mt790440(v=vs.85)#PaymentRequest_params) com o valor de remessa correto.  

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

## Referência da API  

[API da Solicitação de Pagamento](/previous-versions/mt790447(v=vs.85))  

## Especificada
[API da Solicitação de Pagamento](https://w3.org/TR/payment-request)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Ferramentas de desenvolvedor do Microsoft Edge (Chromium) | Documentos da Microsoft"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "O que é o Microsoft Edge herdado?"  
