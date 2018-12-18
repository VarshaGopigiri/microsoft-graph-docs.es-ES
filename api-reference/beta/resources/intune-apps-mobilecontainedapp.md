---
title: tipo de recurso mobileContainedApp
description: Una clase abstracta que representa una aplicación de contenidos en una mobileApp que actúa como un paquete.
author: tfitzmac
ms.openlocfilehash: 314225c46247bd122c825f0f883378513445ce0a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340799"
---
# <a name="mobilecontainedapp-resource-type"></a>tipo de recurso mobileContainedApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase abstracta que representa una aplicación de contenidos en una mobileApp que actúa como un paquete.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista mobileContainedApps](../api/intune-apps-mobilecontainedapp-list.md)|colección de [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)|Propiedades de la lista y relaciones de los objetos [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) .|
|[Obtener mobileContainedApp](../api/intune-apps-mobilecontainedapp-get.md)|[mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)|Leer las propiedades y las relaciones del objeto [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileContainedApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileContainedApp",
  "id": "String (identifier)"
}
```





