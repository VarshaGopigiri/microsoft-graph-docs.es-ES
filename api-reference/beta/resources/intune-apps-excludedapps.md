---
title: tipo de recurso excludedApps
description: Contiene las propiedades para las aplicaciones de Office365 excluidos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 90216c639d36a989b2fad5dbdc1adbd11fe46ede
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943952"
---
# <a name="excludedapps-resource-type"></a>tipo de recurso excludedApps

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades para las aplicaciones de Office365 excluidos.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|Access|Booleano|El valor de if MS Office Access debería excluirse o no.|
|de Excel|Booleano|El valor de if MS Office Excel debería excluirse o no.|
|Groove|Booleano|El valor de if MS Office OneDrive para la empresa - Groove se deben excluir o no.|
|infoPath|Booleano|El valor de if MS Office InfoPath se deben excluir o no.|
|Lync|Booleano|El valor de if MS Office Skype para la empresa - Lync se deben excluir o no.|
|oneDrive|Booleano|El valor de if se deben excluir MS Office OneDrive o no.|
|oneNote|Booleano|El valor de if MS Office OneNote debe excluir o no.|
|Outlook|Booleano|El valor de if MS Office Outlook debería excluirse o no.|
|powerPoint|Booleano|El valor de if MS Office PowerPoint se deben excluir o no.|
|publicador|Booleano|El valor de if MS Office Publisher se deben excluir o no.|
|SharePoint Designer|Booleano|El valor de if SharePoint Designer de MS Office debería excluirse o no.|
|Visio|Booleano|El valor de if MS Office Visio se deben excluir o no.|
|Word|Booleano|El valor de if se deben excluir MS Office Word o no.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.excludedApps"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.excludedApps",
  "access": true,
  "excel": true,
  "groove": true,
  "infoPath": true,
  "lync": true,
  "oneDrive": true,
  "oneNote": true,
  "outlook": true,
  "powerPoint": true,
  "publisher": true,
  "sharePointDesigner": true,
  "visio": true,
  "word": true
}
```





