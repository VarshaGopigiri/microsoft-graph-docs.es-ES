---
title: Actualizar secureScoreControlProfiles
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
ms.openlocfilehash: afbfcd1889c55dd53241ff8d796bb3ab492b2acf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083138"
---
# <a name="update-securescorecontrolprofiles"></a>Actualizar secureScoreControlProfiles

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar una propiedad modificable **secureScoreControlProfiles** dentro de cualquier solución integrada para cambiar varias propiedades, como **assignedTo** o **tenantNote**.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |   SecurityEvents.ReadWrite.All.  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | SecurityEvents.ReadWrite.All. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
PATCH /security/secureScoreControlProfiles/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud

| Nombre       | Descripción|
|:-----------|:-----------|
| Authorization  | {código} del portador. Necesario.|
|Prefer | devolver = representación. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcionar una representación JSON de los valores para los campos relevantes que deben actualizarse. En la siguiente tabla se enumera los campos que se pueden actualizar para un secureScoreControlProfile. Los valores para las propiedades existentes que no se incluyen en el cuerpo de la solicitud no cambiará. Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|assignedTo|String|Nombre de la analista el control se asigna a para la evaluación de errores, la implementación o la corrección.|
|tenantNote|String|Comentarios de los analistas en el control (para la administración de control de clientes).|
|controlStateUpdates| String|Analista controlado por el valor en el control. Los valores posibles son: `ignore`, `thirdParty` y `reviewed`.|


## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.

Si se utiliza el encabezado de solicitud opcional, el método devuelve un `200 OK` código de respuesta y el objeto actualizado [secureScoreControlProfiles](../resources/securescorecontrolprofiles.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "securescorecontrolprofiles_update"
}-->

```http
PATCH https://graph.microsoft.com/beta/security/secureScoreControlProfiles/AdminMFA
Content-type: application/json

{
  "assignedTo": "assignedTo-value",
  "controlStateUpdates": "controlStateUpdates-value",
  "tenantNote": "tenantNote-value"
}
```

### <a name="response"></a>Respuesta

El siguiente es un ejemplo de una respuesta correcta.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.secureScoreControlProfiles"
} -->

```http
HTTP/1.1 204 No Content
```




<!-- {
  "type": "#page.annotation",
  "description": "Update secureScoreControlProfiles",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
