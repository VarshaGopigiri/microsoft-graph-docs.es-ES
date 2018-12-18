---
title: tipo de recurso officeClientConfiguration
description: Configuración de cliente de Office.
author: tfitzmac
ms.openlocfilehash: 67a7845a2e0327e2e5de37d424274f6e2ee35604
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303839"
---
# <a name="officeclientconfiguration-resource-type"></a><span data-ttu-id="42864-103">tipo de recurso officeClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="42864-103">officeClientConfiguration resource type</span></span>

> <span data-ttu-id="42864-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="42864-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="42864-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="42864-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="42864-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="42864-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="42864-107">Configuración de cliente de Office.</span><span class="sxs-lookup"><span data-stu-id="42864-107">Office Client Configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="42864-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="42864-108">Methods</span></span>
|<span data-ttu-id="42864-109">Método</span><span class="sxs-lookup"><span data-stu-id="42864-109">Method</span></span>|<span data-ttu-id="42864-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42864-110">Return Type</span></span>|<span data-ttu-id="42864-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="42864-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="42864-112">Lista officeClientConfigurations</span><span class="sxs-lookup"><span data-stu-id="42864-112">List officeClientConfigurations</span></span>](../api/intune-cirrus-officeclientconfiguration-list.md)|<span data-ttu-id="42864-113">colección de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="42864-113">[officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) collection</span></span>|<span data-ttu-id="42864-114">Propiedades de la lista y relaciones de los objetos [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="42864-114">List properties and relationships of the [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="42864-115">Obtener officeClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="42864-115">Get officeClientConfiguration</span></span>](../api/intune-cirrus-officeclientconfiguration-get.md)|[<span data-ttu-id="42864-116">officeClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="42864-116">officeClientConfiguration</span></span>](../resources/intune-cirrus-officeclientconfiguration.md)|<span data-ttu-id="42864-117">Leer las propiedades y las relaciones del objeto [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="42864-117">Read properties and relationships of the [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) object.</span></span>|
|[<span data-ttu-id="42864-118">Acción assign</span><span class="sxs-lookup"><span data-stu-id="42864-118">assign action</span></span>](../api/intune-cirrus-officeclientconfiguration-assign.md)|<span data-ttu-id="42864-119">colección de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="42864-119">[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) collection</span></span>|<span data-ttu-id="42864-120">Reemplazar todos los grupos para una directiva.</span><span class="sxs-lookup"><span data-stu-id="42864-120">Replace all targeted groups for a policy.</span></span>|
|[<span data-ttu-id="42864-121">acción updatePriorities</span><span class="sxs-lookup"><span data-stu-id="42864-121">updatePriorities action</span></span>](../api/intune-cirrus-officeclientconfiguration-updatepriorities.md)|<span data-ttu-id="42864-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="42864-122">None</span></span>|<span data-ttu-id="42864-123">Actualizar las prioridades de directiva.</span><span class="sxs-lookup"><span data-stu-id="42864-123">Update policy priorities.</span></span>|

## <a name="properties"></a><span data-ttu-id="42864-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42864-124">Properties</span></span>
|<span data-ttu-id="42864-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42864-125">Property</span></span>|<span data-ttu-id="42864-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="42864-126">Type</span></span>|<span data-ttu-id="42864-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="42864-127">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="42864-128">id</span><span class="sxs-lookup"><span data-stu-id="42864-128">id</span></span>|<span data-ttu-id="42864-129">String</span><span class="sxs-lookup"><span data-stu-id="42864-129">String</span></span>|<span data-ttu-id="42864-130">Identificador de la directiva de configuración de cliente de office.</span><span class="sxs-lookup"><span data-stu-id="42864-130">Id of the office client configuration policy.</span></span>|
|<span data-ttu-id="42864-131">userPreferencePayload</span><span class="sxs-lookup"><span data-stu-id="42864-131">userPreferencePayload</span></span>|<span data-ttu-id="42864-132">Stream</span><span class="sxs-lookup"><span data-stu-id="42864-132">Stream</span></span>|<span data-ttu-id="42864-133">Configuración de preferencias de JSON de cadenas en formato binario, estos valores pueden ser anulados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="42864-133">Preference settings JSON string in binary format, these values can be overridden by the user.</span></span>|
|<span data-ttu-id="42864-134">policyPayload</span><span class="sxs-lookup"><span data-stu-id="42864-134">policyPayload</span></span>|<span data-ttu-id="42864-135">Stream</span><span class="sxs-lookup"><span data-stu-id="42864-135">Stream</span></span>|<span data-ttu-id="42864-136">Configuración de la directiva JSON de cadenas en formato binario, no se puede cambiar estos valores por el usuario.</span><span class="sxs-lookup"><span data-stu-id="42864-136">Policy settings JSON string in binary format, these values cannot be changed by the user.</span></span>|
|<span data-ttu-id="42864-137">descripción</span><span class="sxs-lookup"><span data-stu-id="42864-137">description</span></span>|<span data-ttu-id="42864-138">String</span><span class="sxs-lookup"><span data-stu-id="42864-138">String</span></span>|<span data-ttu-id="42864-139">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="42864-139">Not yet documented</span></span>|
|<span data-ttu-id="42864-140">displayName</span><span class="sxs-lookup"><span data-stu-id="42864-140">displayName</span></span>|<span data-ttu-id="42864-141">String</span><span class="sxs-lookup"><span data-stu-id="42864-141">String</span></span>|<span data-ttu-id="42864-142">Administración descripción proporcionada por el del cliente de office de directiva de configuración.</span><span class="sxs-lookup"><span data-stu-id="42864-142">Admin provided description of the office client configuration policy.</span></span>|
|<span data-ttu-id="42864-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="42864-143">lastModifiedDateTime</span></span>|<span data-ttu-id="42864-144">DateTime</span><span class="sxs-lookup"><span data-stu-id="42864-144">DateTime</span></span>|<span data-ttu-id="42864-145">Última marca de datetime modificada de la directiva.</span><span class="sxs-lookup"><span data-stu-id="42864-145">Last modified datetime stamp of the policy.</span></span>|
|<span data-ttu-id="42864-146">prioridad</span><span class="sxs-lookup"><span data-stu-id="42864-146">priority</span></span>|<span data-ttu-id="42864-147">Int32</span><span class="sxs-lookup"><span data-stu-id="42864-147">Int32</span></span>|<span data-ttu-id="42864-148">Valor de prioridad debe ser un valor único para cada directiva de un inquilino y se usará para la resolución de conflictos, los valores más bajos significan prioridad sea alta.</span><span class="sxs-lookup"><span data-stu-id="42864-148">Priority value should be unique value for each policy under a tenant and will be used for conflict resolution, lower values mean priority is high.</span></span>|
|<span data-ttu-id="42864-149">userCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="42864-149">userCheckinSummary</span></span>|[<span data-ttu-id="42864-150">officeUserCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="42864-150">officeUserCheckinSummary</span></span>](../resources/intune-cirrus-officeusercheckinsummary.md)|<span data-ttu-id="42864-151">Protección de resumen de usuario para la directiva.</span><span class="sxs-lookup"><span data-stu-id="42864-151">User check-in summary for the policy.</span></span>|
|<span data-ttu-id="42864-152">checkinStatuses</span><span class="sxs-lookup"><span data-stu-id="42864-152">checkinStatuses</span></span>|<span data-ttu-id="42864-153">colección de [officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)</span><span class="sxs-lookup"><span data-stu-id="42864-153">[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md) collection</span></span>|<span data-ttu-id="42864-154">Lista de comprobación de estado del cliente de office.</span><span class="sxs-lookup"><span data-stu-id="42864-154">List of office Client check-in status.</span></span>|

## <a name="relationships"></a><span data-ttu-id="42864-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="42864-155">Relationships</span></span>
|<span data-ttu-id="42864-156">Relación</span><span class="sxs-lookup"><span data-stu-id="42864-156">Relationship</span></span>|<span data-ttu-id="42864-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="42864-157">Type</span></span>|<span data-ttu-id="42864-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="42864-158">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="42864-159">asignaciones</span><span class="sxs-lookup"><span data-stu-id="42864-159">assignments</span></span>|<span data-ttu-id="42864-160">colección de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="42864-160">[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) collection</span></span>|<span data-ttu-id="42864-161">La lista de las asignaciones de grupo para la directiva.</span><span class="sxs-lookup"><span data-stu-id="42864-161">The list of group assignments for the policy.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="42864-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="42864-162">JSON Representation</span></span>
<span data-ttu-id="42864-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="42864-163">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeClientConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeClientConfiguration",
  "id": "String (identifier)",
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "String",
  "displayName": "String",
  "priority": 1024,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 1024,
    "failedUserCount": 1024
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "String",
      "deviceName": "String",
      "devicePlatform": "String",
      "devicePlatformVersion": "String",
      "wasSuccessful": true,
      "userId": "String",
      "checkinDateTime": "String (timestamp)",
      "errorMessage": "String",
      "appliedPolicies": [
        "String"
      ]
    }
  ]
}
```



