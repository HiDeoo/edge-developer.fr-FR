---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: d669b73edd8def1d8a44491705e0f80888da2b3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653459"
---
# <span data-ttu-id="0d74b-104">interface IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0d74b-104">interface IWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0d74b-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0d74b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0d74b-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="0d74b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="0d74b-107">L’appelant implémente cette interface pour recevoir l’événement PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0d74b-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="0d74b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="0d74b-108">Summary</span></span>

 <span data-ttu-id="0d74b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="0d74b-109">Members</span></span>                        | <span data-ttu-id="0d74b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0d74b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0d74b-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d74b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0d74b-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="0d74b-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0d74b-113">Ses</span><span class="sxs-lookup"><span data-stu-id="0d74b-113">Members</span></span>

#### <span data-ttu-id="0d74b-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d74b-114">Invoke</span></span> 

<span data-ttu-id="0d74b-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="0d74b-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0d74b-116">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0d74b-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>
