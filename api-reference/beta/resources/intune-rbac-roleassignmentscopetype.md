---
title: tipo de enumeración roleAssignmentScopeType
description: Especifica el tipo de ámbito para una asignación de roles.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 738579fbd8bcda9ac438ada2f7746e020396d225
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871543"
---
# <a name="roleassignmentscopetype-enum-type"></a>tipo de enumeración roleAssignmentScopeType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Especifica el tipo de ámbito para una asignación de roles.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|resourceScope|0|Permitir que las asignaciones para el ResourceScopes especificado.|
|allDevices|1|Permitir que las asignaciones a todos los dispositivos de Intune.|
|allLicensedUsers|2|Permitir que las asignaciones a todos los usuarios de Intune con licencia.|
|allDevicesAndLicensedUsers|3|Permitir que las asignaciones a todos los dispositivos Intune y los usuarios con licencia.|





