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
ms.openlocfilehash: d6b51600479f47eebb09d5cff8fb096455fb1766
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653304"
---
# <span data-ttu-id="eeaaa-104">interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="eeaaa-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="eeaaa-105">Réponse HTTP utilisée avec l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="eeaaa-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="eeaaa-106">Summary</span></span>

 <span data-ttu-id="eeaaa-107">Ses</span><span class="sxs-lookup"><span data-stu-id="eeaaa-107">Members</span></span>                        | <span data-ttu-id="eeaaa-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="eeaaa-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eeaaa-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="eeaaa-109">get_Content</span></span>](#get_content) | <span data-ttu-id="eeaaa-110">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="eeaaa-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="eeaaa-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="eeaaa-112">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="eeaaa-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="eeaaa-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="eeaaa-114">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="eeaaa-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="eeaaa-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="eeaaa-116">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-116">The HTTP response status code.</span></span>
[<span data-ttu-id="eeaaa-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="eeaaa-117">put_Content</span></span>](#put_content) | <span data-ttu-id="eeaaa-118">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-118">Set the Content property.</span></span>
[<span data-ttu-id="eeaaa-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="eeaaa-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="eeaaa-120">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="eeaaa-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="eeaaa-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="eeaaa-122">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="eeaaa-123">Ses</span><span class="sxs-lookup"><span data-stu-id="eeaaa-123">Members</span></span>

#### <span data-ttu-id="eeaaa-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="eeaaa-124">get_Content</span></span> 

<span data-ttu-id="eeaaa-125">Contenu de réponse HTTP en tant que flux.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="eeaaa-126">accès public HRESULT [get_Content](#get_content)(IStream \* \* content)</span><span class="sxs-lookup"><span data-stu-id="eeaaa-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="eeaaa-127">Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="eeaaa-128">Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="eeaaa-129">Null signifie qu’il n’y a pas de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-129">Null means no content data.</span></span> <span data-ttu-id="eeaaa-130">La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)</span><span class="sxs-lookup"><span data-stu-id="eeaaa-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="eeaaa-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="eeaaa-131">get_Headers</span></span> 

<span data-ttu-id="eeaaa-132">En-têtes de réponse HTTP ignorés.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="eeaaa-133">[get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httpresponseheaders.md) -têtes \* \*)</span><span class="sxs-lookup"><span data-stu-id="eeaaa-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="eeaaa-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="eeaaa-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="eeaaa-135">Expression de raison de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="eeaaa-136">valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="eeaaa-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="eeaaa-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="eeaaa-137">get_StatusCode</span></span> 

<span data-ttu-id="eeaaa-138">Code d’état de réponse HTTP.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-138">The HTTP response status code.</span></span>

> <span data-ttu-id="eeaaa-139">valeur publique HRESULT [get_StatusCode](#get_statuscode)</span><span class="sxs-lookup"><span data-stu-id="eeaaa-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="eeaaa-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="eeaaa-140">put_Content</span></span> 

<span data-ttu-id="eeaaa-141">Définissez la propriété Content.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-141">Set the Content property.</span></span>

> <span data-ttu-id="eeaaa-142">[put_Content](#put_content)par le biais du contenu public HRESULT</span><span class="sxs-lookup"><span data-stu-id="eeaaa-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="eeaaa-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="eeaaa-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="eeaaa-144">Définissez la propriété ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="eeaaa-145">[put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="eeaaa-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="eeaaa-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="eeaaa-146">put_StatusCode</span></span> 

<span data-ttu-id="eeaaa-147">Définissez la propriété StatusCode.</span><span class="sxs-lookup"><span data-stu-id="eeaaa-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="eeaaa-148">[put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)</span><span class="sxs-lookup"><span data-stu-id="eeaaa-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>
