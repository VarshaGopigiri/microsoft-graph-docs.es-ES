---
title: Tipo de recurso deviceCompliancePolicySettingState
description: Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.
ms.openlocfilehash: 6f0cdbc6ae1e6e1da97bb82f87d235c6d97fd678
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030338"
---
# <a name="devicecompliancepolicysettingstate-resource-type"></a><span data-ttu-id="5fbed-103">Tipo de recurso deviceCompliancePolicySettingState</span><span class="sxs-lookup"><span data-stu-id="5fbed-103">deviceCompliancePolicySettingState resource type</span></span>

> <span data-ttu-id="5fbed-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5fbed-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5fbed-105">Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="5fbed-105">Device Compilance Policy Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="5fbed-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5fbed-106">Properties</span></span>
|<span data-ttu-id="5fbed-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5fbed-107">Property</span></span>|<span data-ttu-id="5fbed-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fbed-108">Type</span></span>|<span data-ttu-id="5fbed-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fbed-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5fbed-110">ajustes</span><span class="sxs-lookup"><span data-stu-id="5fbed-110">setting</span></span>|<span data-ttu-id="5fbed-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-111">String</span></span>|<span data-ttu-id="5fbed-112">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5fbed-112">The setting that is being reported</span></span>|
|<span data-ttu-id="5fbed-113">settingName</span><span class="sxs-lookup"><span data-stu-id="5fbed-113">settingName</span></span>|<span data-ttu-id="5fbed-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-114">String</span></span>|<span data-ttu-id="5fbed-115">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5fbed-115">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="5fbed-116">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="5fbed-116">instanceDisplayName</span></span>|<span data-ttu-id="5fbed-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-117">String</span></span>|<span data-ttu-id="5fbed-118">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="5fbed-118">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="5fbed-119">estado</span><span class="sxs-lookup"><span data-stu-id="5fbed-119">state</span></span>|[<span data-ttu-id="5fbed-120">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="5fbed-120">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="5fbed-121">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="5fbed-121">The compliance state of the setting.</span></span> <span data-ttu-id="5fbed-122">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="5fbed-122">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="5fbed-123">errorCode</span><span class="sxs-lookup"><span data-stu-id="5fbed-123">errorCode</span></span>|<span data-ttu-id="5fbed-124">Int64</span><span class="sxs-lookup"><span data-stu-id="5fbed-124">Int64</span></span>|<span data-ttu-id="5fbed-125">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="5fbed-125">Error code for the setting</span></span>|
|<span data-ttu-id="5fbed-126">errorDescription</span><span class="sxs-lookup"><span data-stu-id="5fbed-126">errorDescription</span></span>|<span data-ttu-id="5fbed-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-127">String</span></span>|<span data-ttu-id="5fbed-128">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="5fbed-128">Error description</span></span>|
|<span data-ttu-id="5fbed-129">userId</span><span class="sxs-lookup"><span data-stu-id="5fbed-129">userId</span></span>|<span data-ttu-id="5fbed-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-130">String</span></span>|<span data-ttu-id="5fbed-131">UserId</span><span class="sxs-lookup"><span data-stu-id="5fbed-131">UserId</span></span>|
|<span data-ttu-id="5fbed-132">userName</span><span class="sxs-lookup"><span data-stu-id="5fbed-132">userName</span></span>|<span data-ttu-id="5fbed-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-133">String</span></span>|<span data-ttu-id="5fbed-134">UserName</span><span class="sxs-lookup"><span data-stu-id="5fbed-134">UserName</span></span>|
|<span data-ttu-id="5fbed-135">userEmail</span><span class="sxs-lookup"><span data-stu-id="5fbed-135">userEmail</span></span>|<span data-ttu-id="5fbed-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-136">String</span></span>|<span data-ttu-id="5fbed-137">UserEmail</span><span class="sxs-lookup"><span data-stu-id="5fbed-137">UserEmail</span></span>|
|<span data-ttu-id="5fbed-138">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5fbed-138">userPrincipalName</span></span>|<span data-ttu-id="5fbed-139">String</span><span class="sxs-lookup"><span data-stu-id="5fbed-139">String</span></span>|<span data-ttu-id="5fbed-140">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="5fbed-140">UserPrincipalName.</span></span>|
|<span data-ttu-id="5fbed-141">orígenes</span><span class="sxs-lookup"><span data-stu-id="5fbed-141">sources</span></span>|<span data-ttu-id="5fbed-142">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="5fbed-142">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="5fbed-143">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="5fbed-143">Contributing policies</span></span>|
|<span data-ttu-id="5fbed-144">currentValue</span><span class="sxs-lookup"><span data-stu-id="5fbed-144">currentValue</span></span>|<span data-ttu-id="5fbed-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="5fbed-145">String</span></span>|<span data-ttu-id="5fbed-146">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="5fbed-146">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="5fbed-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5fbed-147">Relationships</span></span>
<span data-ttu-id="5fbed-148">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5fbed-148">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5fbed-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5fbed-149">JSON Representation</span></span>
<span data-ttu-id="5fbed-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5fbed-150">Here is a JSON representation of the resource.</span></span>
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



