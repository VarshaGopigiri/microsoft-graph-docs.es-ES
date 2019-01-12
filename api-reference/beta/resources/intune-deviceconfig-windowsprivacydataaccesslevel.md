---
title: tipo de enumeración windowsPrivacyDataAccessLevel
description: Determinar el nivel de acceso a la categoría de datos de privacidad de Windows específica.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 64db5eb78708a0cfa835bd695ba01b2c267fc4fd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959320"
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





