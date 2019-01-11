---
title: Tipo de recurso organization
description: El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7c6f99c378bc7fd53f473419a5ca4f4350f7c57b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812050"
---
# <a name="organization-resource-type"></a>Tipo de recurso organization

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar organizaciones](../api/intune-onboarding-organization-list.md)|Colección [organization](../resources/intune-onboarding-organization.md)|Lea las propiedades y las relaciones de los objetos [organization](../resources/intune-onboarding-organization.md).|
|[Obtener organización](../api/intune-onboarding-organization-get.md)|[organization](../resources/intune-onboarding-organization.md)|Lea las propiedades y las relaciones del objeto [organization](../resources/intune-onboarding-organization.md).|
|[Actualizar organization](../api/intune-onboarding-organization-update.md)|[organization](../resources/intune-onboarding-organization.md)|Actualice las propiedades de un objeto [organization](../resources/intune-onboarding-organization.md).|
|[Acción setMobileDeviceManagementAuthority](../api/intune-onboarding-organization-setmobiledevicemanagementauthority.md)|Int32|Establecer la entidad de administración de dispositivos móviles|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El GUID para el objeto.|
|mobileDeviceManagementAuthority|[mdmAuthority](../resources/intune-onboarding-mdmauthority.md)|Entidad de administración de dispositivos móviles. Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.|
|certificateConnectorSetting|[certificateConnectorSetting](../resources/intune-onboarding-certificateconnectorsetting.md)|Configuración del conector del certificado.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.organization"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.organization",
  "id": "String (identifier)",
  "mobileDeviceManagementAuthority": "String",
  "certificateConnectorSetting": {
    "@odata.type": "microsoft.graph.certificateConnectorSetting",
    "status": 1024,
    "certExpiryTime": "String (timestamp)",
    "enrollmentError": "String",
    "lastConnectorConnectionTime": "String (timestamp)",
    "connectorVersion": "String",
    "lastUploadVersion": 1024
  }
}
```





