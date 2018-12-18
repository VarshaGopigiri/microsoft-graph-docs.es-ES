---
title: tipo de recurso hardwareInformation
description: Información de hardware de un dispositivo determinado.
author: tfitzmac
ms.openlocfilehash: c483aa800d920a50392d21c326cd20dea7b72e18
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334527"
---
# <a name="hardwareinformation-resource-type"></a><span data-ttu-id="d9d39-103">tipo de recurso hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="d9d39-103">hardwareInformation resource type</span></span>

> <span data-ttu-id="d9d39-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d9d39-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d9d39-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d9d39-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d9d39-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d9d39-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d9d39-107">Información de hardware de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="d9d39-107">Hardware information of a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="d9d39-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9d39-108">Properties</span></span>
|<span data-ttu-id="d9d39-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9d39-109">Property</span></span>|<span data-ttu-id="d9d39-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9d39-110">Type</span></span>|<span data-ttu-id="d9d39-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d39-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d9d39-112">serialNumber</span><span class="sxs-lookup"><span data-stu-id="d9d39-112">serialNumber</span></span>|<span data-ttu-id="d9d39-113">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-113">String</span></span>|<span data-ttu-id="d9d39-114">Número de serie.</span><span class="sxs-lookup"><span data-stu-id="d9d39-114">Serial number.</span></span>|
|<span data-ttu-id="d9d39-115">totalStorageSpace</span><span class="sxs-lookup"><span data-stu-id="d9d39-115">totalStorageSpace</span></span>|<span data-ttu-id="d9d39-116">Int64</span><span class="sxs-lookup"><span data-stu-id="d9d39-116">Int64</span></span>|<span data-ttu-id="d9d39-117">Espacio de almacenamiento total del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9d39-117">Total storage space of the device.</span></span>|
|<span data-ttu-id="d9d39-118">freeStorageSpace</span><span class="sxs-lookup"><span data-stu-id="d9d39-118">freeStorageSpace</span></span>|<span data-ttu-id="d9d39-119">Int64</span><span class="sxs-lookup"><span data-stu-id="d9d39-119">Int64</span></span>|<span data-ttu-id="d9d39-120">Espacio de almacenamiento libre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9d39-120">Free storage space of the device.</span></span>|
|<span data-ttu-id="d9d39-121">imei</span><span class="sxs-lookup"><span data-stu-id="d9d39-121">imei</span></span>|<span data-ttu-id="d9d39-122">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-122">String</span></span>|<span data-ttu-id="d9d39-123">IMEI</span><span class="sxs-lookup"><span data-stu-id="d9d39-123">IMEI</span></span>|
|<span data-ttu-id="d9d39-124">meid</span><span class="sxs-lookup"><span data-stu-id="d9d39-124">meid</span></span>|<span data-ttu-id="d9d39-125">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-125">String</span></span>|<span data-ttu-id="d9d39-126">MEID</span><span class="sxs-lookup"><span data-stu-id="d9d39-126">MEID</span></span>|
|<span data-ttu-id="d9d39-127">manufacturer</span><span class="sxs-lookup"><span data-stu-id="d9d39-127">manufacturer</span></span>|<span data-ttu-id="d9d39-128">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-128">String</span></span>|<span data-ttu-id="d9d39-129">Fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9d39-129">Manufacturer of the device</span></span>|
|<span data-ttu-id="d9d39-130">model</span><span class="sxs-lookup"><span data-stu-id="d9d39-130">model</span></span>|<span data-ttu-id="d9d39-131">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-131">String</span></span>|<span data-ttu-id="d9d39-132">Modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9d39-132">Model of the device</span></span>|
|<span data-ttu-id="d9d39-133">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="d9d39-133">phoneNumber</span></span>|<span data-ttu-id="d9d39-134">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-134">String</span></span>|<span data-ttu-id="d9d39-135">Número de teléfono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9d39-135">Phone number of the device</span></span>|
|<span data-ttu-id="d9d39-136">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="d9d39-136">subscriberCarrier</span></span>|<span data-ttu-id="d9d39-137">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-137">String</span></span>|<span data-ttu-id="d9d39-138">Operador de suscriptor del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9d39-138">Subscriber carrier of the device</span></span>|
|<span data-ttu-id="d9d39-139">cellularTechnology</span><span class="sxs-lookup"><span data-stu-id="d9d39-139">cellularTechnology</span></span>|<span data-ttu-id="d9d39-140">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-140">String</span></span>|<span data-ttu-id="d9d39-141">Tecnología de telefonía móvil del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9d39-141">Cellular technology of the device</span></span>|
|<span data-ttu-id="d9d39-142">wifiMac</span><span class="sxs-lookup"><span data-stu-id="d9d39-142">wifiMac</span></span>|<span data-ttu-id="d9d39-143">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-143">String</span></span>|<span data-ttu-id="d9d39-144">Dirección MAC de WiFi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9d39-144">WiFi MAC address of the device</span></span>|
|<span data-ttu-id="d9d39-145">operatingSystemLanguage</span><span class="sxs-lookup"><span data-stu-id="d9d39-145">operatingSystemLanguage</span></span>|<span data-ttu-id="d9d39-146">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-146">String</span></span>|<span data-ttu-id="d9d39-147">Idioma del sistema operativo del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9d39-147">Operating system language of the device</span></span>|
|<span data-ttu-id="d9d39-148">isSupervised</span><span class="sxs-lookup"><span data-stu-id="d9d39-148">isSupervised</span></span>|<span data-ttu-id="d9d39-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="d9d39-149">Boolean</span></span>|<span data-ttu-id="d9d39-150">Modo de supervisión del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9d39-150">Supervised mode of the device</span></span>|
|<span data-ttu-id="d9d39-151">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="d9d39-151">isEncrypted</span></span>|<span data-ttu-id="d9d39-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="d9d39-152">Boolean</span></span>|<span data-ttu-id="d9d39-153">Estado de cifrado del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9d39-153">Encryption status of the device</span></span>|
|<span data-ttu-id="d9d39-154">isSharedDevice</span><span class="sxs-lookup"><span data-stu-id="d9d39-154">isSharedDevice</span></span>|<span data-ttu-id="d9d39-155">Boolean</span><span class="sxs-lookup"><span data-stu-id="d9d39-155">Boolean</span></span>|<span data-ttu-id="d9d39-156">IPad compartida</span><span class="sxs-lookup"><span data-stu-id="d9d39-156">Shared iPad</span></span>|
|<span data-ttu-id="d9d39-157">sharedDeviceCachedUsers</span><span class="sxs-lookup"><span data-stu-id="d9d39-157">sharedDeviceCachedUsers</span></span>|<span data-ttu-id="d9d39-158">colección de [sharedAppleDeviceUser](../resources/intune-devices-sharedappledeviceuser.md)</span><span class="sxs-lookup"><span data-stu-id="d9d39-158">[sharedAppleDeviceUser](../resources/intune-devices-sharedappledeviceuser.md) collection</span></span>|<span data-ttu-id="d9d39-159">Todos los usuarios en el dispositivo de Apple compartido</span><span class="sxs-lookup"><span data-stu-id="d9d39-159">All users on the shared Apple device</span></span>|
|<span data-ttu-id="d9d39-160">tpmSpecificationVersion</span><span class="sxs-lookup"><span data-stu-id="d9d39-160">tpmSpecificationVersion</span></span>|<span data-ttu-id="d9d39-161">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-161">String</span></span>|<span data-ttu-id="d9d39-162">Cadena que especifica la versión de la especificación.</span><span class="sxs-lookup"><span data-stu-id="d9d39-162">String that specifies the specification version.</span></span>|
|<span data-ttu-id="d9d39-163">operatingSystemEdition</span><span class="sxs-lookup"><span data-stu-id="d9d39-163">operatingSystemEdition</span></span>|<span data-ttu-id="d9d39-164">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-164">String</span></span>|<span data-ttu-id="d9d39-165">Cadena que especifica la edición del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d9d39-165">String that specifies the OS edition.</span></span>|
|<span data-ttu-id="d9d39-166">deviceFullQualifiedDomainName</span><span class="sxs-lookup"><span data-stu-id="d9d39-166">deviceFullQualifiedDomainName</span></span>|<span data-ttu-id="d9d39-167">String</span><span class="sxs-lookup"><span data-stu-id="d9d39-167">String</span></span>|<span data-ttu-id="d9d39-168">Devuelve el nombre de dominio completo del dispositivo (si hay alguno).</span><span class="sxs-lookup"><span data-stu-id="d9d39-168">Returns the fully qualified domain name of the device (if any).</span></span> <span data-ttu-id="d9d39-169">Si el dispositivo no está unido a un dominio, devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="d9d39-169">If the device is not domain-joined, it returns an empty string.</span></span> |
|<span data-ttu-id="d9d39-170">deviceGuardVirtualizationBasedSecurityHardwareRequirementState</span><span class="sxs-lookup"><span data-stu-id="d9d39-170">deviceGuardVirtualizationBasedSecurityHardwareRequirementState</span></span>|[<span data-ttu-id="d9d39-171">deviceGuardVirtualizationBasedSecurityHardwareRequirementState</span><span class="sxs-lookup"><span data-stu-id="d9d39-171">deviceGuardVirtualizationBasedSecurityHardwareRequirementState</span></span>](../resources/intune-devices-deviceguardvirtualizationbasedsecurityhardwarerequirementstate.md)|<span data-ttu-id="d9d39-172">Estado de requisitos de hardware de seguridad basada en la virtualización.</span><span class="sxs-lookup"><span data-stu-id="d9d39-172">Virtualization-based security hardware requirement status.</span></span> <span data-ttu-id="d9d39-173">Los valores posibles son: `meetHardwareRequirements`, `secureBootRequired`, `dmaProtectionRequired`, `hyperVNotSupportedForGuestVM` y `hyperVNotAvailable`.</span><span class="sxs-lookup"><span data-stu-id="d9d39-173">Possible values are: `meetHardwareRequirements`, `secureBootRequired`, `dmaProtectionRequired`, `hyperVNotSupportedForGuestVM`, `hyperVNotAvailable`.</span></span>|
|<span data-ttu-id="d9d39-174">deviceGuardVirtualizationBasedSecurityState</span><span class="sxs-lookup"><span data-stu-id="d9d39-174">deviceGuardVirtualizationBasedSecurityState</span></span>|[<span data-ttu-id="d9d39-175">deviceGuardVirtualizationBasedSecurityState</span><span class="sxs-lookup"><span data-stu-id="d9d39-175">deviceGuardVirtualizationBasedSecurityState</span></span>](../resources/intune-devices-deviceguardvirtualizationbasedsecuritystate.md)|<span data-ttu-id="d9d39-176">Estado de la seguridad basada en la virtualización.</span><span class="sxs-lookup"><span data-stu-id="d9d39-176">Virtualization-based security status.</span></span> <span data-ttu-id="d9d39-177">.</span><span class="sxs-lookup"><span data-stu-id="d9d39-177"></span></span> <span data-ttu-id="d9d39-178">Los valores posibles son: `running`, `rebootRequired`, `require64BitArchitecture`, `notLicensed`, `notConfigured`, `doesNotMeetHardwareRequirements` y `other`.</span><span class="sxs-lookup"><span data-stu-id="d9d39-178">Possible values are: `running`, `rebootRequired`, `require64BitArchitecture`, `notLicensed`, `notConfigured`, `doesNotMeetHardwareRequirements`, `other`.</span></span>|
|<span data-ttu-id="d9d39-179">deviceGuardLocalSystemAuthorityCredentialGuardState</span><span class="sxs-lookup"><span data-stu-id="d9d39-179">deviceGuardLocalSystemAuthorityCredentialGuardState</span></span>|[<span data-ttu-id="d9d39-180">deviceGuardLocalSystemAuthorityCredentialGuardState</span><span class="sxs-lookup"><span data-stu-id="d9d39-180">deviceGuardLocalSystemAuthorityCredentialGuardState</span></span>](../resources/intune-devices-deviceguardlocalsystemauthoritycredentialguardstate.md)|<span data-ttu-id="d9d39-181">Estado de guard de credencial de autoridad del sistema (LSA) local.</span><span class="sxs-lookup"><span data-stu-id="d9d39-181">Local System Authority (LSA) credential guard status.</span></span> <span data-ttu-id="d9d39-182">.</span><span class="sxs-lookup"><span data-stu-id="d9d39-182"></span></span> <span data-ttu-id="d9d39-183">Los valores posibles son: `running`, `rebootRequired`, `notLicensed`, `notConfigured` y `virtualizationBasedSecurityNotRunning`.</span><span class="sxs-lookup"><span data-stu-id="d9d39-183">Possible values are: `running`, `rebootRequired`, `notLicensed`, `notConfigured`, `virtualizationBasedSecurityNotRunning`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d9d39-184">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d9d39-184">Relationships</span></span>
<span data-ttu-id="d9d39-185">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d9d39-185">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d9d39-186">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9d39-186">JSON Representation</span></span>
<span data-ttu-id="d9d39-187">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d9d39-187">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.hardwareInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.hardwareInformation",
  "serialNumber": "String",
  "totalStorageSpace": 1024,
  "freeStorageSpace": 1024,
  "imei": "String",
  "meid": "String",
  "manufacturer": "String",
  "model": "String",
  "phoneNumber": "String",
  "subscriberCarrier": "String",
  "cellularTechnology": "String",
  "wifiMac": "String",
  "operatingSystemLanguage": "String",
  "isSupervised": true,
  "isEncrypted": true,
  "isSharedDevice": true,
  "sharedDeviceCachedUsers": [
    {
      "@odata.type": "microsoft.graph.sharedAppleDeviceUser",
      "userPrincipalName": "String",
      "dataToSync": true,
      "dataQuota": 1024,
      "dataUsed": 1024
    }
  ],
  "tpmSpecificationVersion": "String",
  "operatingSystemEdition": "String",
  "deviceFullQualifiedDomainName": "String",
  "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "String",
  "deviceGuardVirtualizationBasedSecurityState": "String",
  "deviceGuardLocalSystemAuthorityCredentialGuardState": "String"
}
```





