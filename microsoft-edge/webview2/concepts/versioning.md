---
description: Modèles de contrôle de version utilisés pour Microsoft Edge WebView2
title: Version de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8463ce403af069cf25dbf7b08bb49d44c1e54501
ms.sourcegitcommit: f1aa8925f7985a2bbfd951f188a8c19c97e4ff6f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/18/2020
ms.locfileid: "10659566"
---
# Présentation des versions de navigateur et de WebView2  

WebView2 dépend de Microsoft Edge pour fonctionner.  Chaque SDK WebView2 nécessite qu’une version de navigateur minimum soit installée.  Cette version de navigateur est spécifiée dans nos [notes de publication][Webview2Releasenotes].  La version minimale est susceptible de apparaître dans la version de package du SDK.  Par exemple, si vous utilisez la `SDK package version 0.9.488` , vous devez installer Microsoft Edge avec le numéro de build 488 ou une version ultérieure.  Pour plus d’informations sur les dernières versions du navigateur, voir [canaux de navigateur][DeployedgeChannels].  

> [!NOTE]
> WebView2 est actuellement en version preview.  Même si l’équipe WebView de Microsoft Edge s’efforce de garantir la compatibilité descendante entre les versions de navigateur et les SDK, il n’est pas garanti que certaines versions plus récentes du navigateur ne prennent pas en charge les versions antérieures du SDK.  Si des modifications sont apportées [entre les versions][Webview2Releasenotes]de navigateur et les kits de développement logiciel (SDK) Microsoft Edge  

À l’avenir, l’équipe WebView Microsoft Edge doit changer le modèle de distribution.  Les plans d’équipe de l’équipe Web Microsoft Edge pour supprimer la dépendance directe sur le navigateur Microsoft Edge à partir de WebView2.  <!--To learn more, see [WebView2 Runtime][Webview2IndexEdgeRuntime] in the [Distribution][Webview2Distibution] section.  -->  

<!--todo: dd link to distribution.md after publication  -->  

## API expérimentales  

Si WebView2 est une version d’évaluation, les API du SDK sont censées rester les mêmes au niveau GA.  Il existe des [API expérimentales][Webview2ReferenceWin3209488Experimental] incluses dans le kit de développement logiciel (SDK).  Évaluez les API expérimentales et envoyez vos commentaires à l’aide de l' [référentiel samples de commentaires WebView][GithubMicrosoftedgeWebviewfeedback].  

### Feuille de route  

Une fois que WebView2 atteint un état disponible général stable et que nous publions le kit de développement logiciel (SDK) 1.0.0, l’équipe WebView Microsoft Edge doit déplacer toutes les API expérimentales vers un package de version préliminaire.  La version préliminaire du package continue d’accepter les commentaires et de vous familiariser avec les fonctionnalités les plus récentes, tandis que la version stable conserve la compatibilité descendante.  

<!--links -->

[Webview2Distibution]: ./distribution.md "n’existe pas | Documents Microsoft"  
[Webview2IndexEdgeRuntime]: ../index.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime-Microsoft Edge WebView2 (version préliminaire du développeur) | Documents Microsoft"  
[Webview2ReferenceWin3209488Experimental]: ../reference/win32/0-9-488-reference-webview2.md#experimental "Expérimentation-référence (WebView2) | Documents Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notes de publication pour WebView2 SDK | Documents Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Vue d’ensemble des canaux Microsoft Edge | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  