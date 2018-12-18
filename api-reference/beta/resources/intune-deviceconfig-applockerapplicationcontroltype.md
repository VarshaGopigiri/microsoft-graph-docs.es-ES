---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
author: tfitzmac
ms.openlocfilehash: 0d6190170d6f6695a3303047f9ccb193afd248f3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330208"
---
# <a name="applockerapplicationcontroltype-enum-type"></a>tipo de enumeración appLockerApplicationControlType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles valores de tipos de Control de aplicación de AppLocker
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|No configurado|0|Valor predeterminado de dispositivo, no se ha seleccionado ningún tipo de Control de la aplicación.|
|enforceComponentsAndStoreApps|1|Exigir la aplicación de las aplicaciones de componente y almacenamiento de Windows.|
|auditComponentsAndStoreApps|2|Auditoría de aplicaciones de componente y almacenamiento de Windows.|
|enforceComponentsStoreAppsAndSmartlocker|3|Exigir la aplicación de componentes de Windows, almacenar aplicaciones y almacén inteligente.|
|auditComponentsStoreAppsAndSmartlocker|4|Componentes de Windows de auditoría, almacenar aplicaciones y almacén inteligente.|





