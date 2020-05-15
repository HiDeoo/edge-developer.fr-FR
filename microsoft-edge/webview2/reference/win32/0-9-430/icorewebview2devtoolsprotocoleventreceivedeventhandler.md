---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: b786bae624b5f0649ec443e93f741975d672d0e0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653416"
---
# <span data-ttu-id="0bf9d-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0bf9d-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0bf9d-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="0bf9d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="0bf9d-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="0bf9d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="0bf9d-107">L’appelant implémente cette interface pour recevoir des événements DevToolsProtocolEventReceived du WebView.</span><span class="sxs-lookup"><span data-stu-id="0bf9d-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="0bf9d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="0bf9d-108">Summary</span></span>

 <span data-ttu-id="0bf9d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="0bf9d-109">Members</span></span>                        | <span data-ttu-id="0bf9d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0bf9d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0bf9d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="0bf9d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0bf9d-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="0bf9d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0bf9d-113">Ses</span><span class="sxs-lookup"><span data-stu-id="0bf9d-113">Members</span></span>

#### <span data-ttu-id="0bf9d-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="0bf9d-114">Invoke</span></span> 

<span data-ttu-id="0bf9d-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="0bf9d-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0bf9d-116">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0bf9d-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>
