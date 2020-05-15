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
ms.openlocfilehash: 8ed1a10a65a07fc359deea18b8aadd4df3a7b055
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653687"
---
# <span data-ttu-id="b9bf4-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="b9bf4-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b9bf4-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b9bf4-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="b9bf4-107">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="b9bf4-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b9bf4-108">Summary</span></span>

 <span data-ttu-id="b9bf4-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b9bf4-109">Members</span></span>                        | <span data-ttu-id="b9bf4-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b9bf4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9bf4-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b9bf4-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b9bf4-112">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="b9bf4-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="b9bf4-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="b9bf4-114">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="b9bf4-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="b9bf4-115">get_Message</span></span>](#get_message) | <span data-ttu-id="b9bf4-116">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-116">The message of the dialog box.</span></span>
[<span data-ttu-id="b9bf4-117">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-117">Accept</span></span>](#accept) | <span data-ttu-id="b9bf4-118">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="b9bf4-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="b9bf4-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="b9bf4-120">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="b9bf4-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="b9bf4-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="b9bf4-122">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="b9bf4-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="b9bf4-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="b9bf4-124">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-124">Set the ResultText property.</span></span>
[<span data-ttu-id="b9bf4-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b9bf4-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b9bf4-126">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b9bf4-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="b9bf4-127">Ses</span><span class="sxs-lookup"><span data-stu-id="b9bf4-127">Members</span></span>

#### <span data-ttu-id="b9bf4-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b9bf4-128">get_Uri</span></span> 

<span data-ttu-id="b9bf4-129">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="b9bf4-130">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b9bf4-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="b9bf4-131">get_Kind</span></span> 

<span data-ttu-id="b9bf4-132">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="b9bf4-133">[get_Kinds](#get_kind)par valeur public HRESULT (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* type)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="b9bf4-134">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="b9bf4-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="b9bf4-135">get_Message</span></span> 

<span data-ttu-id="b9bf4-136">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-136">The message of the dialog box.</span></span>

> <span data-ttu-id="b9bf4-137">valeur publique HRESULT [get_Message](#get_message)(LPWSTR \* message)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="b9bf4-138">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="b9bf4-139">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-139">Accept</span></span> 

<span data-ttu-id="b9bf4-140">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="b9bf4-141">[acceptation](#accept)publique HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="b9bf4-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="b9bf4-142">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="b9bf4-143">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="b9bf4-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="b9bf4-144">get_DefaultText</span></span> 

<span data-ttu-id="b9bf4-145">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="b9bf4-146">valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="b9bf4-147">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="b9bf4-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="b9bf4-148">get_ResultText</span></span> 

<span data-ttu-id="b9bf4-149">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="b9bf4-150">valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="b9bf4-151">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="b9bf4-152">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="b9bf4-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="b9bf4-153">put_ResultText</span></span> 

<span data-ttu-id="b9bf4-154">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-154">Set the ResultText property.</span></span>

> <span data-ttu-id="b9bf4-155">[put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="b9bf4-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b9bf4-156">GetDeferral</span></span> 

<span data-ttu-id="b9bf4-157">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b9bf4-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="b9bf4-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="b9bf4-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b9bf4-159">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b9bf4-159">You can use this to complete the event at a later time.</span></span>
