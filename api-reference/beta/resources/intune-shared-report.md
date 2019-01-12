---
title: Tipo de recurso report
description: 'Devuelve el contenido apropiado para el contexto, incluidos:'
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: dbad8a8808d40c2ae1f7769773b6b29ef65d680f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970650"
---
# <a name="report-resource-type"></a>Tipo de recurso report

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Devuelve el contenido apropiado para el contexto, incluidos:

- Informes de historial de perfil de configuración de dispositivo.
- Informes de errores de inscripción.

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|content|Stream|Contenido del informe; detalles varían según el tipo de informe.|

## <a name="relationships"></a>Relaciones
Ninguna

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.report"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.report",
  "content": "<Unknown Primitive Type Edm.Stream>"
}
```



