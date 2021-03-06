---
title: Représentations DateTime et TimeSpan Windows Runtime
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1c51bba74bb7e5182eb25342badcae848eeba339
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942051"
---
# Représentations DateTime et TimeSpan Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

La représentation JavaScript de dates et d’heures est différente de la version Windows Runtime.  La structure [DateTime][UwpWindowsFoundationDatetime] Windows Runtime est représentée dans JavaScript en tant que [Date][MDNDate] contenant un magasin de stockage qui correspond aux `DateTime` données \ (et dont la plage et la précision sont différentes de celles du JavaScript `Date` ).  Si vous modifiez cet `Date` objet personnalisé, il devient un code JavaScript standard `Date` et perd de la précision.  `Date`Les valeurs JavaScript peuvent être transmises à un Windows Runtime `DateTime` et sont contrôlées par plages, ce qui peut entraîner des exceptions de marshaling.  

 La structure [TimeSpan][UwpWindowsFoundationTimespan] Windows Runtime est convertie en millisecondes et retourné en tant que nombre JavaScript.  

## Voir également  

[Utilisation de Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript | Documents Microsoft"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Struct DateTime | Documents Microsoft"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Structure TimeSpan | Documents Microsoft"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Date | MDN"  
