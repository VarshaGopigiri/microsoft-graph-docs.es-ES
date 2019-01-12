---
title: Delete subscription
description: Elimina una suscripción.
localization_priority: Normal
author: piotrci
ms.openlocfilehash: 79ffce638036414469953d6d729229e00cb1662f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945877"
---
# <a name="delete-subscription"></a>Eliminar suscripción

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Elimina una suscripción.

## <a name="permissions"></a>Permisos

En la tabla siguiente se muestra el permiso propuesto que se requiere para cada recurso. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de recurso o elemento        | Permiso          |
|-----------------------------|---------------------|
| Contactos                    | Contacts.Read       |
| Conversaciones               | Group.Read.All      |
| Eventos                      | Calendars.Read      |
| Mensajes                    | Mail.Read           |
| Grupos                      | Group.Read.All      |
| Usuarios                       | User.Read.All       |
| Unidad de disco (OneDrive del usuario)    | Files.ReadWrite     |
| Unidades (contenido de SharePoint compartido y unidades) | Files.ReadWrite.All |
| Alerta de seguridad              | SecurityEvents.ReadWrite.All |

***Nota:*** El extremo de /beta permite que los permisos de aplicación para la mayoría de los recursos. Las conversaciones de un grupo y OneDrive para la unidad raíz los elementos no son compatibles con los permisos de la aplicación.

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
DELETE /subscriptions/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "delete_subscription"
}-->

```http
DELETE https://graph.microsoft.com/beta/subscriptions/{id}
```

##### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.subscription"
} -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Delete subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
