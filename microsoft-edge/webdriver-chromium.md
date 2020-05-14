---
description: Découvrez comment tester votre site Web ou votre application dans Microsoft Edge ou automatiser le navigateur à l’aide du Web.
title: Web Driver (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, html, CSS, JavaScript, développeur, Web Driver, sélénium, test, outils, Automation, test
ms.openlocfilehash: 0cb135553b04cd0cf160755eacc0dbae245d13b7
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645314"
---
# Web Driver (chrome)  

L’API du Web [Driver][W3CWebdriver] W3C est une plate-forme et un protocole câblé qui autorisent des programmes ou des scripts à contrôler le comportement d’un navigateur Web, tel que Microsoft Edge \ (chrome \).  

Le WebDriver permet aux développeurs de créer des tests automatisés qui simulent l’interaction de l’utilisateur.  Les tests et simulations du service WebPart diffèrent des tests unitaires JavaScript, car le service d’application Web a accès aux fonctionnalités et informations affichées par JavaScript en cours d’exécution dans le navigateur et ne peut pas simuler plus précisément des événements utilisateur ou des événements au niveau du système d’exploitation.  Le WebDriver est en mesure de gérer les tests sur plusieurs fenêtres, les onglets et les pages Web au sein d’une seule et même session de test.  

Voici comment prendre en main le WebDriver pour Microsoft Edge \ (chrome \).  

## Installer Microsoft Edge (chrome)  

Si ce n’est déjà fait, [Installez Microsoft Edge (chrome)][MicrosoftEdge].  Si vous utilisez une version préinstallée de Microsoft Edge sur votre ordinateur, vérifiez que vous utilisez Microsoft Edge \ (chrome \) et non Microsoft Edge \ (EdgeHTML \).  Une méthode rapide pour vérifier est de charger `edge://settings/help` dans le navigateur et de vérifier que le numéro de version est V75 ou version ultérieure.  

## Télécharger le pilote Microsoft Edge  

Le WebDriver nécessite un pilote spécifique au navigateur pour automatiser chaque navigateur.  Pour Microsoft Edge \ (chrome \), le WebDriver nécessite le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] approprié pour la build de Microsoft Edge que vous voulez tester ou automatiser.  

Pour trouver le numéro de build que vous utilisez, procédez comme suit.  

1.  Lancer Microsoft Edge 
1.  Affichez la version de Microsoft Edge.  
    *   Accédez à `edge://settings/help`  
    *   Sélectionner des `...`  >  **paramètres**  >   **à propos de Microsoft Edge**  
1.  Assurez-vous que la version correcte du WebDriver est valide pour votre Build, afin qu’elle s’exécute correctement.  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020":::
   Figure1.  Numéro de build de l’Canaries Microsoft Edge le 14 janvier 2020  
:::image-end:::

<!--  
> ##### Figure 1  
> The build number for Microsoft Edge Canary on January 14, 2020
> ![The build number for Microsoft Edge Canary on January 14, 2020][ImageWebdriverChromiumEdgeVersion]  
-->  

À présent, [Téléchargez la version correspondante du pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Section téléchargements de la page du pilote Microsoft Edge":::
   Figure2.  Section téléchargements de la page du [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads]  
:::image-end:::

<!--  
> ##### Figure 2
> The Downloads section of the [Microsoft Edge Driver page][MicrosoftDeveloperEdgeToolsWebdriverDownloads]
> ![The Downloads section of the Microsoft Edge Driver page][ImageWebdriverChromiumEdgeDriverInstall]  
-->  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) ne fonctionne pas avec le [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].  Pour automatiser Microsoft Edge \ (EdgeHTML), vous devez télécharger [Microsoft WebDriver pour Microsoft Edge \ (EdgeHTML \)][Webdriver].  

## Choisir une liaison de langue du WebDriver  

