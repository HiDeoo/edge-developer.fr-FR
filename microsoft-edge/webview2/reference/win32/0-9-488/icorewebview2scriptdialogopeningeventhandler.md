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
ms.openlocfilehash: 8451620cc819a6c2934efe80b241e7127861d48e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653656"
---
# <span data-ttu-id="a676e-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="a676e-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="a676e-105">L’appelant implémente cette interface pour recevoir l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="a676e-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="a676e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a676e-106">Summary</span></span>

 <span data-ttu-id="a676e-107">Ses</span><span class="sxs-lookup"><span data-stu-id="a676e-107">Members</span></span>                        | <span data-ttu-id="a676e-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a676e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a676e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a676e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a676e-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="a676e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a676e-111">Ses</span><span class="sxs-lookup"><span data-stu-id="a676e-111">Members</span></span>

#### <span data-ttu-id="a676e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a676e-112">Invoke</span></span> 

<span data-ttu-id="a676e-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="a676e-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a676e-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a676e-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>
