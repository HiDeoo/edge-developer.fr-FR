---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9196f2d9503efbaf9f15b43e7e6d7e80c2de00f7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653514"
---
# <span data-ttu-id="d9fef-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="d9fef-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="d9fef-105">L’appelant implémente cette interface pour recevoir des événements NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="d9fef-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="d9fef-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d9fef-106">Summary</span></span>

 <span data-ttu-id="d9fef-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d9fef-107">Members</span></span>                        | <span data-ttu-id="d9fef-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d9fef-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9fef-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9fef-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d9fef-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d9fef-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d9fef-111">Ses</span><span class="sxs-lookup"><span data-stu-id="d9fef-111">Members</span></span>

#### <span data-ttu-id="d9fef-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9fef-112">Invoke</span></span> 

<span data-ttu-id="d9fef-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d9fef-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d9fef-114">[appel](#invoke)HRESULT public ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d9fef-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>
