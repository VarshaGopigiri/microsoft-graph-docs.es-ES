---
title: tipo de recurso importedDeviceIdentity
description: El recurso importedDeviceIdentity representa una identidad única de hardware de un dispositivo que se ha almacenado previamente provisionalmente para inscripción previa a la configuración.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6fe03159f79bb1198db80cbba130601614df8865
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966569"
---
# <a name="importeddeviceidentity-resource-type"></a><span data-ttu-id="b4990-103">tipo de recurso importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-103">importedDeviceIdentity resource type</span></span>

> <span data-ttu-id="b4990-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b4990-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b4990-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b4990-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b4990-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b4990-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b4990-107">El recurso importedDeviceIdentity representa una identidad única de hardware de un dispositivo que se ha almacenado previamente provisionalmente para inscripción previa a la configuración.</span><span class="sxs-lookup"><span data-stu-id="b4990-107">The importedDeviceIdentity resource represents a unique hardware identity of a device that has been pre-staged for pre-enrollment configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="b4990-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4990-108">Methods</span></span>
|<span data-ttu-id="b4990-109">Método</span><span class="sxs-lookup"><span data-stu-id="b4990-109">Method</span></span>|<span data-ttu-id="b4990-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4990-110">Return Type</span></span>|<span data-ttu-id="b4990-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4990-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="b4990-112">Lista importedDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="b4990-112">List importedDeviceIdentities</span></span>](../api/intune-enrollment-importeddeviceidentity-list.md)|<span data-ttu-id="b4990-113">colección de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="b4990-113">[importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) collection</span></span>|<span data-ttu-id="b4990-114">Propiedades de la lista y relaciones de los objetos [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="b4990-114">List properties and relationships of the [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) objects.</span></span>|
|[<span data-ttu-id="b4990-115">Obtener importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-115">Get importedDeviceIdentity</span></span>](../api/intune-enrollment-importeddeviceidentity-get.md)|[<span data-ttu-id="b4990-116">importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-116">importedDeviceIdentity</span></span>](../resources/intune-enrollment-importeddeviceidentity.md)|<span data-ttu-id="b4990-117">Leer las propiedades y las relaciones del objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="b4990-117">Read properties and relationships of the [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object.</span></span>|
|[<span data-ttu-id="b4990-118">Crear importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-118">Create importedDeviceIdentity</span></span>](../api/intune-enrollment-importeddeviceidentity-create.md)|[<span data-ttu-id="b4990-119">importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-119">importedDeviceIdentity</span></span>](../resources/intune-enrollment-importeddeviceidentity.md)|<span data-ttu-id="b4990-120">Crear un nuevo objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="b4990-120">Create a new [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object.</span></span>|
|[<span data-ttu-id="b4990-121">Eliminar importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-121">Delete importedDeviceIdentity</span></span>](../api/intune-enrollment-importeddeviceidentity-delete.md)|<span data-ttu-id="b4990-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b4990-122">None</span></span>|<span data-ttu-id="b4990-123">Elimina un [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="b4990-123">Deletes a [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span>|
|[<span data-ttu-id="b4990-124">Actualizar importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-124">Update importedDeviceIdentity</span></span>](../api/intune-enrollment-importeddeviceidentity-update.md)|[<span data-ttu-id="b4990-125">importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="b4990-125">importedDeviceIdentity</span></span>](../resources/intune-enrollment-importeddeviceidentity.md)|<span data-ttu-id="b4990-126">Actualizar las propiedades de un objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="b4990-126">Update the properties of a [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object.</span></span>|
|[<span data-ttu-id="b4990-127">acción importDeviceIdentityList</span><span class="sxs-lookup"><span data-stu-id="b4990-127">importDeviceIdentityList action</span></span>](../api/intune-enrollment-importeddeviceidentity-importdeviceidentitylist.md)|<span data-ttu-id="b4990-128">colección de [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md)</span><span class="sxs-lookup"><span data-stu-id="b4990-128">[importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) collection</span></span>|<span data-ttu-id="b4990-129">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b4990-129">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="b4990-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4990-130">Properties</span></span>
|<span data-ttu-id="b4990-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4990-131">Property</span></span>|<span data-ttu-id="b4990-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4990-132">Type</span></span>|<span data-ttu-id="b4990-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4990-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b4990-134">id</span><span class="sxs-lookup"><span data-stu-id="b4990-134">id</span></span>|<span data-ttu-id="b4990-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4990-135">String</span></span>|<span data-ttu-id="b4990-136">Identificador de la identidad del dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="b4990-136">Id of the imported device identity</span></span>|
|<span data-ttu-id="b4990-137">importedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="b4990-137">importedDeviceIdentifier</span></span>|<span data-ttu-id="b4990-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4990-138">String</span></span>|<span data-ttu-id="b4990-139">Identificador de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="b4990-139">Imported Device Identifier</span></span>|
|<span data-ttu-id="b4990-140">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="b4990-140">importedDeviceIdentityType</span></span>|[<span data-ttu-id="b4990-141">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="b4990-141">importedDeviceIdentityType</span></span>](../resources/intune-enrollment-importeddeviceidentitytype.md)|<span data-ttu-id="b4990-142">Tipo de identidad de dispositivo importada.</span><span class="sxs-lookup"><span data-stu-id="b4990-142">Type of Imported Device Identity.</span></span> <span data-ttu-id="b4990-143">Los valores posibles son: `unknown`, `imei` y `serialNumber`.</span><span class="sxs-lookup"><span data-stu-id="b4990-143">Possible values are: `unknown`, `imei`, `serialNumber`.</span></span>|
|<span data-ttu-id="b4990-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b4990-144">lastModifiedDateTime</span></span>|<span data-ttu-id="b4990-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b4990-145">DateTimeOffset</span></span>|<span data-ttu-id="b4990-146">DateTime última modificación de la descripción</span><span class="sxs-lookup"><span data-stu-id="b4990-146">Last Modified DateTime of the description</span></span>|
|<span data-ttu-id="b4990-147">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b4990-147">createdDateTime</span></span>|<span data-ttu-id="b4990-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b4990-148">DateTimeOffset</span></span>|<span data-ttu-id="b4990-149">Crear fecha hora del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b4990-149">Created Date Time of the device</span></span>|
|<span data-ttu-id="b4990-150">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="b4990-150">lastContactedDateTime</span></span>|<span data-ttu-id="b4990-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b4990-151">DateTimeOffset</span></span>|<span data-ttu-id="b4990-152">Última vez fecha ponerse en contacto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b4990-152">Last Contacted Date Time of the device</span></span>|
|<span data-ttu-id="b4990-153">descripción</span><span class="sxs-lookup"><span data-stu-id="b4990-153">description</span></span>|<span data-ttu-id="b4990-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4990-154">String</span></span>|<span data-ttu-id="b4990-155">La descripción del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b4990-155">The description of the device</span></span>|
|<span data-ttu-id="b4990-156">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="b4990-156">enrollmentState</span></span>|[<span data-ttu-id="b4990-157">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="b4990-157">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="b4990-158">El estado del dispositivo en Intune.</span><span class="sxs-lookup"><span data-stu-id="b4990-158">The state of the device in Intune.</span></span> <span data-ttu-id="b4990-159">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="b4990-159">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="b4990-160">platform</span><span class="sxs-lookup"><span data-stu-id="b4990-160">platform</span></span>|[<span data-ttu-id="b4990-161">plataforma</span><span class="sxs-lookup"><span data-stu-id="b4990-161">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="b4990-162">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4990-162">The platform of the Device.</span></span> <span data-ttu-id="b4990-163">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="b4990-163">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b4990-164">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b4990-164">Relationships</span></span>
<span data-ttu-id="b4990-165">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b4990-165">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b4990-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b4990-166">JSON Representation</span></span>
<span data-ttu-id="b4990-167">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b4990-167">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.importedDeviceIdentity"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedDeviceIdentity",
  "id": "String (identifier)",
  "importedDeviceIdentifier": "String",
  "importedDeviceIdentityType": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "lastContactedDateTime": "String (timestamp)",
  "description": "String",
  "enrollmentState": "String",
  "platform": "String"
}
```





