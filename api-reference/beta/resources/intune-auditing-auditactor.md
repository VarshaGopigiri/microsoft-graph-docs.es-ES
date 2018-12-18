---
title: Tipo de recurso auditActor
description: Una clase que contiene las propiedades del actor de auditoría.
author: tfitzmac
ms.openlocfilehash: 1b1f3a182aa710564bdf5e134a4ceabf22f3fb71
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348933"
---
# <a name="auditactor-resource-type"></a>Tipo de recurso auditActor

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades del actor de auditoría.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|type|cadena|Tipo de actor.|
|userPermissions|Colección de cadenas|Lista de los permisos de usuario cuando se ha realizado la auditoría.|
|applicationId|cadena|Id. de aplicación de AAD|
|applicationDisplayName|cadena|Nombre de la aplicación.|
|userPrincipalName|cadena|Nombre principal de usuario (UPN).|
|servicePrincipalName|cadena|Nombre de entidad de seguridad de servicio (SPN).|
|ipAddress|cadena|IPAddress.|
|userId|cadena|Id. de usuario.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.auditActor"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditActor",
  "type": "String",
  "userPermissions": [
    "String"
  ],
  "applicationId": "String",
  "applicationDisplayName": "String",
  "userPrincipalName": "String",
  "servicePrincipalName": "String",
  "ipAddress": "String",
  "userId": "String"
}
```





