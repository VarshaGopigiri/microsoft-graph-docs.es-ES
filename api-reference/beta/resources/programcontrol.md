---
title: tipo de recurso programControl
description: En el anuncio de Azure access revisa la característica, el objeto de control de programa representa un control, vincular una revisión de acceso a un programa.
ms.openlocfilehash: 03e70ffdf0607eeb11abaf1b12065b4092294d23
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086150"
---
# <a name="programcontrol-resource-type"></a>tipo de recurso programControl

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el objeto de control de programa representa un control, vincular una revisión de acceso a un programa.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear programControl](../api/programcontrol-create.md) |     [programControl](programcontrol.md) |   Agregar un programControl a un programa.|
|[Eliminar programControl](../api/programcontrol-delete.md) |     Ninguna.   |   Quitar un programControl de un programa.|
|[Lista programControls](../api/programcontrol-list.md) | colección de [programControl](programcontrol.md)| Controles de lista a través de todos los programas en el inquilino.|

## <a name="permissions"></a>Permissions

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | ProgramControl.Read.All, ProgramControl.ReadWrite.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| `id`                     |`String`                | El identificador asignado a la característica del vínculo entre el programa y control                                      |
| `programId`              |`String`                | El programId del programa de este control es una parte de. Necesarios en crear.                            |
| `controlId`              |`String`                | ControlId del control, en particular, el identificador de una revisión de access. Necesarios en crear.                                                |
| `controlTypeId`          |`String`                | El programControlType identifica el tipo de control de programa: por ejemplo, se revisa un control de vinculación para acceso de invitado. Necesarios en crear. |
| `displayName`            |`String`                | El nombre del control.                                                             |
| `status`                 |`String`                | El estado de ciclo de vida del control.                                                 |
| `createdDateTime`        |`DateTimeOffset`        | La fecha de creación y la hora del control del programa.                                        |
| `owner`                  |[IdentidadDeUsuario](useridentity.md)   | El usuario que creó el control del programa.                                               |
| `resource`               |`programResource`       | El recurso, un grupo o una aplicación, el objetivo de la revisión de acceso del control de este programa.                   |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
| `program`                |[programa](program.md)               | El programa de. que este control forma parte.                                                |

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[ProgramControls de lista de un programa](../api/program-listcontrols.md) |      colección de [programControl](programcontrol.md)| Obtener una colección de los controles de un programa.|
|[Lista programControlTypes](../api/programcontroltype-list.md) | colección de [programControlType](programcontroltype.md)| Lista de tipos de control de programa. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.programControl"
}-->

```json
{
 "id": "string (identifier)",
 "programId": "string (identifier)",
 "controlId": "string (identifier)",
 "controlTypeId": "string (identifier)",
 "displayName": "string",
 "status": "string",
 "createdDateTime": "string (timestamp)",
 "owner": "microsoft.graph.userIdentity",
 "resource":"microsoft.graph.programResource"
}

```

## <a name="the-programresource-complex-type"></a>El tipo complejo programResource

El recurso de programa, dentro de un objeto de control de programa, es una representación de una referencia a un objeto que es el destino de la revisión de access.

Este tipo se hereda de `microsoft.graph.identity` y tiene una propiedad adicional:

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| `type`               |`String`  | Tipo del recurso, que indica si es un grupo o una aplicación. |     


<!-- {
  "type": "#page.annotation",
  "description": "programControl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->