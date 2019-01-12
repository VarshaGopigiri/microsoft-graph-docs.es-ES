---
title: tipo de enumeración appLockerApplicationControlType
description: Posibles valores de tipos de Control de aplicación de AppLocker
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 258a98b9ec4945c807a6aae2b34a178628952ac4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937960"
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



