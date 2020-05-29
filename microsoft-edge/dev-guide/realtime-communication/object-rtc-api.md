---
ms.assetid: ef705c70-73f8-445b-84ed-4f83679f1980
description: Saiba como o objeto de comunicação em tempo real (ORTC) permite que a mídia seja transmitida em tempo real diretamente entre navegadores da Web, dispositivos móveis ou servidores.
title: Guia de desenvolvimento-API RTC do objeto
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desenvolvimento da Web, HTML, CSS, JavaScript, desenvolvedor
ms.openlocfilehash: ac033ea26fa7c1eb435b0164e5dbd2a3a5428474
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560558"
---
# API RTC Object

O objeto de comunicação em tempo real (ORTC) permite que a mídia (áudio e/ou vídeo) seja transmitida (enviada e recebida) em tempo real diretamente entre navegadores da Web, dispositivos móveis e servidores via APIs JavaScript nativas.

> [!NOTE]
> O Microsoft Edge agora implementa o ORTC para dispositivos Windows 10. No entanto, essa implementação é diferente da versão mais recente da [API ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096). ORTC continuou a evoluir desde o desenvolvimento e o lançamento do Microsoft Edge--o navegador não implementa todos os objetos ou métodos dentro da API ORTC e inclui extensões não incorporadas atualmente na especificação. Posteriormente, o desenvolvimento continuará com a meta para permitir que os desenvolvedores em todo o mundo criem experiências que incluam a capacidade de conversar com usuários do Skype e outros serviços de comunicação compatíveis com o WebRTC.



