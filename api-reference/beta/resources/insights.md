---
title: tipo de recurso de conocimientos
description: Perspectivas son relaciones calculadas utilizando análisis avanzado y técnicas de aprendizaje de una máquina. Por ejemplo, puede identificar documentos de OneDrive tendencias alrededor de los usuarios.
author: simonhult
localization_priority: Priority
ms.prod: insights
ms.openlocfilehash: 38f7afb40c1618a8a7cf9d585c99633e2bb8d940
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938317"
---
# <a name="insights-resource-type"></a>tipo de recurso de conocimientos

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Perspectivas son relaciones calculadas utilizando análisis avanzado y técnicas de aprendizaje de una máquina. Por ejemplo, puede identificar documentos de OneDrive tendencias alrededor de los usuarios.

Perspectivas se devuelven por las API siguientes:

- [Tendencias](insights-trending.md) de - devuelve documentos de OneDrive y de los sitios de SharePoint tendencias alrededor de un usuario.
- [Se usa](insights-used.md) - devuelve documentos, ver y modificar por un usuario. Incluye documentos que el usuario usado en OneDrive para la empresa, SharePoint, que se abren como datos adjuntos de correo electrónico y como datos adjuntos de vínculo de orígenes como cuadro de lista desplegable y unidad de Google.
- [Shared](insights-shared.md) - devuelve documentos compartidos con un usuario. Documentos se pueden compartir como datos adjuntos de correo electrónico o como OneDrive for Business vincula enviados en correos electrónicos.

Se devuelve cada insight con un `resourceVisualization` y `resourceReference` el tipo de valor de tipo complejo (CVT). El resourceVisualization CVT contiene propiedades como `title` y `previewImageUrl`. Microsoft utiliza las propiedades de visualización para representar los archivos en experiencias como Office profundizar.

## <a name="relationships"></a>Relaciones

| Relación      | Tipo          | Descripción  |
| ------------- |---------------| -------------|
| tendencias      | Colección de [tendencias](insights-trending.md)       | Identificación de documentos de tendencias de relación calculada. Tendencias de documentos pueden almacenarse en OneDrive o en sitios de SharePoint.   |
| used      | Colección [se usa](insights-used.md)       | Calcula la relación de identificación de documentos, ver y modificar por un usuario. Incluye documentos que el usuario usado en OneDrive para la empresa, SharePoint, que se abren como datos adjuntos de correo electrónico y como datos adjuntos de vínculo de orígenes como cuadro de lista desplegable y unidad de Google.  |
| compartido        | Colección [compartidos](insights-shared.md)       | Identificación de documentos compartidos con un usuario de relación calculada. Documentos se pueden compartir como datos adjuntos de correo electrónico o como OneDrive for Business vincula enviados en correos electrónicos.   |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso
```json
{
  "trending": [ { "@odata.type": "microsoft.graph.trending" } ],
  "used": [ { "@odata.type": "microsoft.graph.used" } ],
  "shared": [ { "@odata.type": "microsoft.graph.shared" } ]
}
```
