---
description: Ouvrez l’onglet «Affichage», puis sélectionnez «émuler les médias CSS» > «imprimer».
title: Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1b71135c5ed2d86903b76e659434ee2125985a24
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993050"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)   



La [requête imprimer][MDNUsingMediaQueries] sur le média détermine l’apparence de votre page avant son impression.  Pour forcer votre page en mode aperçu avant impression:  

1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menu de commandes" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Tapez `rendering` , sélectionnez **afficher le rendu**, puis appuyez sur `Enter` .  
1.  Sous **émuler le média CSS** , sélectionnez **Imprimer**.  
    
    :::image type="complex" source="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png" alt-text="Mode aperçu avant impression" lightbox="../media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png":::
       Mode aperçu avant impression  
    :::image-end:::  
    
À partir de cet emplacement, vous pouvez afficher et modifier votre CSS, comme n’importe quelle autre page Web.  Voir [commencer à afficher et modifier des feuilles CSS][DevToolsCSSGetStarted].  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevToolsCSSGetStarted]: ./index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
