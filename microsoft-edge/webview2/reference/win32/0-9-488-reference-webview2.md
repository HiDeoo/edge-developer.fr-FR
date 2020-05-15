---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Applications WebView 2 de Microsoft Edge 2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: d7e38f25a3e58d21744c8631319f553f2b0962fb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653610"
---
# <span data-ttu-id="929ac-104">Référence (WebView2)</span><span class="sxs-lookup"><span data-stu-id="929ac-104">Reference (WebView2)</span></span>  

<span data-ttu-id="929ac-105">Le contrôle Microsoft Edge WebView2 vous permet d’héberger le contenu Web de votre application à l’aide de [Microsoft Edge \ (chrome \)](https://www.microsoftedgeinsider.com) en tant que moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="929ac-105">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge \(Chromium\)](https://www.microsoftedgeinsider.com) as the rendering engine.</span></span>  <span data-ttu-id="929ac-106">Pour plus d’informations, voir [vue d’ensemble de Microsoft Edge WebView2](../../index.md)) et [mise en route d’WebView2](../../gettingstarted/win32.md).</span><span class="sxs-lookup"><span data-stu-id="929ac-106">For more information, see [Overview of Microsoft Edge WebView2](../../index.md)) and [Getting Started with WebView2](../../gettingstarted/win32.md).</span></span>  <span data-ttu-id="929ac-107">[ICoreWebView2](0-9-488/ICoreWebView2.md) est l’endroit idéal pour commencer à apprendre les détails de l’API.</span><span class="sxs-lookup"><span data-stu-id="929ac-107">[ICoreWebView2](0-9-488/ICoreWebView2.md) is a great place to start learning the details of the API.</span></span>  

## <span data-ttu-id="929ac-108">Globales</span><span class="sxs-lookup"><span data-stu-id="929ac-108">Globals</span></span>  

*   [<span data-ttu-id="929ac-109">Globales</span><span class="sxs-lookup"><span data-stu-id="929ac-109">Globals</span></span>](0-9-430/webview2-idl.md)  

## <span data-ttu-id="929ac-110">Implément</span><span class="sxs-lookup"><span data-stu-id="929ac-110">Interfaces</span></span>  
*   [<span data-ttu-id="929ac-111">ICoreWebView2</span><span class="sxs-lookup"><span data-stu-id="929ac-111">ICoreWebView2</span></span>](0-9-488/icorewebview2.md)
*   [<span data-ttu-id="929ac-112">ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="929ac-112">ICoreWebView2Controller</span></span>](0-9-488/icorewebview2controller.md)
*   [<span data-ttu-id="929ac-113">ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="929ac-113">ICoreWebView2Deferral</span></span>](0-9-488/icorewebview2deferral.md)
*   [<span data-ttu-id="929ac-114">ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="929ac-114">ICoreWebView2DevToolsProtocolEventReceiver</span></span>](0-9-488/icorewebview2devtoolsprotocoleventreceiver.md)
*   [<span data-ttu-id="929ac-115">ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="929ac-115">ICoreWebView2Environment</span></span>](0-9-488/icorewebview2environment.md)
*   [<span data-ttu-id="929ac-116">ICoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="929ac-116">ICoreWebView2EnvironmentOptions</span></span>](0-9-488/icorewebview2environmentoptions.md)
*   [<span data-ttu-id="929ac-117">ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="929ac-117">ICoreWebView2HttpHeadersCollectionIterator</span></span>](0-9-488/icorewebview2httpheaderscollectioniterator.md)
*   [<span data-ttu-id="929ac-118">ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="929ac-118">ICoreWebView2HttpRequestHeaders</span></span>](0-9-488/icorewebview2httprequestheaders.md)
*   [<span data-ttu-id="929ac-119">ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="929ac-119">ICoreWebView2HttpResponseHeaders</span></span>](0-9-488/icorewebview2httpresponseheaders.md)
*   [<span data-ttu-id="929ac-120">ICoreWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="929ac-120">ICoreWebView2Settings</span></span>](0-9-488/icorewebview2settings.md)
*   [<span data-ttu-id="929ac-121">ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="929ac-121">ICoreWebView2WebResourceRequest</span></span>](0-9-488/icorewebview2webresourcerequest.md)
*   [<span data-ttu-id="929ac-122">ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="929ac-122">ICoreWebView2WebResourceResponse</span></span>](0-9-488/icorewebview2webresourceresponse.md)

### <span data-ttu-id="929ac-123">Arguments d’événement</span><span class="sxs-lookup"><span data-stu-id="929ac-123">Event arguments</span></span>

*   [<span data-ttu-id="929ac-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-124">ICoreWebView2AcceleratorKeyPressedEventArgs</span></span>](0-9-488/icorewebview2acceleratorkeypressedeventargs.md)
*   [<span data-ttu-id="929ac-125">ICoreWebView2ContentLoadingEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-125">ICoreWebView2ContentLoadingEventArgs</span></span>](0-9-488/icorewebview2contentloadingeventargs.md)
*   [<span data-ttu-id="929ac-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-126">ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span>](0-9-488/icorewebview2devtoolsprotocoleventreceivedeventargs.md)
*   [<span data-ttu-id="929ac-127">ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-127">ICoreWebView2MoveFocusRequestedEventArgs</span></span>](0-9-488/icorewebview2movefocusrequestedeventargs.md)
*   [<span data-ttu-id="929ac-128">ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-128">ICoreWebView2NavigationCompletedEventArgs</span></span>](0-9-488/icorewebview2navigationcompletedeventargs.md)
*   [<span data-ttu-id="929ac-129">ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-129">ICoreWebView2NavigationStartingEventArgs</span></span>](0-9-488/icorewebview2navigationstartingeventargs.md)
*   [<span data-ttu-id="929ac-130">ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-130">ICoreWebView2NewWindowRequestedEventArgs</span></span>](0-9-488/icorewebview2newwindowrequestedeventargs.md)
*   [<span data-ttu-id="929ac-131">ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-131">ICoreWebView2PermissionRequestedEventArgs</span></span>](0-9-488/icorewebview2permissionrequestedeventargs.md)
*   [<span data-ttu-id="929ac-132">ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-132">ICoreWebView2ProcessFailedEventArgs</span></span>](0-9-488/icorewebview2processfailedeventargs.md)
*   [<span data-ttu-id="929ac-133">ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-133">ICoreWebView2ScriptDialogOpeningEventArgs</span></span>](0-9-488/icorewebview2scriptdialogopeningeventargs.md)
*   [<span data-ttu-id="929ac-134">ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-134">ICoreWebView2SourceChangedEventArgs</span></span>](0-9-488/icorewebview2sourcechangedeventargs.md)
*   [<span data-ttu-id="929ac-135">ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-135">ICoreWebView2WebMessageReceivedEventArgs</span></span>](0-9-488/icorewebview2webmessagereceivedeventargs.md)
*   [<span data-ttu-id="929ac-136">ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="929ac-136">ICoreWebView2WebResourceRequestedEventArgs</span></span>](0-9-488/icorewebview2webresourcerequestedeventargs.md)

### <span data-ttu-id="929ac-137">Délégués</span><span class="sxs-lookup"><span data-stu-id="929ac-137">Delegates</span></span>

*   [<span data-ttu-id="929ac-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-138">ICoreWebView2AcceleratorKeyPressedEventHandler</span></span>](0-9-488/icorewebview2acceleratorkeypressedeventhandler.md)
*   [<span data-ttu-id="929ac-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-139">ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span>](0-9-488/icorewebview2addscripttoexecuteondocumentcreatedcompletedhandler.md)
*   [<span data-ttu-id="929ac-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-140">ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span>](0-9-488/icorewebview2calldevtoolsprotocolmethodcompletedhandler.md)
*   [<span data-ttu-id="929ac-141">ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-141">ICoreWebView2CapturePreviewCompletedHandler</span></span>](0-9-488/icorewebview2capturepreviewcompletedhandler.md)
*   [<span data-ttu-id="929ac-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-142">ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span>](0-9-488/icorewebview2containsfullscreenelementchangedeventhandler.md)
*   [<span data-ttu-id="929ac-143">ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-143">ICoreWebView2ContentLoadingEventHandler</span></span>](0-9-488/icorewebview2contentloadingeventhandler.md)
*   [<span data-ttu-id="929ac-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-144">ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span>](0-9-488/icorewebview2createcorewebview2controllercompletedhandler.md)
*   [<span data-ttu-id="929ac-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-145">ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span>](0-9-488/icorewebview2createcorewebview2environmentcompletedhandler.md)
*   [<span data-ttu-id="929ac-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-146">ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span>](0-9-488/icorewebview2devtoolsprotocoleventreceivedeventhandler.md)
*   [<span data-ttu-id="929ac-147">ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-147">ICoreWebView2DocumentTitleChangedEventHandler</span></span>](0-9-488/icorewebview2documenttitlechangedeventhandler.md)
*   [<span data-ttu-id="929ac-148">ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-148">ICoreWebView2ExecuteScriptCompletedHandler</span></span>](0-9-488/icorewebview2executescriptcompletedhandler.md)
*   [<span data-ttu-id="929ac-149">ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-149">ICoreWebView2FocusChangedEventHandler</span></span>](0-9-488/icorewebview2focuschangedeventhandler.md)
*   [<span data-ttu-id="929ac-150">ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-150">ICoreWebView2HistoryChangedEventHandler</span></span>](0-9-488/icorewebview2historychangedeventhandler.md)
*   [<span data-ttu-id="929ac-151">ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-151">ICoreWebView2MoveFocusRequestedEventHandler</span></span>](0-9-488/icorewebview2movefocusrequestedeventhandler.md)
*   [<span data-ttu-id="929ac-152">ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-152">ICoreWebView2NavigationCompletedEventHandler</span></span>](0-9-488/icorewebview2navigationcompletedeventhandler.md)
*   [<span data-ttu-id="929ac-153">ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-153">ICoreWebView2NavigationStartingEventHandler</span></span>](0-9-488/icorewebview2navigationstartingeventhandler.md)
*   [<span data-ttu-id="929ac-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-154">ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span>](0-9-488/icorewebview2newbrowserversionavailableeventhandler.md)
*   [<span data-ttu-id="929ac-155">ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-155">ICoreWebView2NewWindowRequestedEventHandler</span></span>](0-9-488/icorewebview2newwindowrequestedeventhandler.md)
*   [<span data-ttu-id="929ac-156">ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-156">ICoreWebView2PermissionRequestedEventHandler</span></span>](0-9-488/icorewebview2permissionrequestedeventhandler.md)
*   [<span data-ttu-id="929ac-157">ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-157">ICoreWebView2ProcessFailedEventHandler</span></span>](0-9-488/icorewebview2processfailedeventhandler.md)
*   [<span data-ttu-id="929ac-158">ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-158">ICoreWebView2ScriptDialogOpeningEventHandler</span></span>](0-9-488/icorewebview2scriptdialogopeningeventhandler.md)
*   [<span data-ttu-id="929ac-159">ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-159">ICoreWebView2SourceChangedEventHandler</span></span>](0-9-488/icorewebview2sourcechangedeventhandler.md)
*   [<span data-ttu-id="929ac-160">ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-160">ICoreWebView2WebMessageReceivedEventHandler</span></span>](0-9-488/icorewebview2webmessagereceivedeventhandler.md)
*   [<span data-ttu-id="929ac-161">ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-161">ICoreWebView2WebResourceRequestedEventHandler</span></span>](0-9-488/icorewebview2webresourcerequestedeventhandler.md)
*   [<span data-ttu-id="929ac-162">ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-162">ICoreWebView2WindowCloseRequestedEventHandler</span></span>](0-9-488/icorewebview2windowcloserequestedeventhandler.md)
*   [<span data-ttu-id="929ac-163">ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-163">ICoreWebView2ZoomFactorChangedEventHandler</span></span>](0-9-488/icorewebview2zoomfactorchangedeventhandler.md)

### <span data-ttu-id="929ac-164">Pratiqué</span><span class="sxs-lookup"><span data-stu-id="929ac-164">Experimental</span></span>

*   [<span data-ttu-id="929ac-165">ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="929ac-165">ICoreWebView2ExperimentalCompositionController</span></span>](0-9-488/icorewebview2experimentalcompositioncontroller.md)
*   [<span data-ttu-id="929ac-166">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-166">ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span>](0-9-488/icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md)
*   [<span data-ttu-id="929ac-167">ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="929ac-167">ICoreWebView2ExperimentalCursorChangedEventHandler</span></span>](0-9-488/icorewebview2experimentalcursorchangedeventhandler.md)
*   [<span data-ttu-id="929ac-168">ICoreWebView2ExperimentalEnvironment</span><span class="sxs-lookup"><span data-stu-id="929ac-168">ICoreWebView2ExperimentalEnvironment</span></span>](0-9-488/icorewebview2experimentalenvironment.md)
*   [<span data-ttu-id="929ac-169">ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="929ac-169">ICoreWebView2ExperimentalPointerInfo</span></span>](0-9-488/icorewebview2experimentalpointerinfo.md)