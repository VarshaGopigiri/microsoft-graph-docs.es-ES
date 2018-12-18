---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
author: tfitzmac
ms.openlocfilehash: d53c2d0f7996edfab610e4206f4d2815ba4000b8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310265"
---
# <a name="applockerapplicationcontroltype-enum-type"></a>tipo de enumeración appLockerApplicationControlType

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



