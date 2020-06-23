---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 64f29f8c771a14d569fd45f7359614795bbc0386
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698738"
---
# <span data-ttu-id="c2cdc-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c2cdc-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c2cdc-105">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="c2cdc-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c2cdc-106">Summary</span></span>

 <span data-ttu-id="c2cdc-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c2cdc-107">Members</span></span>                        | <span data-ttu-id="c2cdc-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c2cdc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c2cdc-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c2cdc-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c2cdc-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c2cdc-111">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="c2cdc-112">Ses</span><span class="sxs-lookup"><span data-stu-id="c2cdc-112">Members</span></span>

#### <span data-ttu-id="c2cdc-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="c2cdc-113">Invoke</span></span> 

<span data-ttu-id="c2cdc-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c2cdc-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c2cdc-115">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c2cdc-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>
