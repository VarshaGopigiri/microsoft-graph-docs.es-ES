---
title: tipo de recurso compartido
description: 'Una idea que representa los archivos compartidos con o por un usuario específico. Se admiten los siguientes archivos compartidos:'
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: 2c3d91023e2d68704b54308dff9566673f71dfb0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973709"
---
# <a name="shared-resource-type"></a>tipo de recurso compartido

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una idea que representa los archivos compartidos con o por un usuario específico. Se admiten los siguientes archivos compartidos:

- Invitar archivos adjuntos directamente en un correo electrónico o una reunión.
- OneDrive para Bussiness y SharePoint moderno datos adjuntos - archivos almacenados en OneDrive para profesionales y SharePoint que los usuarios compartir como vínculos en un correo electrónico.

**Nota**: actualmente estamos trabajando en rellenar los resultados de la API compartidos con datos. Puede haber algunos datos que faltan en las primeras semanas después del lanzamiento.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Lista compartida](../api/insights-list-shared.md) |colección de [insights_shared](insights-shared.md)| Obtener una lista de los archivos compartidos.|

## <a name="properties"></a>Propiedades

| Propiedad              | Tipo                      | Descripción  |
| -------------         |---------------            | -------------|
| id                    | String                    | Identificador único de la relación. Solo lectura.        |
| lastShared            | [sharingDetail](insights-sharingdetail.md)                | Obtener información detallada sobre el elemento compartido. Solo lectura.        |
| resourceVisualization | [resourceVisualization](insights-resourcevisualization.md)                | Propiedades que puede usar para visualizar el documento en su experiencia. Solo lectura      |
| resourceReference     | [resourceReference](insights-resourcereference.md)                      | Propiedades de la referencia del documento compartido, como la dirección url y el tipo de documento. Solo lectura       |

## <a name="relationships"></a>Relaciones

| Propiedad      | Tipo          | Descripción  |
| ------------- |---------------| -------------|
| resource      | Entidad        | Se usa para navegar hasta el elemento que se ha compartido. Los datos adjuntos de archivo, el tipo es *fileAttachment*. Los datos adjuntos vinculados, el tipo es *driveItem*. |

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso

```json
{
  "id": "string",
  "lastShared": "sharingDetail",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```
