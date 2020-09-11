---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: 4a3b5999d38f74fb6b78063e32b3abb0cb59c6b6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011877"
---
# <span data-ttu-id="7c72a-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7c72a-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="7c72a-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="7c72a-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="7c72a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7c72a-106">Summary</span></span>

 <span data-ttu-id="7c72a-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7c72a-107">Members</span></span>                        | <span data-ttu-id="7c72a-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7c72a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7c72a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7c72a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7c72a-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="7c72a-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="7c72a-111">Ses</span><span class="sxs-lookup"><span data-stu-id="7c72a-111">Members</span></span>

#### <span data-ttu-id="7c72a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7c72a-112">Invoke</span></span> 

<span data-ttu-id="7c72a-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="7c72a-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="7c72a-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="7c72a-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>