Le dernier composant que vous devez télécharger est un pilote client spécifique à la langue.  La liaison de langage traduit le code que vous écrivez dans Python, Java, C \ #, Rubi et JavaScript dans les commandes que le pilote Microsoft Edge que vous avez téléchargées dans la [section précédente](#download-microsoft-edge-driver) est capable de s’exécuter dans Microsoft Edge \ (chrome \).  

[Téléchargez la liaison de langue de votre choix][SeleniumDownloads].  L’équipe Microsoft Edge recommande fortement le [sélénium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] ou version ultérieure, car il offre une prise en charge intégrée de Microsoft Edge \ (chrome \).  Toutefois, vous pouvez piloter Microsoft Edge \ (chrome \) dans toutes les versions plus anciennes de sélénium, y compris la version actuelle du sélénium 3D.  

> [!IMPORTANT]
> Si vous avez précédemment automatisé ou testé Microsoft Edge \ (chrome \) en utilisant `ChromeDriver` et `ChromeOptions` , le code de votre lecteur Web ne fonctionne pas correctement avec Microsoft Edge V80 ou une version ultérieure.  Il s’agit d’un changement majeur et Microsoft Edge \ (chrome \) n’accepte plus ces commandes.  Vous devez modifier vos tests pour utiliser le `EdgeOptions` pilote de classe et [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].  

### Utilisation de sélénium 3  

[Sélénium 3][|::ref1::|] est la dernière version stable du sélénium.  Par défaut, le sélénium 3 pilote l’ancien Microsoft Edge \ (EdgeHTML \) et ne dispose pas de la prise en charge intégrée pour Microsoft Edge \ (chrome \).  Pour utiliser le sélénium 3 avec Microsoft Edge \ (chrome \), installez les [outils de sélénium pour le package Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .  Les outils de sélénium pour Microsoft Edge étendent le sélénium 3 avec un pilote mis à jour pour vous aider à écrire des tests automatisés pour les navigateurs Microsoft Edge \ (EdgeHTML \) et Microsoft Edge \ (chrome \).  

Les outils de sélénium pour Microsoft Edge sont une solution pour les développeurs préférant conserver le niveau d’un test de navigateur pour les développeurs et vouloir ajouter une couverture pour le nouveau navigateur Microsoft Edge \ (chrome \) sans changer les versions de sélénium.  Les `EdgeDriver` `EdgeDriverService` classes et incluses dans les outils sont entièrement compatibles avec les équivalents intégrés en sélénium et exécutent Microsoft Edge \ (EdgeHTML \) par défaut, de sorte que les outils puissent être utilisés en tant que remplacement de lâcher en continu pour les classes Edge existantes en sélénium.  

[Installez les outils de sélénium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] pour commencer à utiliser Microsoft Edge \ (chrome \) avec votre projet sélénium 3.  

## Utiliser Microsoft Edge (chrome) avec WebDriver

Les exemples suivants sont Runnable en utilisant sélénium 3 ou 4.  Pour les utiliser avec le sélénium 3, les [outils de sélénium pour Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] doivent être installés.  

### Utilisation de base  

Pour utiliser avec Microsoft Edge \ (EdgeHTML \), il vous suffit de créer une instance par défaut de la `EdgeDriver` classe.

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code" />  

```csharp
var driver = new EdgeDriver();
```  

#### [Software](#tab/python/)  

<a id="basic-usage-code" />  

```python
driver = Edge()
```  

* * *  

### Pilotage de Microsoft Edge (chrome)  

Pour utiliser la fonction avec Microsoft Edge \ (chrome \) à la place, créez une nouvelle `EdgeDriver` classe et transmettez-lui l' `EdgeOptions` objet avec la `UseChromium` propriété définie sur `true` .  

#### [C#](#tab/c-sharp/)  

<a id="diving-microsoft-edge-chromium-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Software](#tab/python/)  

<a id="diving-microsoft-edge-chromium-code" />  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

* * *  

### Choix de fichiers binaires de navigateur spécifiques (chrome uniquement)  

Utilisez la `EdgeOptions` classe pour sélectionner un fichier binaire spécifique.  Cette fonctionnalité est utile pour tester des [canaux Microsoft Edge Preview][MicrosoftedgeinsiderDownload] tels que Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Software](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

* * *  

### Personnalisation du service de pilote Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

Quand une `EdgeDriver` instance de classe est créée à l’aide d’une `EdgeOptions` classe, elle crée et lance automatiquement la `EdgeDriverService` classe appropriée pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \).  

