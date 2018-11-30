---
title: Crear directiva
description: Crear un nuevo objeto de directiva mediante la especificación de nombre para mostrar, el tipo de directiva y la descripción de la directiva.
ms.openlocfilehash: fca6201d7afa6a78f15da0d37fb611e4114783e4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090281"
---
# <a name="create-policy"></a>Crear directiva

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear un nuevo objeto de [Directiva](../resources/policy.md) mediante la especificación de nombre para mostrar, el tipo de directiva y la descripción de la directiva.

>Nota: Los detalles de la directiva se validará antes de que se almacenan. Si no pasa la validación, un 400 Solicitud incorrecta se devolverá.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

```http
POST /policies
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type | application/json  | Naturaleza de los datos en el cuerpo de una entidad. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionan una representación JSON de objeto de [Directiva](../resources/policy.md) .

En la siguiente tabla se muestra las propiedades que son necesarias para crear una directiva.

| Parámetro    | Tipo   |Descripción|
|:---------------|:--------|:----------|
|definición|String|La versión de cadena del objeto de [Directiva](../resources/policy.md) .|
|displayName|String|Un nombre personalizado para la directiva.|
|type|String|Especifica el tipo de directiva. Actualmente, debe ser "TokenLifetimePolicy"|

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve `201 Created` objeto de código y la [Directiva](../resources/policy.md) de respuesta en el cuerpo de la respuesta. Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.  

## <a name="example"></a>Ejemplo
En el ejemplo siguiente se crea una nueva duración del token directiva. Tenga en cuenta que el parámetro de cadena de definición se con caracteres de escape comillas dobles.

##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

```http
POST https://graph.microsoft.com/beta/policies
Content-Type: application/json

{
  "displayName":"CustomTokenLifetimePolicy",
  "definition":["{\"TokenLifetimePolicy\":{\"Version\":1,\"AccessTokenLifetime\":\"8:00:00\"}}"],
  "type":"TokenLifetimePolicy"
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#policies/$entity",
  "id":"id-value",
  "alternativeIdentifier":null,
  "definition":["{\"TokenLifetimePolicy\":{\"Version\":1,\"AccessTokenLifetime\":\"8:00:00\"}}"],
  "displayName":"name-value",
  "isOrganizationDefault":false,
  "keyCredentials",
  "type":"TokenLifetimePolicy"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createReply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
