---
description: Apprenez à exécuter JavaScript dans la console.
title: Commencer à utiliser JavaScript sur la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: d31bcfbdf728e656c9a6fff882f939f8c24cd897
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993120"
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







# Commencer à utiliser JavaScript sur la console   



Ce didacticiel interactif vous montre comment exécuter JavaScript dans la **console**Microsoft Edge devtools.  Pour plus d’informations sur la façon de consigner les messages dans la **console**, voir [utiliser la journalisation des messages][DevToolsConsoleLoggingMessages].  Pour plus d’informations sur la façon de suspendre le code JavaScript et de parcourir ce code une ligne à la fois, voir [commencer à déboguer JavaScript][DevToolsJavascriptIndex].  

:::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La console" lightbox="../media/console-javascript-example-console-playground.msft.png":::
   La **console**  
:::image-end:::  

## Présentation   

La **console** est une valeur [REPL][WikiReadEvalPrintLoop]qui correspond à la lecture, à l’évaluation, à l’impression et au bouclage.  Elle lit le code JavaScript que vous entrez, évalue votre code, imprime le résultat de l' [expression][2alityExpressionsVersusStatements], puis revient à la première étape.  

## Configurer DevTools   

Ce didacticiel est conçu pour vous permettre d’ouvrir la démonstration et d’essayer les flux de travail vous-même.  Lorsque vous effectuez une suivi physique, il est plus probable de mémoriser les flux de travail.

1.  Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir la **console**.  
1.  Maintenez `Control` la touche \ (Windows \) ou `Command` \ (MacOS \), puis cliquez sur l' **exemple de console JavaScript** pour l’ouvrir dans une nouvelle fenêtre.  
    
    *   [Exemple de console JavaScript][GlitchConsoleJavascriptExample]  
    
    :::image type="complex" source="../media/console-javascript-example-console-empty.msft.png" alt-text="Page d’exemple de langage JavaScript de la console à gauche et DevTools sur la droite" lightbox="../media/console-javascript-example-console-empty.msft.png":::
       Page d’exemple de langage JavaScript de la console à gauche et DevTools sur la droite  
    :::image-end:::  
    
## Afficher et modifier le code JavaScript ou DOM de la page   

Lorsque vous créez ou déboguez une page, il est souvent utile d’exécuter des instructions dans la **console** afin de modifier l’apparence ou l’exécution de la page.  
    
1.  Notez le texte du bouton.  
1.  Entrez `document.getElementById('hello').textContent = 'Hello, Console!'` dans la **console** , puis appuyez `Enter` sur pour évaluer l’expression.  Notez la façon dont le texte à l’intérieur du bouton change.  
    
    :::image type="complex" source="../media/console-javascript-example-console-change-button-text.msft.png" alt-text="Aspect de la console après l’évaluation de l’expression" lightbox="../media/console-javascript-example-console-change-button-text.msft.png":::
       Aspect de la **console** après l’évaluation de l’expression  
    :::image-end:::  
    
    Le code que vous avez évalué est affiché sous `"Hello, Console!"` .  Rappelez-vous des 4 étapes de REPL: lecture, évaluation, impression, boucle.  Après avoir évalué votre code, une valeur REPL imprime le résultat de l’expression.  `"Hello, Console!"`Le résultat doit donc être évalué `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## Exécuter du JavaScript arbitraire qui n’est pas lié à la page   

Il arrive parfois que vous souhaitiez créer un code de laboratoire dans lequel vous pouvez tester du code ou essayer de nouvelles fonctionnalités JavaScript que vous ne connaissez pas.  La console est l’endroit idéal pour ces types d’expériences.  

1.  Entrez `5 + 15` dans la console et appuyez sur `Enter` pour évaluer l’expression. La console imprime le résultat de l’expression sous votre code.  Dans l’illustration suivante, votre **console** doit afficher le résultat après l’évaluation de l’expression.  

1.  Tapez le code suivant dans la **console**.  Essayez de taper le texte, caractère par caractère, plutôt que de copier-coller.  
    
    ```javascript
    function add(a, b=20) { return a + b; }
    ```  
    
    Si vous n’êtes pas familiarisé avec la `b=20` syntaxe, voir [définir les valeurs par défaut des arguments de fonction][Esma6DefaultParameterValues].  
    
1.  À présent, exécutez la fonction que vous venez de définir.  
    
    :::row:::
       :::column span="":::
          ```javascript
          add(25);
          ```  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/console-javascript-example-console-playground.msft.png" alt-text="La console s’affiche après l’évaluation des expressions dans l’extrait de code" lightbox="../media/console-javascript-example-console-playground.msft.png":::
             La **console** s’affiche après l’évaluation des expressions dans l’extrait de code  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
    `add(25)` prend la valeur, `45` car lorsque la `add` fonction est appelée sans deuxième argument, la `b` valeur par défaut est `20` .  

## Étapes suivantes   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools vous permet de suspendre un script au milieu de l’exécution.  Lorsque vous êtes en pause, vous pouvez utiliser la **console** pour afficher et modifier le `window` ou la `DOM` page à ce moment précis.  Le flux de travail effectue un flux de travail puissant de débogage.  Pour un didacticiel interactif, voir [prendre en main le débogage JavaScript][DevToolsJavascriptIndex].  

La **console** dispose également d’un ensemble de fonctions pratiques qui facilitent l’interaction avec une page.  Par exemple:  

*   Au lieu de taper `document.querySelector()` pour sélectionner un élément, tapez `$()` .  Cette syntaxe est inspirée par jQuery, mais elle n’est pas réellement jQuery.  Il s’agit simplement d’un alias pour `document.querySelector()` .  
*   `debug(function)` définit efficacement un point d’arrêt sur la première ligne de cette fonction.  
*   `keys(object)` retourne une matrice contenant les clés de l’objet spécifié.  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- links -->  

[DevToolsConsoleLoggingMessages]: ./log.md "Commencer à utiliser la journalisation des messages dans la console | Documents Microsoft"  
[DevToolsConsoleReference]: ./reference.md#run-javascript "Référence de la console | Documents Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Référence sur l’API des utilitaires de console | Documents Microsoft"  
[DevToolsJavascriptIndex]: ../javascript/index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Expressions et instructions dans JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Valeurs de paramètre par défaut-gestion étendue des paramètres-ECMAScript 6: nouvelles fonctionnalités: vue d’ensemble & comparaison"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Exemple de console JavaScript | Problème"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Lecture-eval-imprimer en boucle-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/console/javascript) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
