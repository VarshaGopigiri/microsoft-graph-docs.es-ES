---
title: Tipo de recurso deviceCompliancePolicySettingState
description: Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.
author: tfitzmac
ms.openlocfilehash: 3dcd63327a3518314619cd7add6ac6f23e69396b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27320373"
---
# <a name="devicecompliancepolicysettingstate-resource-type"></a><span data-ttu-id="35231-103">Tipo de recurso deviceCompliancePolicySettingState</span><span class="sxs-lookup"><span data-stu-id="35231-103">deviceCompliancePolicySettingState resource type</span></span>

> <span data-ttu-id="35231-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="35231-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="35231-105">Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="35231-105">Device Compilance Policy Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="35231-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35231-106">Properties</span></span>
|<span data-ttu-id="35231-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="35231-107">Property</span></span>|<span data-ttu-id="35231-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="35231-108">Type</span></span>|<span data-ttu-id="35231-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="35231-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="35231-110">ajustes</span><span class="sxs-lookup"><span data-stu-id="35231-110">setting</span></span>|<span data-ttu-id="35231-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-111">String</span></span>|<span data-ttu-id="35231-112">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="35231-112">The setting that is being reported</span></span>|
|<span data-ttu-id="35231-113">settingName</span><span class="sxs-lookup"><span data-stu-id="35231-113">settingName</span></span>|<span data-ttu-id="35231-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-114">String</span></span>|<span data-ttu-id="35231-115">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="35231-115">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="35231-116">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="35231-116">instanceDisplayName</span></span>|<span data-ttu-id="35231-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-117">String</span></span>|<span data-ttu-id="35231-118">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="35231-118">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="35231-119">estado</span><span class="sxs-lookup"><span data-stu-id="35231-119">state</span></span>|[<span data-ttu-id="35231-120">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="35231-120">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="35231-121">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="35231-121">The compliance state of the setting.</span></span> <span data-ttu-id="35231-122">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="35231-122">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="35231-123">errorCode</span><span class="sxs-lookup"><span data-stu-id="35231-123">errorCode</span></span>|<span data-ttu-id="35231-124">Int64</span><span class="sxs-lookup"><span data-stu-id="35231-124">Int64</span></span>|<span data-ttu-id="35231-125">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="35231-125">Error code for the setting</span></span>|
|<span data-ttu-id="35231-126">errorDescription</span><span class="sxs-lookup"><span data-stu-id="35231-126">errorDescription</span></span>|<span data-ttu-id="35231-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-127">String</span></span>|<span data-ttu-id="35231-128">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="35231-128">Error description</span></span>|
|<span data-ttu-id="35231-129">userId</span><span class="sxs-lookup"><span data-stu-id="35231-129">userId</span></span>|<span data-ttu-id="35231-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-130">String</span></span>|<span data-ttu-id="35231-131">UserId</span><span class="sxs-lookup"><span data-stu-id="35231-131">UserId</span></span>|
|<span data-ttu-id="35231-132">userName</span><span class="sxs-lookup"><span data-stu-id="35231-132">userName</span></span>|<span data-ttu-id="35231-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-133">String</span></span>|<span data-ttu-id="35231-134">UserName</span><span class="sxs-lookup"><span data-stu-id="35231-134">UserName</span></span>|
|<span data-ttu-id="35231-135">userEmail</span><span class="sxs-lookup"><span data-stu-id="35231-135">userEmail</span></span>|<span data-ttu-id="35231-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-136">String</span></span>|<span data-ttu-id="35231-137">UserEmail</span><span class="sxs-lookup"><span data-stu-id="35231-137">UserEmail</span></span>|
|<span data-ttu-id="35231-138">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="35231-138">userPrincipalName</span></span>|<span data-ttu-id="35231-139">String</span><span class="sxs-lookup"><span data-stu-id="35231-139">String</span></span>|<span data-ttu-id="35231-140">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="35231-140">UserPrincipalName.</span></span>|
|<span data-ttu-id="35231-141">orígenes</span><span class="sxs-lookup"><span data-stu-id="35231-141">sources</span></span>|<span data-ttu-id="35231-142">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="35231-142">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="35231-143">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="35231-143">Contributing policies</span></span>|
|<span data-ttu-id="35231-144">currentValue</span><span class="sxs-lookup"><span data-stu-id="35231-144">currentValue</span></span>|<span data-ttu-id="35231-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="35231-145">String</span></span>|<span data-ttu-id="35231-146">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="35231-146">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="35231-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="35231-147">Relationships</span></span>
<span data-ttu-id="35231-148">Ninguna</span><span class="sxs-lookup"><span data-stu-id="35231-148">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="35231-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="35231-149">JSON Representation</span></span>
<span data-ttu-id="35231-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="35231-150">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceCompliancePolicySettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingState",
  "setting": "String",
  "settingName": "String",
  "instanceDisplayName": "String",
  "state": "String",
  "errorCode": 1024,
  "errorDescription": "String",
  "userId": "String",
  "userName": "String",
  "userEmail": "String",
  "userPrincipalName": "String",
  "sources": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "String",
      "displayName": "String"
    }
  ],
  "currentValue": "String"
}
```



