---
title: tipo de recurso officeUserCheckinSummary
description: Entidad que describe el inquilino protección de estadísticas.
author: tfitzmac
ms.openlocfilehash: 5064882f74a13feca726a6ebb91c34cf9a85af86
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306331"
---
# <a name="officeusercheckinsummary-resource-type"></a>tipo de recurso officeUserCheckinSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que describe el inquilino protección de estadísticas.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|succeededUserCount|Int32|Total de usuario correcta comprobar ins para los últimos 3 meses.|
|failedUserCount|Int32|Total usuario erróneas comprobar ins para los últimos 3 meses.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeUserCheckinSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeUserCheckinSummary",
  "succeededUserCount": 1024,
  "failedUserCount": 1024
}
```



