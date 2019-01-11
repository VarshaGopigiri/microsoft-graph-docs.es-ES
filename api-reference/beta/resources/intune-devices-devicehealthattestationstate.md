---
title: Tipo de recurso deviceHealthAttestationState
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 74d802e531757455dbd315785b86f0c13d4e06e9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861799"
---
# <a name="devicehealthattestationstate-resource-type"></a>Tipo de recurso deviceHealthAttestationState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|lastUpdateDateTime|Cadena|Marca de tiempo de la última actualización.|
|contentNamespaceUrl|Cadena|La versión del informe DHA. (Versión del espacio de nombres)|
|deviceHealthAttestationStatus|Cadena|La versión del informe DHA. (Versión del espacio de nombres)|
|contentVersion|Cadena|La versión del esquema de estado HealthAttestation|
|issuedDateTime|DateTimeOffset|Fecha y hora en la que se evaluó el dispositivo o se envió para MDM|
|attestationIdentityKey|Cadena|Cuando hay una clave de identidad de la atestación (AIK) presente en un dispositivo, significa que el dispositivo tiene un certificado de clave de aprobación (EK).|
|resetCount|Int64|El número de veces que un dispositivo PC ha hibernado o se ha reanudado|
|restartCount|Int64|El número de veces que se ha reiniciado un dispositivo PC|
|dataExcutionPolicy|Cadena|La directiva DEP define un conjunto de tecnologías de hardware y software que realizan comprobaciones adicionales en la memoria |
|bitLockerStatus|Cadena|Activar o desactivar el cifrado de unidad BitLocker|
|bootManagerVersion|Cadena|La versión del administrador de inicio|
|codeIntegrityCheckVersion|Cadena|La versión del administrador de inicio|
|secureBoot|Cadena|Cuando el inicio seguro está habilitado, los componentes principales deben tener las firmas cifradas correctas|
|bootDebugging|Cadena|Cuando bootDebugging está habilitado, se usa el dispositivo para desarrollo y pruebas|
|operatingSystemKernelDebugging|Cadena|Cuando operatingSystemKernelDebugging está habilitado, se usa el dispositivo para desarrollo y pruebas|
|codeIntegrity|Cadena| Cuando se habilita la integridad de código, la ejecución de código está restringida al código de integridad comprobada|
|testSigning|Cadena|Cuando se permite la firma de prueba, el dispositivo no fuerza la validación de firma durante el inicio|
|safeMode|Cadena|El modo seguro es una opción de solución de problemas de Windows que inicia el equipo en un estado limitado|
|windowsPE|Cadena|Sistema operativo con servicios limitados que se usa para preparar un equipo para Windows|
|earlyLaunchAntiMalwareDriverProtection|Cadena|El ELAM proporciona protección para los equipos de la red cuando se inician|
|virtualSecureMode|Cadena|VSM es un contenedor que protege los activos de valor alto de un kernel comprometido|
|pcrHashAlgorithm|Cadena|Atributo informativo que identifica el algoritmo HASH que usó el TPM|
|bootAppSecurityVersion|Cadena|El número de versión de seguridad de la aplicación de arranque|
|bootManagerSecurityVersion|Cadena|El número de versión de seguridad de la aplicación de arranque|
|tpmVersion|Cadena|El número de versión de seguridad de la aplicación de arranque|
|pcr0|Cadena|La medida que se captura en PCR\[0\]|
|secureBootConfigurationPolicyFingerPrint|Cadena|Huella digital de la directiva de configuración de arranque seguro personalizada|
|codeIntegrityPolicy|Cadena|La directiva de integridad de código que controla la seguridad del entorno de arranque|
|bootRevisionListInfo|Cadena|La lista de revisión de inicio que se cargó durante el primer inicio en el dispositivo atestiguado|
|operatingSystemRevListInfo|Cadena|La lista de revisión del sistema operativo que se cargó durante el primer inicio en el dispositivo atestiguado|
|healthStatusMismatchInfo|Cadena|Este atributo aparece si el servicio DHA detecta un problema de integridad|
|healthAttestationSupportedStatus|Cadena|Este atributo indica si DHA es compatible con el dispositivo|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceHealthAttestationState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceHealthAttestationState",
  "lastUpdateDateTime": "String",
  "contentNamespaceUrl": "String",
  "deviceHealthAttestationStatus": "String",
  "contentVersion": "String",
  "issuedDateTime": "String (timestamp)",
  "attestationIdentityKey": "String",
  "resetCount": 1024,
  "restartCount": 1024,
  "dataExcutionPolicy": "String",
  "bitLockerStatus": "String",
  "bootManagerVersion": "String",
  "codeIntegrityCheckVersion": "String",
  "secureBoot": "String",
  "bootDebugging": "String",
  "operatingSystemKernelDebugging": "String",
  "codeIntegrity": "String",
  "testSigning": "String",
  "safeMode": "String",
  "windowsPE": "String",
  "earlyLaunchAntiMalwareDriverProtection": "String",
  "virtualSecureMode": "String",
  "pcrHashAlgorithm": "String",
  "bootAppSecurityVersion": "String",
  "bootManagerSecurityVersion": "String",
  "tpmVersion": "String",
  "pcr0": "String",
  "secureBootConfigurationPolicyFingerPrint": "String",
  "codeIntegrityPolicy": "String",
  "bootRevisionListInfo": "String",
  "operatingSystemRevListInfo": "String",
  "healthStatusMismatchInfo": "String",
  "healthAttestationSupportedStatus": "String"
}
```





