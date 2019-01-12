---
title: Tipo de recurso telecomExpenseManagementPartner
description: Los recursos telecomExpenseManagementPartner representan los metadatos y el estado de un servicio TEM específico. Una vez que su organización haya incorporado a un partner, este puede estar habilitado o no para activar o desactivar la funcionalidad TEM.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: c515b21f5727bcb60588a6722cc3fd6b02719e36
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981801"
---
# <a name="telecomexpensemanagementpartner-resource-type"></a>Tipo de recurso telecomExpenseManagementPartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Los recursos telecomExpenseManagementPartner representan los metadatos y el estado de un servicio TEM específico. Una vez que su organización haya incorporado a un partner, este puede estar habilitado o no para activar o desactivar la funcionalidad TEM.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar telecomExpenseManagementPartners](../api/intune-tem-telecomexpensemanagementpartner-list.md)|Colección [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md)|Enumere las propiedades y las relaciones de los objetos [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).|
|[Obtener telecomExpenseManagementPartner](../api/intune-tem-telecomexpensemanagementpartner-get.md)|[telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md)|Lea las propiedades y las relaciones del objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).|
|[Crear telecomExpenseManagementPartner](../api/intune-tem-telecomexpensemanagementpartner-create.md)|[telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md)|Cree un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).|
|[Eliminar telecomExpenseManagementPartner](../api/intune-tem-telecomexpensemanagementpartner-delete.md)|Ninguna|Elimina un [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).|
|[Actualizar telecomExpenseManagementPartner](../api/intune-tem-telecomexpensemanagementpartner-update.md)|[telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md)|Actualice las propiedades de un objeto [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único del partner de TEM.|
|displayName|Cadena|Nombre para mostrar del partner de TEM.|
|url|Cadena|Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.|
|appAuthorized|Booleano|Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.|
|enabled|Booleano|Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.|
|lastConnectionDateTime|DateTimeOffset|Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.telecomExpenseManagementPartner"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "String (identifier)",
  "displayName": "String",
  "url": "String",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "String (timestamp)"
}
```



