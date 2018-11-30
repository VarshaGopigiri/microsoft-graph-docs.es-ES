---
title: utiliza el tipo de recurso
description: 'Una idea que representa documentos usados por un usuario específico. Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario. Esto incluye documentos en:'
ms.openlocfilehash: 3c82d268a67ef52d0ddfdad9193558080048ad6b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088995"
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