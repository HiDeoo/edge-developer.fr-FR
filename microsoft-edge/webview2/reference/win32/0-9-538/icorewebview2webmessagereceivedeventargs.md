---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 58bb4b7f34b2917ec16ead051d1df8d6e6885f6d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010382"
---
# 0.9.579-interface ICoreWebView2WebMessageReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement WebMessageReceived.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Source](#get_source) | URI du document qui a envoyé ce message Web.
[get_WebMessageAsJson](#get_webmessageasjson) | Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.

## Ses

#### get_Source 

URI du document qui a envoyé ce message Web.

> valeur publique HRESULT [get_Source](#get_source)(LPWSTR * source)

#### get_WebMessageAsJson 

Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.

> valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR * WebMessageAsJson)

Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.

Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.

> public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR * webMessageAsString)

Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG. Utilisez cette fonction pour communiquer via des chaînes simples.

Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

