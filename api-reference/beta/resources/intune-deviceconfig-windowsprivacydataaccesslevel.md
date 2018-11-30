---
title: tipo de enumeración windowsPrivacyDataAccessLevel
description: Determinar el nivel de acceso a la categoría de datos de privacidad de Windows específica.
ms.openlocfilehash: 09db03706795cc2aba4cc0c93dce87dc7069cd3c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090909"
---
# <a name="windowsprivacydataaccesslevel-enum-type"></a>tipo de enumeración windowsPrivacyDataAccessLevel

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Determinar el nivel de acceso a la categoría de datos de privacidad de Windows específica.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|Ningún nivel de acceso no especificado, del color. Es posible que se comportan de dispositivo ya sea como en UserInControl o ForceAllow. Es posible que dependen de los datos de privacidad sido tener acceso a las versiones de Windows y otros factores.|
|forceAllow|1|Aplicaciones podrán tener acceso a los datos de privacidad especificado.|
|forceDeny|2|Se denegarán aplicaciones para tener acceso a datos de privacidad especificado.|
|userInControl|3|Se pedirá a los usuarios cuando aplicaciones intenta obtener acceso a datos de privacidad especificado.|





