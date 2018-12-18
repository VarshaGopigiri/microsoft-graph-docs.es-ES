---
title: Tipo de recurso organization
description: El recurso organization representa una instancia de la configuración global y los recursos que funcionan y se aprovisionan en el nivel del espacio empresarial.
author: tfitzmac
ms.openlocfilehash: da2d127dc5ba44187d8a3a066f5fe261d3dee859
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322851"
---
# <a name="organization-resource-type"></a>Tipo de recurso organization

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
|id|String|El GUID para el objeto.|
|mobileDeviceManagementAuthority|[mdmAuthority](../resources/intune-onboarding-mdmauthority.md)|Entidad de administración de dispositivos móviles. Los valores posibles son: `unknown`, `intune`, `sccm` y `office365`.|

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
  "mobileDeviceManagementAuthority": "String"
}
```


<!-- {
  "type": "#page.annotation",
  "suppressions": [

"Warning: Resource microsoft.graph.organization is defined in multiple files: /api-reference/v1.0/resources/intune_onboarding_organization.md, /api-reference/v1.0/resources/organization.md",

"Warning: Schema type organization has a different BaseType value microsoft.graph.directoryObject than the documentation .",

"Warning: Schema type organization has a different OpenType value False than the documentation True.",

"Warning: Resource organization has multiple declarations with mismatched OpenType declarations."

  ],

}
-->

