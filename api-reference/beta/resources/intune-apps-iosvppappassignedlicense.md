---
title: tipo de recurso iosVppAppAssignedLicense
description: asignación de licencias por volumen compra programa iOS. Esta clase no es compatible con Crear, Eliminar ni Actualizar.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 5d2588cd8ceeae44b7e4150544a984c68d4d90e3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991218"
---
# <a name="iosvppappassignedlicense-resource-type"></a>tipo de recurso iosVppAppAssignedLicense

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

asignación de licencias por volumen compra programa iOS. Esta clase no es compatible con Crear, Eliminar ni Actualizar.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista iosVppAppAssignedLicenses](../api/intune-apps-iosvppappassignedlicense-list.md)|colección de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|Propiedades de la lista y relaciones de los objetos [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .|
|[Obtener iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-get.md)|[iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|Leer las propiedades y las relaciones del objeto [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .|
|[Crear iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-create.md)|[iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|Crear un nuevo objeto [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .|
|[Eliminar iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-delete.md)|Ninguno|Elimina un [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md).|
|[Actualizar iosVppAppAssignedLicense](../api/intune-apps-iosvppappassignedlicense-update.md)|[iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)|Actualizar las propiedades de un objeto [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|userEmailAddress|Cadena|La dirección de correo electrónico del usuario.|
|userId|Cadena|El identificador de usuario.|
|userName|Cadena|El nombre de usuario.|
|userPrincipalName|Cadena|El nombre principal del usuario.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppAppAssignedLicense"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedLicense",
  "id": "String (identifier)",
  "userEmailAddress": "String",
  "userId": "String",
  "userName": "String",
  "userPrincipalName": "String"
}
```





