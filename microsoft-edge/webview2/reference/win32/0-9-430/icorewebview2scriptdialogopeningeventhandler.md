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
ms.openlocfilehash: a9cc4c9e2bd13509c25fa5f5faaa9fe65634b47b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653489"
---
# <span data-ttu-id="35154-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="35154-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="35154-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="35154-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="35154-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="35154-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="35154-107">L’appelant implémente cette interface pour recevoir l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="35154-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="35154-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="35154-108">Summary</span></span>

 <span data-ttu-id="35154-109">Ses</span><span class="sxs-lookup"><span data-stu-id="35154-109">Members</span></span>                        | <span data-ttu-id="35154-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="35154-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35154-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="35154-111">Invoke</span></span>](#invoke) | <span data-ttu-id="35154-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="35154-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="35154-113">Ses</span><span class="sxs-lookup"><span data-stu-id="35154-113">Members</span></span>

#### <span data-ttu-id="35154-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="35154-114">Invoke</span></span> 

<span data-ttu-id="35154-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="35154-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="35154-116">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="35154-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>
