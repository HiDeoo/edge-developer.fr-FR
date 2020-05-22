---
description: Options de distribution lors de la publication d’une application à l’aide de Microsoft Edge WebView2
title: Distribution de l’application Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a789b0f4f9c482670f843ed21368b4168f99abe0
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659697"
---
# <span data-ttu-id="77f1c-104">Distribution d’applications à l’aide de WebView2</span><span class="sxs-lookup"><span data-stu-id="77f1c-104">Distribution of Applications using WebView2</span></span> 

<span data-ttu-id="77f1c-105">Le contrôle WebView2 utilise le navigateur Microsoft Edge \ (chrome \).</span><span class="sxs-lookup"><span data-stu-id="77f1c-105">The WebView2 control utilizes the Microsoft Edge \(Chromium\) browser.</span></span> <span data-ttu-id="77f1c-106">Lors de la distribution de votre application, assurez-vous que le navigateur Edge est installé sur tous les ordinateurs utilisateurs exécutant votre application.</span><span class="sxs-lookup"><span data-stu-id="77f1c-106">When distributing your app, ensure that the Edge browser is installed on all user machines where your application runs.</span></span> <span data-ttu-id="77f1c-107">Le contrôle WebView2 utilise la version la plus stable du navigateur installée sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="77f1c-107">The WebView2 control uses the most stable version of the browser that’s installed on a machine.</span></span> <span data-ttu-id="77f1c-108">Par exemple, il est possible que vous disposiez de la version stable, bêta, dev et Canaries en même temps, et dans ce cas, les contrôles WebView2 s’exécutent dans le canal stable.</span><span class="sxs-lookup"><span data-stu-id="77f1c-108">For example, you may have Stable, Beta, Dev, and Canary installed at the same time, and in this situation, WebView2 controls run in the Stable channel.</span></span> <span data-ttu-id="77f1c-109">Assurez-vous de consulter les notes de publication pour vous assurer que la version du navigateur installée sur vos ordinateurs qui exécutent vos contrôles WebView2 répond à la configuration minimale requise pour la version.</span><span class="sxs-lookup"><span data-stu-id="77f1c-109">Ensure you review the release notes to ensure that the version of the browser installed on your machines that run your WebView2 controls meet the minimum version requirements.</span></span>

## <span data-ttu-id="77f1c-110">Feuille de route</span><span class="sxs-lookup"><span data-stu-id="77f1c-110">Roadmap</span></span>

<span data-ttu-id="77f1c-111">Nous sommes conscients que le navigateur Edge peut ne pas être disponible sur tous les ordinateurs des utilisateurs dans lesquels votre application sera exécutée ou si l’installation de votre navigateur Edge au sein de votre organisation risque d’être difficile.</span><span class="sxs-lookup"><span data-stu-id="77f1c-111">We recognize that the Edge browser may not be available on all user machines where your application will run, or that installing Edge browser throughout your organization may be difficult.</span></span> <span data-ttu-id="77f1c-112">Pour vous assurer que votre application s’exécute sur tous les ordinateurs, indépendamment du navigateur Microsoft Edge installé, nous allons libérer Microsoft Edge WebView2 Runtime.</span><span class="sxs-lookup"><span data-stu-id="77f1c-112">To ensure your application runs on all machines, independent of the installed Microsoft Edge browser, we will release the Microsoft Edge WebView2 Runtime.</span></span> <span data-ttu-id="77f1c-113">Par ailleurs, nous mettons à jour WebView2 pour rechercher la version stable du runtime avant de rechercher des versions préliminaires du navigateur installé.</span><span class="sxs-lookup"><span data-stu-id="77f1c-113">Additionally, we will update WebView2 to search for the stable version of the runtime before searching for pre-release versions of the installed browser.</span></span>

<span data-ttu-id="77f1c-114">Les deux options de distribution sont prises en charge à l’aide du WebView2 Runtime: persistant et de la version corrigée.</span><span class="sxs-lookup"><span data-stu-id="77f1c-114">There will be support for two distribution options using the WebView2 Runtime: evergreen, and fixed version.</span></span>

