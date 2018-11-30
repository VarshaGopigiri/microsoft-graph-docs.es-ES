---
title: Tipo de recurso deviceConfigurationSettingState
description: Estado de la configuración de dispositivos de un dispositivo determinado.
ms.openlocfilehash: 551b5ccb215492f48d9cd26bcf8b7e2cb80ed787
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086597"
---
# <a name="deviceconfigurationsettingstate-resource-type"></a><span data-ttu-id="a283b-103">Tipo de recurso deviceConfigurationSettingState</span><span class="sxs-lookup"><span data-stu-id="a283b-103">deviceConfigurationSettingState resource type</span></span>

> <span data-ttu-id="a283b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a283b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a283b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a283b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a283b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a283b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a283b-107">Estado de la configuración de dispositivos de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="a283b-107">Device Configuration Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="a283b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a283b-108">Properties</span></span>
|<span data-ttu-id="a283b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a283b-109">Property</span></span>|<span data-ttu-id="a283b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a283b-110">Type</span></span>|<span data-ttu-id="a283b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a283b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a283b-112">ajustes</span><span class="sxs-lookup"><span data-stu-id="a283b-112">setting</span></span>|<span data-ttu-id="a283b-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-113">String</span></span>|<span data-ttu-id="a283b-114">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a283b-114">The setting that is being reported</span></span>|
|<span data-ttu-id="a283b-115">settingName</span><span class="sxs-lookup"><span data-stu-id="a283b-115">settingName</span></span>|<span data-ttu-id="a283b-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-116">String</span></span>|<span data-ttu-id="a283b-117">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="a283b-117">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="a283b-118">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="a283b-118">instanceDisplayName</span></span>|<span data-ttu-id="a283b-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-119">String</span></span>|<span data-ttu-id="a283b-120">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="a283b-120">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="a283b-121">estado</span><span class="sxs-lookup"><span data-stu-id="a283b-121">state</span></span>|[<span data-ttu-id="a283b-122">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="a283b-122">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="a283b-123">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="a283b-123">The compliance state of the setting.</span></span> <span data-ttu-id="a283b-124">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="a283b-124">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="a283b-125">errorCode</span><span class="sxs-lookup"><span data-stu-id="a283b-125">errorCode</span></span>|<span data-ttu-id="a283b-126">Int64</span><span class="sxs-lookup"><span data-stu-id="a283b-126">Int64</span></span>|<span data-ttu-id="a283b-127">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="a283b-127">Error code for the setting</span></span>|
|<span data-ttu-id="a283b-128">errorDescription</span><span class="sxs-lookup"><span data-stu-id="a283b-128">errorDescription</span></span>|<span data-ttu-id="a283b-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-129">String</span></span>|<span data-ttu-id="a283b-130">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="a283b-130">Error description</span></span>|
|<span data-ttu-id="a283b-131">userId</span><span class="sxs-lookup"><span data-stu-id="a283b-131">userId</span></span>|<span data-ttu-id="a283b-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-132">String</span></span>|<span data-ttu-id="a283b-133">UserId</span><span class="sxs-lookup"><span data-stu-id="a283b-133">UserId</span></span>|
|<span data-ttu-id="a283b-134">userName</span><span class="sxs-lookup"><span data-stu-id="a283b-134">userName</span></span>|<span data-ttu-id="a283b-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-135">String</span></span>|<span data-ttu-id="a283b-136">UserName</span><span class="sxs-lookup"><span data-stu-id="a283b-136">UserName</span></span>|
|<span data-ttu-id="a283b-137">userEmail</span><span class="sxs-lookup"><span data-stu-id="a283b-137">userEmail</span></span>|<span data-ttu-id="a283b-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-138">String</span></span>|<span data-ttu-id="a283b-139">UserEmail</span><span class="sxs-lookup"><span data-stu-id="a283b-139">UserEmail</span></span>|
|<span data-ttu-id="a283b-140">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a283b-140">userPrincipalName</span></span>|<span data-ttu-id="a283b-141">String</span><span class="sxs-lookup"><span data-stu-id="a283b-141">String</span></span>|<span data-ttu-id="a283b-142">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="a283b-142">UserPrincipalName.</span></span>|
|<span data-ttu-id="a283b-143">orígenes</span><span class="sxs-lookup"><span data-stu-id="a283b-143">sources</span></span>|<span data-ttu-id="a283b-144">Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="a283b-144">[settingSource](../resources/intune-deviceconfig-settingsource.md) collection</span></span>|<span data-ttu-id="a283b-145">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="a283b-145">Contributing policies</span></span>|
|<span data-ttu-id="a283b-146">currentValue</span><span class="sxs-lookup"><span data-stu-id="a283b-146">currentValue</span></span>|<span data-ttu-id="a283b-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="a283b-147">String</span></span>|<span data-ttu-id="a283b-148">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="a283b-148">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="a283b-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a283b-149">Relationships</span></span>
<span data-ttu-id="a283b-150">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a283b-150">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a283b-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a283b-151">JSON Representation</span></span>
<span data-ttu-id="a283b-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a283b-152">Here is a JSON representation of the resource.</span></span>
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




