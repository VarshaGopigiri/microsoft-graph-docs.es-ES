---
title: tipo de recurso de tendencias
description: Relación enriquecida conecta un usuario a los documentos que se tendencias alrededor del usuario (son relevante para el usuario). Archivos de OneDrive, y los archivos almacenados en sitios de grupo de SharePoint pueden tendencias alrededor del usuario.
ms.openlocfilehash: 7d240c4358047ca9ba3d6b8340fbfb7d893a6a1d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087163"
---
# <a name="trending-resource-type"></a>tipo de recurso de tendencias

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Relación enriquecida conecta un usuario a los documentos que se tendencias alrededor del usuario (son relevante para el usuario). Archivos de OneDrive, y los archivos almacenados en sitios de grupo de SharePoint pueden tendencias alrededor del usuario.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Tendencias de lista](../api/insights-list-trending.md) |colección de [insights_trending](insights-trending.md)| Obtener una lista de los archivos de tendencias.|

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo                              | Descripción  |
| ------------- |---------------                    | -------------|
| id                    | String                    | Identificador único de la relación. Solo lectura.        |
| weight                | Doble                    | Valor que indica cuánto el documento actualmente es tendencias. Cuanto mayor sea el número, más el documento está actualmente tendencias alrededor del usuario (más relevante es). Los documentos devueltos se ordenan por este valor.  |
| resourceVisualization | [resourceVisualization](insights-resourcevisualization.md)    | Propiedades que puede usar para visualizar el documento en su experiencia. |
| resourceReference     | [resourceReference](insights-resourcereference.md)        | Propiedades de la referencia del documento tendencia, como la dirección url y el tipo de documento. |

## <a name="relationships"></a>Relaciones

| Propiedad      | Tipo          | Descripción  |
| ------------- |---------------| -------------|
| resource      | Entidad        | Se usa para navegar hasta el documento tendencia. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

```json
{
  "id": "string",
  "weight": "double",
  "resourceVisualization": [{"@odata.type": "microsoft.graph.resourceVisualization"}],
  "resourceReference": [{"@odata.type": "microsoft.graph.resourceReference"}],
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```