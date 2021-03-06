---
title: tipo de recurso outOfBoxExperienceSettings
description: Fuera de la experiencia del cuadro Configuración
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 70f1fb573409a55dd1e586b8e88133c5535de894
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977293"
---
# <a name="outofboxexperiencesettings-resource-type"></a>tipo de recurso outOfBoxExperienceSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Fuera de la experiencia del cuadro Configuración
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|hidePrivacySettings|Booleano|Mostrar u ocultar opciones de privacidad para los usuarios|
|hideEULA|Booleano|Mostrar u ocultar los términos de licencia para el usuario|
|userType|[windowsUserType](../resources/intune-enrollment-windowsusertype.md)|Tipo de usuario. Los valores posibles son: `administrator` y `standard`.|
|deviceUsageType|[windowsDeviceUsageType](../resources/intune-enrollment-windowsdeviceusagetype.md)|Tipo de autenticación de combinación AAD. Los valores posibles son: `singleUser` y `shared`.|
|skipKeyboardSelectionPage|Booleano|Si el conjunto y, a continuación, omitir la selección de teclado página si se establecen el idioma y región|
|hideEscapeLink|Booleano|Si se establece en true, a continuación, el usuario no se puede iniciar a través de con una cuenta diferente, en el inicio de sesión de compañía|

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