Si vous souhaitez créer un, créez-en un à l' `EdgeDriverService` aide de la `CreateChromiumService()` méthode.  Il peut s’avérer utile pour des personnalisations supplémentaires telles que l’activation de la sortie détaillée du journal dans le code suivant.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> Vous n’avez pas besoin de fournir l' `EdgeOptions` objet lors du passage de l' `EdgeDriver` instance de classe `EdgeDriverService` .  La `EdgeDriver` classe utilise les options par défaut pour Microsoft Edge \ (EdgeHTML \) ou Microsoft Edge \ (chrome \), en fonction du type de service que vous fournissez.  
> 
> Toutefois, si vous souhaitez fournir des `EdgeDriverService` `EdgeOptions` classes et, vous devez vous assurer que les deux sont configurées pour la même version de Microsoft Edge.  Par exemple, il n’est pas possible d’utiliser une classe Microsoft Edge \ (EdgeHTML \) par défaut `EdgeDriverService` dans la `EdgeOptions` classe.  La `EdgeDriver` classe lève une erreur pour empêcher l’utilisation de différentes versions.  

#### [Software](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

Lorsque vous utilisez Python, l' `Edge` objet crée et gère l’objet `EdgeService` .  Pour configurer le `EdgeService` , passez des arguments supplémentaires à l' `Edge` objet:

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

* * *  

### Utilisation des options spécifiques au chrome  

L’utilisation de la `EdgeOptions` classe avec la `UseChromium` propriété définie pour `true` vous permet d’accéder à toutes les méthodes et propriétés de la classe [ChromeOptions][SeleniumWebDriverChromeoptionsClass] en sélénium.  Par exemple, comme avec d’autres navigateurs de chrome, utilisez la `EdgeOptions.AddArguments()` méthode pour exécuter Microsoft Edge \ (chrome \) en [mode headless][WikiHeadlessBrowser] dans le code suivant.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Software](#tab/python/)  

<a id="using-chromium-specific-options-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

* * *  

> [!NOTE]
> Ces [Propriétés et méthodes propres au chrome][SeleniumWebDriverChromeoptionsClass] sont toujours disponibles, mais n’ont aucun effet si la `UseChromium` propriété n’est pas définie sur `true` .  De la même façon, les propriétés existantes et les méthodes destinées à Microsoft Edge \ (EdgeHTML \) n’ont aucun effet si la `UseChromium` propriété a la valeur `true` .  

<!--  
### [C#](#tab/c-sharp/)  

<a id="selenium-usage" />  

#### Basic Usage  

To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.

```csharp
var driver = new EdgeDriver();
```  

#### Driving Microsoft Edge (Chromium)  

To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### Choosing Specific Browser Binaries (Chromium-Only)  

Use the `EdgeOptions` class to choose a specific binary.  It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### Customizing the Edge Driver Service  

When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).  

If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.  You may find it useful for additional customizations like enabling verbose log output in the following code.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.  The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.  
> 
> However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.  For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.  The `EdgeDriver` class throws an error to prevent using different versions.  

#### Using Chromium-Specific Options  

Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.  For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

> [!NOTE]
> These [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.  Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.  

### [Python](#tab/python/)  

<a id="selenium-usage" />  

#### Basic Usage  

To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.

```python
driver = Edge()
```  

#### Driving Microsoft Edge (Chromium)  

To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### Choosing Specific Browser Binaries (Chromium-Only)  

Use the `EdgeOptions` class to choose a specific binary.  It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### Customizing the Edge Driver Service  

When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).  

If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.  You may find it useful for additional customizations like enabling verbose log output in the following code.  

