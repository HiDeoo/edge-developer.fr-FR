---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8b29e3a4262afc708608de20d81e3463718a50c2
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884224"
---
# 0.9.430-interface ICoreWebView2DevToolsProtocolEventReceiver 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

Un destinataire est créé pour un événement de protocole DevTools particulier et vous permet de vous abonner et de unsubsribe à partir de cet événement.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | S’abonner à un événement DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.

Obtenu à partir de l’objet WebView par le biais de GetDevToolsProtocolEventReceiver.

## Ses

#### add_DevToolsProtocolEventReceived 

S’abonner à un événement DevToolsProtocol.

> [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)par le biais[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) du public HRESULT

La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché. Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement de protocole DevTools sous la forme d’une chaîne JSON.

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### remove_DevToolsProtocolEventReceived 

Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.

> [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)par le biais du mot-clé public HRESULT

