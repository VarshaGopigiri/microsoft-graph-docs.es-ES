---
title: Tipo de recurso deviceConfigurationSettingState
description: Estado de la configuración de dispositivos de un dispositivo determinado.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: beed55d68c3ef7005a307d75fc1ee58ea78ed8d6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845846"
---
# <a name="deviceconfigurationsettingstate-resource-type"></a><span data-ttu-id="7156f-103">Tipo de recurso deviceConfigurationSettingState</span><span class="sxs-lookup"><span data-stu-id="7156f-103">deviceConfigurationSettingState resource type</span></span>

> <span data-ttu-id="7156f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7156f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7156f-105">Estado de la configuración de dispositivos de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="7156f-105">Device Configuration Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="7156f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7156f-106">Properties</span></span>
|<span data-ttu-id="7156f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7156f-107">Property</span></span>|<span data-ttu-id="7156f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7156f-108">Type</span></span>|<span data-ttu-id="7156f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7156f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7156f-110">ajustes</span><span class="sxs-lookup"><span data-stu-id="7156f-110">setting</span></span>|<span data-ttu-id="7156f-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-111">String</span></span>|<span data-ttu-id="7156f-112">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="7156f-112">The setting that is being reported</span></span>|
|<span data-ttu-id="7156f-113">settingName</span><span class="sxs-lookup"><span data-stu-id="7156f-113">settingName</span></span>|<span data-ttu-id="7156f-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-114">String</span></span>|<span data-ttu-id="7156f-115">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="7156f-115">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="7156f-116">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="7156f-116">instanceDisplayName</span></span>|<span data-ttu-id="7156f-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-117">String</span></span>|<span data-ttu-id="7156f-118">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="7156f-118">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="7156f-119">estado</span><span class="sxs-lookup"><span data-stu-id="7156f-119">state</span></span>|[<span data-ttu-id="7156f-120">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="7156f-120">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="7156f-121">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="7156f-121">The compliance state of the setting.</span></span> <span data-ttu-id="7156f-122">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="7156f-122">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="7156f-123">errorCode</span><span class="sxs-lookup"><span data-stu-id="7156f-123">errorCode</span></span>|<span data-ttu-id="7156f-124">Int64</span><span class="sxs-lookup"><span data-stu-id="7156f-124">Int64</span></span>|<span data-ttu-id="7156f-125">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="7156f-125">Error code for the setting</span></span>|
|<span data-ttu-id="7156f-126">errorDescription</span><span class="sxs-lookup"><span data-stu-id="7156f-126">errorDescription</span></span>|<span data-ttu-id="7156f-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-127">String</span></span>|<span data-ttu-id="7156f-128">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="7156f-128">Error description</span></span>|
|<span data-ttu-id="7156f-129">userId</span><span class="sxs-lookup"><span data-stu-id="7156f-129">userId</span></span>|<span data-ttu-id="7156f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-130">String</span></span>|<span data-ttu-id="7156f-131">UserId</span><span class="sxs-lookup"><span data-stu-id="7156f-131">UserId</span></span>|
|<span data-ttu-id="7156f-132">userName</span><span class="sxs-lookup"><span data-stu-id="7156f-132">userName</span></span>|<span data-ttu-id="7156f-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-133">String</span></span>|<span data-ttu-id="7156f-134">UserName</span><span class="sxs-lookup"><span data-stu-id="7156f-134">UserName</span></span>|
|<span data-ttu-id="7156f-135">userEmail</span><span class="sxs-lookup"><span data-stu-id="7156f-135">userEmail</span></span>|<span data-ttu-id="7156f-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-136">String</span></span>|<span data-ttu-id="7156f-137">UserEmail</span><span class="sxs-lookup"><span data-stu-id="7156f-137">UserEmail</span></span>|
|<span data-ttu-id="7156f-138">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7156f-138">userPrincipalName</span></span>|<span data-ttu-id="7156f-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-139">String</span></span>|<span data-ttu-id="7156f-140">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="7156f-140">UserPrincipalName.</span></span>|
|<span data-ttu-id="7156f-141">orígenes</span><span class="sxs-lookup"><span data-stu-id="7156f-141">sources</span></span>|<span data-ttu-id="7156f-142">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="7156f-142">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="7156f-143">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="7156f-143">Contributing policies</span></span>|
|<span data-ttu-id="7156f-144">currentValue</span><span class="sxs-lookup"><span data-stu-id="7156f-144">currentValue</span></span>|<span data-ttu-id="7156f-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="7156f-145">String</span></span>|<span data-ttu-id="7156f-146">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="7156f-146">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="7156f-147">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7156f-147">Relationships</span></span>
<span data-ttu-id="7156f-148">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7156f-148">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7156f-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7156f-149">JSON Representation</span></span>
<span data-ttu-id="7156f-150">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7156f-150">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceConfigurationSettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationSettingState",
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



