---
title: utiliza el tipo de recurso
description: Una idea que representa documentos usados por un usuario específico. Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario.
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: 2f8479896f8c06fdc6193cfa8c18a0c3d8293bc7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976062"
---
# <a name="used-resource-type"></a>utiliza el tipo de recurso

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una idea que representa documentos usados por un usuario específico. Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario. Esto incluye documentos en:

- OneDrive para la Empresa
- SharePoint

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Lista usada](../api/insights-list-used.md) |colección de [insights_used](insights-used.md)| Obtener una lista de archivos usados.|

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo                      | Descripción  |
| -------------         |---------------            | -------------|
| id                    | String                    | Identificador único de la relación. Solo lectura.        |
| lastUsed              | [usageDetails](insights-usagedetails.md)              | Obtener información acerca de cuándo por última vez el elemento de ve y modifica el usuario. Solo lectura.     |
| resourceVisualization | [resourceVisualization](insights-resourcevisualization.md)                | Propiedades que puede usar para visualizar el documento en su experiencia. Solo lectura      |
| resourceReference     | [resourceReference](insights-resourcereference.md)                      | Propiedades de la referencia del documento usado, por ejemplo, la dirección url y el tipo de documento. Solo lectura     |

## <a name="relationships"></a>Relaciones

| Propiedad      | Tipo          | Descripción  |
| ------------- |---------------| -------------|
| resource      | Entidad        | Se usa para navegar hasta el elemento que se usó. Los datos adjuntos de archivo, el tipo es *fileAttachment*. Los datos adjuntos vinculados, el tipo es *driveItem*. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

```json
{
  "id": "string",
  "lastUsed": "usageDetails",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```
