---
title: tipo de enumeración roleAssignmentScopeType
description: Especifica el tipo de ámbito para una asignación de roles.
author: tfitzmac
ms.openlocfilehash: 0a3286b3b7bc583323204ca39ff85e01869ddbe7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343130"
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





