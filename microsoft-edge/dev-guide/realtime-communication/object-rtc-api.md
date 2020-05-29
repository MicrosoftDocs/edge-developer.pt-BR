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
# <span data-ttu-id="49203-104">API RTC Object</span><span class="sxs-lookup"><span data-stu-id="49203-104">Object RTC API</span></span>

<span data-ttu-id="49203-105">O objeto de comunicação em tempo real (ORTC) permite que a mídia (áudio e/ou vídeo) seja transmitida (enviada e recebida) em tempo real diretamente entre navegadores da Web, dispositivos móveis e servidores via APIs JavaScript nativas.</span><span class="sxs-lookup"><span data-stu-id="49203-105">Object Real-Time Communications (ORTC) enables media (audio and/or video) to be streamed (sent and received) in real-time directly between web browsers, mobile devices, and servers via native Javascript APIs.</span></span>

> [!NOTE]
> <span data-ttu-id="49203-106">O Microsoft Edge agora implementa o ORTC para dispositivos Windows 10.</span><span class="sxs-lookup"><span data-stu-id="49203-106">Microsoft Edge now implements ORTC for Windows 10 devices.</span></span> <span data-ttu-id="49203-107">No entanto, essa implementação é diferente da versão mais recente da [API ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span><span class="sxs-lookup"><span data-stu-id="49203-107">However, this implementation differs from the most recent version of the [ORTC API](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span></span> <span data-ttu-id="49203-108">ORTC continuou a evoluir desde o desenvolvimento e o lançamento do Microsoft Edge--o navegador não implementa todos os objetos ou métodos dentro da API ORTC e inclui extensões não incorporadas atualmente na especificação.</span><span class="sxs-lookup"><span data-stu-id="49203-108">ORTC has continued to evolve since the development and release of Microsoft Edge -- the browser does not implement every object or method within the ORTC API, and includes extensions not currently incorporated within the specification.</span></span> <span data-ttu-id="49203-109">Posteriormente, o desenvolvimento continuará com a meta para permitir que os desenvolvedores em todo o mundo criem experiências que incluam a capacidade de conversar com usuários do Skype e outros serviços de comunicação compatíveis com o WebRTC.</span><span class="sxs-lookup"><span data-stu-id="49203-109">Further development will continue with the goal to enable developers around the world to build experiences that include the ability to talk to Skype users and other WebRTC compatible communication services.</span></span>



<span data-ttu-id="49203-110">Para obter uma experiência prática com o ORTC, experimente estas demonstrações no Test Drive:</span><span class="sxs-lookup"><span data-stu-id="49203-110">To get a hands-on experience with ORTC, try out these demos on Test Drive:</span></span>
-  [<span data-ttu-id="49203-111">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="49203-111">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [<span data-ttu-id="49203-112">Chamada telefônica ORTC</span><span class="sxs-lookup"><span data-stu-id="49203-112">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [<span data-ttu-id="49203-113">Demonstração de ORTC</span><span class="sxs-lookup"><span data-stu-id="49203-113">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


<span data-ttu-id="49203-114">Para obter mais informações sobre ORTC, consulte o [API ORTC agora está disponível no Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) no blog de desenvolvimento do Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="49203-114">For more information about ORTC, check out [ORTC API is now available in Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) on the Microsoft Edge dev blog.</span></span>


## <span data-ttu-id="49203-115">Diagrama de visão geral</span><span class="sxs-lookup"><span data-stu-id="49203-115">Overview Diagram</span></span>


<span data-ttu-id="49203-116">O diagrama abaixo fornece um resumo descrevendo relações entre objetos ORTC.</span><span class="sxs-lookup"><span data-stu-id="49203-116">The diagram below provides a summary describing relationships between ORTC objects.</span></span> <span data-ttu-id="49203-117">As setas horizontais ou inclinadas indicam o fluxo de mídia ou dados, enquanto as setas verticais indicam interações por meio de métodos e eventos.</span><span class="sxs-lookup"><span data-stu-id="49203-117">Horizontal or slanted arrows denote the flow of media or data, whereas vertical arrows denote interactions via methods and events.</span></span>

<span data-ttu-id="49203-118">ORTC usa objetos "*Sender*", "*Receiver*" e "*Transport*", que têm "*recursos*" que descrevem o que são capazes de fazer, bem como "*parâmetros*", que definem o que eles estão configurados para fazer.</span><span class="sxs-lookup"><span data-stu-id="49203-118">ORTC uses "*sender*", "*receiver*" and "*transport*" objects, which have "*capabilities*" describing what they are capable of doing, as well as "*parameters*" which define what they are configured to do.</span></span> <span data-ttu-id="49203-119">"*Controla*" a captura e a codificação de fluxos de mídia por remetentes, a viagem por transportes e decodificados pelos receptores que renderizam as faixas de fluxo de mídia para marcas de vídeo/áudio.</span><span class="sxs-lookup"><span data-stu-id="49203-119">"*Tracks*" capture and encode media streams by senders, traveling over transports, then decoded by receivers that render the media stream tracks to video/audio tags.</span></span>

![<span data-ttu-id="49203-120">Diagrama de fluxo de ORTC do Microsoft Edge ](./../media/ortc_diagram.png) na figura acima, ele [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) codifica a faixa fornecida como entrada, que é transportada por uma [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) ou em um [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) .</span><span class="sxs-lookup"><span data-stu-id="49203-120">Microsoft Edge ORTC Flow Diagram](./../media/ortc_diagram.png) In the figure above, the [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) encodes the track provided as input, which is transported over a [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) or an [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527).</span></span> <span data-ttu-id="49203-121">Não há suporte para o envio de toques de radiofrequência (DTMF) de tom dual via [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .</span><span class="sxs-lookup"><span data-stu-id="49203-121">Sending of Dual Tone Multi Frequency (DTMF) tones is supported via the [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496).</span></span>

<span data-ttu-id="49203-122">O [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) e [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) usar um [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) caminho de comunicação para selecionar um caminho de comunicação para alcançar o par de recebimento `RTCIceTransport` , que, por sua vez, é associado a um `RTCDtlsTransport` ou `RTCSrtpSdesTransport` que desmultiplexa mídia para o [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="49203-122">The [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) and [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) utilize an [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) to select a communication path to reach the receiving peer's `RTCIceTransport`, which is in turn associated with an `RTCDtlsTransport` or `RTCSrtpSdesTransport` which de-multiplexes media to the [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span> <span data-ttu-id="49203-123">`RTCRtpReceiver`Em seguida, o decodifica mídia, produzindo uma faixa que é renderizada por uma marca de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="49203-123">The `RTCRtpReceiver` then decodes media, producing a track which is rendered by an audio or video tag.</span></span>

<span data-ttu-id="49203-124">Vários outros objetos também desempenham uma função.</span><span class="sxs-lookup"><span data-stu-id="49203-124">Several other objects also play a role.</span></span> <span data-ttu-id="49203-125">O [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) reúne candidatos de Ice locais para uso por um único [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) objeto.</span><span class="sxs-lookup"><span data-stu-id="49203-125">The [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) gathers local ICE candidates for use by a single [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) object.</span></span> <span data-ttu-id="49203-126">As seções restantes da API preenchem detalhes relacionados a *funcionalidades* e *parâmetros*de RTP, *estatísticas operacionais* e compatibilidade com a [API WebRTC 1,0](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span><span class="sxs-lookup"><span data-stu-id="49203-126">Remaining sections of the API fill in details relating to RTP *capabilities* and *parameters*, *operational statistics* and compatibility with the [WebRTC 1.0 API](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span></span>

> [!NOTE]
> <span data-ttu-id="49203-127">Como o Microsoft Edge não implementa o canal de dados, `RTCDataChannel` `RTCSctpTransport` não há suporte para objetos e objetos.</span><span class="sxs-lookup"><span data-stu-id="49203-127">Since Microsoft Edge does not implement the data channel, the `RTCDataChannel` and `RTCSctpTransport` objects are not supported.</span></span>




## <span data-ttu-id="49203-128">Componentes com suporte na implementação inicial do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="49203-128">Components supported in the initial Microsoft Edge implementation</span></span>


* **<span data-ttu-id="49203-129">Suporte à API ORTC.</span><span class="sxs-lookup"><span data-stu-id="49203-129">ORTC API support.</span></span>** <span data-ttu-id="49203-130">As comunicações de áudio/vídeo são o foco principal, incluindo os seguintes objetos:,,,, e [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) também as [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces que não são mostradas diretamente no diagrama.</span><span class="sxs-lookup"><span data-stu-id="49203-130">Audio/video communications is the primary focus, including the following objects: [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107), [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112), [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495), [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516), [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508), as well as the [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces that are not shown directly in the diagram.</span></span>
* **<span data-ttu-id="49203-131">Suporte para multiplexação RTP/RTCP.</span><span class="sxs-lookup"><span data-stu-id="49203-131">RTP/RTCP multiplexing support.</span></span>** <span data-ttu-id="49203-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)é necessário para uso com o [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) .</span><span class="sxs-lookup"><span data-stu-id="49203-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503) is required for use with the [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495).</span></span> <span data-ttu-id="49203-133">Também há suporte para A multiplexação de/V.</span><span class="sxs-lookup"><span data-stu-id="49203-133">A/V multiplexing is also supported.</span></span>
* **<span data-ttu-id="49203-134">Suporte STUN/TURN/ICE.</span><span class="sxs-lookup"><span data-stu-id="49203-134">STUN/TURN/ICE support.</span></span>** <span data-ttu-id="49203-135">Há suporte para STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) e Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621).</span><span class="sxs-lookup"><span data-stu-id="49203-135">STUN [(RFC 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), TURN [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) as well as ICE [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621), are supported.</span></span> <span data-ttu-id="49203-136">Na ICE, a indicações regulares tem suporte, com uma indicações agressiva parcialmente suportada (como um receptor).</span><span class="sxs-lookup"><span data-stu-id="49203-136">Within ICE, regular nomination is supported, with aggressive nomination partially supported (as a receiver).</span></span> <span data-ttu-id="49203-137">O DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) tem suporte, com base no DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span><span class="sxs-lookup"><span data-stu-id="49203-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) is supported, based on DTLS 1.0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span></span>
* **<span data-ttu-id="49203-138">Suporte a codecs.</span><span class="sxs-lookup"><span data-stu-id="49203-138">Codec support.</span></span>** <span data-ttu-id="49203-139">Para [codecs de áudio](https://msdn.microsoft.com/library/Mt599587), damos suporte a g. 711, g. 722, Opus e Silk.</span><span class="sxs-lookup"><span data-stu-id="49203-139">For [audio codecs](https://msdn.microsoft.com/library/Mt599587), we support G.711, G.722, Opus and SILK.</span></span> <span data-ttu-id="49203-140">Também suportamos ruído de conforto (CN) e DTMF de acordo com os requisitos de áudio do RTCWEB.</span><span class="sxs-lookup"><span data-stu-id="49203-140">We also support Comfort Noise (CN) and DTMF according to the RTCWEB audio requirements.</span></span> <span data-ttu-id="49203-141">Para o vídeo, atualmente damos suporte ao [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) codec usado pelos serviços da Skype, oferecendo suporte a recursos avançados, como a Simulcast, a codificação de vídeo dimensionável e a correção de erros de encaminhamento.</span><span class="sxs-lookup"><span data-stu-id="49203-141">For video we currently support the [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) codec used by Skype services, supporting advanced features such as simulcast, scalable video coding and forward error correction.</span></span> <span data-ttu-id="49203-142">Estamos nos empenhando para habilitar o vídeo interoperável com H. 264.</span><span class="sxs-lookup"><span data-stu-id="49203-142">We're working toward to enabling interoperable video with H.264.</span></span>

> [!NOTE]
> <span data-ttu-id="49203-143">Se você estiver familiarizado com as implementações do WebRTC 1,0 e estiver interessado na evolução do suporte a objetos dentro do WebRTC 1,0 e do ORTC, recomendamos a apresentação a seguir pelo Google, pela Microsoft e pela hookflash da 2014 RTC Conference: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".</span><span class="sxs-lookup"><span data-stu-id="49203-143">If you are familiar with WebRTC 1.0 implementations, and are interested in the evolution of object support within WebRTC 1.0 and ORTC, we recommend the following presentation by Google, Microsoft, and Hookflash from the 2014 IIT RTC Conference: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)."</span></span>




## <span data-ttu-id="49203-144">Fluxo de código de nível de aplicativo para comunicações do 1:1</span><span class="sxs-lookup"><span data-stu-id="49203-144">App level code flow for 1:1 communications</span></span>


<span data-ttu-id="49203-145">Para esse cenário, duas máquinas com o Windows 10 atuarão como dois pares com um servidor WebCOMO canal de sinalização para trocar informações entre os pares para que uma conexão possa ser estabelecida entre eles.</span><span class="sxs-lookup"><span data-stu-id="49203-145">For this scenario, two Windows 10 machines will act as two peers with a webserver as the signaling channel to exchange information between the peers so that a connection may be established between them.</span></span>

<span data-ttu-id="49203-146">As etapas a seguir têm o escopo das operações feitas por um par.</span><span class="sxs-lookup"><span data-stu-id="49203-146">The steps below are scoped to operations taken by one peer.</span></span> <span data-ttu-id="49203-147">Os dois pares devem passar por etapas semelhantes para configurar as comunicações do 1:1.</span><span class="sxs-lookup"><span data-stu-id="49203-147">Both peers must go through similar steps in order to set up the 1:1 communications.</span></span> <span data-ttu-id="49203-148">Para melhorar ainda mais os trechos de código a seguir, confira a [demonstração da unidade de teste do Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="49203-148">To make better sense out of the code snippets below, refer to the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

<span data-ttu-id="49203-149">Este exemplo usa a multiplexação de áudio-vídeo e RTP/RTCP, portanto, você verá apenas um único transporte ICE e DTLS, usado para transportar pacotes RTP e RTCP para áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="49203-149">This example uses audio-video and RTP/RTCP multiplexing, so you will see only a single ICE and DTLS transport, used to transport RTP and RTCP packets for both audio and video.</span></span>

`Step #1.` <span data-ttu-id="49203-150">Criar [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) objeto (ou seja, a [API de captura e fluxo de mídia](./../multimedia/media-Capture-and-Streams.md)) com uma faixa de áudio e uma faixa de vídeo.</span><span class="sxs-lookup"><span data-stu-id="49203-150">Create [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) object (i.e. [Media Capture and Streams API](./../multimedia/media-Capture-and-Streams.md)) with one audio track and one video track.</span></span>

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

`Step #2.` <span data-ttu-id="49203-151">Crie [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) e habilite local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) para ser sinalizado para o par remoto.</span><span class="sxs-lookup"><span data-stu-id="49203-151">Create the [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx), and enable local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) to be signaled to remote peer.</span></span>

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

<span data-ttu-id="49203-152">Para ajudar a proteger a privacidade do usuário, o Microsoft Edge introduz uma opção que permite que um usuário controle se os endereços IP de host locais podem ser expostos pelos [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objetos.</span><span class="sxs-lookup"><span data-stu-id="49203-152">To help protect user privacy, Microsoft Edge introduces an option that allows a user to control whether local host IP addresses can be exposed by the [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objects.</span></span> <span data-ttu-id="49203-153">Uma opção de interface será fornecida para alternar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="49203-153">An interface option will be provided to toggle this setting.</span></span>

<span data-ttu-id="49203-154">Na [demonstração da unidade de teste do Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635), foi configurada uma vez que o servidor foi configurado.</span><span class="sxs-lookup"><span data-stu-id="49203-154">In the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635), a TURN server has been set up.</span></span> <span data-ttu-id="49203-155">Esse servidor de ativação tem uma produtividade muito limitada, portanto, é limitado somente para uso da página de demonstração.</span><span class="sxs-lookup"><span data-stu-id="49203-155">This TURN server has a very limited throughput, so is limited to only demo page use.</span></span>

`Step #3.` <span data-ttu-id="49203-156">Crie o [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) para áudio e vídeo e prepare-se para manipular [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) o controle remoto no transporte Ice.</span><span class="sxs-lookup"><span data-stu-id="49203-156">Create the [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) for audio and video, and prepare to handle remote [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) on the ICE transport.</span></span>

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

<span data-ttu-id="49203-157">Outra opção é acumular todos os candidatos remotos do ICE em um array `remoteCandidates` e `iceTr.setRemoteCandidates(remoteCandidates)` fazer chamadas para adicionar todos os candidatos remotos juntos.</span><span class="sxs-lookup"><span data-stu-id="49203-157">Another option here is to accumulate all the remote ICE candidates into an array `remoteCandidates` and call `iceTr.setRemoteCandidates(remoteCandidates)` to add all the remote candidates together.</span></span>

`Step #4.` <span data-ttu-id="49203-158">Crie o transporte DTLS.</span><span class="sxs-lookup"><span data-stu-id="49203-158">Create the DTLS transport.</span></span>

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` <span data-ttu-id="49203-159">Crie os objetos do remetente e do destinatário.</span><span class="sxs-lookup"><span data-stu-id="49203-159">Create the sender and receiver objects.</span></span>

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

<span data-ttu-id="49203-160">Etapa #6.</span><span class="sxs-lookup"><span data-stu-id="49203-160">Step #6.</span></span> <span data-ttu-id="49203-161">Recupere os recursos de receptor e remetente.</span><span class="sxs-lookup"><span data-stu-id="49203-161">Retrieve the receiver and sender capabilities.</span></span>

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` <span data-ttu-id="49203-162">Os parâmetros ICE/DTLS e recursos de envio/recebimento podem ser trocados.</span><span class="sxs-lookup"><span data-stu-id="49203-162">ICE/DTLS parameters and Send/Receive capabilities can be exchanged.</span></span>

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

`Step #8.` <span data-ttu-id="49203-163">Obter parâmetros remotos, iniciar o [`ICE`](https://msdn.microsoft.com/library/Mt433112) e [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transportes e definir os parâmetros de envio e recebimento de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="49203-163">Get remote params, start the [`ICE`](https://msdn.microsoft.com/library/Mt433112) and [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transports, and set the audio and video send and receive parameters.</span></span>

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

<span data-ttu-id="49203-164">Veja a seguir um esqueleto das funções do auxiliar.</span><span class="sxs-lookup"><span data-stu-id="49203-164">Below is a skeleton of the helper functions.</span></span> <span data-ttu-id="49203-165">Encontre mais detalhes na [demonstração da unidade de teste do Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="49203-165">Find more details in the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

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

`Step #9.` <span data-ttu-id="49203-166">Renderize e reproduza o fluxo de mídia remoto acompanha uma marca de vídeo.</span><span class="sxs-lookup"><span data-stu-id="49203-166">Render and play the remote media stream tracks through a video tag.</span></span>

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

<span data-ttu-id="49203-167">Depois de familiarizar-se com a configuração de chamadas do 1:1, aplique os mesmos princípios para configurar chamadas em grupo pequenos usando uma topologia de malha, em que cada par terá uma conexão 1:1 com o restante do grupo.</span><span class="sxs-lookup"><span data-stu-id="49203-167">Once familiar with setting up 1:1 calls, apply the same principles to set up small group calls using a mesh topology, where each peer will have a 1:1 connection with the rest of the group.</span></span> <span data-ttu-id="49203-168">Como a bifurcação paralela não é suportada na plataforma Microsoft Edge, isso deve ser manipulado via sinalização 1:1, de modo que os [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objetos independentes e [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) objetos serão usados para cada conexão.</span><span class="sxs-lookup"><span data-stu-id="49203-168">Since parallel forking is not supported on the Microsoft Edge platform, this should be handled via 1:1 signaling, so that independent [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) and [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) objects will be used for each connection.</span></span>

## <span data-ttu-id="49203-169">Detalhes da implementação no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="49203-169">Implementation details in Microsoft Edge</span></span>


<span data-ttu-id="49203-170">A especificação ORTC foi relativamente estável, pois o grupo da Comunidade ORTC emitiu a "chamada para implementações", e desafios significativos no nível da API do JavaScript não são esperados.</span><span class="sxs-lookup"><span data-stu-id="49203-170">The ORTC spec has been relatively stable since the ORTC Community Group issued the "Call for Implementations," and significant challenges at the JavaScript API level are not expected.</span></span> <span data-ttu-id="49203-171">Com base nele, a implementação do Microsoft Edge foi lançada para testes de interoperabilidade entre navegadores no nível de protocolo.</span><span class="sxs-lookup"><span data-stu-id="49203-171">Based on this, Microsoft Edge implementation has been released for cross-browser interoperability testing at the protocol level.</span></span>

<span data-ttu-id="49203-172">Algumas limitações na implementação do Microsoft Edge devem ser observadas:</span><span class="sxs-lookup"><span data-stu-id="49203-172">A few limitations in the Microsoft Edge implementation should be noted:</span></span>

* `RTCIceTransportController` <span data-ttu-id="49203-173">Não é suportada.</span><span class="sxs-lookup"><span data-stu-id="49203-173">is not supported.</span></span> <span data-ttu-id="49203-174">A implementação do Microsoft Edge manipula o congelamento/descongelamento em uma base por transporte, para que o pedido de todas as outras `IceTransports` não seja necessário.</span><span class="sxs-lookup"><span data-stu-id="49203-174">Microsoft Edge implementation handles ICE freezing/unfreezing on a per-transport basis, so that ordering all the `IceTransports` is not necessary.</span></span> <span data-ttu-id="49203-175">Essa abordagem deve interoperar com implementações existentes.</span><span class="sxs-lookup"><span data-stu-id="49203-175">This approach should interoperate with existing implementations.</span></span>
* `RtpListener` <span data-ttu-id="49203-176">Ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="49203-176">is not yet supported.</span></span> <span data-ttu-id="49203-177">Isso significa que o SSRCs (origens de fluxo e sincronização) precisa ser especificado antecipadamente dentro do [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="49203-177">This means that SSRCs (stream and synchronization sources) need to be specified in advance within the [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span>
* <span data-ttu-id="49203-178">A bifurcação ainda não é suportada em um `IceTransport` `IceGatherer` ou mais `DtlsTransport` .</span><span class="sxs-lookup"><span data-stu-id="49203-178">Forking is not yet supported in either `IceTransport`, `IceGatherer`, or `DtlsTransport`.</span></span> <span data-ttu-id="49203-179">A solução para `DtlsTransport` bifurcação ainda está em discussão no grupo da Comunidade ORTC.</span><span class="sxs-lookup"><span data-stu-id="49203-179">The solution to `DtlsTransport` forking is still under discussion in the ORTC Community Group.</span></span>
* <span data-ttu-id="49203-180">Não há suporte para RTP/RTCP não-MUX com `DtlsTransport` ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="49203-180">RTP/RTCP non-mux with `DtlsTransport` is not yet supported.</span></span> <span data-ttu-id="49203-181">Ao usar `DtlsTransport` seu aplicativo, será necessário dar suporte a RTP/RTCP Mux.</span><span class="sxs-lookup"><span data-stu-id="49203-181">When using `DtlsTransport` your application will need to support RTP/RTCP mux.</span></span>
* <span data-ttu-id="49203-182">No [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) momento, o Microsoft Edge ignora a maioria dos controles de qualidade de codificação, mas exige a configuração dos atributos ' active ' e ' SSRC '.</span><span class="sxs-lookup"><span data-stu-id="49203-182">In [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx), Microsoft Edge currently ignores most of the encoding quality controls, but does require setting the 'active' and 'ssrc' attributes.</span></span>
* <span data-ttu-id="49203-183">O `icecandidatepairchanged` evento ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="49203-183">The `icecandidatepairchanged` event is not yet supported.</span></span> <span data-ttu-id="49203-184">Você pode extrair as informações de par de candidatos por meio do [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) método.</span><span class="sxs-lookup"><span data-stu-id="49203-184">You can extract the candidate pair information through the [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) method.</span></span>
* <span data-ttu-id="49203-185">Atualmente o Microsoft Edge não oferece suporte a nenhuma das `DataChannel` funcionalidades definidas atualmente na especificação ORTC.</span><span class="sxs-lookup"><span data-stu-id="49203-185">Microsoft Edge currently does not support any of the `DataChannel` functionality currently defined in the ORTC spec.</span></span>

#### <span data-ttu-id="49203-186">Olhando para o futuro</span><span class="sxs-lookup"><span data-stu-id="49203-186">Looking forward</span></span>

<span data-ttu-id="49203-187">A implementação do Microsoft Edge ainda está cedo, espere que o conjunto de recursos continue crescendo nos próximos meses.</span><span class="sxs-lookup"><span data-stu-id="49203-187">Microsoft Edge implementation is still early, expect the feature set to continue to grow in the coming months.</span></span> <span data-ttu-id="49203-188">O objetivo da implementação do Microsoft Edge é a interoperabilidade entre a Web hoje e também com o setor de comunicação em tempo real a longo prazo.</span><span class="sxs-lookup"><span data-stu-id="49203-188">The goal for Microsoft Edge implementation is interoperability across the web today as well as with the real-time communications industry in the long term.</span></span>



## <span data-ttu-id="49203-189">Referência de API</span><span class="sxs-lookup"><span data-stu-id="49203-189">API reference</span></span>

[<span data-ttu-id="49203-190">ORTC (comunicações em tempo real do objeto)</span><span class="sxs-lookup"><span data-stu-id="49203-190">ORTC (Object Real-Time Communications)</span></span>](https://msdn.microsoft.com/library/Mt433097)

## <span data-ttu-id="49203-191">Demonstrações</span><span class="sxs-lookup"><span data-stu-id="49203-191">Demos</span></span>

[<span data-ttu-id="49203-192">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="49203-192">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[<span data-ttu-id="49203-193">Chamada telefônica ORTC</span><span class="sxs-lookup"><span data-stu-id="49203-193">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[<span data-ttu-id="49203-194">Demonstração de ORTC</span><span class="sxs-lookup"><span data-stu-id="49203-194">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## <span data-ttu-id="49203-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49203-195">Related topics</span></span>

[<span data-ttu-id="49203-196">A API ORTC agora está disponível no Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="49203-196">ORTC API is now available in Microsoft Edge</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[<span data-ttu-id="49203-197">SimpleWebRTC: Use a API ORTC do Microsoft Edge e as APIs do WebRTC no Chrome e Firefox para fazer chamadas em conferência entre navegadores.</span><span class="sxs-lookup"><span data-stu-id="49203-197">SimpleWebRTC: Use Microsoft Edge's ORTC API and the WebRTC APIs in Chrome and Firefox to make cross-browser conference calls.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[<span data-ttu-id="49203-198">Habilitar experiências de comunicação contínua para a Web com o Skype, o Skype for Business e o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="49203-198">Enabling Seamless Communication Experiences for the Web with Skype, Skype for Business, and Microsoft Edge.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[<span data-ttu-id="49203-199">GRUPO DA COMUNIDADE ORTC (COMUNICAÇÕES EM TEMPO REAL DO OBJETO)</span><span class="sxs-lookup"><span data-stu-id="49203-199">ORTC (OBJECT REAL-TIME COMMUNICATIONS) COMMUNITY GROUP</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## <span data-ttu-id="49203-200">Especificada</span><span class="sxs-lookup"><span data-stu-id="49203-200">Specification</span></span>

[<span data-ttu-id="49203-201">API do objeto W3C RTC (ORTC) para WebRTC</span><span class="sxs-lookup"><span data-stu-id="49203-201">W3C Object RTC (ORTC) API for WebRTC</span></span>](http://draft.ortc.org/)  
