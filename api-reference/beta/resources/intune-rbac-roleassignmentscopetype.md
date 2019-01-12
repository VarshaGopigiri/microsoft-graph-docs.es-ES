---
title: tipo de enumeración roleAssignmentScopeType
description: Especifica el tipo de ámbito para una asignación de roles.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b72e74bdb401f556214470b4c0aeda651339e332
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916085"
---
# <a name="roleassignmentscopetype-enum-type"></a>tipo de enumeración roleAssignmentScopeType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Especifica el tipo de ámbito para una asignación de roles.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|resourceScope|0|Permitir que las asignaciones para el ResourceScopes especificado.|
|allDevices|1|Permitir que las asignaciones a todos los dispositivos de Intune.|
|allLicensedUsers|2|Permitir que las asignaciones a todos los usuarios de Intune con licencia.|
|allDevicesAndLicensedUsers|3|Permitir que las asignaciones a todos los dispositivos Intune y los usuarios con licencia.|