<span data-ttu-id="77f1c-115">Les feuilles de distribution seront les modèles de distribution recommandés pour la plupart des développeurs.</span><span class="sxs-lookup"><span data-stu-id="77f1c-115">Evergreen will be the recommended distribution model for most developers.</span></span> <span data-ttu-id="77f1c-116">Dans ce mode, les mises à jour sont transmises automatiquement à l’WebView2 Runtime sans effort supplémentaire de votre application.</span><span class="sxs-lookup"><span data-stu-id="77f1c-116">In this mode, updates are pushed automatically to the WebView2 Runtime without additional effort from your application.</span></span> <span data-ttu-id="77f1c-117">Le modèle persistant garantit que votre application tire parti des dernières fonctionnalités et des mises à jour de sécurité pour le contenu Web hébergé.</span><span class="sxs-lookup"><span data-stu-id="77f1c-117">The evergreen model ensures that your app is taking advantage of the latest features and security updates for hosted web content.</span></span>

<span data-ttu-id="77f1c-118">Pour les environnements restreints, un modèle de distribution de version fixe est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="77f1c-118">For constrained environments there will be support for a fixed version distribution model.</span></span> <span data-ttu-id="77f1c-119">Dans ce modèle, votre application sélectionne et compresse une version spécifique de WebView2.</span><span class="sxs-lookup"><span data-stu-id="77f1c-119">In this model, your application selects and packages a specific version of WebView2.</span></span> <span data-ttu-id="77f1c-120">Les mises à jour apportées à la version WebView ne se produisent pas automatiquement et incombent à l’application.</span><span class="sxs-lookup"><span data-stu-id="77f1c-120">Updates to the WebView version do not occur automatically, and will be the responsibility of the application.</span></span> <span data-ttu-id="77f1c-121">Le modèle de version fixe est utile lorsque vous devez contrôler la version du navigateur et lorsque votre application est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="77f1c-121">The fixed version model is beneficial when you need to control the browser version, and when your application updates.</span></span> 

### <span data-ttu-id="77f1c-122">Microsoft Edge WebView2 Runtime</span><span class="sxs-lookup"><span data-stu-id="77f1c-122">Microsoft Edge WebView2 Runtime</span></span>

<span data-ttu-id="77f1c-123">Le runtime Microsoft Edge WebView2 va empaqueter les fichiers binaires de navigateur optimisés pour être utilisés par les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="77f1c-123">The Microsoft Edge WebView2 Runtime will package the browser binaries optimized for use by WebView2 applications.</span></span> <span data-ttu-id="77f1c-124">Ce service fonctionne autonome ou côte à côte avec un navigateur côté client installé.</span><span class="sxs-lookup"><span data-stu-id="77f1c-124">It will function standalone or side-by-side with a client Edge Browser installed.</span></span> <span data-ttu-id="77f1c-125">Pour installer le runtime, de nombreuses applications WebView2 peuvent être exécutées sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="77f1c-125">Installing the runtime once will support many WebView2 applications running on the client machine.</span></span> <span data-ttu-id="77f1c-126">L’installation du runtime n’apparaîtra pas sous la forme d’un navigateur pour les utilisateurs finaux et n’aura aucun raccourci sur le bureau, point d’entrée du menu Démarrer ou enregistrement de protocole.</span><span class="sxs-lookup"><span data-stu-id="77f1c-126">Installing the runtime will not appear as a browser to end-users, and will have no desktop shortcuts, start menu entry point, or protocol registration.</span></span>

<span data-ttu-id="77f1c-127">Les applications qui utilisent le runtime WebView2 doivent vérifier que l’installation du runtime est terminée.</span><span class="sxs-lookup"><span data-stu-id="77f1c-127">Applications that use the WebView2 Runtime will need to ensure that the runtime installation completed.</span></span> <span data-ttu-id="77f1c-128">Pour vous assurer que votre application installe le runtime en tant que dépendance, vous pouvez ajouter le runtime à votre flux d’installation.</span><span class="sxs-lookup"><span data-stu-id="77f1c-128">To ensure your application installs the runtime as a dependency, you’ll be able to add the runtime to your install flow.</span></span> 