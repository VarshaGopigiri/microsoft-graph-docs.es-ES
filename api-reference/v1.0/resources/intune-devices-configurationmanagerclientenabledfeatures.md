---
title: Tipo de recurso configurationManagerClientEnabledFeatures
description: Características habilitadas del cliente de Configuration Manager
ms.openlocfilehash: 54d5d40a50b2946fec1c69c619dc76bec1f32502
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031394"
---
# <a name="configurationmanagerclientenabledfeatures-resource-type"></a><span data-ttu-id="de401-103">Tipo de recurso configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="de401-103">configurationManagerClientEnabledFeatures resource type</span></span>

> <span data-ttu-id="de401-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="de401-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="de401-105">Características habilitadas del cliente de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="de401-105">configuration Manager client enabled features</span></span>
## <a name="properties"></a><span data-ttu-id="de401-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de401-106">Properties</span></span>
|<span data-ttu-id="de401-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="de401-107">Property</span></span>|<span data-ttu-id="de401-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="de401-108">Type</span></span>|<span data-ttu-id="de401-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="de401-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="de401-110">inventario</span><span class="sxs-lookup"><span data-stu-id="de401-110">inventory</span></span>|<span data-ttu-id="de401-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="de401-111">Boolean</span></span>|<span data-ttu-id="de401-112">Si el inventario se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="de401-112">Whether inventory is managed by Intune</span></span>|
|<span data-ttu-id="de401-113">modernApps</span><span class="sxs-lookup"><span data-stu-id="de401-113">modernApps</span></span>|<span data-ttu-id="de401-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="de401-114">Boolean</span></span>|<span data-ttu-id="de401-115">Si la aplicación moderna se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="de401-115">Whether modern application is managed by Intune</span></span>|
|<span data-ttu-id="de401-116">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="de401-116">resourceAccess</span></span>|<span data-ttu-id="de401-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="de401-117">Boolean</span></span>|<span data-ttu-id="de401-118">Si el acceso a los recursos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="de401-118">Whether resource access is managed by Intune</span></span>|
|<span data-ttu-id="de401-119">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="de401-119">deviceConfiguration</span></span>|<span data-ttu-id="de401-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="de401-120">Boolean</span></span>|<span data-ttu-id="de401-121">Si la configuración de dispositivos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="de401-121">Whether device configuration is managed by Intune</span></span>|
|<span data-ttu-id="de401-122">compliancePolicy</span><span class="sxs-lookup"><span data-stu-id="de401-122">compliancePolicy</span></span>|<span data-ttu-id="de401-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="de401-123">Boolean</span></span>|<span data-ttu-id="de401-124">Si la directiva de cumplimiento se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="de401-124">Whether compliance policy is managed by Intune</span></span>|
|<span data-ttu-id="de401-125">windowsUpdateForBusiness</span><span class="sxs-lookup"><span data-stu-id="de401-125">windowsUpdateForBusiness</span></span>|<span data-ttu-id="de401-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="de401-126">Boolean</span></span>|<span data-ttu-id="de401-127">Si Windows Update para empresas se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="de401-127">Whether Windows Update for Business is managed by Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="de401-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="de401-128">Relationships</span></span>
<span data-ttu-id="de401-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="de401-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="de401-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="de401-130">JSON Representation</span></span>
<span data-ttu-id="de401-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="de401-131">Here is a JSON representation of the resource.</span></span>
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



