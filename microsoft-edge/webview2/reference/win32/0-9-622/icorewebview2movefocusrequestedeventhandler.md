---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: 89b1e7fada56bcf535ae07be109acbb340fdc9a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011881"
---
# <span data-ttu-id="4af74-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4af74-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4af74-105">L’appelant implémente cette méthode pour recevoir l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="4af74-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="4af74-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="4af74-106">Summary</span></span>

 <span data-ttu-id="4af74-107">Ses</span><span class="sxs-lookup"><span data-stu-id="4af74-107">Members</span></span>                        | <span data-ttu-id="4af74-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4af74-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4af74-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4af74-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4af74-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4af74-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4af74-111">Ses</span><span class="sxs-lookup"><span data-stu-id="4af74-111">Members</span></span>

#### <span data-ttu-id="4af74-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4af74-112">Invoke</span></span> 

<span data-ttu-id="4af74-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4af74-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4af74-114">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4af74-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>
