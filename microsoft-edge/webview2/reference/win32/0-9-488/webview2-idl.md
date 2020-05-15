---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 1e1fb60935c1706ab8d9ffb21d06186bfea3f6d0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653258"
---
# <span data-ttu-id="113a3-104">Globales</span><span class="sxs-lookup"><span data-stu-id="113a3-104">Globals</span></span> 

## <span data-ttu-id="113a3-105">Résumé</span><span class="sxs-lookup"><span data-stu-id="113a3-105">Summary</span></span>

 <span data-ttu-id="113a3-106">Ses</span><span class="sxs-lookup"><span data-stu-id="113a3-106">Members</span></span>                        | <span data-ttu-id="113a3-107">Descriptions</span><span class="sxs-lookup"><span data-stu-id="113a3-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="113a3-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="113a3-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="113a3-109">Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="113a3-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="113a3-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="113a3-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="113a3-111">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="113a3-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="113a3-112">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="113a3-112">CreateCoreWebView2EnvironmentWithDetails</span></span>](#createcorewebview2environmentwithdetails) | <span data-ttu-id="113a3-113">Cette API va être supprimée dans la version SDK suivante.</span><span class="sxs-lookup"><span data-stu-id="113a3-113">This API is going to be removed in next SDK release.</span></span>
[<span data-ttu-id="113a3-114">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="113a3-114">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="113a3-115">Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée d’Edge, un répertoire de données utilisateur et/ou des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="113a3-115">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="113a3-116">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="113a3-116">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="113a3-117">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="113a3-117">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="113a3-118">Ses</span><span class="sxs-lookup"><span data-stu-id="113a3-118">Members</span></span>

#### <span data-ttu-id="113a3-119">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="113a3-119">CompareBrowserVersions</span></span> 

> <span data-ttu-id="113a3-120">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span><span class="sxs-lookup"><span data-stu-id="113a3-120">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="113a3-121">Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.</span><span class="sxs-lookup"><span data-stu-id="113a3-121">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="113a3-122">Il peut être utilisé pour déterminer s’il est possible d’utiliser webview2 ou certaines fonctionnalités de la version.</span><span class="sxs-lookup"><span data-stu-id="113a3-122">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="113a3-123">Définit la valeur de result sur-1, 0 ou 1 si la valeur version1 est inférieure ou égale ou supérieure à la valeur version2 respectivement.</span><span class="sxs-lookup"><span data-stu-id="113a3-123">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="113a3-124">Renvoie E_INVALIDARG s’il n’y a pas d’analyse des chaînes de version ou si aucun paramètre d’entrée n’a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="113a3-124">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="113a3-125">Les données d’entrée peuvent utiliser directement le versionInfo obtenu à partir de GetAvailableCoreWebView2BrowserVersionString, les informations de canal seront ignorées.</span><span class="sxs-lookup"><span data-stu-id="113a3-125">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="113a3-126">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="113a3-126">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="113a3-127">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="113a3-127">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="113a3-128">Crée un environnement WebView2 persistant à l’aide de la version latérale installée.</span><span class="sxs-lookup"><span data-stu-id="113a3-128">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="113a3-129">Cela équivaut à appeler CreateCoreWebView2EnvironmentWithOptions avec nullptr pour browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="113a3-129">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="113a3-130">Pour plus d’informations, consultez CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="113a3-130">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="113a3-131">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="113a3-131">CreateCoreWebView2EnvironmentWithDetails</span></span> 

> <span data-ttu-id="113a3-132">public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR USERDATAFOLDER, PCWSTR AdditionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="113a3-132">public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, PCWSTR additionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="113a3-133">Cette API va être supprimée dans la version SDK suivante.</span><span class="sxs-lookup"><span data-stu-id="113a3-133">This API is going to be removed in next SDK release.</span></span>

<span data-ttu-id="113a3-134">Utilisez CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="113a3-134">Please use CreateCoreWebView2EnvironmentWithOptions.</span></span>

#### <span data-ttu-id="113a3-135">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="113a3-135">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="113a3-136">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="113a3-136">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="113a3-137">Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée d’Edge, un répertoire de données utilisateur et/ou des options supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="113a3-137">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="113a3-138">browserExecutableFolder est le chemin d’accès relatif au dossier qui contient le bord incorporé.</span><span class="sxs-lookup"><span data-stu-id="113a3-138">browserExecutableFolder is the relative path to the folder that contains the embedded Edge.</span></span> <span data-ttu-id="113a3-139">Le bord intégré peut être obtenu en copiant la version nommée dossier d’une bordure installée, telle que 73.0.52.0 sous-dossier d’un bord 73.0.52.0 installé.</span><span class="sxs-lookup"><span data-stu-id="113a3-139">The embedded Edge can be obtained by copying the version named folder of an installed Edge, like 73.0.52.0 sub folder of an installed 73.0.52.0 Edge.</span></span> <span data-ttu-id="113a3-140">Le dossier doit comporter msedge. exe, msedge. dll, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="113a3-140">The folder should have msedge.exe, msedge.dll, and so on.</span></span> <span data-ttu-id="113a3-141">Utilisez la valeur null ou une chaîne vide pour browserExecutableFolder pour créer un WebView à l’aide de Edge installé sur l’ordinateur, auquel cas l’API tente de rechercher une version compatible de Edge installée sur l’ordinateur en fonction de la préférence de canal qui tente de rechercher la première installation par utilisateur, puis par installation par machine.</span><span class="sxs-lookup"><span data-stu-id="113a3-141">Use null or empty string for browserExecutableFolder to create WebView using Edge installed on the machine, in which case the API will try to find a compatible version of Edge installed on the machine according to the channel preference trying to find first per user install and then per machine install.</span></span>

<span data-ttu-id="113a3-142">L’ordre de recherche de canal par défaut est stable, bêta, dev et Canaries.</span><span class="sxs-lookup"><span data-stu-id="113a3-142">The default channel search order is stable, beta, dev, and canary.</span></span> <span data-ttu-id="113a3-143">S’il existe une substitution WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable d’environnement ou une valeur de Registre releaseChannelPreference applicable ayant la valeur 1, l’ordre de recherche de canal est inversé.</span><span class="sxs-lookup"><span data-stu-id="113a3-143">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="113a3-144">userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2.</span><span class="sxs-lookup"><span data-stu-id="113a3-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="113a3-145">Il peut s’agir d’un chemin d’accès absolu ou d’un chemin de fichier relatif qui est interprété comme relatif au fichier exécutable du processus actuel.</span><span class="sxs-lookup"><span data-stu-id="113a3-145">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="113a3-146">Dans le cas contraire, pour les applications UWP, le dossier de données utilisateur par défaut sera le dossier Data App pour le package. dans le cas des applications non UWP, le dossier de données utilisateur par défaut `{Executable File Name}.WebView2` sera créé dans le même répertoire en regard du fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="113a3-146">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="113a3-147">La création de WebView2 peut échouer si le fichier exécutable s’exécute dans un répertoire dans lequel le processus n’est pas autorisé à créer un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="113a3-147">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="113a3-148">Lorsque l’application est exécutée, l’application est chargée de nettoyer son dossier de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="113a3-148">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="113a3-149">Notez que, dans la mesure où le processus de navigateur peut être partagé entre les WebViews, la création de WebView échoue avec HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) si les options spécifiées ne correspondent pas aux options des webvues actuellement en cours d’exécution dans le processus de navigateur partagé.</span><span class="sxs-lookup"><span data-stu-id="113a3-149">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="113a3-150">environment_created_handler est le résultat du gestionnaire à l’opération asynchrone qui contient le WebView2Environment qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="113a3-150">environment_created_handler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="113a3-151">Le browserExecutableFolder, userDataFolder et additionalBrowserArguments du environmentOptions peut être substitué par les valeurs spécifiées dans les variables d’environnement ou dans le registre.</span><span class="sxs-lookup"><span data-stu-id="113a3-151">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="113a3-152">Lors de la création d’un WebView2Environment, les variables d’environnement suivantes sont activées:</span><span class="sxs-lookup"><span data-stu-id="113a3-152">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="113a3-153">S’il existe une variable d’environnement de substitution, nous utilisons les valeurs browserExecutableFolder, userDataFolder et additionalBrowserArguments en tant que remplacement des valeurs correspondantes dans les paramètres CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="113a3-153">If an override environment variable is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="113a3-154">Bien qu’il ne soit pas nécessaire de remplacer strictement, il existe d’autres variables d’environnement qui peuvent être définies:</span><span class="sxs-lookup"><span data-stu-id="113a3-154">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="113a3-155">Dans le cas d’une valeur non vide, cela indique que le WebView est démarré sous un débogueur de script.</span><span class="sxs-lookup"><span data-stu-id="113a3-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="113a3-156">Dans ce cas, le WebView lancera une `Page.waitForDebugger` commande CDP qui entraînera l’exécution du script à l’intérieur du WebView sur le lancement, jusqu’à ce qu’un débogueur publie une `Runtime.runIfWaitingForDebugger` commande CDP correspondante pour reprendre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="113a3-156">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="113a3-157">Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="113a3-157">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="113a3-158">Dans le cas d’une valeur non vide, cela signifie que l’application WebView est lancée sous un débogueur de script qui prend également en charge les applications hébergées sur plusieurs vues Web.</span><span class="sxs-lookup"><span data-stu-id="113a3-158">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="113a3-159">La valeur est utilisée comme identificateur pour un canal nommé qui sera ouvert et écrit lors de la création d’un nouveau WebView par l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="113a3-159">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="113a3-160">La charge utile correspond à celle de la cible JSON du débogage à distance et peut être utilisée par le débogueur externe pour être attachée à une instance WebView spécifique.</span><span class="sxs-lookup"><span data-stu-id="113a3-160">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="113a3-161">Le format du canal créé par le débogueur doit être `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` le suivant:</span><span class="sxs-lookup"><span data-stu-id="113a3-161">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="113a3-162">est le nom de fichier exe de l’application hôte (par exemple, WebView2Example. exe)</span><span class="sxs-lookup"><span data-stu-id="113a3-162">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="113a3-163">est la valeur définie pour WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="113a3-163">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="113a3-164">Pour activer le débogage des cibles identifiées par le JSON, vous devez également définir la variable d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS à envoyer `--remote-debugging-port={port_num}` :</span><span class="sxs-lookup"><span data-stu-id="113a3-164">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="113a3-165">correspond au port sur lequel est lié le serveur CDP.</span><span class="sxs-lookup"><span data-stu-id="113a3-165">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="113a3-166">N’ayez pas à faire en sorte que la définition des variables d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS et WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER entraîne l’affichage des webvues hébergées dans votre application et de leur contenu aux applications tierces, telles que les débogueurs.</span><span class="sxs-lookup"><span data-stu-id="113a3-166">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="113a3-167">Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="113a3-167">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="113a3-168">S’il n’existe aucune de ces variables d’environnement, le Registre est examiné suivant.</span><span class="sxs-lookup"><span data-stu-id="113a3-168">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="113a3-169">Les clés de Registre suivantes sont activées:</span><span class="sxs-lookup"><span data-stu-id="113a3-169">The following registry keys are checked:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="113a3-170">Dans le cas improbable où certaines instances de WebView sont ouvertes lors d’une mise à jour de navigateur, nous pouvons dès lors bloquer la suppression de anciens navigateurs de bord.</span><span class="sxs-lookup"><span data-stu-id="113a3-170">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="113a3-171">Pour éviter de manquer d’espace disque, une nouvelle création d’affichage WebView échoue avec l’erreur suivante s’il détecte qu’il existe de nombreuses versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="113a3-171">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="113a3-172">Le nombre maximal de versions Edge autorisées par défaut est 20.</span><span class="sxs-lookup"><span data-stu-id="113a3-172">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="113a3-173">Il est possible d’écraser le nombre maximal de versions latérales antérieures autorisées avec la valeur de la variable d’environnement suivante.</span><span class="sxs-lookup"><span data-stu-id="113a3-173">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="113a3-174">Si WebView dépend d’une périphérie installée et qu’elle est désinstallée, tout création ultérieure échoue avec l’erreur suivante</span><span class="sxs-lookup"><span data-stu-id="113a3-174">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="113a3-175">Tout d’abord, nous allons vérifier avec root, puis HKCU.</span><span class="sxs-lookup"><span data-stu-id="113a3-175">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="113a3-176">AppId est d’abord défini sur l’ID de modèle utilisateur de l’application du processus de l’appelant, s’il n’y a pas de clé de Registre correspondante, l’AppId est défini sur le nom exécutable du processus de l’appelant, ou si ce n’est pas une clé de Registre, ' \* '.</span><span class="sxs-lookup"><span data-stu-id="113a3-176">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="113a3-177">S’il existe une clé de registre de remplacement, nous utilisons les valeurs de Registre browserExecutableFolder, userDataFolder et additionalBrowserArguments en tant que remplacement des valeurs correspondantes dans les paramètres CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="113a3-177">If an override registry key is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments registry values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="113a3-178">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="113a3-178">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="113a3-179">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr \* VERSIONINFO)</span><span class="sxs-lookup"><span data-stu-id="113a3-179">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="113a3-180">Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.</span><span class="sxs-lookup"><span data-stu-id="113a3-180">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="113a3-181">Les noms de canaux sont Beta, dev et Canaries.</span><span class="sxs-lookup"><span data-stu-id="113a3-181">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="113a3-182">S’il existe un remplacement pour le browserExecutableFolder ou l’option de canal, la substitution est utilisée.</span><span class="sxs-lookup"><span data-stu-id="113a3-182">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="113a3-183">S’il n’y a pas de remplacement, le paramètre transmis à GetAvailableCoreWebView2BrowserVersionString est utilisé.</span><span class="sxs-lookup"><span data-stu-id="113a3-183">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>
