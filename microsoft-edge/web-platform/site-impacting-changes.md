---
description: Cette page fournit un récapitulatif des changements à forte impact qui peuvent avoir un impact sur la compatibilité de site
title: Compatibilité de site-modification affectant les modifications apportées à Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilité, plateforme Web
ms.openlocfilehash: c35f38bd43255ab9a8c965c8fa9f3b1c8a95bff6
ms.sourcegitcommit: 1760ea15e83045168aec6bf507bc4fe7dfb5568f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652299"
---
# Compatibilité de site-modification affectant les modifications apportées à Microsoft Edge  

Le Web évolue en permanence pour améliorer l’interface utilisateur, la sécurité et la confidentialité.  Dans certains cas, les modifications apportées risquent d’avoir une incidence sur les fonctionnalités des pages existantes.  Le tableau ci-dessous récapitule les changements particulièrement importants que l’équipe Microsoft Edge effectue actuellement.  Vérifiez régulièrement. l’équipe Microsoft Edge est chargée de mettre à jour cette page en apportant des réflexions, des chronologies et de nouvelles modifications.  

| Changement | Canal Stable | Expérimentation | Informations complémentaires |  
|:--- |:--- |:--- |:--- |
| Cookies par défaut `SameSite=Lax` | [Chrome ou chrome + 1](#release-comments)  | V82 Canaries, dev V82 | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, consultez l’entrée d’état de la [plateforme chrome][ChromePlatformStatus5088147346030592].  |  
| Stratégie de renvoi: par défaut `strict-origin-when-cross-origin` | [Chrome ou chrome + 1](#release-comments)  | V79 Canaries, dev V79 | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, consultez l’entrée d’état de la [plateforme chrome][ChromePlatformStatus6251880185331712].  |  
| Ne pas autoriser les XmlHttpRequest synchrones dans la page de masquage | [Chrome + 1](#release-comments) \ (Edge V83 \) |  | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Dans le chrome, Microsoft Edge propose une stratégie de groupe pour désactiver cette modification jusqu’au 88 Edge.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, consultez l’entrée d’état de la [plateforme chrome][ChromePlatformStatus4664843055398912].  |  
| Afficher une invite discrète pour les demandes d’autorisation de notification |  | V83 Canaries, dev V83 | Les utilisateurs peuvent désormais accepter des demandes de notification quiet en `edge://settings/content/notifications` .  Lorsque ce paramètre est activé, Microsoft Edge affiche une icône de requête subtile dans la barre d’adresse pour les sites qui demandent d’envoyer à l’utilisateur des notifications à l’aide de l' `Notifications` `Push` API ou.  Cette icône discrète remplace l’invite d’autorisation flyout.  Dans le cas d’une expérience de la Canaries et du dev, ce comportement est activé par défaut pour certains utilisateurs, sur tous les sites qui demandent des autorisations de notifications.  Les utilisateurs peuvent choisir de désactiver `edge://settings/content/notifications` .  À l’avenir, l’équipe Microsoft Edge risque d’explorer l’affichage de l’invite de menu volant dans des situations spécifiques en fonction des comportements d’utilisateur et d’autres entrées.  |  
| Désactiver TLS/1.0 et TLS/1.1 par défaut | Bordure V84 |  | Pour vous aider à découvrir les sites concernés, vous pouvez définir le `edge://flags/#display-legacy-tls-warnings` drapeau de sorte que Microsoft Edge affiche une notification de non-blocage «non sécurisée» lors du chargement de pages qui nécessitent des protocoles TLS hérités.  La stratégie de groupe [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] autorise la réactivation de TLS/1.0 et TLS/1.1; la stratégie reste disponible jusqu’au 88 Edge.  |  
| Bloquer les téléchargements de contenu mixte | [Chrome + 1](#release-comments) \ (Edge V85 \)  |  | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, consultez l' [entrée de blog Google Security][GoogleBlogSecurity20200206].  Le planning de déploiement Microsoft des types de fichiers à avertir ou bloquer est planifié pour une version après chrome.  |  

##### Commentaires de publication  

:::row:::
   :::column span="1":::
      Chrome + 1
   :::column-end:::
   :::column span="2":::
      Sur la base des commentaires des utilisateurs et des développeurs, la fonctionnalité indiquée ou la modification d’une version après chrome.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome ou chrome + 1
   :::column-end:::
   :::column span="2":::
      En fonction des commentaires des utilisateurs et des développeurs, de la fonctionnalité ou du changement de navires en même temps ou en une seule dissémination après chrome.
   :::column-end:::
:::row-end:::


<!-- image links -->  

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-politiques"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Désactiver la synchronisation XHR dans l’état de la plateforme JavaScript-chrome de la page"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies par défaut de l’état de la plateforme SameSite = Lax-chrome"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Stratégie de point d’ouverture: par défaut sur l’état de la plateforme chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protection des utilisateurs contre les téléchargements insécurisés dans Google Chrome-blog de sécurité Google Online"  