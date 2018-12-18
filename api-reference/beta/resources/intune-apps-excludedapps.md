---
title: tipo de recurso excludedApps
description: Contiene las propiedades para las aplicaciones de Office365 excluidos.
author: tfitzmac
ms.openlocfilehash: b8c9eff985783c953ff099dbf4d5ba00826652c4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344628"
---
# <a name="excludedapps-resource-type"></a>tipo de recurso excludedApps

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades para las aplicaciones de Office365 excluidos.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|Access|Boolean|El valor de if MS Office Access debería excluirse o no.|
|de Excel|Boolean|El valor de if MS Office Excel debería excluirse o no.|
|Groove|Boolean|El valor de if MS Office OneDrive para la empresa - Groove se deben excluir o no.|
|infoPath|Boolean|El valor de if MS Office InfoPath se deben excluir o no.|
|Lync|Boolean|El valor de if MS Office Skype para la empresa - Lync se deben excluir o no.|
|oneDrive|Boolean|El valor de if se deben excluir MS Office OneDrive o no.|
|oneNote|Boolean|El valor de if MS Office OneNote debe excluir o no.|
|Outlook|Boolean|El valor de if MS Office Outlook debería excluirse o no.|
|powerPoint|Boolean|El valor de if MS Office PowerPoint se deben excluir o no.|
|publicador|Boolean|El valor de if MS Office Publisher se deben excluir o no.|
|SharePoint Designer|Boolean|El valor de if SharePoint Designer de MS Office debería excluirse o no.|
|Visio|Boolean|El valor de if MS Office Visio se deben excluir o no.|
|Word|Boolean|El valor de if se deben excluir MS Office Word o no.|

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





