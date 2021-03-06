---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 98cfec908a0e1ad73046f7740f6e9a2efad8a853
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886286"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement NewWindowRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Handled](#handled) | Si NewWindowRequestedEvent est géré par Host.
[IsUserInitiated](#isuserinitiated) | IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.
[NewWindow](#newwindow) | Obtient la nouvelle fenêtre.
[URI](#uri) | URI cible du NewWindowRequest.
[GetDeferral](#getdeferral) | Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)

## Ses

#### Handled 

Si NewWindowRequestedEvent est géré par Host.

> propriété booléenne [gérée](#handled)

S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte. Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée. La valeur par défaut est false.

#### IsUserInitiated 

IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.

> public bool [IsUserInitiated](#isuserinitiated)

#### NewWindow 

Obtient la nouvelle fenêtre.

> public CoreWebView2 [NewWindow](#newwindow)

#### URI 

URI cible du NewWindowRequest.

> [URI](#uri) de chaîne publique

Le WebView cible ne doit pas être parcouru. Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.

#### GetDeferral 

Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

> public CoreWebView2Deferral [GetDeferral](#getdeferral)()

Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête d’ouverture de fenêtre ultérieurement. Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.