When using Python, the `Edge` object creates and manages the `EdgeService`.  To configure the `EdgeService`, pass additional arguments to the `Edge` object:

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### Using Chromium-Specific Options  

Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.  For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

> [!NOTE]
> These [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.  Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.  

* * *  

-->  

<!--  
### Basic Usage  

To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.

#### C\#  

```csharp
var driver = new EdgeDriver();
```  

#### Python  

```python
driver = Edge()
```  

### Driving Microsoft Edge (Chromium)  

To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.  

#### C\#  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### Python  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

### Choosing Specific Browser Binaries (Chromium-Only)  

Use the `EdgeOptions` class to choose a specific binary.  It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.  

#### C\#  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### Python  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

### Customizing the Edge Driver Service  

#### C\#  

When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).  

If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.  You may find it useful for additional customizations like enabling verbose log output in the following code.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.  The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.  
> 
> However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.  For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.  The `EdgeDriver` class throws an error to prevent using different versions.  

#### Python  

When using Python, the `Edge` object creates and manages the `EdgeService`.  To configure the `EdgeService`, pass additional arguments to the `Edge` object:

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

### Using Chromium-Specific Options  

Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.  For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.  

#### C\#  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### Python  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

> [!NOTE]
> These [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.  Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.  
-->  

## Autres méthodes de configuration de WebDriver  

### Chocolat  

Si vous utilisez le programme [chocolaté][Chocolatey] en tant que gestionnaire de package, installez le pilote Microsoft Edge en exécutant la commande suivante.  

```console
choco install selenium-chromium-edge-driver
```  

Pour plus d’informations, voir [pilote de contour de chrome de sélénium au chocolat][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Si vous utilisez la version d' [arrimateur][DockerHub], téléchargez une image préconfigurée avec Microsoft Edge \ (chrome \) et [pilote Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] déjà installé en exécutant la commande suivante.  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Pour plus d’informations, consultez [conteneur sur le hub de l’ancrage][DockerHubMsedgedriver].  

## Contacter l’équipe Microsoft Edge DevTools    

L’équipe Microsoft Edge a hâte d’entendre vos commentaires concernant l’utilisation de WebDriver, de sélénium et de Microsoft Edge.  Vous pouvez utiliser l’icône de **Commentaires** dans le Microsoft Edge devtools ou le tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] pour indiquer à l’équipe ce que vous en pensez.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools":::
   Icône de **Commentaires** dans le Microsoft Edge devtools  
:::image-end:::

<!--  
> ##### Figure 3  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The example.png file produced by example.js][ImageDevtoolsGuideChromiumMediaDevtoolsFeedback])  
-->  

<!-- image links -->  

<!--[ImageWebdriverChromiumEdgeVersion]: ./media/webdriver-chromium/edge-version.png "Figure 1: The build number for Microsoft Edge Canary on January 14, 2020"  -->  
<!--[ImageWebdriverChromiumEdgeDriverInstall]: ./media/webdriver-chromium/edge-driver-install.png "Figure 2: The Downloads section of the Microsoft Edge Driver page"  -->
<!--[ImageDevtoolsGuideChromiumMediaDevtoolsFeedback]: ./devtools-guide-chromium/media/devtools-feedback.png "Figure 3: The example.png file produced by example.js"  -->  

<!-- links -->  

[Webdriver]: ./webdriver.md "Web Driver (EdgeHTML) | Documents Microsoft"  

[Chocolatey]: https://chocolatey.org "Chocolat Programme en chocolat"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Pilote du périphérique de chrome de sélénium Chocolat"  

[DockerHub]: https://hub.docker.com "Hub de l’ancrage"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Hub de l’ancrage"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-sélénium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/sélénium | GitHub"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Web Driver | Développeur Microsoft"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Téléchargements-WebDriver | Développeur Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galerie NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Sélénium. WebDriver 3.141.0 | Galerie NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Sélénium. WebDriver 4.0.0-alpha05 | Galerie NuGet"  

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Téléchargements | Sélénium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Classe ChromeOptions-WebDriver | Sélénium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publiez un tweet"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"