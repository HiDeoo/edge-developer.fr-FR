---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 640926481e99c6571c0cbf9c345efa56d97e3f66
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885596"
---
# 0.9.430-interface ICoreWebView2HttpHeadersCollectionIterator 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Itérateur pour une collection d’en-têtes HTTP.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.
[get_HasCurrentHeader](#get_hascurrentheader) | True lorsque l’itérateur n’a plus d’en-têtes.
[MoveNext](#movenext) | Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

Voir [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) et [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md). 

```cpp
std::wstring RequestHeadersToJsonString(ICoreWebView2HttpRequestHeaders* requestHeaders)
{
    wil::com_ptr<ICoreWebView2HttpHeadersCollectionIterator> iterator;
    CHECK_FAILURE(requestHeaders->GetIterator(&iterator));
    BOOL hasCurrent = FALSE;
    std::wstring result = L"[";

    while (SUCCEEDED(iterator->get_HasCurrentHeader(&hasCurrent)) && hasCurrent)
    {
        wil::unique_cotaskmem_string name;
        wil::unique_cotaskmem_string value;

        CHECK_FAILURE(iterator->GetCurrentHeader(&name, &value));
        result += L"{\"name\": " + EncodeQuote(name.get())
            + L", \"value\": " + EncodeQuote(value.get()) + L"}";

        BOOL hasNext = FALSE;
        CHECK_FAILURE(iterator->MoveNext(&hasNext));
        if (hasNext)
        {
            result += L", ";
        }
    }

    return result + L"]";
}
```

## Ses

#### GetCurrentHeader 

Obtenez le nom et la valeur de l’en-tête HTTP actuel de l’itérateur.

> public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * Name, LPWStr * value)

Cette méthode échoue si le dernier appel à MoveNext définit has_next sur FALSe.

#### get_HasCurrentHeader 

True lorsque l’itérateur n’a plus d’en-têtes.

> valeur publique HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool * hasCurrent)

Si la collection sur laquelle l’itérateur est une itération est vide ou si l’itérateur a dépassé la fin de la collection, il s’agit de la valeur false.

#### MoveNext 

Déplacer l’itérateur vers l’en-tête HTTP suivant dans la collection.

> public HRESULT [MoveNext](#movenext)(bool * hasNext)

Le paramètre hasNext est défini sur FALSe s’il n’y a plus d’en-têtes HTTP. Après cela, la méthode GetCurrentHeader échoue si elle est appelée.

