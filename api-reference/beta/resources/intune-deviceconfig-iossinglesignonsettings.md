---
title: tipo de recurso iosSingleSignOnSettings
description: configuración de autenticación de Kerberos para el inicio de sesión único de iOS
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 54c5656de6262692324cce8ab71a0e100672c050
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952674"
---
# <a name="iossinglesignonsettings-resource-type"></a>tipo de recurso iosSingleSignOnSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

configuración de autenticación de Kerberos para el inicio de sesión único de iOS
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|allowedAppsList|Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)|Lista de identificadores de aplicación que tienen permiso para utilizar este inicio de sesión. Si se omite este campo, el inicio de sesión se aplica a todas las aplicaciones en el dispositivo. Esta colección puede contener un máximo de 500 elementos.|
|allowedUrls|Colección String|Lista de direcciones URL de HTTP que se debe coincidir con el fin de utilizar este inicio de sesión. Con iOS 9.0 o posterior, se puede usar un carácter comodín.|
|displayName|Cadena|El nombre para mostrar de la configuración de inicio de sesión que se muestra en el dispositivo receptor.|
|kerberosPrincipalName|Cadena|Un nombre principal de Kerberos. Si no se proporciona, el usuario se le pida durante la instalación del perfil.|
|kerberosRealm|Cadena|Un nombre de territorio Kerberos. Distingue entre mayúsculas y minúsculas.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosSingleSignOnSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosSingleSignOnSettings",
  "allowedAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "String",
      "publisher": "String",
      "appStoreUrl": "String",
      "appId": "String"
    }
  ],
  "allowedUrls": [
    "String"
  ],
  "displayName": "String",
  "kerberosPrincipalName": "String",
  "kerberosRealm": "String"
}
```





