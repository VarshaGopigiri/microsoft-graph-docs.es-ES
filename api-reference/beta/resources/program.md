---
title: tipo de recurso de programa
description: 'En el anuncio de Azure access revisa la característica, un programa es un contenedor, manteniendo los controles de programa. Un inquilino puede tener uno o varios programas.  Cada control vincula una revisión de acceso a un programa, para que sea más fácil buscar relacionado acceso revisa.  '
localization_priority: Normal
ms.openlocfilehash: a342fd159bba3f7e31c55ffab9a64a72353bc7ac
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863906"
---
# <a name="program-resource-type"></a>tipo de recurso de programa

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](accessreviews-root.md) Azure AD, un programa es un contenedor, manteniendo los controles de programa. Un inquilino puede tener uno o varios programas.  Cada control vincula una revisión de acceso a un programa, para que sea más fácil buscar relacionado acceso revisa.  

Cada inquilino que ha en-efectuar Azure AD revisiones de acceso tiene uno de los programas, `Default program`.  Un administrador global puede crear programas adicionales, por ejemplo, para representar las iniciativas de cumplimiento. 


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Creación de programa](../api/program-create.md) |   [programa](program.md)   |   Crear un nuevo programa.|
|[Eliminar programa](../api/program-delete.md) |   Ninguno.   |   Eliminar un programa.|
|[Programas de lista](../api/program-list.md) |  colección de [programa](program.md)|   Obtener una colección de todos los programas.|
|[ProgramControls de lista de un programa](../api/program-listcontrols.md) |      colección de [programControl](programcontrol.md)| Obtener una colección de los controles de un programa.|
|[Programa de actualización](../api/program-update.md) |   [programa](program.md)|  Actualizar un programa.|

## <a name="permissions"></a>Permisos

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | ProgramControl.Read.All, ProgramControl.ReadWrite.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
| `id`                        |`String`                              |  El identificador asignado a la característica del programa.                    |
| `displayName`               |`String`                              |  El nombre del programa.  Necesarios en crear.                  |
| `description`               |`String`                              |  La descripción del programa.           |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
| `controls`                  |[programControl](programcontrol.md) | Controles asociados con el programa. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.program"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string",
 "description": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "program resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
