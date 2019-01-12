---
title: Tipo de recurso userInstallStateSummary
description: Contiene las propiedades del resumen del estado de la instalación para un usuario.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6835dcad87fbf16a8dc81b6c9f9ab124a9834a3c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931856"
---
# <a name="userinstallstatesummary-resource-type"></a>Tipo de recurso userInstallStateSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del resumen del estado de la instalación para un usuario.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar userInstallStateSummaries](../api/intune-books-userinstallstatesummary-list.md)|Colección [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)|Enumere las propiedades y las relaciones de los objetos [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).|
|[Obtener userInstallStateSummary](../api/intune-books-userinstallstatesummary-get.md)|[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)|Lea las propiedades y las relaciones del objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).|
|[Crear userInstallStateSummary](../api/intune-books-userinstallstatesummary-create.md)|[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)|Cree un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).|
|[Eliminar userInstallStateSummary](../api/intune-books-userinstallstatesummary-delete.md)|Ninguna|Elimina un [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)|
|[Actualizar userInstallStateSummary](../api/intune-books-userinstallstatesummary-update.md)|[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)|Actualice las propiedades de un objeto [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|userName|String|Nombre de usuario.|
|installedDeviceCount|Int32|Número de dispositivos instalados.|
|failedDeviceCount|Int32|Número de dispositivos erróneos.|
|notInstalledDeviceCount|Int32|Número de dispositivos no instalados.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceStates|Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)|El estado de instalación del libro electrónico.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userInstallStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userInstallStateSummary",
  "id": "String (identifier)",
  "userName": "String",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024
}
```





