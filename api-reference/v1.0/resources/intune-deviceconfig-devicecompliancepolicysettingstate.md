---
title: Tipo de recurso deviceCompliancePolicySettingState
description: Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 63c60b2d7d714f7040c894da872c017e06ad0249
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832879"
---
# <a name="devicecompliancepolicysettingstate-resource-type"></a><span data-ttu-id="a49a9-103">Tipo de recurso deviceCompliancePolicySettingState</span><span class="sxs-lookup"><span data-stu-id="a49a9-103">deviceCompliancePolicySettingState resource type</span></span>

> <span data-ttu-id="a49a9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a49a9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a49a9-105">Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="a49a9-105">Device Compilance Policy Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="a49a9-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a49a9-106">Properties</span></span>
|<span data-ttu-id="a49a9-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a49a9-107">Property</span></span>|<span data-ttu-id="a49a9-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a49a9-108">Type</span></span>|<span data-ttu-id="a49a9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a49a9-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a49a9-110">ajustes</span><span class="sxs-lookup"><span data-stu-id="a49a9-110">setting</span></span>|<span data-ttu-id="a49a9-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-111">String</span></span>|<span data-ttu-id="a49a9-112">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a49a9-112">The setting that is being reported</span></span>|
|<span data-ttu-id="a49a9-113">settingName</span><span class="sxs-lookup"><span data-stu-id="a49a9-113">settingName</span></span>|<span data-ttu-id="a49a9-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-114">String</span></span>|<span data-ttu-id="a49a9-115">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a49a9-115">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="a49a9-116">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="a49a9-116">instanceDisplayName</span></span>|<span data-ttu-id="a49a9-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-117">String</span></span>|<span data-ttu-id="a49a9-118">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="a49a9-118">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="a49a9-119">estado</span><span class="sxs-lookup"><span data-stu-id="a49a9-119">state</span></span>|[<span data-ttu-id="a49a9-120">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="a49a9-120">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="a49a9-121">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="a49a9-121">The compliance state of the setting.</span></span> <span data-ttu-id="a49a9-122">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="a49a9-122">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="a49a9-123">errorCode</span><span class="sxs-lookup"><span data-stu-id="a49a9-123">errorCode</span></span>|<span data-ttu-id="a49a9-124">Int64</span><span class="sxs-lookup"><span data-stu-id="a49a9-124">Int64</span></span>|<span data-ttu-id="a49a9-125">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="a49a9-125">Error code for the setting</span></span>|
|<span data-ttu-id="a49a9-126">errorDescription</span><span class="sxs-lookup"><span data-stu-id="a49a9-126">errorDescription</span></span>|<span data-ttu-id="a49a9-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-127">String</span></span>|<span data-ttu-id="a49a9-128">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="a49a9-128">Error description</span></span>|
|<span data-ttu-id="a49a9-129">userId</span><span class="sxs-lookup"><span data-stu-id="a49a9-129">userId</span></span>|<span data-ttu-id="a49a9-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-130">String</span></span>|<span data-ttu-id="a49a9-131">UserId</span><span class="sxs-lookup"><span data-stu-id="a49a9-131">UserId</span></span>|
|<span data-ttu-id="a49a9-132">userName</span><span class="sxs-lookup"><span data-stu-id="a49a9-132">userName</span></span>|<span data-ttu-id="a49a9-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-133">String</span></span>|<span data-ttu-id="a49a9-134">UserName</span><span class="sxs-lookup"><span data-stu-id="a49a9-134">UserName</span></span>|
|<span data-ttu-id="a49a9-135">userEmail</span><span class="sxs-lookup"><span data-stu-id="a49a9-135">userEmail</span></span>|<span data-ttu-id="a49a9-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-136">String</span></span>|<span data-ttu-id="a49a9-137">UserEmail</span><span class="sxs-lookup"><span data-stu-id="a49a9-137">UserEmail</span></span>|
|<span data-ttu-id="a49a9-138">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a49a9-138">userPrincipalName</span></span>|<span data-ttu-id="a49a9-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-139">String</span></span>|<span data-ttu-id="a49a9-140">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="a49a9-140">UserPrincipalName.</span></span>|
|<span data-ttu-id="a49a9-141">orígenes</span><span class="sxs-lookup"><span data-stu-id="a49a9-141">sources</span></span>|<span data-ttu-id="a49a9-142">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="a49a9-142">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="a49a9-143">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="a49a9-143">Contributing policies</span></span>|
|<span data-ttu-id="a49a9-144">currentValue</span><span class="sxs-lookup"><span data-stu-id="a49a9-144">currentValue</span></span>|<span data-ttu-id="a49a9-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="a49a9-145">String</span></span>|<span data-ttu-id="a49a9-146">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="a49a9-146">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="a49a9-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a49a9-147">Relationships</span></span>
<span data-ttu-id="a49a9-148">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a49a9-148">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a49a9-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a49a9-149">JSON Representation</span></span>
<span data-ttu-id="a49a9-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a49a9-150">Here is a JSON representation of the resource.</span></span>
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



