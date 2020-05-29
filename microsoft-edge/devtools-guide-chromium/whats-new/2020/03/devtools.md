---
title: Nouveautés de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 17dab9120535ae11ea5a5456552d47dbd7f9e236
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684719"
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







# Nouveautés de DevTools (Microsoft Edge 83)   

  

Suite à la mise à jour de la planification de chrome, nous devons nous ajuster notre planning pour les versions à venir de Microsoft Edge et en annulant la version 82 de Microsoft Edge. Pour plus d’informations, consultez le [billet de blog][WindowsBlogStableRelease] .

Voici les nouvelles fonctionnalités disponibles dans le DevTools de Microsoft Edge 83.

## Annonces de l’équipe Microsoft Edge DevTools  

Les sections suivantes répertorient les annonces que vous pouvez avoir manquées de l’équipe Microsoft Edge DevTools. Découvrez-les pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.  Pour vous tenir au courant de toutes les fonctionnalités les plus récentes et les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [Suivez-nous sur Twitter][EdgeDevToolsTwitterAccount].  

### Déboguer à distance Microsoft Edge sur les appareils Windows 10  

L’application [outils de contrôle à distance pour Microsoft Edge \ (Beta)][RemoteTools] est désormais disponible dans le [Microsoft Store][MicrosoftStore].  À l’aide de cette application, qui étend [Windows Device Portal][WindowsDevicePortal], vous pouvez vous connecter à partir de l’instance de Microsoft Edge qui s’exécute sur votre ordinateur de développement sur un appareil Windows 10 distant, afficher une liste des cibles \ (tous les onglets dans Microsoft Edge et [PWAS][PWADoc] s’ouvrent sur l’appareil Windows 10) et utiliser devtools sur votre ordinateur de développement sur une cible qui s’exécute sur  

> ##### Figure1  
> Application [outils de contrôle à distance pour Microsoft Edge (Beta)][RemoteTools] disponible dans le [Microsoft Store][MicrosoftStore]  
> ![Application outils de contrôle à distance pour Microsoft Edge (Beta) disponible dans le Microsoft Store][ImageRemoteTools]  