Para obter uma experiência prática com o ORTC, experimente estas demonstrações no Test Drive:
-  [SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [Chamada telefônica ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [Demonstração de ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


Para obter mais informações sobre ORTC, consulte o [API ORTC agora está disponível no Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) no blog de desenvolvimento do Microsoft Edge.


## Diagrama de visão geral


O diagrama abaixo fornece um resumo descrevendo relações entre objetos ORTC. As setas horizontais ou inclinadas indicam o fluxo de mídia ou dados, enquanto as setas verticais indicam interações por meio de métodos e eventos.

ORTC usa objetos "*Sender*", "*Receiver*" e "*Transport*", que têm "*recursos*" que descrevem o que são capazes de fazer, bem como "*parâmetros*", que definem o que eles estão configurados para fazer. "*Controla*" a captura e a codificação de fluxos de mídia por remetentes, a viagem por transportes e decodificados pelos receptores que renderizam as faixas de fluxo de mídia para marcas de vídeo/áudio.

![Diagrama de fluxo de ORTC do Microsoft Edge ](./../media/ortc_diagram.png) na figura acima, ele [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) codifica a faixa fornecida como entrada, que é transportada por uma [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) ou em um [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) . Não há suporte para o envio de toques de radiofrequência (DTMF) de tom dual via [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .

O [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) e [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) usar um [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) caminho de comunicação para selecionar um caminho de comunicação para alcançar o par de recebimento `RTCIceTransport` , que, por sua vez, é associado a um `RTCDtlsTransport` ou `RTCSrtpSdesTransport` que desmultiplexa mídia para o [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) . `RTCRtpReceiver`Em seguida, o decodifica mídia, produzindo uma faixa que é renderizada por uma marca de áudio ou vídeo.

Vários outros objetos também desempenham uma função. O [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) reúne candidatos de Ice locais para uso por um único [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) objeto. As seções restantes da API preenchem detalhes relacionados a *funcionalidades* e *parâmetros*de RTP, *estatísticas operacionais* e compatibilidade com a [API WebRTC 1,0](https://go.microsoft.com/fwlink/p/?LinkID=627573).

> [!NOTE]
> Como o Microsoft Edge não implementa o canal de dados, `RTCDataChannel` `RTCSctpTransport` não há suporte para objetos e objetos.




## Componentes com suporte na implementação inicial do Microsoft Edge


* **Suporte à API ORTC.** As comunicações de áudio/vídeo são o foco principal, incluindo os seguintes objetos:,,,, e [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) também as [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces que não são mostradas diretamente no diagrama.
* **Suporte para multiplexação RTP/RTCP.** [`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)é necessário para uso com o [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) . Também há suporte para A multiplexação de/V.
* **Suporte STUN/TURN/ICE.** Há suporte para STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) e Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621). Na ICE, a indicações regulares tem suporte, com uma indicações agressiva parcialmente suportada (como um receptor). O DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) tem suporte, com base no DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).
* **Suporte a codecs.** Para [codecs de áudio](https://msdn.microsoft.com/library/Mt599587), damos suporte a g. 711, g. 722, Opus e Silk. Também suportamos ruído de conforto (CN) e DTMF de acordo com os requisitos de áudio do RTCWEB. Para o vídeo, atualmente damos suporte ao [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) codec usado pelos serviços da Skype, oferecendo suporte a recursos avançados, como a Simulcast, a codificação de vídeo dimensionável e a correção de erros de encaminhamento. Estamos nos empenhando para habilitar o vídeo interoperável com H. 264.

> [!NOTE]
> Se você estiver familiarizado com as implementações do WebRTC 1,0 e estiver interessado na evolução do suporte a objetos dentro do WebRTC 1,0 e do ORTC, recomendamos a apresentação a seguir pelo Google, pela Microsoft e pela hookflash da 2014 RTC Conference: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".




## Fluxo de código de nível de aplicativo para comunicações do 1:1


Para esse cenário, duas máquinas com o Windows 10 atuarão como dois pares com um servidor WebCOMO canal de sinalização para trocar informações entre os pares para que uma conexão possa ser estabelecida entre eles.

As etapas a seguir têm o escopo das operações feitas por um par. Os dois pares devem passar por etapas semelhantes para configurar as comunicações do 1:1. Para melhorar ainda mais os trechos de código a seguir, confira a [demonstração da unidade de teste do Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).

Este exemplo usa a multiplexação de áudio-vídeo e RTP/RTCP, portanto, você verá apenas um único transporte ICE e DTLS, usado para transportar pacotes RTP e RTCP para áudio e vídeo.

`Step #1.` Criar [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) objeto (ou seja, a [API de captura e fluxo de mídia](./../multimedia/media-Capture-and-Streams.md)) com uma faixa de áudio e uma faixa de vídeo.

```js
navigator.MediaDevices.getUserMedia ({
    "audio": true,
    "video": {
        width: 640,
        height: 360,
        facingMode: "user"
    }
}).then(
    gotStream
).catch(
    gotMediaError
);

function gotStream(stream) {
    var mediaStreamLocal = stream;
    …
}
```

`Step #2.` Crie [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) e habilite local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) para ser sinalizado para o par remoto.

```js
var iceOptions = new RTCIceGatherOptions;
iceOptions.gatherPolicy = "all";
iceOptions.iceservers = ... ;
var iceGathr = new RTCIceGatherer(iceOptions);
iceGathr.onlocalcandidate = function(evt) {
    mySignaller.signalMessage({
        "candidate": evt.candidate
    });
};
```

Para ajudar a proteger a privacidade do usuário, o Microsoft Edge introduz uma opção que permite que um usuário controle se os endereços IP de host locais podem ser expostos pelos [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objetos. Uma opção de interface será fornecida para alternar essa configuração.

Na [demonstração da unidade de teste do Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635), foi configurada uma vez que o servidor foi configurado. Esse servidor de ativação tem uma produtividade muito limitada, portanto, é limitado somente para uso da página de demonstração.

`Step #3.` Crie o [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) para áudio e vídeo e prepare-se para manipular [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) o controle remoto no transporte Ice.

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

Outra opção é acumular todos os candidatos remotos do ICE em um array `remoteCandidates` e `iceTr.setRemoteCandidates(remoteCandidates)` fazer chamadas para adicionar todos os candidatos remotos juntos.

`Step #4.` Crie o transporte DTLS.

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` Crie os objetos do remetente e do destinatário.

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

Etapa #6. Recupere os recursos de receptor e remetente.

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` Os parâmetros ICE/DTLS e recursos de envio/recebimento podem ser trocados.

```js
mySignaller.signalMessage({
    "ice": iceGathr.getLocalParameters(),
    "dtls": dtlsTr.getLocalParameters(),
    "recvAudioCaps": recvAudioCaps,
    "recvVideoCaps": recvVideoCaps,
    "sendAudioCaps": sendAudioCaps,
    "sendVideoCaps": sendVideoCaps
};
```

`Step #8.` Obter parâmetros remotos, iniciar o [`ICE`](https://msdn.microsoft.com/library/Mt433112) e [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transportes e definir os parâmetros de envio e recebimento de áudio e vídeo.

```js
mySignaller.onRemoteParams = function(params) {
    // The responder answers with its preferences, parameters and capabilities
    // Derive the send and receive parameters.
    var audioSendParams = myCapsToSendParams(sendAudioCaps, params.recvAudioCaps);
    var videoSendParams = myCapsToSendParams(sendVideoCaps, params.recvVideoCaps);
    var audioRecvParams = myCapsToRecvParams(recvAudioCaps, params.sendAudioCaps);
    var videoRecvParams = myCapsToRecvParams(recvVideoCaps, params.sendVideoCaps);
    iceTr.start(iceGathr, params.ice, RTCIceRole.controlling);
    dtlsTr.start(params.dtls);
    audioSender.send(audioSendParams);
    videoSender.send(videoSendParams);
    audioReceiver.receive(audioRecvParams);
    videoReceiver.receive(videoRecvParams);
};
```

Veja a seguir um esqueleto das funções do auxiliar. Encontre mais detalhes na [demonstração da unidade de teste do Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).

```js
RTCRtpParameters function myCapsToSendParams (RTCRtpCapabilities sendCaps, RTCRtpCapabilities remoteRecvCaps) {
    // Function returning the sender RTCRtpParameters, based on intersection of the local sender and remote receiver capabilities.
    // Steps to be followed:
    // 1. Determine the RTP features that the receiver and sender have in common.
    // 2. Determine the codecs that the sender and receiver have in common.
    // 3. Within each common codec, determine the common formats and rtcpFeedback mechanisms.
    // 4. Determine the payloadType to be used, based on the receiver preferredPayloadType.
    // 5. Set RTCRtcpParameters such as mux to their default values.  
}

RTCRtpParameters function myCapsToRecvParams(RTCRtpCapabilities recvCaps, RTCRtpCapabilities remoteSendCaps) {
    return myCapsToSendParams(remoteSendCaps, recvCaps);
}
```

`Step #9.` Renderize e reproduza o fluxo de mídia remoto acompanha uma marca de vídeo.

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

Depois de familiarizar-se com a configuração de chamadas do 1:1, aplique os mesmos princípios para configurar chamadas em grupo pequenos usando uma topologia de malha, em que cada par terá uma conexão 1:1 com o restante do grupo. Como a bifurcação paralela não é suportada na plataforma Microsoft Edge, isso deve ser manipulado via sinalização 1:1, de modo que os [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objetos independentes e [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) objetos serão usados para cada conexão.

## Detalhes da implementação no Microsoft Edge


A especificação ORTC foi relativamente estável, pois o grupo da Comunidade ORTC emitiu a "chamada para implementações", e desafios significativos no nível da API do JavaScript não são esperados. Com base nele, a implementação do Microsoft Edge foi lançada para testes de interoperabilidade entre navegadores no nível de protocolo.

Algumas limitações na implementação do Microsoft Edge devem ser observadas:

* `RTCIceTransportController` Não é suportada. A implementação do Microsoft Edge manipula o congelamento/descongelamento em uma base por transporte, para que o pedido de todas as outras `IceTransports` não seja necessário. Essa abordagem deve interoperar com implementações existentes.
* `RtpListener` Ainda não tem suporte. Isso significa que o SSRCs (origens de fluxo e sincronização) precisa ser especificado antecipadamente dentro do [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .
* A bifurcação ainda não é suportada em um `IceTransport` `IceGatherer` ou mais `DtlsTransport` . A solução para `DtlsTransport` bifurcação ainda está em discussão no grupo da Comunidade ORTC.
* Não há suporte para RTP/RTCP não-MUX com `DtlsTransport` ainda não tem suporte. Ao usar `DtlsTransport` seu aplicativo, será necessário dar suporte a RTP/RTCP Mux.
* No [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) momento, o Microsoft Edge ignora a maioria dos controles de qualidade de codificação, mas exige a configuração dos atributos ' active ' e ' SSRC '.
* O `icecandidatepairchanged` evento ainda não tem suporte. Você pode extrair as informações de par de candidatos por meio do [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) método.
* Atualmente o Microsoft Edge não oferece suporte a nenhuma das `DataChannel` funcionalidades definidas atualmente na especificação ORTC.

#### Olhando para o futuro

A implementação do Microsoft Edge ainda está cedo, espere que o conjunto de recursos continue crescendo nos próximos meses. O objetivo da implementação do Microsoft Edge é a interoperabilidade entre a Web hoje e também com o setor de comunicação em tempo real a longo prazo.



## Referência de API

[ORTC (comunicações em tempo real do objeto)](https://msdn.microsoft.com/library/Mt433097)

## Demonstrações

[SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[Chamada telefônica ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[Demonstração de ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## Tópicos relacionados

[A API ORTC agora está disponível no Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[SimpleWebRTC: Use a API ORTC do Microsoft Edge e as APIs do WebRTC no Chrome e Firefox para fazer chamadas em conferência entre navegadores.](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[Habilitar experiências de comunicação contínua para a Web com o Skype, o Skype for Business e o Microsoft Edge.](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[GRUPO DA COMUNIDADE ORTC (COMUNICAÇÕES EM TEMPO REAL DO OBJETO)](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## Especificada

[API do objeto W3C RTC (ORTC) para WebRTC](http://draft.ortc.org/)  
