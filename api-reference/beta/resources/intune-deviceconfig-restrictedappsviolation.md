---
title: tipo de recurso restrictedAppsViolation
description: Infracción de perfil de configuración de aplicaciones restringido por dispositivo por usuario
author: tfitzmac
ms.openlocfilehash: cb614bc56f27281198fcecb73bae2b7beddfa266
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304938"
---
# <a name="restrictedappsviolation-resource-type"></a><span data-ttu-id="26f91-103">tipo de recurso restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-103">restrictedAppsViolation resource type</span></span>

> <span data-ttu-id="26f91-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="26f91-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="26f91-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="26f91-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="26f91-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="26f91-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="26f91-107">Infracción de perfil de configuración de aplicaciones restringido por dispositivo por usuario</span><span class="sxs-lookup"><span data-stu-id="26f91-107">Violation of restricted apps configuration profile per device per user</span></span>
## <a name="methods"></a><span data-ttu-id="26f91-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="26f91-108">Methods</span></span>
|<span data-ttu-id="26f91-109">Método</span><span class="sxs-lookup"><span data-stu-id="26f91-109">Method</span></span>|<span data-ttu-id="26f91-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f91-110">Return Type</span></span>|<span data-ttu-id="26f91-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="26f91-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="26f91-112">Lista restrictedAppsViolations</span><span class="sxs-lookup"><span data-stu-id="26f91-112">List restrictedAppsViolations</span></span>](../api/intune-deviceconfig-restrictedappsviolation-list.md)|<span data-ttu-id="26f91-113">colección de [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md)</span><span class="sxs-lookup"><span data-stu-id="26f91-113">[restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) collection</span></span>|<span data-ttu-id="26f91-114">Propiedades de la lista y relaciones de los objetos [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="26f91-114">List properties and relationships of the [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) objects.</span></span>|
|[<span data-ttu-id="26f91-115">Obtener restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-115">Get restrictedAppsViolation</span></span>](../api/intune-deviceconfig-restrictedappsviolation-get.md)|[<span data-ttu-id="26f91-116">restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-116">restrictedAppsViolation</span></span>](../resources/intune-deviceconfig-restrictedappsviolation.md)|<span data-ttu-id="26f91-117">Leer las propiedades y las relaciones del objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="26f91-117">Read properties and relationships of the [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object.</span></span>|
|[<span data-ttu-id="26f91-118">Crear restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-118">Create restrictedAppsViolation</span></span>](../api/intune-deviceconfig-restrictedappsviolation-create.md)|[<span data-ttu-id="26f91-119">restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-119">restrictedAppsViolation</span></span>](../resources/intune-deviceconfig-restrictedappsviolation.md)|<span data-ttu-id="26f91-120">Crear un nuevo objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="26f91-120">Create a new [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object.</span></span>|
|[<span data-ttu-id="26f91-121">Eliminar restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-121">Delete restrictedAppsViolation</span></span>](../api/intune-deviceconfig-restrictedappsviolation-delete.md)|<span data-ttu-id="26f91-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="26f91-122">None</span></span>|<span data-ttu-id="26f91-123">Elimina un [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md).</span><span class="sxs-lookup"><span data-stu-id="26f91-123">Deletes a [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md).</span></span>|
|[<span data-ttu-id="26f91-124">Actualizar restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-124">Update restrictedAppsViolation</span></span>](../api/intune-deviceconfig-restrictedappsviolation-update.md)|[<span data-ttu-id="26f91-125">restrictedAppsViolation</span><span class="sxs-lookup"><span data-stu-id="26f91-125">restrictedAppsViolation</span></span>](../resources/intune-deviceconfig-restrictedappsviolation.md)|<span data-ttu-id="26f91-126">Actualizar las propiedades de un objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .</span><span class="sxs-lookup"><span data-stu-id="26f91-126">Update the properties of a [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="26f91-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26f91-127">Properties</span></span>
|<span data-ttu-id="26f91-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26f91-128">Property</span></span>|<span data-ttu-id="26f91-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="26f91-129">Type</span></span>|<span data-ttu-id="26f91-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="26f91-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="26f91-131">id</span><span class="sxs-lookup"><span data-stu-id="26f91-131">id</span></span>|<span data-ttu-id="26f91-132">String</span><span class="sxs-lookup"><span data-stu-id="26f91-132">String</span></span>|<span data-ttu-id="26f91-133">Identificador único para el objeto.</span><span class="sxs-lookup"><span data-stu-id="26f91-133">Unique identifier for the object.</span></span> <span data-ttu-id="26f91-134">Creados a partir de accountId, deviceId, Id. de directiva y userId</span><span class="sxs-lookup"><span data-stu-id="26f91-134">Composed from accountId, deviceId, policyId and userId</span></span>|
|<span data-ttu-id="26f91-135">userId</span><span class="sxs-lookup"><span data-stu-id="26f91-135">userId</span></span>|<span data-ttu-id="26f91-136">String</span><span class="sxs-lookup"><span data-stu-id="26f91-136">String</span></span>|<span data-ttu-id="26f91-137">Identificador único del usuario, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="26f91-137">User unique identifier, must be Guid</span></span>|
|<span data-ttu-id="26f91-138">userName</span><span class="sxs-lookup"><span data-stu-id="26f91-138">userName</span></span>|<span data-ttu-id="26f91-139">String</span><span class="sxs-lookup"><span data-stu-id="26f91-139">String</span></span>|<span data-ttu-id="26f91-140">Nombre de usuario</span><span class="sxs-lookup"><span data-stu-id="26f91-140">User name</span></span>|
|<span data-ttu-id="26f91-141">managedDeviceId</span><span class="sxs-lookup"><span data-stu-id="26f91-141">managedDeviceId</span></span>|<span data-ttu-id="26f91-142">String</span><span class="sxs-lookup"><span data-stu-id="26f91-142">String</span></span>|<span data-ttu-id="26f91-143">Identificador único de dispositivos administrados, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="26f91-143">Managed device unique identifier, must be Guid</span></span>|
|<span data-ttu-id="26f91-144">deviceName</span><span class="sxs-lookup"><span data-stu-id="26f91-144">deviceName</span></span>|<span data-ttu-id="26f91-145">String</span><span class="sxs-lookup"><span data-stu-id="26f91-145">String</span></span>|<span data-ttu-id="26f91-146">Nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="26f91-146">Device name</span></span>|
|<span data-ttu-id="26f91-147">deviceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="26f91-147">deviceConfigurationId</span></span>|<span data-ttu-id="26f91-148">String</span><span class="sxs-lookup"><span data-stu-id="26f91-148">String</span></span>|<span data-ttu-id="26f91-149">Identificador único de dispositivo configuración perfil, debe ser el Guid</span><span class="sxs-lookup"><span data-stu-id="26f91-149">Device configuration profile unique identifier, must be Guid</span></span>|
|<span data-ttu-id="26f91-150">deviceConfigurationName</span><span class="sxs-lookup"><span data-stu-id="26f91-150">deviceConfigurationName</span></span>|<span data-ttu-id="26f91-151">String</span><span class="sxs-lookup"><span data-stu-id="26f91-151">String</span></span>|<span data-ttu-id="26f91-152">Nombre del perfil de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="26f91-152">Device configuration profile name</span></span>|
|<span data-ttu-id="26f91-153">platformType</span><span class="sxs-lookup"><span data-stu-id="26f91-153">platformType</span></span>|[<span data-ttu-id="26f91-154">policyPlatformType</span><span class="sxs-lookup"><span data-stu-id="26f91-154">policyPlatformType</span></span>](../resources/intune-deviceconfig-policyplatformtype.md)|<span data-ttu-id="26f91-155">Tipo de plataforma.</span><span class="sxs-lookup"><span data-stu-id="26f91-155">Platform type.</span></span> <span data-ttu-id="26f91-156">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.</span><span class="sxs-lookup"><span data-stu-id="26f91-156">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `all`.</span></span>|
|<span data-ttu-id="26f91-157">restrictedAppsState</span><span class="sxs-lookup"><span data-stu-id="26f91-157">restrictedAppsState</span></span>|[<span data-ttu-id="26f91-158">restrictedAppsState</span><span class="sxs-lookup"><span data-stu-id="26f91-158">restrictedAppsState</span></span>](../resources/intune-deviceconfig-restrictedappsstate.md)|<span data-ttu-id="26f91-159">Estado de aplicaciones restringidos.</span><span class="sxs-lookup"><span data-stu-id="26f91-159">Restricted apps state.</span></span> <span data-ttu-id="26f91-160">Los valores posibles son: `prohibitedApps` y `notApprovedApps`.</span><span class="sxs-lookup"><span data-stu-id="26f91-160">Possible values are: `prohibitedApps`, `notApprovedApps`.</span></span>|
|<span data-ttu-id="26f91-161">restrictedApps</span><span class="sxs-lookup"><span data-stu-id="26f91-161">restrictedApps</span></span>|<span data-ttu-id="26f91-162">colección de [managedDeviceReportedApp](../resources/intune-deviceconfig-manageddevicereportedapp.md)</span><span class="sxs-lookup"><span data-stu-id="26f91-162">[managedDeviceReportedApp](../resources/intune-deviceconfig-manageddevicereportedapp.md) collection</span></span>|<span data-ttu-id="26f91-163">Lista de aplicaciones restringidas infringidas</span><span class="sxs-lookup"><span data-stu-id="26f91-163">List of violated restricted apps</span></span>|

## <a name="relationships"></a><span data-ttu-id="26f91-164">Relaciones</span><span class="sxs-lookup"><span data-stu-id="26f91-164">Relationships</span></span>
<span data-ttu-id="26f91-165">Ninguna</span><span class="sxs-lookup"><span data-stu-id="26f91-165">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="26f91-166">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26f91-166">JSON Representation</span></span>
<span data-ttu-id="26f91-167">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="26f91-167">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.restrictedAppsViolation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.restrictedAppsViolation",
  "id": "String (identifier)",
  "userId": "String",
  "userName": "String",
  "managedDeviceId": "String",
  "deviceName": "String",
  "deviceConfigurationId": "String",
  "deviceConfigurationName": "String",
  "platformType": "String",
  "restrictedAppsState": "String",
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.managedDeviceReportedApp",
      "appId": "String"
    }
  ]
}
```





