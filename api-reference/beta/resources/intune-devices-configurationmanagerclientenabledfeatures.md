---
title: Tipo de recurso configurationManagerClientEnabledFeatures
description: Características habilitadas del cliente de Configuration Manager
ms.openlocfilehash: 60d0e9e78bc4b641bb1f9ee0d61cc09744500424
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084507"
---
# <a name="configurationmanagerclientenabledfeatures-resource-type"></a><span data-ttu-id="823ff-103">Tipo de recurso configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="823ff-103">configurationManagerClientEnabledFeatures resource type</span></span>

> <span data-ttu-id="823ff-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="823ff-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="823ff-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="823ff-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="823ff-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="823ff-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="823ff-107">Características habilitadas del cliente de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="823ff-107">configuration Manager client enabled features</span></span>
## <a name="properties"></a><span data-ttu-id="823ff-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="823ff-108">Properties</span></span>
|<span data-ttu-id="823ff-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="823ff-109">Property</span></span>|<span data-ttu-id="823ff-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="823ff-110">Type</span></span>|<span data-ttu-id="823ff-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="823ff-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="823ff-112">inventario</span><span class="sxs-lookup"><span data-stu-id="823ff-112">inventory</span></span>|<span data-ttu-id="823ff-113">Booleano</span><span class="sxs-lookup"><span data-stu-id="823ff-113">Boolean</span></span>|<span data-ttu-id="823ff-114">Si el inventario se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="823ff-114">Whether inventory is managed by Intune</span></span>|
|<span data-ttu-id="823ff-115">modernApps</span><span class="sxs-lookup"><span data-stu-id="823ff-115">modernApps</span></span>|<span data-ttu-id="823ff-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="823ff-116">Boolean</span></span>|<span data-ttu-id="823ff-117">Si la aplicación moderna se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="823ff-117">Whether modern application is managed by Intune</span></span>|
|<span data-ttu-id="823ff-118">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="823ff-118">resourceAccess</span></span>|<span data-ttu-id="823ff-119">Booleano</span><span class="sxs-lookup"><span data-stu-id="823ff-119">Boolean</span></span>|<span data-ttu-id="823ff-120">Si el acceso a los recursos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="823ff-120">Whether resource access is managed by Intune</span></span>|
|<span data-ttu-id="823ff-121">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="823ff-121">deviceConfiguration</span></span>|<span data-ttu-id="823ff-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="823ff-122">Boolean</span></span>|<span data-ttu-id="823ff-123">Si la configuración de dispositivos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="823ff-123">Whether device configuration is managed by Intune</span></span>|
|<span data-ttu-id="823ff-124">compliancePolicy</span><span class="sxs-lookup"><span data-stu-id="823ff-124">compliancePolicy</span></span>|<span data-ttu-id="823ff-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="823ff-125">Boolean</span></span>|<span data-ttu-id="823ff-126">Si la directiva de cumplimiento se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="823ff-126">Whether compliance policy is managed by Intune</span></span>|
|<span data-ttu-id="823ff-127">windowsUpdateForBusiness</span><span class="sxs-lookup"><span data-stu-id="823ff-127">windowsUpdateForBusiness</span></span>|<span data-ttu-id="823ff-128">Booleano</span><span class="sxs-lookup"><span data-stu-id="823ff-128">Boolean</span></span>|<span data-ttu-id="823ff-129">Si Windows Update para empresas se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="823ff-129">Whether Windows Update for Business is managed by Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="823ff-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="823ff-130">Relationships</span></span>
<span data-ttu-id="823ff-131">Ninguna</span><span class="sxs-lookup"><span data-stu-id="823ff-131">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="823ff-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="823ff-132">JSON Representation</span></span>
<span data-ttu-id="823ff-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="823ff-133">Here is a JSON representation of the resource.</span></span>
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





