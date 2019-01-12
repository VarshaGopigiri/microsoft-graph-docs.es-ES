---
title: Tipo de recurso configurationManagerClientEnabledFeatures
description: Características habilitadas del cliente de Configuration Manager
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 07b143a8d61335c44c83d1d88b9a67d2d3c2e4dc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962089"
---
# <a name="configurationmanagerclientenabledfeatures-resource-type"></a><span data-ttu-id="97331-103">Tipo de recurso configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="97331-103">configurationManagerClientEnabledFeatures resource type</span></span>

> <span data-ttu-id="97331-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="97331-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="97331-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="97331-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="97331-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97331-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97331-107">Características habilitadas del cliente de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="97331-107">configuration Manager client enabled features</span></span>
## <a name="properties"></a><span data-ttu-id="97331-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97331-108">Properties</span></span>
|<span data-ttu-id="97331-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97331-109">Property</span></span>|<span data-ttu-id="97331-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="97331-110">Type</span></span>|<span data-ttu-id="97331-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="97331-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="97331-112">inventario</span><span class="sxs-lookup"><span data-stu-id="97331-112">inventory</span></span>|<span data-ttu-id="97331-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="97331-113">Boolean</span></span>|<span data-ttu-id="97331-114">Si el inventario se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="97331-114">Whether inventory is managed by Intune</span></span>|
|<span data-ttu-id="97331-115">modernApps</span><span class="sxs-lookup"><span data-stu-id="97331-115">modernApps</span></span>|<span data-ttu-id="97331-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="97331-116">Boolean</span></span>|<span data-ttu-id="97331-117">Si la aplicación moderna se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="97331-117">Whether modern application is managed by Intune</span></span>|
|<span data-ttu-id="97331-118">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="97331-118">resourceAccess</span></span>|<span data-ttu-id="97331-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="97331-119">Boolean</span></span>|<span data-ttu-id="97331-120">Si el acceso a los recursos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="97331-120">Whether resource access is managed by Intune</span></span>|
|<span data-ttu-id="97331-121">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="97331-121">deviceConfiguration</span></span>|<span data-ttu-id="97331-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="97331-122">Boolean</span></span>|<span data-ttu-id="97331-123">Si la configuración de dispositivos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="97331-123">Whether device configuration is managed by Intune</span></span>|
|<span data-ttu-id="97331-124">compliancePolicy</span><span class="sxs-lookup"><span data-stu-id="97331-124">compliancePolicy</span></span>|<span data-ttu-id="97331-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="97331-125">Boolean</span></span>|<span data-ttu-id="97331-126">Si la directiva de cumplimiento se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="97331-126">Whether compliance policy is managed by Intune</span></span>|
|<span data-ttu-id="97331-127">windowsUpdateForBusiness</span><span class="sxs-lookup"><span data-stu-id="97331-127">windowsUpdateForBusiness</span></span>|<span data-ttu-id="97331-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="97331-128">Boolean</span></span>|<span data-ttu-id="97331-129">Si Windows Update para empresas se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="97331-129">Whether Windows Update for Business is managed by Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="97331-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="97331-130">Relationships</span></span>
<span data-ttu-id="97331-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="97331-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="97331-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="97331-132">JSON Representation</span></span>
<span data-ttu-id="97331-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="97331-133">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.configurationManagerClientEnabledFeatures",
  "inventory": true,
  "modernApps": true,
  "resourceAccess": true,
  "deviceConfiguration": true,
  "compliancePolicy": true,
  "windowsUpdateForBusiness": true
}
```





