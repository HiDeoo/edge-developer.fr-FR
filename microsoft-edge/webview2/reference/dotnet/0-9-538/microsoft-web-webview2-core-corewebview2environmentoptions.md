---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 7bade615e2783631901b6e5146a636d824f909c1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698605"
---
# <span data-ttu-id="2264a-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="2264a-104">Microsoft.Web.WebView2.Core.CoreWebView2EnvironmentOptions class</span></span> 

<span data-ttu-id="2264a-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2264a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2264a-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="2264a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2264a-107">Options permettant de créer un environnement WebView2.</span><span class="sxs-lookup"><span data-stu-id="2264a-107">Options used to create WebView2 Environment.</span></span>

## <span data-ttu-id="2264a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="2264a-108">Summary</span></span>

 <span data-ttu-id="2264a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="2264a-109">Members</span></span>                        | <span data-ttu-id="2264a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2264a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2264a-111">AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="2264a-111">AdditionalBrowserArguments</span></span>](#additionalbrowserarguments) | <span data-ttu-id="2264a-112">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="2264a-112">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>
[<span data-ttu-id="2264a-113">Langue</span><span class="sxs-lookup"><span data-stu-id="2264a-113">Language</span></span>](#language) | <span data-ttu-id="2264a-114">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="2264a-114">The default language that WebView will run with.</span></span>
[<span data-ttu-id="2264a-115">TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="2264a-115">TargetCompatibleBrowserVersion</span></span>](#targetcompatiblebrowserversion) | <span data-ttu-id="2264a-116">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2264a-116">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
[<span data-ttu-id="2264a-117">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="2264a-117">CoreWebView2EnvironmentOptions</span></span>](#corewebview2environmentoptions) | <span data-ttu-id="2264a-118">Initialise une nouvelle instance de la classe CoreWebView2EnvironmentOptions.</span><span class="sxs-lookup"><span data-stu-id="2264a-118">Initializes a new instance of the CoreWebView2EnvironmentOptions class.</span></span>

<span data-ttu-id="2264a-119">Une implémentation par défaut est fournie dans WebView2EnvironmentOptions. h.</span><span class="sxs-lookup"><span data-stu-id="2264a-119">A default implementation is provided in WebView2EnvironmentOptions.h.</span></span>

## <span data-ttu-id="2264a-120">Ses</span><span class="sxs-lookup"><span data-stu-id="2264a-120">Members</span></span>

#### <span data-ttu-id="2264a-121">AdditionalBrowserArguments</span><span class="sxs-lookup"><span data-stu-id="2264a-121">AdditionalBrowserArguments</span></span> 

<span data-ttu-id="2264a-122">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="2264a-122">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span>

> <span data-ttu-id="2264a-123">[AdditionalBrowserArguments](#additionalbrowserarguments) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="2264a-123">public string [AdditionalBrowserArguments](#additionalbrowserarguments)</span></span>

<span data-ttu-id="2264a-124">Celles-ci sont transmises au processus de navigateur dans le cadre de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2264a-124">These will be passed to the browser process as part of the command line.</span></span> <span data-ttu-id="2264a-125">Pour plus d’informations sur les commutateurs de ligne de commande pour les navigateurs, voir [exécuter du chrome avec des indicateurs](https://aka.ms/RunChromiumWithFlags) .</span><span class="sxs-lookup"><span data-stu-id="2264a-125">See [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags) for more information about command line switches to browser process.</span></span> <span data-ttu-id="2264a-126">Si l’application est lancée à l’aide d’un commutateur de ligne `--edge-webview-switches=xxx` de commande, la valeur de ce commutateur (xxx dans l’exemple ci-dessus) est également ajoutée à la ligne de commande du processus du navigateur.</span><span class="sxs-lookup"><span data-stu-id="2264a-126">If the app is launched with a command line switch `--edge-webview-switches=xxx` the value of that switch (xxx in the above example) will also be appended to the browser process command line.</span></span> <span data-ttu-id="2264a-127">Certains commutateurs comme `--user-data-dir` les éléments internes et importants sont importants pour le WebView.</span><span class="sxs-lookup"><span data-stu-id="2264a-127">Certain switches like `--user-data-dir` are internal and important to WebView.</span></span> <span data-ttu-id="2264a-128">Ces commutateurs seront ignorés même en cas de spécification.</span><span class="sxs-lookup"><span data-stu-id="2264a-128">Those switches will be ignored even if specified.</span></span> <span data-ttu-id="2264a-129">Si les mêmes commutateurs sont spécifiés plusieurs fois, le dernier gagne.</span><span class="sxs-lookup"><span data-stu-id="2264a-129">If the same switches are specified multiple times, the last one wins.</span></span> <span data-ttu-id="2264a-130">Il n’est pas possible de fusionner les différentes valeurs du même commutateur, à l’exception des fonctionnalités désactivé et activé.</span><span class="sxs-lookup"><span data-stu-id="2264a-130">There is no attempt to merge the different values of the same switch, except for disabled and enabled features.</span></span> <span data-ttu-id="2264a-131">Les fonctionnalités spécifiées par `--enable-features` and `--disable-features` seront fusionnées avec la logique simple: les fonctionnalités seront l’Union des fonctionnalités définies et des fonctionnalités intégrées, et si une fonctionnalité est désactivée, elle sera supprimée de la liste des fonctionnalités activées.</span><span class="sxs-lookup"><span data-stu-id="2264a-131">The features specified by `--enable-features` and `--disable-features` will be merged with simple logic: the features will be the union of the specified features and built-in features, and if a feature is disabled, it will be removed from the enabled features list.</span></span> <span data-ttu-id="2264a-132">La valeur de la ligne de commande du processus d’application est `--edge-webview-switches` traitée après le traitement du paramètre additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="2264a-132">App process's command line `--edge-webview-switches` value are processed after the additionalBrowserArguments parameter is processed.</span></span> <span data-ttu-id="2264a-133">Certaines fonctionnalités sont désactivées en interne et ne peuvent pas être activées.</span><span class="sxs-lookup"><span data-stu-id="2264a-133">Certain features are disabled internally and can't be enabled.</span></span> <span data-ttu-id="2264a-134">Si l’analyse a échoué pour les commutateurs spécifiés, elle est ignorée.</span><span class="sxs-lookup"><span data-stu-id="2264a-134">If parsing failed for the specified switches, they will be ignored.</span></span> <span data-ttu-id="2264a-135">Par défaut, le processus de navigateur s’exécute sans indicateurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2264a-135">Default is to run browser process with no extra flags.</span></span>

#### <span data-ttu-id="2264a-136">Langue</span><span class="sxs-lookup"><span data-stu-id="2264a-136">Language</span></span> 

<span data-ttu-id="2264a-137">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="2264a-137">The default language that WebView will run with.</span></span>

> <span data-ttu-id="2264a-138">[langage](#language) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="2264a-138">public string [Language](#language)</span></span>

<span data-ttu-id="2264a-139">Il s’applique aux interfaces utilisateur du navigateur comme le menu contextuel et les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2264a-139">It applies to browser UIs like context menu and dialogs.</span></span> <span data-ttu-id="2264a-140">Il s’applique également à l’en-tête HTTP Accept-Language que le WebView envoie aux sites Web.</span><span class="sxs-lookup"><span data-stu-id="2264a-140">It also applies to the accept-languages HTTP header that WebView sends to web sites.</span></span> <span data-ttu-id="2264a-141">La mise en forme est de l' `language[-country]` endroit où `language` se trouve le code à deux lettres ISO 639 et `country` correspond au code 2 lettres de l’ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="2264a-141">It is in the format of `language[-country]` where `language` is the 2 letter code from ISO 639 and `country` is the 2 letter code from ISO 3166.</span></span>

#### <span data-ttu-id="2264a-142">TargetCompatibleBrowserVersion</span><span class="sxs-lookup"><span data-stu-id="2264a-142">TargetCompatibleBrowserVersion</span></span> 

<span data-ttu-id="2264a-143">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2264a-143">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>

> <span data-ttu-id="2264a-144">[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="2264a-144">public string [TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion)</span></span>

<span data-ttu-id="2264a-145">Par défaut, il s’agit de la version latérale du runtime WebView2 qui correspond à la version du SDK utilisée par l’application.</span><span class="sxs-lookup"><span data-stu-id="2264a-145">This defaults to the Edge WebView2 Runtime version that corresponds with the version of the SDK the application is using.</span></span> <span data-ttu-id="2264a-146">Le format de cette valeur est identique à celui de la propriété BrowserVersionString et des autres valeurs BrowserVersion.</span><span class="sxs-lookup"><span data-stu-id="2264a-146">The format of this value is the same as the format of the BrowserVersionString property and other BrowserVersion values.</span></span> <span data-ttu-id="2264a-147">Seule la partie version de la valeur BrowserVersion est respectée.</span><span class="sxs-lookup"><span data-stu-id="2264a-147">Only the version part of the BrowserVersion value is respected.</span></span> <span data-ttu-id="2264a-148">Le suffixe de canal, s’il existe, est ignoré.</span><span class="sxs-lookup"><span data-stu-id="2264a-148">The channel suffix, if it exists, is ignored.</span></span> <span data-ttu-id="2264a-149">La version des fichiers binaires Edge WebView2 Runtime utilisés est susceptible d’être différente de la TargetCompatibleBrowserVersion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2264a-149">The version of the Edge WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion.</span></span> <span data-ttu-id="2264a-150">Ils sont uniquement compatibles.</span><span class="sxs-lookup"><span data-stu-id="2264a-150">They are only guaranteed to be compatible.</span></span> <span data-ttu-id="2264a-151">Vous pouvez vérifier la version réelle sur la propriété BrowserVersionString sur CoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="2264a-151">You can check the actual version on the BrowserVersionString property on the CoreWebView2Environment.</span></span>

#### <span data-ttu-id="2264a-152">CoreWebView2EnvironmentOptions</span><span class="sxs-lookup"><span data-stu-id="2264a-152">CoreWebView2EnvironmentOptions</span></span> 

<span data-ttu-id="2264a-153">Initialise une nouvelle instance de la classe CoreWebView2EnvironmentOptions.</span><span class="sxs-lookup"><span data-stu-id="2264a-153">Initializes a new instance of the CoreWebView2EnvironmentOptions class.</span></span>

> <span data-ttu-id="2264a-154">public [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(chaîne additionalBrowserArguments, langage de chaîne, chaîne targetCompatibleBrowserVersion)</span><span class="sxs-lookup"><span data-stu-id="2264a-154">public  [CoreWebView2EnvironmentOptions](#corewebview2environmentoptions)(string additionalBrowserArguments, string language, string targetCompatibleBrowserVersion)</span></span>

##### <span data-ttu-id="2264a-155">Parameters</span><span class="sxs-lookup"><span data-stu-id="2264a-155">Parameters</span></span>
* `additionalBrowserArguments` <span data-ttu-id="2264a-156">AdditionalBrowserArguments peut être spécifié pour modifier le comportement du WebView.</span><span class="sxs-lookup"><span data-stu-id="2264a-156">AdditionalBrowserArguments can be specified to change the behavior of the WebView.</span></span> 

* `language` <span data-ttu-id="2264a-157">La langue par défaut avec laquelle le WebView sera exécuté.</span><span class="sxs-lookup"><span data-stu-id="2264a-157">The default language that WebView will run with.</span></span> 

* `targetCompatibleBrowserVersion` <span data-ttu-id="2264a-158">La version des fichiers binaires Edge WebView2 Runtime doit être compatible avec l’application à l’origine de l’appel.</span><span class="sxs-lookup"><span data-stu-id="2264a-158">The version of the Edge WebView2 Runtime binaries required to be compatible with the calling application.</span></span>
