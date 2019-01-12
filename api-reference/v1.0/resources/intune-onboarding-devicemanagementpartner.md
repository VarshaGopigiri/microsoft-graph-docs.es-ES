---
title: Tipo de recurso deviceManagementPartner
description: Entidad que representa una conexión a un partner de administración de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cd91f139824051ec76cd214a8b87b0024608574d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972848"
---
# <a name="devicemanagementpartner-resource-type"></a>Tipo de recurso deviceManagementPartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que representa una conexión a un partner de administración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceManagementPartners](../api/intune-onboarding-devicemanagementpartner-list.md)|Colección [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md)|Enumere las propiedades y las relaciones de los objetos [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).|
|[Obtener deviceManagementPartner](../api/intune-onboarding-devicemanagementpartner-get.md)|[deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md)|Lea las propiedades y las relaciones del objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).|
|[Crear deviceManagementPartner](../api/intune-onboarding-devicemanagementpartner-create.md)|[deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md)|Cree un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).|
|[Eliminar deviceManagementPartner](../api/intune-onboarding-devicemanagementpartner-delete.md)|Ninguna|Elimina un [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).|
|[Actualizar deviceManagementPartner](../api/intune-onboarding-devicemanagementpartner-update.md)|[deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md)|Actualice las propiedades de un objeto [deviceManagementPartner](../resources/intune-onboarding-devicemanagementpartner.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Todavía no documentado|
|lastHeartbeatDateTime|DateTimeOffset|Marca de tiempo del último latido después de habilitar la opción de administrador Conectarse a los partners de administración de dispositivos|
|partnerState|[deviceManagementPartnerTenantState](../resources/intune-onboarding-devicemanagementpartnertenantstate.md)|Estado de socio de este inquilino. Los valores posibles son: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.|
|partnerAppType|[deviceManagementPartnerAppType](../resources/intune-onboarding-devicemanagementpartnerapptype.md)|Tipo de aplicación de socio. Los valores posibles son: `unknown`, `singleTenantApp` y `multiTenantApp`.|
|singleTenantAppId|String|Identificador de aplicación de espacio empresarial único de partner|
|displayName|String|Nombre para mostrar del partner|
|isConfigured|Booleano|Si el partner de administración de dispositivos está configurado o no|
|whenPartnerDevicesWillBeRemovedDateTime|DateTimeOffset|Fecha y hora en UTC de cuándo se quitará PartnerDevices|
|whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime|DateTimeOffset|Fecha y hora en UTC de cuándo PartnerDevices se marcará como no compatible|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementPartner"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "id": "String (identifier)",
  "lastHeartbeatDateTime": "String (timestamp)",
  "partnerState": "String",
  "partnerAppType": "String",
  "singleTenantAppId": "String",
  "displayName": "String",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "String (timestamp)",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "String (timestamp)"
}
```



