---
title: tipo de recurso outOfBoxExperienceSettings
description: Fuera de la experiencia del cuadro Configuración
author: tfitzmac
ms.openlocfilehash: 545fbe5c27063397a4d08c40729227804ebfc56d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308410"
---
# <a name="outofboxexperiencesettings-resource-type"></a>tipo de recurso outOfBoxExperienceSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Fuera de la experiencia del cuadro Configuración
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|hidePrivacySettings|Boolean|Mostrar u ocultar opciones de privacidad para los usuarios|
|hideEULA|Boolean|Mostrar u ocultar los términos de licencia para el usuario|
|userType|[windowsUserType](../resources/intune-enrollment-windowsusertype.md)|Tipo de usuario. Los valores posibles son: `administrator` y `standard`.|
|deviceUsageType|[windowsDeviceUsageType](../resources/intune-enrollment-windowsdeviceusagetype.md)|Tipo de autenticación de combinación AAD. Los valores posibles son: `singleUser` y `shared`.|
|skipKeyboardSelectionPage|Boolean|Si el conjunto y, a continuación, omitir la selección de teclado página si se establecen el idioma y región|
|hideEscapeLink|Boolean|Si se establece en true, a continuación, el usuario no se puede iniciar a través de con una cuenta diferente, en el inicio de sesión de compañía|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.outOfBoxExperienceSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.outOfBoxExperienceSettings",
  "hidePrivacySettings": true,
  "hideEULA": true,
  "userType": "String",
  "deviceUsageType": "String",
  "skipKeyboardSelectionPage": true,
  "hideEscapeLink": true
}
```





