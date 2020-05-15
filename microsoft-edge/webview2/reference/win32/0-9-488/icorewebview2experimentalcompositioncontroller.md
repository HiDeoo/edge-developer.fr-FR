---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: e6499c77a17fd9ff4563359cdf05dc4a32f19a51
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653465"
---
# <span data-ttu-id="6a02b-104">interface ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="6a02b-104">interface ICoreWebView2ExperimentalCompositionController</span></span> 

> [!NOTE]
> <span data-ttu-id="6a02b-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="6a02b-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="6a02b-106">Cette interface est une extension de l’interface ICoreWebView2Controller pour prendre en charge l’hébergement visuel.</span><span class="sxs-lookup"><span data-stu-id="6a02b-106">This interface is an extension of the ICoreWebView2Controller interface to support visual hosting.</span></span>

## <span data-ttu-id="6a02b-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="6a02b-107">Summary</span></span>

 <span data-ttu-id="6a02b-108">Ses</span><span class="sxs-lookup"><span data-stu-id="6a02b-108">Members</span></span>                        | <span data-ttu-id="6a02b-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6a02b-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6a02b-110">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="6a02b-110">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="6a02b-111">Ajoutez un gestionnaire d’événements pour l’événement CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="6a02b-111">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="6a02b-112">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="6a02b-112">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="6a02b-113">Fonction d’assistance permettant de convertir un pointerId reçu du système en [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="6a02b-113">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="6a02b-114">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="6a02b-114">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="6a02b-115">Le curseur actuel attendu par le WebView devrait être.</span><span class="sxs-lookup"><span data-stu-id="6a02b-115">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="6a02b-116">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="6a02b-116">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="6a02b-117">Le RootVisualTarget est un élément visuel de l’arborescence visuelle de l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="6a02b-117">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="6a02b-118">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="6a02b-118">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="6a02b-119">Renvoie le fournisseur UI Automation pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-119">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="6a02b-120">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="6a02b-120">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="6a02b-121">Définissez la propriété RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="6a02b-121">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="6a02b-122">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="6a02b-122">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="6a02b-123">Supprimez un gestionnaire d’événements préalablement ajouté à add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="6a02b-123">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="6a02b-124">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="6a02b-124">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="6a02b-125">Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData spécifie la quantité de mouvement du volant.</span><span class="sxs-lookup"><span data-stu-id="6a02b-125">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="6a02b-126">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="6a02b-126">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="6a02b-127">SendPointerInput accepte les entrées de pointeur en forme d’effleurement ou de stylet définies dans COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="6a02b-127">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="6a02b-128">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="6a02b-128">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="6a02b-129">Matrice qui représente une transformation 3D.</span><span class="sxs-lookup"><span data-stu-id="6a02b-129">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="6a02b-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="6a02b-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="6a02b-131">Type d’événement de souris utilisé par SendMouseInput pour transmettre le type d’événement de souris envoyé à WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-131">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="6a02b-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="6a02b-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="6a02b-133">Touches virtuelles d’événement de souris associées à une COREWEBVIEW2_MOUSE_EVENT_KIND pour SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="6a02b-133">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="6a02b-134">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="6a02b-134">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="6a02b-135">Type d’événement de pointeur utilisé par SendPointerInput pour transmettre le type d’événement de pointeur envoyé à WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-135">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="6a02b-136">Un objet qui implémente l’interface ICoreWebView2ExperimentalCompositionController implémente également ICoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="6a02b-136">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement ICoreWebView2Controller.</span></span> <span data-ttu-id="6a02b-137">Les appelants peuvent utiliser ICoreWebView2Controller pour le redimensionnement, la visibilité, le focus, etc., puis utiliser ICoreWebView2ExperimentalCompositionController pour se connecter à une arborescence de composition et fournir des entrées destinées au WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-137">Callers are expected to use ICoreWebView2Controller for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="6a02b-138">Ses</span><span class="sxs-lookup"><span data-stu-id="6a02b-138">Members</span></span>

#### <span data-ttu-id="6a02b-139">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="6a02b-139">add_CursorChanged</span></span> 

<span data-ttu-id="6a02b-140">Ajoutez un gestionnaire d’événements pour l’événement CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="6a02b-140">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="6a02b-141">[add_CursorChanged](#add_cursorchanged)par le biais du[mot de passe](icorewebview2experimentalcursorchangedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="6a02b-141">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="6a02b-142">L’événement se déclenche lorsque WebView considère que le curseur doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="6a02b-142">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="6a02b-143">Par exemple, lorsque le curseur de la souris est actuellement le curseur par défaut, mais qu’il est alors déplacé sur du texte, il peut essayer de basculer vers le curseur IBeam.</span><span class="sxs-lookup"><span data-stu-id="6a02b-143">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                       IUnknown* args) -> HRESULT {
                    HCURSOR cursor;
                    CHECK_FAILURE(sender->get_Cursor(&cursor));
                    SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    return S_OK;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### <span data-ttu-id="6a02b-144">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="6a02b-144">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="6a02b-145">Fonction d’assistance permettant de convertir un pointerId reçu du système en [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="6a02b-145">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="6a02b-146">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND FenêtreParent, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="6a02b-146">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="6a02b-147">FenêtreParent est le HWND qui contient le WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-147">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="6a02b-148">Il peut s’agir d’un HWND de l’arborescence HWND qui contient le WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-148">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="6a02b-149">Le COREWEBVIEW2_MATRIX_4X4 est la transformation de ce HWND vers le WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-149">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="6a02b-150">Le [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) renvoyé est utilisé dans SendPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="6a02b-150">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="6a02b-151">Le type de pointeur doit être PEN ou Touch, ou la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="6a02b-151">The pointer type must be either pen or touch or the function will fail.</span></span>



#### <span data-ttu-id="6a02b-152">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="6a02b-152">get_Cursor</span></span> 

<span data-ttu-id="6a02b-153">Le curseur actuel attendu par le WebView devrait être.</span><span class="sxs-lookup"><span data-stu-id="6a02b-153">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="6a02b-154">valeur publique HRESULT [get_Cursor](#get_cursor)(HCURSOR \* Cursor)</span><span class="sxs-lookup"><span data-stu-id="6a02b-154">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="6a02b-155">Le curseur doit être défini dans WM_SETCURSOR through:: SetCursor ou défini sur le HWND parent/ancêtre correspondant du WebView via:: SetClassLongPtr.</span><span class="sxs-lookup"><span data-stu-id="6a02b-155">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="6a02b-156">Le HCURSOR peut être retardée de sorte que CopyCursor/DestroyCursor est recommandé de conserver votre propre copie si vous ne faites pas immédiatement la définition du curseur.</span><span class="sxs-lookup"><span data-stu-id="6a02b-156">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="6a02b-157">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="6a02b-157">get_RootVisualTarget</span></span> 

<span data-ttu-id="6a02b-158">Le RootVisualTarget est un élément visuel de l’arborescence visuelle de l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="6a02b-158">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="6a02b-159">[get_RootVisualTarget](#get_rootvisualtarget)publiques HRESULT (IUnknown \* \* cible)</span><span class="sxs-lookup"><span data-stu-id="6a02b-159">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="6a02b-160">Cet élément visuel est l’endroit où le WebView se connecte à son arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="6a02b-160">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="6a02b-161">L’application utilise cet élément visuel pour positionner le WebView dans l’application.</span><span class="sxs-lookup"><span data-stu-id="6a02b-161">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="6a02b-162">L’application doit toujours utiliser la propriété Bounds pour redimensionner le WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-162">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="6a02b-163">La propriété RootVisualTarget peut être IDCompositionVisual ou Windows:: UI:: composition:: ContainerVisual.</span><span class="sxs-lookup"><span data-stu-id="6a02b-163">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="6a02b-164">WebView va connecter son arborescence d’éléments visuels à l’élément visuel fourni avant de revenir à partir de la méthode setter de propriété.</span><span class="sxs-lookup"><span data-stu-id="6a02b-164">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="6a02b-165">L’application doit valider sur son appareil définissant la propriété RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="6a02b-165">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="6a02b-166">La propriété RootVisualTarget prend en charge la valeur nullptr pour déconnecter le WebView de l’arborescence visuelle de l’application.</span><span class="sxs-lookup"><span data-stu-id="6a02b-166">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### <span data-ttu-id="6a02b-167">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="6a02b-167">get_UIAProvider</span></span> 

<span data-ttu-id="6a02b-168">Renvoie le fournisseur UI Automation pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-168">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="6a02b-169">[get_UIAProvider](#get_uiaprovider)par le biais du service public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6a02b-169">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="6a02b-170">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="6a02b-170">put_RootVisualTarget</span></span> 

<span data-ttu-id="6a02b-171">Définissez la propriété RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="6a02b-171">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="6a02b-172">[put_RootVisualTarget](#put_rootvisualtarget)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6a02b-172">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="6a02b-173">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="6a02b-173">remove_CursorChanged</span></span> 

<span data-ttu-id="6a02b-174">Supprimez un gestionnaire d’événements préalablement ajouté à add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="6a02b-174">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="6a02b-175">[remove_CursorChanged](#remove_cursorchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="6a02b-175">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="6a02b-176">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="6a02b-176">SendMouseInput</span></span> 

<span data-ttu-id="6a02b-177">Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData spécifie la quantité de mouvement du volant.</span><span class="sxs-lookup"><span data-stu-id="6a02b-177">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="6a02b-178">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) VIRTUALKEYS, UInt32 mouseData, point point)</span><span class="sxs-lookup"><span data-stu-id="6a02b-178">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="6a02b-179">Valeur positive indiquant que la roue a été pivotée vers l’avant, en dehors de l’utilisateur; une valeur négative indique que la roue a été pivotée vers l’arrière, pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a02b-179">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="6a02b-180">Un clic sur un seul volant définit en tant que WHEEL_DELTA, soit 120.</span><span class="sxs-lookup"><span data-stu-id="6a02b-180">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="6a02b-181">Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN ou COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, mouseData spécifie les boutons X ayant été pressés ou relâchements.</span><span class="sxs-lookup"><span data-stu-id="6a02b-181">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="6a02b-182">Cette valeur doit être 1 si le premier bouton X est appuyé sur/officialisé et 2 si le second bouton X est enfoncé/officialisé.</span><span class="sxs-lookup"><span data-stu-id="6a02b-182">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="6a02b-183">Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, virtualKeys, mouseData et point doivent tous être zéro.</span><span class="sxs-lookup"><span data-stu-id="6a02b-183">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="6a02b-184">Si eventKind est une autre valeur, mouseData doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6a02b-184">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="6a02b-185">Le point est censé figurer dans l’espace de coordonnées client du WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-185">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="6a02b-186">Pour effectuer le suivi des événements de souris qui démarrent dans le WebView et qui peuvent être déplacés en dehors de l’application WebView et hôte, il est recommandé d’appeler SetCapture et ReleaseCapture.</span><span class="sxs-lookup"><span data-stu-id="6a02b-186">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="6a02b-187">Pour faire disparaître les fenêtres de survol, il est également recommandé d’envoyer WM_MOUSELEAVE messages.</span><span class="sxs-lookup"><span data-stu-id="6a02b-187">To dismiss hover popups, it is also recommended to send WM_MOUSELEAVE messages.</span></span> 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### <span data-ttu-id="6a02b-188">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="6a02b-188">SendPointerInput</span></span> 

<span data-ttu-id="6a02b-189">SendPointerInput accepte les entrées de pointeur en forme d’effleurement ou de stylet définies dans COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="6a02b-189">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="6a02b-190">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="6a02b-190">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="6a02b-191">Toute entrée de pointeur à partir du système doit d’abord être convertie en [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6a02b-191">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="6a02b-192">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="6a02b-192">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="6a02b-193">Matrice qui représente une transformation 3D.</span><span class="sxs-lookup"><span data-stu-id="6a02b-193">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="6a02b-194">[COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4) typedef</span><span class="sxs-lookup"><span data-stu-id="6a02b-194">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="6a02b-195">Cette transformation est utilisée pour calculer les coordonnées correctes lors de l’appel de CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="6a02b-195">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="6a02b-196">Ceci équivaut à une D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="6a02b-196">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="6a02b-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="6a02b-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="6a02b-198">Type d’événement de souris utilisé par SendMouseInput pour transmettre le type d’événement de souris envoyé à WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-198">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="6a02b-199">énumération [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span><span class="sxs-lookup"><span data-stu-id="6a02b-199">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="6a02b-200">Doubl</span><span class="sxs-lookup"><span data-stu-id="6a02b-200">Values</span></span>                         | <span data-ttu-id="6a02b-201">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6a02b-201">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6a02b-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="6a02b-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="6a02b-203">Événement de défilement de la molette horizontale de la souris, WM_MOUSEHWHEEL.</span><span class="sxs-lookup"><span data-stu-id="6a02b-203">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="6a02b-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="6a02b-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="6a02b-205">Double-cliquez sur le bouton gauche de la souris, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="6a02b-205">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="6a02b-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="6a02b-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="6a02b-207">Bouton gauche de la souris, WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="6a02b-207">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="6a02b-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="6a02b-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="6a02b-209">Bouton gauche de la souris, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="6a02b-209">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="6a02b-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="6a02b-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="6a02b-211">Événement de départ de la souris, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="6a02b-211">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="6a02b-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="6a02b-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="6a02b-213">Bouton du milieu cliquez deux fois sur événement de souris, WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="6a02b-213">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="6a02b-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="6a02b-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="6a02b-215">Bouton du milieu de la souris, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="6a02b-215">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="6a02b-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="6a02b-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="6a02b-217">Bouton du milieu de la souris, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="6a02b-217">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="6a02b-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="6a02b-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="6a02b-219">Événement de déplacement de la souris, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="6a02b-219">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="6a02b-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="6a02b-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="6a02b-221">Cliquez deux fois sur le bouton droit de la souris, WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="6a02b-221">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="6a02b-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="6a02b-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="6a02b-223">Bouton droit de la souris, WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="6a02b-223">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="6a02b-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="6a02b-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="6a02b-225">Cliquez sur le bouton droit de la souris, WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="6a02b-225">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="6a02b-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="6a02b-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="6a02b-227">Événement de défilement de la roulette de la souris, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="6a02b-227">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="6a02b-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="6a02b-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="6a02b-229">Premier ou deuxième bouton X Cliquez deux fois sur événement de souris, WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="6a02b-229">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="6a02b-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="6a02b-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="6a02b-231">Premier ou deuxième X boutons de la souris, WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="6a02b-231">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="6a02b-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="6a02b-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="6a02b-233">Premier ou deuxième X boutons vers le haut, WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="6a02b-233">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="6a02b-234">Les valeurs de l’énumération sont alignées avec les messages de fenêtre WM_ \* correspondants.</span><span class="sxs-lookup"><span data-stu-id="6a02b-234">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="6a02b-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="6a02b-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="6a02b-236">Touches virtuelles d’événement de souris associées à une COREWEBVIEW2_MOUSE_EVENT_KIND pour SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="6a02b-236">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="6a02b-237">énumération [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span><span class="sxs-lookup"><span data-stu-id="6a02b-237">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="6a02b-238">Doubl</span><span class="sxs-lookup"><span data-stu-id="6a02b-238">Values</span></span>                         | <span data-ttu-id="6a02b-239">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6a02b-239">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6a02b-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="6a02b-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="6a02b-241">Aucune touche supplémentaire enfoncée.</span><span class="sxs-lookup"><span data-stu-id="6a02b-241">No additional keys pressed.</span></span>
<span data-ttu-id="6a02b-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="6a02b-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="6a02b-243">Le bouton gauche de la souris est enfoncé, MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="6a02b-243">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="6a02b-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="6a02b-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="6a02b-245">Le bouton droit de la souris est en bas, MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="6a02b-245">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="6a02b-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="6a02b-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="6a02b-247">La touche Maj est enfoncée, MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="6a02b-247">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="6a02b-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="6a02b-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="6a02b-249">Touche CTRL enfoncée, MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="6a02b-249">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="6a02b-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="6a02b-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="6a02b-251">Le bouton du milieu de la souris est en bas, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="6a02b-251">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="6a02b-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="6a02b-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="6a02b-253">Le premier bouton X est en bas, MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="6a02b-253">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="6a02b-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="6a02b-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="6a02b-255">Le deuxième bouton X est en bas, MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="6a02b-255">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="6a02b-256">Ces valeurs peuvent être combinées en un indicateur de bit si plusieurs touches virtuelles sont utilisées pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="6a02b-256">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="6a02b-257">Les valeurs de l’énumération sont alignées avec les touches de souris et de MK_ correspondantes.</span><span class="sxs-lookup"><span data-stu-id="6a02b-257">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="6a02b-258">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="6a02b-258">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="6a02b-259">Type d’événement de pointeur utilisé par SendPointerInput pour transmettre le type d’événement de pointeur envoyé à WebView.</span><span class="sxs-lookup"><span data-stu-id="6a02b-259">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="6a02b-260">énumération [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span><span class="sxs-lookup"><span data-stu-id="6a02b-260">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="6a02b-261">Doubl</span><span class="sxs-lookup"><span data-stu-id="6a02b-261">Values</span></span>                         | <span data-ttu-id="6a02b-262">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6a02b-262">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="6a02b-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="6a02b-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="6a02b-264">Correspond à WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="6a02b-264">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="6a02b-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="6a02b-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="6a02b-266">Correspond à WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="6a02b-266">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="6a02b-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="6a02b-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="6a02b-268">Correspond à WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="6a02b-268">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="6a02b-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="6a02b-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="6a02b-270">Correspond à WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="6a02b-270">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="6a02b-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="6a02b-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="6a02b-272">Correspond à WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="6a02b-272">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="6a02b-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="6a02b-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="6a02b-274">Correspond à WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="6a02b-274">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="6a02b-275">Les valeurs de l’énumération sont alignées avec les messages de fenêtre WM_POINTER \* correspondants.</span><span class="sxs-lookup"><span data-stu-id="6a02b-275">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>
