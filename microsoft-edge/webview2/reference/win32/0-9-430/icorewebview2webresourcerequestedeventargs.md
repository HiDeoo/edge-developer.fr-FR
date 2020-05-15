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
ms.openlocfilehash: 59557ca86e8b044fb937fe93b3060c0879abb6f1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653587"
---
# <span data-ttu-id="76832-104">interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="76832-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="76832-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="76832-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="76832-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="76832-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="76832-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="76832-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="76832-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="76832-108">Summary</span></span>

 <span data-ttu-id="76832-109">Ses</span><span class="sxs-lookup"><span data-stu-id="76832-109">Members</span></span>                        | <span data-ttu-id="76832-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="76832-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="76832-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="76832-111">get_Request</span></span>](#get_request) | <span data-ttu-id="76832-112">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="76832-112">The HTTP request.</span></span>
[<span data-ttu-id="76832-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="76832-113">get_Response</span></span>](#get_response) | <span data-ttu-id="76832-114">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="76832-114">The HTTP response.</span></span>
[<span data-ttu-id="76832-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="76832-115">put_Response</span></span>](#put_response) | <span data-ttu-id="76832-116">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="76832-116">Set the Response property.</span></span>
[<span data-ttu-id="76832-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="76832-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="76832-118">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="76832-118">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="76832-119">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="76832-119">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="76832-120">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="76832-120">The web resource request contexts.</span></span>

## <span data-ttu-id="76832-121">Ses</span><span class="sxs-lookup"><span data-stu-id="76832-121">Members</span></span>

#### <span data-ttu-id="76832-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="76832-122">get_Request</span></span> 

<span data-ttu-id="76832-123">La requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="76832-123">The HTTP request.</span></span>

> <span data-ttu-id="76832-124">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="76832-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="76832-125">get_Response</span><span class="sxs-lookup"><span data-stu-id="76832-125">get_Response</span></span> 

<span data-ttu-id="76832-126">Réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="76832-126">The HTTP response.</span></span>

> <span data-ttu-id="76832-127">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="76832-127">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="76832-128">put_Response</span><span class="sxs-lookup"><span data-stu-id="76832-128">put_Response</span></span> 

<span data-ttu-id="76832-129">Définissez la propriété Response.</span><span class="sxs-lookup"><span data-stu-id="76832-129">Set the Response property.</span></span>

> <span data-ttu-id="76832-130">[put_Response](#put_response)par le biais du public[HRESULT (réponse](ICoreWebView2WebResourceResponse.md) )</span><span class="sxs-lookup"><span data-stu-id="76832-130">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="76832-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="76832-131">GetDeferral</span></span> 

<span data-ttu-id="76832-132">Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="76832-132">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="76832-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="76832-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="76832-134">Vous pouvez utiliser l’objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) pour terminer la requête réseau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="76832-134">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="76832-135">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="76832-135">get_ResourceContext</span></span> 

<span data-ttu-id="76832-136">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="76832-136">The web resource request contexts.</span></span>

> <span data-ttu-id="76832-137">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="76832-137">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>
