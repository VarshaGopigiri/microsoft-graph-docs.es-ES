---
title: 'usuario: translateExchangeIds'
description: Traducir identificadores de recursos relacionados con Outlook entre formatos.
ms.openlocfilehash: e18c59df5a7ecbaa16b954bf74221c8d8d1de5d3
ms.sourcegitcommit: 4aebfaefc23e02a98b2fec35958cd2110020f15f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/06/2018
ms.locfileid: "27184493"
---
# <a name="user-translateexchangeids"></a>usuario: translateExchangeIds

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Traducir identificadores de recursos relacionados con Outlook entre formatos.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Tipo de permiso | Permisos (de menos a más privilegiados) |
|:----------------|:--------------------------------------------|
| Delegado (cuenta profesional o educativa) | User.ReadBasic, User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All |
| Delegado (cuenta personal de Microsoft) | User.ReadBasic, User.Read, User.ReadWrite |
| Aplicación | User.Read.All, User.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /me/translateExchangeIds
POST /users/{id|userPrincipalName}/translateExchangeIds
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre | Valor |
|:-----|:------|
| Authorization | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud

| Parámetro | Tipo | Descripción |
|:----------|:-----|:------------|
| inputIds | Colección de Edm.String | Una colección de identificadores para convertir. Todos los identificadores de la colección deben tener el mismo tipo de identificador de origen y deben ser el de los elementos en el mismo buzón. Tamaño máximo de esta colección es 1000 cadenas. |
| sourceIdType | exchangeIdFormat | El tipo de identificador de los identificadores en el `InputIds` parámetro. |
| targetIdType | exchangeIdFormat | El tipo de identificador solicitado para convertir a. |

### <a name="exchangeidformat-values"></a>valores de exchangeIdFormat

| Valores | Descripción |
|:-------|:------------|
| propiedad entryId | El formato de identificador de entrada binario utilizado por los clientes MAPI. |
| ewsId | El formato de identificador utilizado por los clientes de servicios Web de Exchange. |
| immutableEntryId | El formato de identificador inmutable compatible con MAPI. |
| restId | El formato de identificador predeterminado utilizado por Microsoft Graph. |
| restImmutableEntryId | El formato de identificador inmutable utilizado por Microsoft Graph. |

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `200 OK` código de respuesta y una colección de [convertIdResult](../resources/convertidresult.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo convertir varios identificadores desde el formato de la API de REST normal (`restId`) para el formato inmutable REST (`restImmutableEntryId`).

##### <a name="request"></a>Solicitud

Aquí está la solicitud de ejemplo.
<!-- {
  "blockType": "request",
  "name": "user_translateexchangeids"
}-->

```http
POST https://graph.microsoft.com/beta/me/translateExchangeIds
Content-Type: application/json

{
  "inputIds" : [
    "{rest-formatted-id-1}",
    "{rest-formatted-id-2}"
  ],
  "sourceIdType": "restId",
  "targetIdType": "restImmutableEntryId"
}
```

##### <a name="response"></a>Respuesta

Aquí está la respuesta de ejemplo
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.convertIdResult",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/testexchangebeta/$metadata#Collection(microsoft.graph.convertIdResult)",
  "value": [
    {
      "sourceId": "{rest-formatted-id-1},
      "targetId": "{rest-immutable-formatted-id-1}"
    },
    {
      "sourceId": "{rest-formatted-id-2},
      "targetId": "{rest-immutable-formatted-id-2}"
    }
  ]
}
```