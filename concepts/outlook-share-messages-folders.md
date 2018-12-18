---
title: Obtener mensajes de Outlook en una carpeta compartida o delegada
description: 'Estos temas también tienen sección similar: lista de eventos, obtener evento, obtener calendario, lista de contactos, obtener contactos, obtener la carpeta de contactos.'
author: angelgolfer-ms
ms.openlocfilehash: d90fa5d37fd7a07e4069bd5bcc0eb46f0cae29a6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320114"
---
# <a name="get-outlook-messages-in-a-shared-or-delegated-folder"></a>Obtener mensajes de Outlook en una carpeta compartida o delegada

<!-- remove similar content in other topics when ready to publish - list messages, get message, get mail folder.
These topics also have similar section - list events, get event, get calendar, list contacts, get contact, get contact folder.
-->

Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de "lectura", "creación", "edición" o "eliminación" a las carpetas individuales. Outlook también permite a un cliente delegar en otro usuario en nombre del cliente y tener acceso a carpetas de correo específico o a todo buzón del cliente; esto también se denomina "delegación" en Outlook.

Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que se han compartido con otros usuarios, así como obtener esas carpetas compartidas. El soporte también se aplica a los calendarios que se han delegado.

Por ejemplo, Jorge ha compartido con Juan y se le ha dado acceso de lectura a la Bandeja de entrada de Jorge. Si Juan ha iniciado sesión en la aplicación y proporciona permisos delegados (Mail.Read.Shared o Mail.ReadWrite.Shared), la aplicación podrá acceder al correo de Jorge y a su Bandeja de entrada tal como se describe a continuación.

## <a name="get-a-message-in-the-shared-folder"></a>Obtener un mensaje en la carpeta compartida

Puede obtener un mensaje específico en la Bandeja de entrada de Jorge:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages/{id}
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [mensaje](/graph/api/resources/message?view=graph-rest-1.0) identificada por `{id}` de la Bandeja de entrada de Jorge.

## <a name="get-all-messages-in-the-shared-folder"></a>Obtener todos los mensajes en la carpeta compartida

Obtenga todos los mensajes en la Bandeja de entrada de Jorge:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages
```

Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias de [mensajes](/graph/api/resources/message?view=graph-rest-1.0) en la Bandeja de entrada de Jorge.

## <a name="get-the-shared-folder"></a>Obtener la carpeta compartida

Obtenga la carpeta (Bandeja de entrada) que compartió Jorge con Juan.

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0) que representa la Bandeja de entrada de Jorge.

Se aplican las mismas capacidades de GET si Jorge había delegado a Juan acceso a la Bandeja de entrada de Jorge o había delegado Juan todo su buzón.

Si Jorge no ha compartido su Bandeja de entrada con John ni ha delegado su buzón a Juan, especificar el identificador de usuario de Jorge o el nombre principal de usuario en esas operaciones GET devolverá un error. 


## <a name="next-steps"></a>Pasos siguientes

Obtenga más información sobre:

- [¿Por qué integrar con el correo de Outlook?](outlook-mail-concept-overview.md)
- [Usar la API de correo](/graph/api/resources/mail-api-overview?view=graph-rest-1.0) y sus [casos de uso](/graph/api/resources/mail-api-overview?view=graph-rest-1.0#common-use-cases) en Microsoft Graph v1.0.