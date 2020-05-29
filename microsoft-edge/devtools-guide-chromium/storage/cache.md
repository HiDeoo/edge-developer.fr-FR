---
title: Afficher les données du cache avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612073"
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





# <span data-ttu-id="f86c5-103">Afficher les données du cache avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f86c5-103">View Cache Data With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="f86c5-104">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les données [du cache][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="f86c5-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="f86c5-105">Si vous essayez d’inspecter les données [du cache http][MDNHTTPCaching] , il ne s’agit pas du guide souhaité.</span><span class="sxs-lookup"><span data-stu-id="f86c5-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  
<span data-ttu-id="f86c5-106">Recherchez les informations dans la colonne **taille** du journal du **réseau**.</span><span class="sxs-lookup"><span data-stu-id="f86c5-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="f86c5-107">Voir [enregistrement][DevtoolsNetworkLogActivity]de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="f86c5-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="f86c5-108">Afficher les données du cache</span><span class="sxs-lookup"><span data-stu-id="f86c5-108">View cache data</span></span>   

1.  <span data-ttu-id="f86c5-109">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="f86c5-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="f86c5-110">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="f86c5-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-111">Figure1</span><span class="sxs-lookup"><span data-stu-id="f86c5-111">Figure 1</span></span>  
    > <span data-ttu-id="f86c5-112">Volet manifeste</span><span class="sxs-lookup"><span data-stu-id="f86c5-112">The Manifest pane</span></span>  
    > ![Volet manifeste][ImageManifestPane]  

1.  <span data-ttu-id="f86c5-114">Développez la section **stockage du cache** pour afficher les caches disponibles.</span><span class="sxs-lookup"><span data-stu-id="f86c5-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-115">Figure 2</span><span class="sxs-lookup"><span data-stu-id="f86c5-115">Figure 2</span></span>  
    > <span data-ttu-id="f86c5-116">Caches disponibles</span><span class="sxs-lookup"><span data-stu-id="f86c5-116">Available caches</span></span>  
    > ![Caches disponibles][ImageCache]  

1.  <span data-ttu-id="f86c5-118">Sélectionnez un cache pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="f86c5-118">Select a cache to view the contents.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-119">Figure3</span><span class="sxs-lookup"><span data-stu-id="f86c5-119">Figure 3</span></span>  
    > <span data-ttu-id="f86c5-120">Affichage du contenu d’un cache</span><span class="sxs-lookup"><span data-stu-id="f86c5-120">Viewing the contents of a cache</span></span>  
    > ![Affichage du contenu d’un cache][ImageCacheView]  

1.  <span data-ttu-id="f86c5-122">Sélectionnez une ressource pour afficher les en-têtes HTTP dans la section située sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="f86c5-122">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-123">Figure 4</span><span class="sxs-lookup"><span data-stu-id="f86c5-123">Figure 4</span></span>  
    > <span data-ttu-id="f86c5-124">Affichage des en-têtes HTTP d’une ressource</span><span class="sxs-lookup"><span data-stu-id="f86c5-124">Viewing the HTTP headers of a resource</span></span>  
    > ![Affichage des en-têtes HTTP d’une ressource][ImageViewCacheResource]  

1.  <span data-ttu-id="f86c5-126">Sélectionnez **Aperçu** pour afficher le contenu d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="f86c5-126">Select **Preview** to view the content of a resource.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-127">Figure 5</span><span class="sxs-lookup"><span data-stu-id="f86c5-127">Figure 5</span></span>  
    > <span data-ttu-id="f86c5-128">Affichage du contenu d’une ressource</span><span class="sxs-lookup"><span data-stu-id="f86c5-128">Viewing the content of a resource</span></span>  
    > ![Affichage du contenu d’une ressource][ImageCacheContent]  

## <span data-ttu-id="f86c5-130">Actualiser une ressource</span><span class="sxs-lookup"><span data-stu-id="f86c5-130">Refresh a resource</span></span>   

