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
# <a name="devicehealthattestationstate-resource-type"></a><span data-ttu-id="48d48-103">Tipo de recurso deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="48d48-103">deviceHealthAttestationState resource type</span></span>

> <span data-ttu-id="48d48-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="48d48-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="48d48-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="48d48-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="48d48-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="48d48-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="48d48-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="48d48-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="48d48-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48d48-108">Properties</span></span>
|<span data-ttu-id="48d48-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48d48-109">Property</span></span>|<span data-ttu-id="48d48-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="48d48-110">Type</span></span>|<span data-ttu-id="48d48-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="48d48-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="48d48-112">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="48d48-112">lastUpdateDateTime</span></span>|<span data-ttu-id="48d48-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-113">String</span></span>|<span data-ttu-id="48d48-114">Marca de tiempo de la última actualización.</span><span class="sxs-lookup"><span data-stu-id="48d48-114">The Timestamp of the last update.</span></span>|
|<span data-ttu-id="48d48-115">contentNamespaceUrl</span><span class="sxs-lookup"><span data-stu-id="48d48-115">contentNamespaceUrl</span></span>|<span data-ttu-id="48d48-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-116">String</span></span>|<span data-ttu-id="48d48-117">La versión del informe DHA.</span><span class="sxs-lookup"><span data-stu-id="48d48-117">The DHA report version.</span></span> <span data-ttu-id="48d48-118">(Versión del espacio de nombres)</span><span class="sxs-lookup"><span data-stu-id="48d48-118">(Namespace version)</span></span>|
|<span data-ttu-id="48d48-119">deviceHealthAttestationStatus</span><span class="sxs-lookup"><span data-stu-id="48d48-119">deviceHealthAttestationStatus</span></span>|<span data-ttu-id="48d48-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-120">String</span></span>|<span data-ttu-id="48d48-121">La versión del informe DHA.</span><span class="sxs-lookup"><span data-stu-id="48d48-121">The DHA report version.</span></span> <span data-ttu-id="48d48-122">(Versión del espacio de nombres)</span><span class="sxs-lookup"><span data-stu-id="48d48-122">(Namespace version)</span></span>|
|<span data-ttu-id="48d48-123">contentVersion</span><span class="sxs-lookup"><span data-stu-id="48d48-123">contentVersion</span></span>|<span data-ttu-id="48d48-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-124">String</span></span>|<span data-ttu-id="48d48-125">La versión del esquema de estado HealthAttestation</span><span class="sxs-lookup"><span data-stu-id="48d48-125">The HealthAttestation state schema version</span></span>|
|<span data-ttu-id="48d48-126">issuedDateTime</span><span class="sxs-lookup"><span data-stu-id="48d48-126">issuedDateTime</span></span>|<span data-ttu-id="48d48-127">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="48d48-127">DateTimeOffset</span></span>|<span data-ttu-id="48d48-128">Fecha y hora en la que se evaluó el dispositivo o se envió para MDM</span><span class="sxs-lookup"><span data-stu-id="48d48-128">The DateTime when device was evaluated or issued to MDM</span></span>|
|<span data-ttu-id="48d48-129">attestationIdentityKey</span><span class="sxs-lookup"><span data-stu-id="48d48-129">attestationIdentityKey</span></span>|<span data-ttu-id="48d48-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-130">String</span></span>|<span data-ttu-id="48d48-131">Cuando hay una clave de identidad de la atestación (AIK) presente en un dispositivo, significa que el dispositivo tiene un certificado de clave de aprobación (EK).</span><span class="sxs-lookup"><span data-stu-id="48d48-131">TWhen an Attestation Identity Key (AIK) is present on a device, it indicates that the device has an endorsement key (EK) certificate.</span></span>|
|<span data-ttu-id="48d48-132">resetCount</span><span class="sxs-lookup"><span data-stu-id="48d48-132">resetCount</span></span>|<span data-ttu-id="48d48-133">Int64</span><span class="sxs-lookup"><span data-stu-id="48d48-133">Int64</span></span>|<span data-ttu-id="48d48-134">El número de veces que un dispositivo PC ha hibernado o se ha reanudado</span><span class="sxs-lookup"><span data-stu-id="48d48-134">The number of times a PC device has hibernated or resumed</span></span>|
|<span data-ttu-id="48d48-135">restartCount</span><span class="sxs-lookup"><span data-stu-id="48d48-135">restartCount</span></span>|<span data-ttu-id="48d48-136">Int64</span><span class="sxs-lookup"><span data-stu-id="48d48-136">Int64</span></span>|<span data-ttu-id="48d48-137">El número de veces que se ha reiniciado un dispositivo PC</span><span class="sxs-lookup"><span data-stu-id="48d48-137">The number of times a PC device has rebooted</span></span>|
|<span data-ttu-id="48d48-138">dataExcutionPolicy</span><span class="sxs-lookup"><span data-stu-id="48d48-138">dataExcutionPolicy</span></span>|<span data-ttu-id="48d48-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-139">String</span></span>|<span data-ttu-id="48d48-140">La directiva DEP define un conjunto de tecnologías de hardware y software que realizan comprobaciones adicionales en la memoria</span><span class="sxs-lookup"><span data-stu-id="48d48-140">DEP Policy defines a set of hardware and software technologies that perform additional checks on memory</span></span> |
|<span data-ttu-id="48d48-141">bitLockerStatus</span><span class="sxs-lookup"><span data-stu-id="48d48-141">bitLockerStatus</span></span>|<span data-ttu-id="48d48-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-142">String</span></span>|<span data-ttu-id="48d48-143">Activar o desactivar el cifrado de unidad BitLocker</span><span class="sxs-lookup"><span data-stu-id="48d48-143">On or Off of BitLocker Drive Encryption</span></span>|
|<span data-ttu-id="48d48-144">bootManagerVersion</span><span class="sxs-lookup"><span data-stu-id="48d48-144">bootManagerVersion</span></span>|<span data-ttu-id="48d48-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-145">String</span></span>|<span data-ttu-id="48d48-146">La versión del administrador de inicio</span><span class="sxs-lookup"><span data-stu-id="48d48-146">The version of the Boot Manager</span></span>|
|<span data-ttu-id="48d48-147">codeIntegrityCheckVersion</span><span class="sxs-lookup"><span data-stu-id="48d48-147">codeIntegrityCheckVersion</span></span>|<span data-ttu-id="48d48-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-148">String</span></span>|<span data-ttu-id="48d48-149">La versión del administrador de inicio</span><span class="sxs-lookup"><span data-stu-id="48d48-149">The version of the Boot Manager</span></span>|
|<span data-ttu-id="48d48-150">secureBoot</span><span class="sxs-lookup"><span data-stu-id="48d48-150">secureBoot</span></span>|<span data-ttu-id="48d48-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-151">String</span></span>|<span data-ttu-id="48d48-152">Cuando el inicio seguro está habilitado, los componentes principales deben tener las firmas cifradas correctas</span><span class="sxs-lookup"><span data-stu-id="48d48-152">When Secure Boot is enabled, the core components must have the correct cryptographic signatures</span></span>|
|<span data-ttu-id="48d48-153">bootDebugging</span><span class="sxs-lookup"><span data-stu-id="48d48-153">bootDebugging</span></span>|<span data-ttu-id="48d48-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-154">String</span></span>|<span data-ttu-id="48d48-155">Cuando bootDebugging está habilitado, se usa el dispositivo para desarrollo y pruebas</span><span class="sxs-lookup"><span data-stu-id="48d48-155">When bootDebugging is enabled, the device is used in development and testing</span></span>|
|<span data-ttu-id="48d48-156">operatingSystemKernelDebugging</span><span class="sxs-lookup"><span data-stu-id="48d48-156">operatingSystemKernelDebugging</span></span>|<span data-ttu-id="48d48-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-157">String</span></span>|<span data-ttu-id="48d48-158">Cuando operatingSystemKernelDebugging está habilitado, se usa el dispositivo para desarrollo y pruebas</span><span class="sxs-lookup"><span data-stu-id="48d48-158">When operatingSystemKernelDebugging is enabled, the device is used in development and testing</span></span>|
|<span data-ttu-id="48d48-159">codeIntegrity</span><span class="sxs-lookup"><span data-stu-id="48d48-159">codeIntegrity</span></span>|<span data-ttu-id="48d48-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-160">String</span></span>| <span data-ttu-id="48d48-161">Cuando se habilita la integridad de código, la ejecución de código está restringida al código de integridad comprobada</span><span class="sxs-lookup"><span data-stu-id="48d48-161">When code integrity is enabled, code execution is restricted to integrity verified code</span></span>|
|<span data-ttu-id="48d48-162">testSigning</span><span class="sxs-lookup"><span data-stu-id="48d48-162">testSigning</span></span>|<span data-ttu-id="48d48-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-163">String</span></span>|<span data-ttu-id="48d48-164">Cuando se permite la firma de prueba, el dispositivo no fuerza la validación de firma durante el inicio</span><span class="sxs-lookup"><span data-stu-id="48d48-164">When test signing is allowed, the device does not enforce signature validation during boot</span></span>|
|<span data-ttu-id="48d48-165">safeMode</span><span class="sxs-lookup"><span data-stu-id="48d48-165">safeMode</span></span>|<span data-ttu-id="48d48-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-166">String</span></span>|<span data-ttu-id="48d48-167">El modo seguro es una opción de solución de problemas de Windows que inicia el equipo en un estado limitado</span><span class="sxs-lookup"><span data-stu-id="48d48-167">Safe mode is a troubleshooting option for Windows that starts your computer in a limited state</span></span>|
|<span data-ttu-id="48d48-168">windowsPE</span><span class="sxs-lookup"><span data-stu-id="48d48-168">windowsPE</span></span>|<span data-ttu-id="48d48-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-169">String</span></span>|<span data-ttu-id="48d48-170">Sistema operativo con servicios limitados que se usa para preparar un equipo para Windows</span><span class="sxs-lookup"><span data-stu-id="48d48-170">Operating system running with limited services that is used to prepare a computer for Windows</span></span>|
|<span data-ttu-id="48d48-171">earlyLaunchAntiMalwareDriverProtection</span><span class="sxs-lookup"><span data-stu-id="48d48-171">earlyLaunchAntiMalwareDriverProtection</span></span>|<span data-ttu-id="48d48-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-172">String</span></span>|<span data-ttu-id="48d48-173">El ELAM proporciona protección para los equipos de la red cuando se inician</span><span class="sxs-lookup"><span data-stu-id="48d48-173">ELAM provides protection for the computers in your network when they start up</span></span>|
|<span data-ttu-id="48d48-174">virtualSecureMode</span><span class="sxs-lookup"><span data-stu-id="48d48-174">virtualSecureMode</span></span>|<span data-ttu-id="48d48-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-175">String</span></span>|<span data-ttu-id="48d48-176">VSM es un contenedor que protege los activos de valor alto de un kernel comprometido</span><span class="sxs-lookup"><span data-stu-id="48d48-176">VSM is a container that protects high value assets from a compromised kernel</span></span>|
|<span data-ttu-id="48d48-177">pcrHashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="48d48-177">pcrHashAlgorithm</span></span>|<span data-ttu-id="48d48-178">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-178">String</span></span>|<span data-ttu-id="48d48-179">Atributo informativo que identifica el algoritmo HASH que usó el TPM</span><span class="sxs-lookup"><span data-stu-id="48d48-179">Informational attribute that identifies the HASH algorithm that was used by TPM</span></span>|
|<span data-ttu-id="48d48-180">bootAppSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="48d48-180">bootAppSecurityVersion</span></span>|<span data-ttu-id="48d48-181">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-181">String</span></span>|<span data-ttu-id="48d48-182">El número de versión de seguridad de la aplicación de arranque</span><span class="sxs-lookup"><span data-stu-id="48d48-182">The security version number of the Boot Application</span></span>|
|<span data-ttu-id="48d48-183">bootManagerSecurityVersion</span><span class="sxs-lookup"><span data-stu-id="48d48-183">bootManagerSecurityVersion</span></span>|<span data-ttu-id="48d48-184">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-184">String</span></span>|<span data-ttu-id="48d48-185">El número de versión de seguridad de la aplicación de arranque</span><span class="sxs-lookup"><span data-stu-id="48d48-185">The security version number of the Boot Application</span></span>|
|<span data-ttu-id="48d48-186">tpmVersion</span><span class="sxs-lookup"><span data-stu-id="48d48-186">tpmVersion</span></span>|<span data-ttu-id="48d48-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-187">String</span></span>|<span data-ttu-id="48d48-188">El número de versión de seguridad de la aplicación de arranque</span><span class="sxs-lookup"><span data-stu-id="48d48-188">The security version number of the Boot Application</span></span>|
|<span data-ttu-id="48d48-189">pcr0</span><span class="sxs-lookup"><span data-stu-id="48d48-189">pcr0</span></span>|<span data-ttu-id="48d48-190">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-190">String</span></span>|<span data-ttu-id="48d48-191">La medida que se captura en PCR\[0\]</span><span class="sxs-lookup"><span data-stu-id="48d48-191">The measurement that is captured in PCR\[0\]</span></span>|
|<span data-ttu-id="48d48-192">secureBootConfigurationPolicyFingerPrint</span><span class="sxs-lookup"><span data-stu-id="48d48-192">secureBootConfigurationPolicyFingerPrint</span></span>|<span data-ttu-id="48d48-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-193">String</span></span>|<span data-ttu-id="48d48-194">Huella digital de la directiva de configuración de arranque seguro personalizada</span><span class="sxs-lookup"><span data-stu-id="48d48-194">Fingerprint of the Custom Secure Boot Configuration Policy</span></span>|
|<span data-ttu-id="48d48-195">codeIntegrityPolicy</span><span class="sxs-lookup"><span data-stu-id="48d48-195">codeIntegrityPolicy</span></span>|<span data-ttu-id="48d48-196">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-196">String</span></span>|<span data-ttu-id="48d48-197">La directiva de integridad de código que controla la seguridad del entorno de arranque</span><span class="sxs-lookup"><span data-stu-id="48d48-197">The Code Integrity policy that is controlling the security of the boot environment</span></span>|
|<span data-ttu-id="48d48-198">bootRevisionListInfo</span><span class="sxs-lookup"><span data-stu-id="48d48-198">bootRevisionListInfo</span></span>|<span data-ttu-id="48d48-199">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-199">String</span></span>|<span data-ttu-id="48d48-200">La lista de revisión de inicio que se cargó durante el primer inicio en el dispositivo atestiguado</span><span class="sxs-lookup"><span data-stu-id="48d48-200">The Boot Revision List that was loaded during initial boot on the attested device</span></span>|
|<span data-ttu-id="48d48-201">operatingSystemRevListInfo</span><span class="sxs-lookup"><span data-stu-id="48d48-201">operatingSystemRevListInfo</span></span>|<span data-ttu-id="48d48-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-202">String</span></span>|<span data-ttu-id="48d48-203">La lista de revisión del sistema operativo que se cargó durante el primer inicio en el dispositivo atestiguado</span><span class="sxs-lookup"><span data-stu-id="48d48-203">The Operating System Revision List that was loaded during initial boot on the attested device</span></span>|
|<span data-ttu-id="48d48-204">healthStatusMismatchInfo</span><span class="sxs-lookup"><span data-stu-id="48d48-204">healthStatusMismatchInfo</span></span>|<span data-ttu-id="48d48-205">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-205">String</span></span>|<span data-ttu-id="48d48-206">Este atributo aparece si el servicio DHA detecta un problema de integridad</span><span class="sxs-lookup"><span data-stu-id="48d48-206">This attribute appears if DHA-Service detects an integrity issue</span></span>|
|<span data-ttu-id="48d48-207">healthAttestationSupportedStatus</span><span class="sxs-lookup"><span data-stu-id="48d48-207">healthAttestationSupportedStatus</span></span>|<span data-ttu-id="48d48-208">Cadena</span><span class="sxs-lookup"><span data-stu-id="48d48-208">String</span></span>|<span data-ttu-id="48d48-209">Este atributo indica si DHA es compatible con el dispositivo</span><span class="sxs-lookup"><span data-stu-id="48d48-209">This attribute indicates if DHA is supported for the device</span></span>|

## <a name="relationships"></a><span data-ttu-id="48d48-210">Relaciones</span><span class="sxs-lookup"><span data-stu-id="48d48-210">Relationships</span></span>
<span data-ttu-id="48d48-211">Ninguna</span><span class="sxs-lookup"><span data-stu-id="48d48-211">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="48d48-212">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="48d48-212">JSON Representation</span></span>
<span data-ttu-id="48d48-213">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="48d48-213">Here is a JSON representation of the resource.</span></span>
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





