---
title: Tipo de recurso eBookInstallSummary
description: Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.
ms.openlocfilehash: 59754a8b925f573e44abd9ae1f674ab3f08f51c6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032045"
---
# <a name="ebookinstallsummary-resource-type"></a>Tipo de recurso eBookInstallSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del resumen de la instalación de un libro para un dispositivo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener eBookInstallSummary](../api/intune-books-ebookinstallsummary-get.md)|[eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md)|Lea las propiedades y las relaciones del objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).|
|[Actualizar eBookInstallSummary](../api/intune-books-ebookinstallsummary-update.md)|[eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md)|Actualice las propiedades de un objeto [eBookInstallSummary](../resources/intune-books-ebookinstallsummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|installedDeviceCount|Int32|Número de dispositivos que han instalado correctamente este libro.|
|failedDeviceCount|Int32|Número de dispositivos que no han podido instalar este libro.|
|notInstalledDeviceCount|Int32|Número de dispositivos que no han instalado este libro.|
|installedUserCount|Int32|Número de usuarios cuyos dispositivos al completo han instalado este libro.|
|failedUserCount|Int32|Número de usuarios que tienen 1 o más dispositivos que no han podido instalar este libro.|
|notInstalledUserCount|Int32|Número de usuarios que no han instalado este libro.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.eBookInstallSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.eBookInstallSummary",
  "id": "String (identifier)",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024,
  "installedUserCount": 1024,
  "failedUserCount": 1024,
  "notInstalledUserCount": 1024
}
```



