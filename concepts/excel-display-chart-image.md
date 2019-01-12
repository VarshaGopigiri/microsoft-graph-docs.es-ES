---
title: Mostrar una imagen de gráfico de Excel con Microsoft Graph
description: Al realizar una operación GET para recuperar una imagen de gráfico, la API de Excel devuelve una imagen como una cadena Base 64.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 5cdf5522ccd0a72798ee62211e9221cf2ea9cd53
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946374"
---
# <a name="display-a-chart-image-in-excel-with-microsoft-graph"></a>Mostrar una imagen de gráfico de Excel con Microsoft Graph

Al realizar una [operación GET para recuperar una imagen de gráfico](/api-reference/v1.0/api/chart-image.md), la API de Excel devuelve una imagen como una cadena Base 64.

Puede mostrar la cadena Base 64 en una etiqueta de imagen HTML: `<img src="data:image/png;base64,{base-64 chart image string}/>`.

Para usar el comportamiento predeterminado, utilice `Image(width=0,height=0,fittingMode='fit')`. Este es un ejemplo de una imagen de gráfico devuelta con los parámetros predeterminados.

![Imagen de gráfico de Excel con alto y ancho predeterminados.](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/GetChart-default.png)

Si quiere personalizar la visualización de la imagen, especifique un alto, un ancho y un modo de ajuste. Esta es la apariencia de la misma imagen de gráfico si la recupera con estos parámetros: `Image(width=500,height=500,fittingMode='Fill')`.

## <a name="see-also"></a>Vea también

* [Administrar sesiones en Excel con Microsoft Graph](excel-manage-sessions.md)
* [Escribir en un libro de Excel con Microsoft Graph](excel-write-to-workbook.md)
* [Usar funciones de libro en Excel con Microsoft Graph](excel-use-functions.md)
* [Actualizar el formato de un rango en Excel con Microsoft Graph](excel-update-range-format.md)
* [Usar la API de REST de Excel](/graph/api/resources/excel?view=graph-rest-1.0)
