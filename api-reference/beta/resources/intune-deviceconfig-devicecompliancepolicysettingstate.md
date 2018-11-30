---
title: Tipo de recurso deviceCompliancePolicySettingState
description: Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.
ms.openlocfilehash: d73cbe591e30e465065e0c446c6d98d7232a049c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088452"
---
# <a name="devicecompliancepolicysettingstate-resource-type"></a><span data-ttu-id="10703-103">Tipo de recurso deviceCompliancePolicySettingState</span><span class="sxs-lookup"><span data-stu-id="10703-103">deviceCompliancePolicySettingState resource type</span></span>

> <span data-ttu-id="10703-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="10703-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="10703-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="10703-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="10703-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="10703-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="10703-107">Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="10703-107">Device Compilance Policy Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="10703-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10703-108">Properties</span></span>
|<span data-ttu-id="10703-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="10703-109">Property</span></span>|<span data-ttu-id="10703-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="10703-110">Type</span></span>|<span data-ttu-id="10703-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="10703-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="10703-112">ajustes</span><span class="sxs-lookup"><span data-stu-id="10703-112">setting</span></span>|<span data-ttu-id="10703-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-113">String</span></span>|<span data-ttu-id="10703-114">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="10703-114">The setting that is being reported</span></span>|
|<span data-ttu-id="10703-115">settingName</span><span class="sxs-lookup"><span data-stu-id="10703-115">settingName</span></span>|<span data-ttu-id="10703-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-116">String</span></span>|<span data-ttu-id="10703-117">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="10703-117">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="10703-118">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="10703-118">instanceDisplayName</span></span>|<span data-ttu-id="10703-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-119">String</span></span>|<span data-ttu-id="10703-120">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="10703-120">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="10703-121">estado</span><span class="sxs-lookup"><span data-stu-id="10703-121">state</span></span>|[<span data-ttu-id="10703-122">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="10703-122">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="10703-123">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="10703-123">The compliance state of the setting.</span></span> <span data-ttu-id="10703-124">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="10703-124">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="10703-125">errorCode</span><span class="sxs-lookup"><span data-stu-id="10703-125">errorCode</span></span>|<span data-ttu-id="10703-126">Int64</span><span class="sxs-lookup"><span data-stu-id="10703-126">Int64</span></span>|<span data-ttu-id="10703-127">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="10703-127">Error code for the setting</span></span>|
|<span data-ttu-id="10703-128">errorDescription</span><span class="sxs-lookup"><span data-stu-id="10703-128">errorDescription</span></span>|<span data-ttu-id="10703-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-129">String</span></span>|<span data-ttu-id="10703-130">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="10703-130">Error description</span></span>|
|<span data-ttu-id="10703-131">userId</span><span class="sxs-lookup"><span data-stu-id="10703-131">userId</span></span>|<span data-ttu-id="10703-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-132">String</span></span>|<span data-ttu-id="10703-133">UserId</span><span class="sxs-lookup"><span data-stu-id="10703-133">UserId</span></span>|
|<span data-ttu-id="10703-134">userName</span><span class="sxs-lookup"><span data-stu-id="10703-134">userName</span></span>|<span data-ttu-id="10703-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-135">String</span></span>|<span data-ttu-id="10703-136">UserName</span><span class="sxs-lookup"><span data-stu-id="10703-136">UserName</span></span>|
|<span data-ttu-id="10703-137">userEmail</span><span class="sxs-lookup"><span data-stu-id="10703-137">userEmail</span></span>|<span data-ttu-id="10703-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-138">String</span></span>|<span data-ttu-id="10703-139">UserEmail</span><span class="sxs-lookup"><span data-stu-id="10703-139">UserEmail</span></span>|
|<span data-ttu-id="10703-140">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="10703-140">userPrincipalName</span></span>|<span data-ttu-id="10703-141">String</span><span class="sxs-lookup"><span data-stu-id="10703-141">String</span></span>|<span data-ttu-id="10703-142">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="10703-142">UserPrincipalName.</span></span>|
|<span data-ttu-id="10703-143">orígenes</span><span class="sxs-lookup"><span data-stu-id="10703-143">sources</span></span>|<span data-ttu-id="10703-144">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="10703-144">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="10703-145">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="10703-145">Contributing policies</span></span>|
|<span data-ttu-id="10703-146">currentValue</span><span class="sxs-lookup"><span data-stu-id="10703-146">currentValue</span></span>|<span data-ttu-id="10703-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="10703-147">String</span></span>|<span data-ttu-id="10703-148">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="10703-148">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="10703-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="10703-149">Relationships</span></span>
<span data-ttu-id="10703-150">Ninguna</span><span class="sxs-lookup"><span data-stu-id="10703-150">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="10703-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="10703-151">JSON Representation</span></span>
<span data-ttu-id="10703-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="10703-152">Here is a JSON representation of the resource.</span></span>
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





