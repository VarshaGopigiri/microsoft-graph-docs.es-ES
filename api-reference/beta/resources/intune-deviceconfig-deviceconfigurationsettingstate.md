---
title: Tipo de recurso deviceConfigurationSettingState
description: Estado de la configuración de dispositivos de un dispositivo determinado.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 59eff07d2f609b69f5e5971e407733e0dbfc2577
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982172"
---
# <a name="deviceconfigurationsettingstate-resource-type"></a><span data-ttu-id="71e00-103">Tipo de recurso deviceConfigurationSettingState</span><span class="sxs-lookup"><span data-stu-id="71e00-103">deviceConfigurationSettingState resource type</span></span>

> <span data-ttu-id="71e00-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="71e00-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="71e00-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="71e00-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="71e00-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71e00-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71e00-107">Estado de la configuración de dispositivos de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="71e00-107">Device Configuration Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="71e00-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="71e00-108">Properties</span></span>
|<span data-ttu-id="71e00-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71e00-109">Property</span></span>|<span data-ttu-id="71e00-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="71e00-110">Type</span></span>|<span data-ttu-id="71e00-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="71e00-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="71e00-112">ajustes</span><span class="sxs-lookup"><span data-stu-id="71e00-112">setting</span></span>|<span data-ttu-id="71e00-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-113">String</span></span>|<span data-ttu-id="71e00-114">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="71e00-114">The setting that is being reported</span></span>|
|<span data-ttu-id="71e00-115">settingName</span><span class="sxs-lookup"><span data-stu-id="71e00-115">settingName</span></span>|<span data-ttu-id="71e00-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-116">String</span></span>|<span data-ttu-id="71e00-117">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="71e00-117">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="71e00-118">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="71e00-118">instanceDisplayName</span></span>|<span data-ttu-id="71e00-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-119">String</span></span>|<span data-ttu-id="71e00-120">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="71e00-120">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="71e00-121">estado</span><span class="sxs-lookup"><span data-stu-id="71e00-121">state</span></span>|[<span data-ttu-id="71e00-122">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="71e00-122">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="71e00-123">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="71e00-123">The compliance state of the setting.</span></span> <span data-ttu-id="71e00-124">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="71e00-124">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="71e00-125">errorCode</span><span class="sxs-lookup"><span data-stu-id="71e00-125">errorCode</span></span>|<span data-ttu-id="71e00-126">Int64</span><span class="sxs-lookup"><span data-stu-id="71e00-126">Int64</span></span>|<span data-ttu-id="71e00-127">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="71e00-127">Error code for the setting</span></span>|
|<span data-ttu-id="71e00-128">errorDescription</span><span class="sxs-lookup"><span data-stu-id="71e00-128">errorDescription</span></span>|<span data-ttu-id="71e00-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-129">String</span></span>|<span data-ttu-id="71e00-130">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="71e00-130">Error description</span></span>|
|<span data-ttu-id="71e00-131">userId</span><span class="sxs-lookup"><span data-stu-id="71e00-131">userId</span></span>|<span data-ttu-id="71e00-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-132">String</span></span>|<span data-ttu-id="71e00-133">UserId</span><span class="sxs-lookup"><span data-stu-id="71e00-133">UserId</span></span>|
|<span data-ttu-id="71e00-134">userName</span><span class="sxs-lookup"><span data-stu-id="71e00-134">userName</span></span>|<span data-ttu-id="71e00-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-135">String</span></span>|<span data-ttu-id="71e00-136">UserName</span><span class="sxs-lookup"><span data-stu-id="71e00-136">UserName</span></span>|
|<span data-ttu-id="71e00-137">userEmail</span><span class="sxs-lookup"><span data-stu-id="71e00-137">userEmail</span></span>|<span data-ttu-id="71e00-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-138">String</span></span>|<span data-ttu-id="71e00-139">UserEmail</span><span class="sxs-lookup"><span data-stu-id="71e00-139">UserEmail</span></span>|
|<span data-ttu-id="71e00-140">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="71e00-140">userPrincipalName</span></span>|<span data-ttu-id="71e00-141">String</span><span class="sxs-lookup"><span data-stu-id="71e00-141">String</span></span>|<span data-ttu-id="71e00-142">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="71e00-142">UserPrincipalName.</span></span>|
|<span data-ttu-id="71e00-143">orígenes</span><span class="sxs-lookup"><span data-stu-id="71e00-143">sources</span></span>|<span data-ttu-id="71e00-144">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="71e00-144">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="71e00-145">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="71e00-145">Contributing policies</span></span>|
|<span data-ttu-id="71e00-146">currentValue</span><span class="sxs-lookup"><span data-stu-id="71e00-146">currentValue</span></span>|<span data-ttu-id="71e00-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="71e00-147">String</span></span>|<span data-ttu-id="71e00-148">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="71e00-148">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="71e00-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="71e00-149">Relationships</span></span>
<span data-ttu-id="71e00-150">Ninguna</span><span class="sxs-lookup"><span data-stu-id="71e00-150">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="71e00-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="71e00-151">JSON Representation</span></span>
<span data-ttu-id="71e00-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="71e00-152">Here is a JSON representation of the resource.</span></span>
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





