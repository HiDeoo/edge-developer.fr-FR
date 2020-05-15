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
ms.openlocfilehash: 85de243c00364f7fb57d3842b2ddbf78848905f6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653589"
---
# <span data-ttu-id="f9c18-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f9c18-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f9c18-105">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="f9c18-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="f9c18-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f9c18-106">Summary</span></span>

 <span data-ttu-id="f9c18-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f9c18-107">Members</span></span>                        | <span data-ttu-id="f9c18-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f9c18-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f9c18-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f9c18-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f9c18-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f9c18-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f9c18-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="f9c18-111">There are no event args for this event.</span></span>

## <span data-ttu-id="f9c18-112">Ses</span><span class="sxs-lookup"><span data-stu-id="f9c18-112">Members</span></span>

#### <span data-ttu-id="f9c18-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="f9c18-113">Invoke</span></span> 

<span data-ttu-id="f9c18-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f9c18-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f9c18-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f9c18-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f9c18-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f9c18-116">There are no event args and the args parameter will be null.</span></span>
