---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 06f7f664acb5f169215b603841d935730532b62b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653431"
---
# <span data-ttu-id="02c03-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="02c03-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="02c03-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="02c03-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="02c03-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="02c03-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="02c03-107">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="02c03-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="02c03-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="02c03-108">Summary</span></span>

 <span data-ttu-id="02c03-109">Ses</span><span class="sxs-lookup"><span data-stu-id="02c03-109">Members</span></span>                        | <span data-ttu-id="02c03-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="02c03-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="02c03-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="02c03-111">Invoke</span></span>](#invoke) | <span data-ttu-id="02c03-112">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="02c03-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="02c03-113">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="02c03-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="02c03-114">Ses</span><span class="sxs-lookup"><span data-stu-id="02c03-114">Members</span></span>

#### <span data-ttu-id="02c03-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="02c03-115">Invoke</span></span> 

<span data-ttu-id="02c03-116">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="02c03-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="02c03-117">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="02c03-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>
