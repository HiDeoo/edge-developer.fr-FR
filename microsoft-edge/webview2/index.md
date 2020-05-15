---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Applications WebView 2 de Microsoft Edge 2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b1ec0c43b57fb107490ddb34b330bb6ec378ac41
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653359"
---
# <span data-ttu-id="02690-104">Microsoft Edge WebView2 (version préliminaire du développeur)</span><span class="sxs-lookup"><span data-stu-id="02690-104">Microsoft Edge WebView2 (developer preview)</span></span>

<span data-ttu-id="02690-105">Le contrôle Microsoft Edge WebView2 vous permet d’héberger le contenu Web de votre application à l’aide de [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/) comme moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="02690-105">The Microsoft Edge WebView2 control enables you to host web content in your application using [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/) as the rendering engine.</span></span>

<span data-ttu-id="02690-106">Le contrôle WebView2 est actuellement dans la version préliminaire du développeur, au cours de laquelle vous pouvez prototyper vos solutions et partager vos commentaires nous permettant de façonner l’API stable future.</span><span class="sxs-lookup"><span data-stu-id="02690-106">The WebView2 control is currently in developer preview, during which you can prototype your solutions and share feedback with us to shape the future stable API.</span></span> <span data-ttu-id="02690-107">Dans certains cas, il est probable que nous ayons modifié l’API lors de la prévisualisation, et dans ce cas, vous devez mettre à jour le kit de développement logiciel (SDK) WebView2 et le navigateur Microsoft Edge (chrome).</span><span class="sxs-lookup"><span data-stu-id="02690-107">There will likely be some breaking changes as we evolve the API during preview, and when this happens, you will need to have both the WebView2 SDK and the Microsoft Edge (Chromium) browser updated.</span></span> <span data-ttu-id="02690-108">Les modifications importantes seront mentionnées dans les [notes de publication](./releasenotes.md) du SDK.</span><span class="sxs-lookup"><span data-stu-id="02690-108">Breaking changes will be noted in the [release notes](./releasenotes.md) of the SDK.</span></span> <span data-ttu-id="02690-109">Cela se verrouille en tant qu’approche WebView2 et stable.</span><span class="sxs-lookup"><span data-stu-id="02690-109">This will lock down as WebView2 approaches beta and stable.</span></span>

## <span data-ttu-id="02690-110">Plates-formes prises en charge</span><span class="sxs-lookup"><span data-stu-id="02690-110">Supported Platforms</span></span>