[Consultez notre guide de configuration de votre appareil Windows 10 et de votre ordinateur de développement pour le débogage à distance][RemoteDebuggingWin10].  Donnez-nous votre avis concernant le débogage à distance par le biais du [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .  

### Nouvelles méthodes d’accès aux paramètres 

Il existe de nombreux paramètres pour le DevTools que vous pouvez personnaliser pour améliorer l’aspect et l’apparence de DevTools, ainsi que les tâches dont vous avez besoin. Dans Microsoft Edge 83, il est désormais plus facile d’accéder aux [paramètres][OverviewSettings] dans le devtools. Ouvrez les paramètres à l’aide de l’icône d’engrenage en regard des alertes de console et du menu principal.

> ##### Figure 2 
> L’icône d’engrenage s’ouvre dans l’DevTools ![ l’icône d’engrenage qui s’ouvre dans la devtools][ImageSettingsGearIcon]  

Vous pouvez également ouvrir les [paramètres][OverviewSettings] à partir du **menu principal** sous **autres outils**.

> ##### Figure3 
> Menu principal > plus d’outils > ![ menu principal paramètres > autres outils > paramètres][ImageSettingsMainMenu]  

[#1050855][crbug1050855] problème de chrome

### Infobars nouveau et amélioré

Les barres de notification d’information \ (infobars \) dans DevTools présentent désormais une meilleure interface et de nouvelles fonctionnalités. Dans Microsoft Edge 83, infobars est plus facile à lire et à proposer des boutons pour vous permettre d’effectuer l’action appropriée immédiatement.

> ##### Figure 4
> Barre d’informations pour l’impression d’un fichier minified dans la ![ barre d’informations Microsoft edge 83 pour l’impression d’un fichier minified dans Microsoft edge 83][ImageInfobar]  

[#1056348][crbug1056348] problème de chrome

### Parcourir le sélecteur de couleurs à l’aide du clavier  

Le [Sélecteur de couleurs][ColorPicker] est une interface utilisateur du [panneau éléments][ElementsDoc] permettant de changer et de faire des `color` `background-color` déclarations.  Dans les versions précédentes de Microsoft Edge, vous ne parvenez pas à naviguer dans la section **nuances** du [Sélecteur de couleur][ColorPicker] à l’aide du clavier.  

> ##### Figure 5  
> Vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section **nuances** du [Sélecteur de couleurs][ColorPicker] .  
> ![Vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section nuances du sélecteur de couleurs.][ImageColorPicker]  

Dans Microsoft Edge 83, vous pouvez maintenant utiliser le clavier pour déplacer le sélecteur dans la section **tons** du sélecteur de couleurs.  

[#963183][crbug963183] problème de chrome  

### L’onglet Propriétés est désormais rempli après une actualisation de page  

Dans Microsoft Edge 81 et les versions antérieures, l' **onglet Propriétés** dans le [panneau éléments][ElementsDoc] a été rompu par l’actualisation de la page.  Lorsque vous actualisez la page, l' **onglet Propriétés** ne remplissait pas les propriétés de l’élément actuellement sélectionné.  

> ##### Figure 6  
> Dans Microsoft Edge 81 et versions antérieures, l' **onglet Propriétés** était vide après une actualisation de page  
> ![Dans Microsoft Edge 81 et versions antérieures, l’onglet Propriétés était vide après une actualisation de page][ImagePropertiesIn81]  

Dans Microsoft Edge 83, vous pouvez désormais voir les propriétés de l’élément actuellement sélectionné après une actualisation de page dans l' **onglet Propriétés**.  

> ##### Figure 7  
> Dans Microsoft Edge 83, l' **onglet Propriétés** affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page  
> ![Dans Microsoft Edge 83, l’onglet Propriétés affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page][ImagePropertiesIn82]  

[#1050999][crbug1050999] problème de chrome  

### Utiliser les touches de direction pour faire défiler l’outil modifications  

L' **outil modifications** effectue le suivi des modifications que vous avez apportées à CSS ou JavaScript dans le devtools.  Vous pouvez utiliser l' **outil modifications** pour afficher rapidement toutes vos modifications et revenir à votre éditeur/IDE.  

Ouvrez l' **outil modifications** en appuyant sur `Ctrl` + `Shift` + `P` la devtools pour ouvrir le [menu de commandes][DevToolsCommandMenuIndex] et en tapant `changes` .  Activez et exécutez la commande **afficher les modifications** pour ouvrir l' **outil modifications** dans le tiroir devtools.  

Lorsque vous avez apporté une modification à un fichier minified, l' **outil modifications** vous permet de faire défiler horizontalement pour afficher l’ensemble de votre code minified.  À partir de Microsoft Edge 83, vous pouvez à présent faire défiler les touches de direction de votre clavier.  

> ##### Figure8  
> Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour voir les modifications que vous avez apportées à votre code minified dans l' **outil modifications** .  
> ![Dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher votre code minified dans l’outil modifications.][ImageChanges]  

Si vous utilisez un lecteur d’écran ou le clavier pour naviguer dans DevTools, envoyez-nous vos commentaires en nous appuyant sur un [Tweet][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .  

[#963183][crbug963183] problème de chrome  

## Annonces du projet de chrome  

Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 83 qui ont été fournies au projet de chrome Open source.  

### Émuler les déficiences de la vision   

Ouvrez l' [onglet rendu][RenderingDoc] , puis utilisez la nouvelle fonctionnalité **émuler les déficiences** de la vision pour mieux comprendre comment les personnes présentant différents types d’déficiences de la vision connaissent votre site.  

> ##### Figure9  
> Émulation d’une vision floue  
> ![Émulation d’une vision floue][ImageEmulatingBlurredVision]  

DevTools est en mesure d’émuler une vision floue et des [types de troubles de la vision couleur][ColorBlindnessTypes]suivants.  

| Déficience de la vision couleur | Détails |  
|:--- |:--- | 
| Protanopia | L’impossibilité de percevoir des lumières rouges. |  
| Deuteranopia | L’impossibilité de percevoir une lumière verte. |  
| Tritanopia | L’impossibilité de percevoir une lumière bleue. |  
| Achromatopsia | L’impossibilité de percevoir une couleur, à l’exception des nuances de gris. | 

Il existe des versions moins extrêmes de ces déficiences de vision couleur, et en fait, elles sont plus courantes.
Par exemple, protanomaly est une sensibilité réduite de l’éclairage rouge (par opposition à protanopia, qui est la possibilité d’obtenir une lumière rouge). Toutefois, ces déficiences en matière de vision omaly n’ont pas été aussi clairement définies: chaque personne ayant une déficience de la vision est différente et peut voir ce qui se passe d’un point de vue différent (il est en mesure de percevoir plus ou moins des couleurs pertinentes).

En concevant des simulations plus extrêmes dans DevTools, il est garanti que les applications Web sont accessibles aux personnes utilisant protanomaly, Deuteranomaly, tritanomaly et achromatomaly.

Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .  

[#1003700][crbug1003700] problème de chrome  

### Émuler des paramètres régionaux 

Émulez des paramètres régionaux en définissant un **Sensors**emplacement dans la  >  **zone**capteurs. [Ouvrez le **menu de commandes** ][DevToolsCommandMenuIndex] et tapez `Sensors` pour accéder à l’onglet **capteurs** . Après avoir effectué ces actions, DevTools modifie les paramètres régionaux actuels par défaut, ce qui affecte les éléments suivants:

- `Intl.*` Par exemple: `new Intl.NumberFormat().resolvedOptions().locale`
- autres API JavaScript prenant en charge des paramètres régionaux tels que `String.prototype.localeCompare` et `*.prototype.toLocaleString` , par exemple:`123_456..toLocaleString()`
- API DOM telles que `navigator.language` et `navigator.languages`
- [`Accept-Language`][MDNAcceptLanguage]en-tête de requête http

> ##### Figure10  
> Émulation d’un paramètre régional  
> ![Émulation d’un paramètre régional][ImageEmulatingLocales]  

Pour essayer une démonstration, voir [exemple de code dépendant des paramètres régionaux][MathiasByensLocaleDemo].

[#1051822][crbug1051822] problème de chrome

### Stratégie d’intégrateur à l’origine du débogage   

Le panneau réseau fournit désormais des informations de débogage de la [stratégie d’incorporation][COEP] à l’origine.  

La colonne **État** donne désormais une explication rapide de la raison pour laquelle une requête a été bloquée ainsi qu’un lien pour afficher les en-têtes de cette requête pour un débogage supplémentaire:  

> ##### Figure11  
> Demandes bloquées dans la colonne **État**  
> ![Demandes bloquées dans la colonne État][ImageNetworkStatus]  

La section **en-têtes de réponse** de l’onglet **en-têtes** fournit davantage d’instructions pour résoudre les problèmes:  

> ##### Figure12  
> Conseils supplémentaires dans la section en-têtes de réponse  
> ![Conseils supplémentaires dans la section en-têtes de réponse][ImageNetworkGuidance]  

Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .  

[#1051466][crbug1051466] problème de chrome  

### Afficher les requêtes réseau qui définissent un chemin de cookie spécifique 

Utilisez le nouveau `cookie-path` mot clé de filtre dans le panneau **réseau** pour vous concentrer sur les requêtes réseau qui définissent un [chemin de cookie][MDNCookiePath]spécifique.

Consultez les [demandes de filtre par propriétés][NetworkProperties] pour découvrir d’autres mots clés comme `cookie-path` .

### **Ancrer à gauche** à partir du menu de commandes   

Ouvrez le [menu de commandes][DevToolsCommandMenuIndex] et exécutez la `Dock to left` commande pour déplacer devtools à gauche de votre fenêtre d’affichage.  

> ##### Figure13  
> DevTools ancré à gauche de la fenêtre d’affichage  
> ![DevTools ancré à gauche de la fenêtre d’affichage][ImageDockToLeft]  

> [!NOTE]
> La fonctionnalité **ancrer à gauche** est disponible depuis Microsoft Edge 75, mais uniquement accessible à partir du [**menu principal**][MainMenuDoc].  La nouvelle fonctionnalité de Microsoft Edge 83 est que vous pouvez maintenant accéder à cette fonctionnalité à partir du menu de commandes.  

Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .  

[#1011679][crbug1011679] problème de chrome  

### Le panneau **d’audit** est désormais le panneau de **signalisation** .   

L’équipe DevTools a fréquemment reçu des commentaires de la part des développeurs Web, alors qu’il était possible d’exécuter un [phare][GithubGoogleChromeLighthouse] à partir de devtools, **lorsque l’utilisateur** a essayé le panneau de configuration, il n’a pas été en mesure de trouver le panneau de **signalisation.**  

> ##### Figure14  
> Panneau de signalisation  
> ![Panneau de signalisation][ImageLighthouse]  

> [!NOTE]
> Le panneau de **signalisation** comporte des liens vers du contenu hébergé sur des sites Web tiers.  Microsoft n’est pas responsable et n’a aucun contrôle sur le contenu de ces sites et sur les données qu’ils peuvent recueillir.  

### Supprimer tous les remplacements locaux dans un dossier   

Après avoir configuré les **remplacements locaux** , vous pouvez cliquer avec le bouton droit sur un dossier et sélectionner l’option **supprimer toutes les substitutions** dans ce dossier.  

> ##### Figure15  
> Supprimer tous les remplacements  
> ![Supprimer tous les remplacements][ImageDeleteOverrides]  

Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .  

[#1016501][crbug1016501] problème de chrome  

### Interface utilisateur de tâches longues mise à jour   

Une **tâche longue** correspond à du code JavaScript qui monopolit le thread principal pendant un certain temps, provoquant le gel d’une page Web.  

Vous avez la possibilité de [visualiser de longs tâches dans le panneau de performance][LongTasksInPerformancePanel] pour un certain temps, mais dans Microsoft Edge 83, l’interface utilisateur d’une visualisation de tâches longues du panneau de performance a été mise à jour.  La partie tâches longues d’une tâche est désormais colorée avec un arrière-plan rouge rayé.  

> ##### Figure16  
> Nouvelle interface utilisateur de tâche longue  
> ![Nouvelle interface utilisateur de tâche longue][ImageLongTask]  

Envoyez-nous vos commentaires en le [tweetant][PostTweetEdgeDevTools] ou en cliquant sur l’icône de [Commentaires](#feedback) .  

[#1054447][crbug1054447] problème de chrome  

### Icône masquable dans le volet manifeste   

Android Oreo introduit des icônes adaptatives qui affichent des icônes d’application dans différentes formes sur différents modèles d’appareil.  Les icônes qui peuvent être **masquées** sont un nouveau format d’icône qui prend en charge les icônes adaptatives, qui vous permettent de vous assurer que votre icône [PWA][PWADoc] fonctionne correctement sur les appareils qui prennent en charge la norme d’icônes masquées.  

Activez la case à cocher nouveau **afficher uniquement la zone sécurisée minimum pour les icônes masquées** dans le volet **manifeste** pour vérifier que votre icône MASKABLE fonctionne correctement sur les appareils Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

> ##### Figure17  
> Case à cocher «Afficher uniquement la zone sécurisée minimum pour les icônes masquées»  
> ![Case à cocher «Afficher uniquement la zone sécurisée minimum pour les icônes masquées»][ImageMaskableIcons]  

> [!NOTE]
> Cette fonctionnalité est lancée dans Microsoft Edge 81.  Les mises à jour abordées ici dans Microsoft Edge 83 n’ont pas été abordées dans [les nouveautés de devtools (Microsoft edge 81)][WhatsNew81].  

## Commentaires   

  

Découvrir les nouvelles fonctionnalités et les modifications de cette publication ou tout autre sujet lié à DevTools:  

*   Envoyez vos commentaires à l’aide de l’icône de **Commentaires** dans le devtools  
*   Tweeter sur [@EdgeDevTools][PostTweetEdgeDevTools]  
*   Envoyez une suggestion au [site Web de votre choix][TheWebWeWant]  
*   Classer des bogues sur ce document dans le référentiel [Edge-développeurs][GitHubMicrosoftDocsEdgeDeveloperNewIssue]  

> ##### Figure 18  
> Icône de **Commentaires** dans le Microsoft Edge devtools  
> ![L’icône * * Feedback * * dans Microsoft Edge DevTools][ImageFeedbackIcon]  

## Télécharger les canaux Microsoft Edge preview   

Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.  Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.  

<!-- <<../../_shared/devtools-feedback.md>>

<<../../_shared/canary.md>>

<<../../_shared/discover.md>> -->

  

<!-- image links -->  

[ImageRemoteTools]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/remote-tools.msft.png "Figure 1: application outils de contrôle à distance pour Microsoft Edge (Beta) disponible dans le Microsoft Store"  
[ImageSettingsGearIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings.msft.png "Figure 2: l’icône d’engrenage s’ouvre pour afficher les paramètres dans le DevTools"
[ImageSettingsMainMenu]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings2.msft.png "Figure 3: menu principal > plus d’outils > paramètres"
[ImageInfobar]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/infobar.msft.png "Figure 4: barre d’informations pour l’impression d’un fichier minified dans Microsoft Edge 83"
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/color-picker.msft.png "Figure 5: vous pouvez maintenant utiliser votre clavier pour déplacer le sélecteur dans la section tons du sélecteur de couleurs"  
[ImagePropertiesIn81]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-81.msft.png "Figure 6: image de l’onglet Propriétés dans Microsoft Edge 81 et versions antérieures"  
[ImagePropertiesIn82]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-82.msft.png "Figure 7: dans le 83 Microsoft Edge, l’onglet Propriétés affiche les propriétés de l’élément actuellement sélectionné après une actualisation de la page"  
[ImageChanges]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/changes.msft.png "Figure 8: dans Microsoft Edge 83, vous pouvez faire défiler horizontalement avec les touches de direction pour afficher votre code minified dans l’outil modifications."  
[ImageEmulatingBlurredVision]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/vision.msft.png "Figure 9: émulation d’une vision floue"  
[ImageEmulatingLocales]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/locale.msft.png "Figure 10: émulation d’un paramètre régional"
[ImageNetworkStatus]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/status.msft.png "Figure 11: demandes bloquées dans la colonne État"  
[ImageNetworkGuidance]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/guidance.msft.png "Figure 12: conseils supplémentaires dans la section en-têtes de réponse"  
[ImageDockToLeft]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/dock-to-left.msft.png "Figure 13: DevTools fixé à gauche de la fenêtre d’affichage"  
[ImageLighthouse]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/lighthouse.msft.png "Figure 14: panneau de signalisation"  
[ImageDeleteOverrides]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/overrides.msft.png "Figure 15: supprimer tous les remplacements"  
[ImageLongTask]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/long-task.msft.png "Figure 16: interface utilisateur de nouvelle tâche longue"  
[ImageMaskableIcons]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/maskable-icons.msft.png "Figure 17: activez la case à cocher Afficher uniquement la zone sécurisée minimum pour les icônes masquées."  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/feedback-icon.msft.png "Figure 18: icône de commentaires dans le Microsoft Edge DevTools"  

[ImageLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/breakpoint.msft.png
[ImageLogpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/logpoint.msft.png

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools compte Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nouveau problème-MicrosoftDocs/Edge-développeur"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canaux Microsoft Edge preview"  
[TheWebWeWant]: https://aka.ms/webwewant "Le site Web de votre choix"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "Nouveautés de DevTools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Changer les couleurs à l’aide du sélecteur de couleurs"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Changer la position dans le menu principal"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Afficher l’activité du thread principal"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analyser les performances de rendu à l’aide de l’onglet rendu"  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Prendre en main les appareils Windows 10 de débogage à distance"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Points d’arrêt de code de ligne"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Vue d’ensemble de Windows Device Portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Outils de contrôle à distance pour Microsoft Edge (bêta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Mise à jour sur les versions de canal stable pour Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Types de cécité du Colour"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Exemple de code dépendant des paramètres régionaux"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Problème 963183: DevTools n’est pas conforme à la norme WCAG"  
[crbug1003700]: https://crbug.com/1003700 "Problème 1003700: ajout de la prise en charge de DevTools pour la simulation d’déficience de vision couleur"  
[crbug1011679]: https://crbug.com/1011679 "Problème 1011679: Introduisez l’option ancrer à gauche dans le menu de commandes"  
[crbug1016501]: https://crbug.com/1016501 "Problème 1016501: demande de fonctionnalité: bouton permettant de supprimer tous les remplacements locaux"  
[crbug1050999]: https://crbug.com/1050999 "Problème 1050999: onglet Propriétés"  
[crbug1051466]: https://crbug.com/1051466 "Problème 1051466: prendre en charge le débogage de COOP/COEP dans DevTools"  
[crbug1054447]: https://crbug.com/1054447 "Problème 1054447: mettre à jour les métriques de performance dans DevTools Timeline"  
[crbug1051822]: https://crbug.com/1051822 "Problème 1051822: DevTools: ajouter une interface utilisateur pour émuler des paramètres régionaux"
[crbug1041830]: https://crbug.com/1041830 "Problème 1041830: améliorer les couleurs pour les points d’arrêt"
[crbug1050855]: https://crbug.com/1050855 "Problème 1050855: l’affichage des paramètres est difficile à découvrir"
[crbug1056348]: https://crbug.com/1056348 "Problème 1056348: actualisation du composant barre d’informations"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Explication de COOP et de COEP-explication-la politique d’ouverture"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Explication de la stratégie d’intégration de COOP et COEP"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Phare GitHub référentiel Samples"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/03/devtools/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  