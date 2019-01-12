---
title: tipo de enumeración deviceEnrollmentType
description: Posibles maneras de agregar un dispositivo móvil a la administración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: bffe0e592240cbeee22a63dac8c339a0d3b3ff3d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946847"
---
# <a name="deviceenrollmenttype-enum-type"></a>tipo de enumeración deviceEnrollmentType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Posibles maneras de agregar un dispositivo móvil a la administración.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|desconocido|0|No se recopiló el valor predeterminado, el tipo de inscripción.|
|userEnrollment|1|Inscripción impulsada de usuario a través del canal BYOD.|
|deviceEnrollmentManager|2|Inscripción de usuario con una cuenta de administrador de inscripción de dispositivo.|
|appleBulkWithUser|3|Inscripción masiva de Apple con desafío de usuario. (DEP, Configurador de Apple)|
|appleBulkWithoutUser|4|Inscripción masiva de Apple sin desafío de usuario. (Configuración DEP, Configurador de Apple, móvil)|
|windowsAzureADJoin|5|Unirse Windows Azure AD de 10.|
|windowsBulkUserless|6|Inscripción de Windows 10 masiva a través de ICD con certificado.|
|windowsAutoEnrollment|7|10 de Windows la inscripción automática. (Agregar la cuenta de trabajo)|
|windowsBulkAzureDomainJoin|8|Windows 10 masivo participar en Azure AD.|
|windowsCoManagement|9|10 CO-administración de Windows desencadenadas por piloto automático o directiva de grupo.|





