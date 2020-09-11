---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NewWindowRequestedEventHandler
ms.openlocfilehash: 99fb8261e6ed170b09bc87f9a1372e0e2cc53954
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011975"
---
# <span data-ttu-id="66e73-104">interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="66e73-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="66e73-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="66e73-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="66e73-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="66e73-106">Summary</span></span>

 <span data-ttu-id="66e73-107">Ses</span><span class="sxs-lookup"><span data-stu-id="66e73-107">Members</span></span>                        | <span data-ttu-id="66e73-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="66e73-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66e73-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="66e73-109">Invoke</span></span>](#invoke) | <span data-ttu-id="66e73-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="66e73-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="66e73-111">Ses</span><span class="sxs-lookup"><span data-stu-id="66e73-111">Members</span></span>

#### <span data-ttu-id="66e73-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="66e73-112">Invoke</span></span> 

<span data-ttu-id="66e73-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="66e73-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="66e73-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="66e73-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>
