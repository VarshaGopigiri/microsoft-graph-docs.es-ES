---
title: Obtener grupo
description: Obtiene las propiedades y relaciones de un objeto de grupo.
author: dkershaw10
localization_priority: Priority
ms.prod: groups
ms.openlocfilehash: 99215af564be186edaf57563ae493f363c9cc2fa
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941054"
---
# <a name="get-group"></a>Obtener grupo

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtener las propiedades y relaciones de un objeto de [grupo](../resources/group.md) .

##### <a name="default-properties"></a>Propiedades predeterminadas

Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener o enumerar grupos. Son un subconjunto de todas las propiedades disponibles. 

* classification
* createdDateTime
* descripción
* displayName
* groupTypes
* id
* mail
* mailEnabled
* mailNickname
* membershipRule
* membershipRuleProcessingState
* onPremisesLastSyncDateTime
* onPremisesSecurityIdentifier
* onPremisesSyncEnabled
* preferredLanguage - no se admite; no puede ser un valor para esta propiedad conjunto y devuelve `null` cuando llama.
* proxyAddresses
* renewedDateTime
* securityEnabled
* tema
* visibility

De forma predeterminada, no se devuelven las siguientes propiedades de grupo:

* accessType
* allowExternalSenders
* autoSubscribeNewMembers
* hasMembersWithLicenseErrors
* isSubscribedByMail
* isFavorite
* unseenConversationsCount
* unseenCount
* unseenMessagesCount

Para obtener estas propiedades (excepto **isFavorite** y **hasMembersWithLicenseErrors**), utilice la `$select` parámetro de consulta. Estos son algunos ejemplos: 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=allowExternalSenders,autoSubscribeNewMembers,isSubscribedByMail,unseenCount

GET https://graph.microsoft.com/beta/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=description,allowExternalSenders
```

Para devolver los grupos que contienen a miembros con errores de licencia, use el parámetro de consulta **$filter** :

<!-- { "blockType": "ignored" } -->
```http
GET GET https://graph.microsoft.com/beta/groups?$filter=hasMembersWithLicenseErrors+eq+true
```

Puesto que el recurso de **grupo** admite [extensiones](/graph/extensibility-overview), también se puede usar el `GET` operación para obtener las propiedades personalizadas y los datos de extensión en una instancia de **grupo** .

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.Read.All, Group.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.Read.All, Group.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 
>**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad. Se devolverán todas las propiedades predeterminadas de una llamada real, como se describió anteriormente.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
  "id": "id-value",
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value",
  "onPremisesLastSyncDateTime": "onPremisesLastSyncDateTime-value",
  "onPremisesSecurityIdentifier": "onPremisesSecurityIdentifier-value",
  "onPremisesSyncEnabled": true,
  "proxyAddresses": [
    "proxyAddresses-value"
   ],
   "securityEnabled": true,
   "visibility": "visibility-value"
}
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
