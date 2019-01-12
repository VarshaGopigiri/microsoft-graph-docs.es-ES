---
title: Actualizar educationassignment
description: Actualizar el objeto de asignación. Sólo los profesores en la clase pueden hacerlo. Tenga en cuenta que no se puede usar una solicitud de revisión para cambiar el estado de una asignación. Utilice la acción de publicación para cambiar el estado de la asignación.
localization_priority: Normal
author: dipakboyed
ms.prod: education
ms.openlocfilehash: f8d79e11628e3a02a20c9ecdcd46bcd1bff05e7f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960353"
---
# <a name="update-educationassignment"></a>Actualizar educationassignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar el objeto de asignación. Sólo los profesores en la clase pueden hacerlo. Tenga en cuenta que no se puede usar una solicitud de revisión para cambiar el estado de una asignación. Use la acción [Publicar](../api/educationassignment-publish.md) para cambiar el estado de asignación.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) |  EduAssignments.ReadWriteBasic, EduAssignments.ReadWrite  |
|Delegado (cuenta personal de Microsoft) |  No admitida.  |
|Aplicación | No admitida. | 

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /education/classes/{id}/assignments/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no incluya valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowLateSubmissions|Booleano| Si se pueden enviar envíos después de la fecha de vencimiento.|
|allowStudentsToAddResourcesToSubmission|Booleano| Si un estudiante puede agregar recursos a una presentación. Indica si los únicos elementos en el envío proceden de la lista de recursos de la asignación. |
|assignDateTime|DateTimeOffset| Fecha de que la asignación debe publicarse a los alumnos. |
|assignTo|educationAssignmentRecipient| Alumnos que obtener la asignación.|
|displayName|Cadena| Nombre de asignación. |
|dueDateTime|DateTimeOffset| Asignación de fecha es de vencimiento. |
|Puntuar|educationAssignmentGradeType| ¿Cómo se corregirán la asignación.|
|instrucciones|itemBody| Instrucciones que se proporcionará a los alumnos junto con la asignación. |

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [educationAssignment](../resources/educationassignment.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_educationassignment"
}-->
```http
PATCH https://graph.microsoft.com/beta/education/classes/11021/assignments/19002
Content-type: application/json
Content-length: 279

{
  "displayName": "Week 1 reading assignment",
  "instructions": {
    "contentType": "Text",
    "content": "Read chapters 1 through 3"
  },
  "dueDateTime": "2014-02-01T00:00:00Z"
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. 

>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Todas las propiedades se devolverán desde una llamada real.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
  "classId": "11021",
  "displayName": "Week 1 reading assignment",
  "instructions": {
    "contentType": "Text",
    "content": "Read chapters 1 through 3"
  },
  "dueDateTime": "2014-02-01T00:00:00Z",
  "assignDateTime": "2014-01-01T00:00:00Z",
  "assignedDateTime": "2014-01-01T00:00:00Z"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update educationassignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
