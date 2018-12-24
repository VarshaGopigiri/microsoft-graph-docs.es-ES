---
title: Obtener contactos de Outlook en una carpeta compartida
description: Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de lectura, creación, edición o eliminación a las carpetas de contactos individuales. Outlook también permite a un cliente delegar en otro usuario para actuar en nombre del cliente.
author: angelgolfer-ms
ms.openlocfilehash: d0dc5be8df709c3d736ff0baa55667926cfc5936
ms.sourcegitcommit: 8feddb85e436be5581557a199f2e46d5b4ebfa21
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/22/2018
ms.locfileid: "27413158"
---
# <a name="get-outlook-contacts-in-a-shared-folder"></a>Obtener contactos de Outlook en una carpeta compartida

Outlook permite a los clientes compartir carpetas entre ellos y proporcionar acceso de "lectura", "creación", "edición" o "eliminación" a las carpetas de contactos individuales. Outlook también permite a un cliente delegar en otro usuario en nombre del cliente y tener acceso a carpetas de correo específico o a todo buzón del cliente; esto también se denomina "delegación" en Outlook.

Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que han compartido otros usuarios, así como obtener esas carpetas compartidas. El soporte también se aplica a los archivos en un buzón de correo delegado.

Por ejemplo, Juan ha compartido con Miguel una carpeta de contactos personalizada y le ha concedido el acceso de lectura. Si Miguel ha iniciado sesión en la aplicación y ha proporcionado permisos delegados (Contacts.Read.Shared o Contacts.ReadWrite.Shared), la aplicación podrá acceder a la carpeta de contactos personalizada de Juan y a los contactos en dicha carpeta, tal y como se describe a continuación.

> **Nota** Los permisos de uso compartidos (Contacts.Read.Shared o Contacts.ReadWrite.Shared) le permiten leer o escribir contactos en una carpeta compartida o delegada. No admiten la [suscripción a notificaciones de cambios](webhooks.md) en elementos de dichas carpetas. Para configurar las suscripciones de notificación de cambios a los contactos en una carpeta compartida o delegada, o cualquier otra carpeta de contactos de un usuario en el espacio empresarial, use los permisos de aplicación Contacts.Read.

## <a name="get-a-contact-in-the-shared-folder"></a>Obtener un contacto en la carpeta compartida

Puede obtener un contacto específico en la carpeta de contactos personalizada que Juan ha compartido con Miguel:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts/{id}
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [contacto](/graph/api/resources/contact?view=graph-rest-1.0) identificada por `{id}` desde la carpeta de contactos que ha compartido Juan.

## <a name="get-all-contacts-in-the-shared-folder"></a>Obtener todos los contactos en la carpeta compartida

Obtener todos los contactos en la carpeta de contactos que ha compartido Juan:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts
```

Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias [contacto](/graph/api/resources/contact?view=graph-rest-1.0) en la carpeta de contactos que ha compartido Juan.

## <a name="get-the-shared-folder"></a>Obtener la carpeta compartida

Obtener la carpeta que Juan ha compartido con Miguel.

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) que representa la carpeta de contactos que ha compartido Juan.

Las mismas capacidades de "obtener" aplican si Jorge hubiera delegado en Juan todo su buzón.

Si Juan no ha compartido su carpeta de contactos con Miguel ni ha delegado su buzón en él, especificar el identificador de usuario del Juan o el nombre principal de usuario en esas operaciones "obtener" devolverá un error. 


## <a name="next-steps"></a>Pasos siguientes

Obtenga más información sobre:

- [¿Por qué integrar con contactos personales de Outlook?](outlook-contacts-concept-overview.md)
- La [API de contactos](/graph/api/resources/contact?view=graph-rest-1.0) en la versión 1.0 de Microsoft Graph