<span data-ttu-id="02690-111">Un aperçu des développeurs est disponible pour Win32 C/C++ et Windows Forms et WPF sur .NET Framework 4.6.2 ou version ultérieure et .NET Core 3,0 ou version ultérieure sur Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="02690-111">A developer preview is available for Win32 C/C++ and Windows Forms and WPF on .NET Framework 4.6.2 or later and .NET Core 3.0 or later on Windows 10, Windows 8.1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2, and Windows Server 2008 R2.</span></span> <span data-ttu-id="02690-112">Une version alpha pour WinUI 3,0 est disponible [ici](https://docs.microsoft.com/uwp/toolkits/winui3/).</span><span class="sxs-lookup"><span data-stu-id="02690-112">An Alpha version for WinUI 3.0 is available [here](https://docs.microsoft.com/uwp/toolkits/winui3/).</span></span>

## <span data-ttu-id="02690-113">Prise en main</span><span class="sxs-lookup"><span data-stu-id="02690-113">Getting Started</span></span>

<span data-ttu-id="02690-114">Pour générer et tester votre application à l’aide du contrôle WebView2, vous devez disposer de [Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/download/) et du [SDK WebView2](https://aka.ms/webviewnuget) .</span><span class="sxs-lookup"><span data-stu-id="02690-114">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) and the [WebView2 SDK](https://aka.ms/webviewnuget) installed.</span></span> <span data-ttu-id="02690-115">Sélectionnez l’une des options ci-dessous pour commencer.</span><span class="sxs-lookup"><span data-stu-id="02690-115">Select one of the options below to get started!</span></span>

* [<span data-ttu-id="02690-116">Commencer à utiliser Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="02690-116">Getting Started with Win32 C/C++</span></span>](./gettingstarted/win32.md)
* [<span data-ttu-id="02690-117">Mise en route de WPF</span><span class="sxs-lookup"><span data-stu-id="02690-117">Getting Started with WPF</span></span>](./gettingstarted/wpf.md)
* [<span data-ttu-id="02690-118">Mise en route de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="02690-118">Getting Started with Windows Forms</span></span>](./gettingstarted/winforms.md)

<span data-ttu-id="02690-119">N’hésitez pas à nous faire part de vos commentaires [WebView2](https://aka.ms/webviewfeedback) référentiel Samples.</span><span class="sxs-lookup"><span data-stu-id="02690-119">Please leave us feedback in our [WebView2 Feedback](https://aka.ms/webviewfeedback) repo.</span></span>

## <span data-ttu-id="02690-120">Exemples de WebView2</span><span class="sxs-lookup"><span data-stu-id="02690-120">WebView2 Samples</span></span>

<span data-ttu-id="02690-121">Le référentiel d' [exemples WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contient des exemples qui décrivent toutes les fonctionnalités du SDK WebView2 et leurs modèles d’utilisation de l’API.</span><span class="sxs-lookup"><span data-stu-id="02690-121">The [WebView2 Samples](https://github.com/MicrosoftEdge/WebView2Samples) repository contains samples that demonstrate all of the WebView2 SDK's features and their API use patterns.</span></span> <span data-ttu-id="02690-122">À mesure que nous ajoutons des fonctionnalités au kit de développement logiciel (SDK) WebView2, nous mettons à jour régulièrement nos exemples d’applications.</span><span class="sxs-lookup"><span data-stu-id="02690-122">As we add more features to the WebView2 SDK, we will regularly update our sample applications.</span></span>

## <span data-ttu-id="02690-123">Distribution de l’application</span><span class="sxs-lookup"><span data-stu-id="02690-123">App Distribution</span></span>

<span data-ttu-id="02690-124">Le contrôle WebView2 utilise le navigateur Microsoft Edge (chrome).</span><span class="sxs-lookup"><span data-stu-id="02690-124">The WebView2 control utilizes the Microsoft Edge (Chromium) browser.</span></span> <span data-ttu-id="02690-125">Lors de la distribution de votre application, il est important de veiller à ce que le navigateur Edge soit installé sur tous les ordinateurs des utilisateurs dans lesquels votre application sera exécutée.</span><span class="sxs-lookup"><span data-stu-id="02690-125">When distributing your app it is important to ensure that the Edge browser is installed on all user machines where your application will run.</span></span> <span data-ttu-id="02690-126">Vous devez également savoir quelle version et quel canal est installé (par exemple, stable, bêta, dev ou Canaries).</span><span class="sxs-lookup"><span data-stu-id="02690-126">You should also be aware of which version and channel is installed, e.g. Stable, Beta, Dev, or Canary.</span></span> <span data-ttu-id="02690-127">Le contrôleur WebView2 utilisera la version la plus stable du navigateur lorsqu’il est installé sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="02690-127">The WebView2 controller will utilize the most stable version of the browser when installed on a machine.</span></span>

### <span data-ttu-id="02690-128">Futures modifications planifiées</span><span class="sxs-lookup"><span data-stu-id="02690-128">Future Planned Changes</span></span>

<span data-ttu-id="02690-129">Nous sommes conscients du fait que le navigateur Edge n’est peut-être pas disponible sur tous les ordinateurs utilisateur que votre application est conçue pour s’exécuter, ou ce contrôle du processus d’installation du navigateur Edge peut s’avérer difficile.</span><span class="sxs-lookup"><span data-stu-id="02690-129">We recognize that the Edge browser may not be available on all user machines your application is intended to run, or that control of the Edge browser install process may be difficult.</span></span> <span data-ttu-id="02690-130">Pour vous assurer que votre application s’exécutera sur tous les ordinateurs, indépendamment de l’état d’installation du navigateur Microsoft Edge du client, nous allons libérer Microsoft Edge WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="02690-130">To ensure your application will run on all machines, independent of the install status of the client Microsoft Edge browser, we will release the Microsoft Edge WebView2 Runtime.</span></span> <span data-ttu-id="02690-131">Nous allons mettre à jour WebView2 pour rechercher la version stable du runtime avant de rechercher des versions préliminaires du navigateur installé.</span><span class="sxs-lookup"><span data-stu-id="02690-131">We will further update WebView2 to search for the stable version of the Runtime before searching for pre-release versions of the installed browser.</span></span>

<span data-ttu-id="02690-132">Nous sommes conscients également du bon fonctionnement de certains développeurs d’applications dans les environnements restreints, et de la prise en charge de deux options de distribution, de persistants et de la version corrigée.</span><span class="sxs-lookup"><span data-stu-id="02690-132">We also recognize that some app developers operate in constrained environments, and so intend to support two distribution options, evergreen and fixed version.</span></span>

<span data-ttu-id="02690-133">L’option persistant est le modèle de distribution recommandé pour la plupart des développeurs.</span><span class="sxs-lookup"><span data-stu-id="02690-133">Evergreen is the recommended distribution model for most developers.</span></span> <span data-ttu-id="02690-134">Dans ce mode, les mises à jour de WebView2 Runtime seront entièrement gérées par Microsoft pour vous tenir au courant, sans aucun effort supplémentaire de votre application.</span><span class="sxs-lookup"><span data-stu-id="02690-134">In this mode updates to the WebView2 Runtime will be fully managed by Microsoft keeping you up to date automatically without additional effort from your application.</span></span> <span data-ttu-id="02690-135">Avec ce modèle de mise à jour automatique, vous pouvez être sûr que votre application tire parti des fonctionnalités et des mises à jour de sécurité les plus récentes pour le contenu Web hébergé.</span><span class="sxs-lookup"><span data-stu-id="02690-135">With this self-updating model you can be assured that your app is taking advantage of the latest features and security updates for hosted web content.</span></span>

<span data-ttu-id="02690-136">En ce qui concerne les environnements restreints, nous mettrons également en charge un modèle de distribution de version fixe.</span><span class="sxs-lookup"><span data-stu-id="02690-136">For constrained environments we will also support a fixed version distribution model.</span></span> <span data-ttu-id="02690-137">Dans ce modèle, votre application sélectionne et empaquetait une version WebView2 spécifique.</span><span class="sxs-lookup"><span data-stu-id="02690-137">In this model your application will select and package a specific WebView2 version.</span></span> <span data-ttu-id="02690-138">Les mises à jour apportées à la version du WebView seront responsables de l’application et seront indépendantes de tout mécanisme Microsoft Update géré.</span><span class="sxs-lookup"><span data-stu-id="02690-138">Updates to the WebView version will be the responsibility of the application and will be independent of any managed Microsoft update mechanisms.</span></span> <span data-ttu-id="02690-139">Vous devez choisir ce modèle s’il est essentiel de pouvoir contrôler en tout lieu la version du navigateur et les durées de mise à jour dont votre application tire parti.</span><span class="sxs-lookup"><span data-stu-id="02690-139">You should choose this model if it is crucial to be able to have absolute control over the browser version and update times your application is taking advantage of.</span></span>

## <span data-ttu-id="02690-140">Microsoft Edge WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="02690-140">Microsoft Edge WebView2 Runtime</span></span>

<span data-ttu-id="02690-141">Microsoft Edge WebView2 Runtime est un ensemble de fichiers binaires de navigateur optimisés pour une utilisation par des applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="02690-141">The Microsoft Edge WebView2 Runtime is a packaging of the browser binaries optimized for use by WebView2 applications.</span></span> <span data-ttu-id="02690-142">Ce mode fonctionne autonome ou côte à côte à l’aide d’une installation de navigateur côté client.</span><span class="sxs-lookup"><span data-stu-id="02690-142">It will function stand alone or side-by-side with a client Edge Browser install.</span></span> <span data-ttu-id="02690-143">Une installation unique du runtime prend en charge un nombre quelconque d’applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="02690-143">A single install of the run-time will support any number of WebView2 applications.</span></span> <span data-ttu-id="02690-144">L’installation de la version d’exécution ne s’affiche pas sous la forme d’une installation de navigateur pour l’utilisateur final, par exemple, aucun raccourci sur le bureau, entrée du menu Démarrer ou enregistrement du protocole.</span><span class="sxs-lookup"><span data-stu-id="02690-144">Install of the runtime will not appear as a browser install to end-user, i.e. no desktop shortcuts, start menu entry, or protocol registration.</span></span>

<span data-ttu-id="02690-145">Une application utilisant WebView2 doit vérifier que l’installation de Microsoft Edge WebView2 Runtime s’est produite.</span><span class="sxs-lookup"><span data-stu-id="02690-145">An application utilizing WebView2 must ensure the installation of the Microsoft Edge WebView2 Runtime has occurred.</span></span> <span data-ttu-id="02690-146">Au moment de l’installation de l’application, vous devez vérifier l’état d’installation actuel, qui peut être déterminé à l’aide de [GetAvailableCoreWebView2BrowserVersionString](./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring).</span><span class="sxs-lookup"><span data-stu-id="02690-146">At application install time you should check the current install status, which can be determined by using [GetAvailableCoreWebView2BrowserVersionString](./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring).</span></span> <span data-ttu-id="02690-147">Si le runtime WebView2 n’est pas disponible, vous devez chaîner le programme d’installation de Microsoft Edge WebView2 Runtime dans votre flux d’installation.</span><span class="sxs-lookup"><span data-stu-id="02690-147">If the WebView2 Runtime is not available, you should chain the Microsoft Edge WebView2 Runtime Installer to your install flow.</span></span>

## <span data-ttu-id="02690-148">Kit de développement logiciel (SDK) Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="02690-148">Microsoft Edge WebView2 SDK</span></span>

<span data-ttu-id="02690-149">Pour utiliser WebView2 au sein de votre application, vous devez installer et faire référence au [Kit de développement logiciel (SDK) WebView2](https://aka.ms/webviewnuget) dans votre application.</span><span class="sxs-lookup"><span data-stu-id="02690-149">To utilize WebView2 within your app you'll need to install and reference the [WebView2 SDK](https://aka.ms/webviewnuget) in your application.</span></span> <span data-ttu-id="02690-150">Nos publications NuGet contiendront une version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="02690-150">Our NuGet releases will contain both a release and pre-release version.</span></span> <span data-ttu-id="02690-151">La version commerciale contient les API publiques que nous envisageons actuellement de publier pour une disponibilité générale.</span><span class="sxs-lookup"><span data-stu-id="02690-151">The release version contains the public APIs we currently intend to release to general availability.</span></span>

<span data-ttu-id="02690-152">La version préliminaire contient des [API expérimentales](./reference/win32/0-9-488-reference-webview2.md#experimental)supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="02690-152">The pre-release version will contain additional [experimental APIs](./reference/win32/0-9-488-reference-webview2.md#experimental).</span></span> <span data-ttu-id="02690-153">Il s’agit d’API et de fonctionnalités que nous évaluons et pour lesquelles nous aimerions les [Commentaires](https://aka.ms/webviewfeedback) avant de les promouvoir dans la version finale.</span><span class="sxs-lookup"><span data-stu-id="02690-153">These are APIs and functionality we are evaluating and would like [feedback](https://aka.ms/webviewfeedback) on before promoting them to the release version.</span></span>

## <span data-ttu-id="02690-154">Développement pour les versions à venir</span><span class="sxs-lookup"><span data-stu-id="02690-154">Development against Upcoming Versions</span></span>

<span data-ttu-id="02690-155">Pour le développement, vous souhaiterez peut-être cibler la version bêta, le dev ou le Canaries pour vous assurer que votre application fonctionne avec les versions à venir ou pour tirer parti des fonctionnalités à venir.</span><span class="sxs-lookup"><span data-stu-id="02690-155">For development you may want to target Beta, Dev, or Canary to ensure your application will work with upcoming versions or to take advantage of upcoming features.</span></span> <span data-ttu-id="02690-156">Tous les canaux préconfigurés sont fournis par le navigateur Microsoft Edge du client installé.</span><span class="sxs-lookup"><span data-stu-id="02690-156">All pre-released channels are provided by the installed client Microsoft Edge browser.</span></span> <span data-ttu-id="02690-157">Pour cibler l’un de ces canaux, assurez-vous que le navigateur Edge installé sur votre ordinateur de développement est le canal que vous voulez.</span><span class="sxs-lookup"><span data-stu-id="02690-157">To target one of these channels ensure the installed Edge browser on your development machine is the channel you'd like.</span></span> <span data-ttu-id="02690-158">Les développeurs peuvent utiliser une clé de registre ou une variable d’environnement pour modifier WebView2 à partir de la version la plus stable qui est la plus stable trouvée.</span><span class="sxs-lookup"><span data-stu-id="02690-158">Developers can use a registry key or environment variable to change the WebView2 from the most stable version found to the least stable found.</span></span> <span data-ttu-id="02690-159">Pour plus d’informations, voir [CreateCoreWebView2EnvironmentWithOptions](./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).</span><span class="sxs-lookup"><span data-stu-id="02690-159">See more details in [CreateCoreWebView2EnvironmentWithOptions](./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).</span></span>

## <span data-ttu-id="02690-160">Débogage de WebView2</span><span class="sxs-lookup"><span data-stu-id="02690-160">Debugging WebView2</span></span>

### <span data-ttu-id="02690-161">DevTools</span><span class="sxs-lookup"><span data-stu-id="02690-161">DevTools</span></span>

<span data-ttu-id="02690-162">Vous pouvez utiliser les [outils de développement Microsoft Edge (chrome)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium) pour déboguer le contenu Web affiché dans WebView, comme vous le feriez dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="02690-162">You can use [Microsoft Edge (Chromium) Developer Tools](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium) to debug web content displayed in WebView, just as you would in the browser.</span></span> <span data-ttu-id="02690-163">Lorsque vous avez la possibilité de mettre le focus sur la fenêtre WebView, appuyez `F12` ou appuyez sur `Ctrl`  +  `Shift`  +  `I` ou cliquez avec le bouton droit sur le bouton droit `Inspect` pour ouvrir les outils de développement.</span><span class="sxs-lookup"><span data-stu-id="02690-163">While having focus on the WebView window, press `F12`, or press `Ctrl` + `Shift` + `I`, or Right Click + choose `Inspect` to open Developer Tools.</span></span>

:::image type="complex" source="./media/f12.png" alt-text="F12":::
   <span data-ttu-id="02690-165">F12</span><span class="sxs-lookup"><span data-stu-id="02690-165">F12</span></span>
:::image-end:::  

<!--![F12](./media/f12.png)  -->  

**<span data-ttu-id="02690-166">Remarque lors du débogage d’une application dans Visual Studio avec le débogueur natif en pièce jointe, `F12` il est possible que le débogueur natif se déclenche au lieu des outils de développement.</span><span class="sxs-lookup"><span data-stu-id="02690-166">Note when debugging application in Visual Studio with the native debugger attached, `F12` may trigger the native debugger instead of Developer Tools.</span></span> <span data-ttu-id="02690-167">Utiliser `Ctrl`  +  `Shift`  +  `I` , ou cliquer avec le bouton droit + `Inspect` pour éviter les conflits de raccourcis clavier potentiels.</span><span class="sxs-lookup"><span data-stu-id="02690-167">Use `Ctrl` + `Shift` + `I`, or Right Click + `Inspect` to avoid potential hotkey conflict.</span></span>**

### <span data-ttu-id="02690-168">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02690-168">Visual Studio</span></span>

<span data-ttu-id="02690-169">Vous pouvez utiliser le débogueur de script dans Visual Studio 2019 (version minimum 16,4 Preview 2) pour déboguer votre script dans WebView2 directement à partir de l’environnement de développement intégré (IDE).</span><span class="sxs-lookup"><span data-stu-id="02690-169">You can use the script debugger in Visual Studio 2019 (minimum version 16.4 Preview 2) to debug your script within WebView2 right from the IDE.</span></span> <span data-ttu-id="02690-170">Assurez-vous que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.</span><span class="sxs-lookup"><span data-stu-id="02690-170">Make sure the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>

:::image type="complex" source="./media/vs-js-diagnostics.jpg" alt-text="Diagnostics JavaScript Visual Studio":::
   <span data-ttu-id="02690-172">Diagnostics JavaScript Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02690-172">Visual Studio JavaScript diagnostics</span></span>
:::image-end:::  

<!--![vs-js-diagnostics](./media/vs-js-diagnostics.jpg)  -->  

<span data-ttu-id="02690-173">Cliquez avec le bouton droit sur votre projet, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="02690-173">Right click on your project and select **Properties**.</span></span> <span data-ttu-id="02690-174">Sous **Propriétés**  >  **Debugging**  >  de configuration du**type de débogueur**, sélectionnez l’option **JavaScript (WebView2)** pour activer le débogage de script WebView2.</span><span class="sxs-lookup"><span data-stu-id="02690-174">Under **Configuration Properties** > **Debugging** > **Debugger Type**,  choose the **JavaScript (WebView2)** option to enable WebView2 script debugging.</span></span> <span data-ttu-id="02690-175">Vous pouvez en savoir plus sur le suivi.</span><span class="sxs-lookup"><span data-stu-id="02690-175">More details to follow soon.</span></span>

:::image type="complex" source="./media/vs-script-debugger.jpg" alt-text="Débogueur de script Visual Studio":::
   <span data-ttu-id="02690-177">Débogueur de script Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02690-177">Visual Studio script debugger</span></span>
:::image-end:::  

<!--![vs-script-debugger](./media/vs-script-debugger.jpg)  -->  

### <span data-ttu-id="02690-178">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="02690-178">Visual Studio Code</span></span>

<span data-ttu-id="02690-179">Vous pouvez également utiliser du code Visual Studio pour déboguer votre script dans le WebView2 directement à partir de l’IDE.</span><span class="sxs-lookup"><span data-stu-id="02690-179">You can also use Visual Studio Code to debug your script within the WebView2 right from the IDE.</span></span> <span data-ttu-id="02690-180">Pour en savoir plus, cliquez [ici](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span><span class="sxs-lookup"><span data-stu-id="02690-180">For more details click [here](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span></span>

## <span data-ttu-id="02690-181">Contacter l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="02690-181">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="02690-182">Aidez-nous à créer une expérience WebView2 plus riche en partageant vos commentaires!</span><span class="sxs-lookup"><span data-stu-id="02690-182">Help us build a richer WebView2 experience by sharing your feedback!</span></span> <span data-ttu-id="02690-183">Consultez notre page de [Commentaires référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues.</span><span class="sxs-lookup"><span data-stu-id="02690-183">Visit our [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>

<span data-ttu-id="02690-184">C’est également le bon endroit pour rechercher des problèmes connus.</span><span class="sxs-lookup"><span data-stu-id="02690-184">It's also a good place to search for known issues.</span></span>
<span data-ttu-id="02690-185">Pendant la version préliminaire du développeur, nous recueillerons également des données de télémétrie pour nous aider à créer un meilleur affichage du WebView.</span><span class="sxs-lookup"><span data-stu-id="02690-185">During developer preview, we will also be collecting telemetry data to help us build a better WebView.</span></span> <span data-ttu-id="02690-186">Les utilisateurs peuvent désactiver la collecte des données WebView en accédant à edge://settings/privacy dans le navigateur et en désactivant la collecte des données du navigateur.</span><span class="sxs-lookup"><span data-stu-id="02690-186">Users can turn off WebView data collection by navigating to edge://settings/privacy in the browser and turning off browser data collection.</span></span>