---
description: Découvrez comment détecter les problèmes de réseau dans le volet réseau de Microsoft Edge DevTools.
title: Guide des problèmes réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ccd78c34a50bf235416df58aad28df9253b1b24e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993372"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Guide de problèmes réseau   




Ce guide vous montre comment détecter les problèmes de réseau ou les opportunités d’optimisation dans le volet réseau de Microsoft Edge DevTools.  

Pour [plus d’informations][NetworkPerformance] sur les concepts de base du **réseau** , voir découvrir le panneau de configuration.  

## Demandes mises en file d’attente ou bloquées   

**Symptômes**  

Six demandes sont en train de télécharger simultanément.  Après cela, une série de demandes est mise en file d’attente ou bloquée.  Après l’exécution de l’une des six premières demandes, une des requêtes de la file d’attente démarre.  

Dans la **figure** ci-dessous, les six premières demandes de l' `edge-iconx1024.msft.png` actif commencent simultanément.  Les demandes ultérieures sont bloquées jusqu’à ce que l’une des six nouvelles préfinissements.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Exemple d’une série mise en file d’attente ou bloquée dans le panneau **réseau**  
:::image-end:::  

**Causes**  

Il y a trop de demandes sur un domaine unique.  Sur les connexions HTTP/1.0 ou HTTP/1.1, Microsoft Edge autorise un maximum de six connexions TCP simultanées par hôte.  

**Correctifs**  

*   Implémentez Domain sharding si vous devez utiliser HTTP/1.0 ou HTTP/1.1.  
*   Utiliser HTTP/2.  N’utilisez pas le domaine sharding avec HTTP/2.  
*   Supprimez ou différez les demandes inutiles de manière à ce que les demandes critiques soient téléchargées plus tôt.  
    
## Temps lent vers le premier octet (TTFB)   

**Symptômes**  

Une requête passe un certain temps en attente de réception du premier octet du serveur.  

Dans l’illustration ci-dessous, la barre verte longue de la **cascade** indique que la requête attendait un certain temps.  Il a été simulé à l’aide d’un profil afin de limiter la vitesse du réseau et d’ajouter un délai.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Exemple d’une requête avec un délai de première octet lent" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Exemple d’une requête avec un délai de première octet lent  
:::image-end:::  

**Causes**  

*   La connexion entre le client et le serveur est lente.  
*   La réponse du serveur est lente.  Hébergez le serveur localement pour déterminer s’il s’agit d’une connexion ou d’un serveur lent.  Si vous obtenez encore un temps lente pour le premier octet \ (TTFB \) lors de l’accès à un serveur local, le serveur est lent.  
    
**Correctifs**  

*   Si la connexion est lente, envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.  
*   Si le serveur est lent, envisagez d’optimiser les requêtes de base de données, de mettre en cache ou de modifier votre configuration serveur.  
    
## Téléchargement de contenu lent   

**Symptômes**  

Le téléchargement d’une requête prend beaucoup de temps.  

Dans l’illustration ci-dessous, la barre bleue longue en **regard du** fichier PNG signifie que le téléchargement a duré longtemps.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Exemple d’une requête prenant du temps à télécharger" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Exemple d’une requête prenant du temps à télécharger  
:::image-end:::  

**Causes**  

*   La connexion entre le client et le serveur est lente.  
*   Un grand nombre de contenus est en cours de téléchargement.  
    
**Correctifs**  

*   Envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.  
*   Envoyez moins d’octets en optimisant vos demandes.  
    
## Compétences de collaboration  

Vous rencontrez un problème réseau qui doit être ajouté à ce guide?  

*   Envoyez un tweet à [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Pour **Envoyer** ![ des ][ImageSendFeedbackIcon] `Alt` + `Shift` + `I` `Option` + `Shift` + `I` commentaires ou des demandes de fonctionnalité, sélectionnez Envoyer des commentaires \ (envoyer des commentaires \) dans le devtools ou appuyez sur \  
*   [Ouvrez un problème][WebFundamentalsIssue] dans le référentiel Samples docs.  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Examiner l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nouveau problème-MicrosoftDocs/Edge-développeur"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/issues) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Jonathan Garbee][JonathanGarbee] \ (Google Developer expertise pour Web Technology \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