1.  <span data-ttu-id="f86c5-131">[Afficher les données d’un cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="f86c5-131">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="f86c5-132">Sélectionnez la ressource que vous voulez actualiser.</span><span class="sxs-lookup"><span data-stu-id="f86c5-132">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="f86c5-133">DevTools le met en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f86c5-133">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-134">Figure 6</span><span class="sxs-lookup"><span data-stu-id="f86c5-134">Figure 6</span></span>  
    > <span data-ttu-id="f86c5-135">Sélection d’une ressource</span><span class="sxs-lookup"><span data-stu-id="f86c5-135">Selecting a resource</span></span>  
    > ![Sélection d’une ressource][ImageCacheSelected]  

1.  <span data-ttu-id="f86c5-137">Sélectionnez **Actualiser** l' ![ actualisation ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="f86c5-137">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="f86c5-138">Filtrer les ressources</span><span class="sxs-lookup"><span data-stu-id="f86c5-138">Filter resources</span></span>   

1.  <span data-ttu-id="f86c5-139">[Afficher les données d’un cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="f86c5-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="f86c5-140">Utilisez la zone de texte **Filtrer par chemin** pour filtrer les ressources qui ne correspondent pas au chemin que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="f86c5-140">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-141">Figure 7</span><span class="sxs-lookup"><span data-stu-id="f86c5-141">Figure 7</span></span>  
    > <span data-ttu-id="f86c5-142">Filtrage des ressources qui ne correspondent pas au chemin spécifié</span><span class="sxs-lookup"><span data-stu-id="f86c5-142">Filtering out resources that do not match the specified path</span></span>  
    > ![Filtrage des ressources qui ne correspondent pas au chemin spécifié][ImageCacheFilter]  

## <span data-ttu-id="f86c5-144">Suppression d'une ressource</span><span class="sxs-lookup"><span data-stu-id="f86c5-144">Delete a resource</span></span>   

1.  <span data-ttu-id="f86c5-145">[Afficher les données d’un cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="f86c5-145">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="f86c5-146">Sélectionnez la ressource que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="f86c5-146">Select the resource that you want to delete.</span></span>  <span data-ttu-id="f86c5-147">DevTools le met en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="f86c5-147">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-148">Figure8</span><span class="sxs-lookup"><span data-stu-id="f86c5-148">Figure 8</span></span>  
    > <span data-ttu-id="f86c5-149">Sélection d’une ressource</span><span class="sxs-lookup"><span data-stu-id="f86c5-149">Selecting a resource</span></span>  
    > ![Sélection d’une ressource][ImageCacheSelected2]  

1.  <span data-ttu-id="f86c5-151">Sélectionnez **supprimer** la ![ suppression sélectionnée ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="f86c5-151">Select **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="f86c5-152">Supprimer toutes les données du cache</span><span class="sxs-lookup"><span data-stu-id="f86c5-152">Delete all cache data</span></span>   

1.  <span data-ttu-id="f86c5-153">Ouvrez l' **application**  >  **Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="f86c5-153">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="f86c5-154">Vérifiez que la case à cocher **stockage du cache** est activée.</span><span class="sxs-lookup"><span data-stu-id="f86c5-154">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-155">Figure9</span><span class="sxs-lookup"><span data-stu-id="f86c5-155">Figure 9</span></span>  
    > <span data-ttu-id="f86c5-156">Case à cocher **stockage du cache**</span><span class="sxs-lookup"><span data-stu-id="f86c5-156">The **Cache Storage** checkbox</span></span>  
    > ![Case à cocher stockage du cache][ImageCacheCheckbox]  

1.  <span data-ttu-id="f86c5-158">Sélectionnez **effacer les données du site**.</span><span class="sxs-lookup"><span data-stu-id="f86c5-158">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="f86c5-159">Figure10</span><span class="sxs-lookup"><span data-stu-id="f86c5-159">Figure 10</span></span>  
    > <span data-ttu-id="f86c5-160">Bouton **effacer les données du site**</span><span class="sxs-lookup"><span data-stu-id="f86c5-160">The **Clear Site Data** button</span></span>  
    > ![Bouton Effacer les données du site][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Figure 2: caches disponibles"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Figure 3: affichage du contenu d’un cache"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Figure 4: affichage des en-têtes HTTP d’une ressource"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Figure 5: affichage du contenu d’une ressource"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Figure 6: sélectionner une ressource"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Figure 7: filtrage des ressources qui ne correspondent pas au chemin spécifié"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Figure 8: sélectionner une ressource"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Figure 9: case à cocher stockage du cache"  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Figure 10: bouton Effacer les données du site"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Journalisation de l’activité du réseau"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP MDN"  

> [!NOTE]
> <span data-ttu-id="f86c5-176">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f86c5-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f86c5-177">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cache) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="f86c5-177">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="f86c5-179">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f86c5-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  