---
title: Directiva de actualización
description: Actualizar las propiedades de una directiva existente.
localization_priority: Normal
ms.openlocfilehash: 2992f2f76c0e8b213ad8aabca1bfd0fe59883989
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857158"
---
# <a name="update-policy"></a>Directiva de actualización

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades de una [Directiva](../resources/policy.md)de ya existente.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Directory.AccessAsUser.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

```http
PATCH /policies/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Autorización  | string  | {token} de portador. Obligatorio. |
| Content-Type | application/json  | Naturaleza de los datos en el cuerpo de una entidad. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los parámetros que necesitan actualizarse. La siguiente tabla muestran los posibles parámetros.

| Parámetro    | Tipo   |Description|
|:---------------|:--------|:----------|
|definición|Cadena|La versión stringified del objeto de [Directiva](../resources/policy.md) .|
|displayName|Cadena|Un nombre personalizado para la directiva.|
|isOrganizationDefault|Booleano|Especifica si se aplica esta directiva de forma predeterminada.|
|type|Cadena|Especifica el tipo de directiva. Actualmente, debe ser "TokenLifetimePolicy"|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. Si no lo consigue, un `4xx` se devolverá el error con detalles específicos.

## <a name="example"></a>Ejemplo
En el ejemplo siguiente se actualiza la definición de la directiva de duración del token y se establece como el valor predeterminado de la organización.

##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

```http
PATCH https://graph.microsoft.com/beta/policies/{id}
Content-Type: application/json
{
    "definition":["{\"TokenLifetimePolicy\":{\"Version\":1,\"AccessTokenLifetime\":\"8:00:00\",\"MaxInactiveTime\":\"20:00:00\",}}"],
    "isOrganizationDefault":true
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.

```http
HTTP/1.1 204 No Content
```
