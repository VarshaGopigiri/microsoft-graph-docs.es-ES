---
title: Tipo de recurso configurationManagerClientEnabledFeatures
description: Características habilitadas del cliente de Configuration Manager
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dc1b994615c89b1a6e73785a5ebcdc85f0638953
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987597"
---
# <a name="configurationmanagerclientenabledfeatures-resource-type"></a><span data-ttu-id="8f16c-103">Tipo de recurso configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="8f16c-103">configurationManagerClientEnabledFeatures resource type</span></span>

> <span data-ttu-id="8f16c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8f16c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8f16c-105">Características habilitadas del cliente de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="8f16c-105">configuration Manager client enabled features</span></span>
## <a name="properties"></a><span data-ttu-id="8f16c-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8f16c-106">Properties</span></span>
|<span data-ttu-id="8f16c-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f16c-107">Property</span></span>|<span data-ttu-id="8f16c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f16c-108">Type</span></span>|<span data-ttu-id="8f16c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f16c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8f16c-110">inventario</span><span class="sxs-lookup"><span data-stu-id="8f16c-110">inventory</span></span>|<span data-ttu-id="8f16c-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="8f16c-111">Boolean</span></span>|<span data-ttu-id="8f16c-112">Si el inventario se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="8f16c-112">Whether inventory is managed by Intune</span></span>|
|<span data-ttu-id="8f16c-113">modernApps</span><span class="sxs-lookup"><span data-stu-id="8f16c-113">modernApps</span></span>|<span data-ttu-id="8f16c-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="8f16c-114">Boolean</span></span>|<span data-ttu-id="8f16c-115">Si la aplicación moderna se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="8f16c-115">Whether modern application is managed by Intune</span></span>|
|<span data-ttu-id="8f16c-116">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="8f16c-116">resourceAccess</span></span>|<span data-ttu-id="8f16c-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="8f16c-117">Boolean</span></span>|<span data-ttu-id="8f16c-118">Si el acceso a los recursos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="8f16c-118">Whether resource access is managed by Intune</span></span>|
|<span data-ttu-id="8f16c-119">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f16c-119">deviceConfiguration</span></span>|<span data-ttu-id="8f16c-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="8f16c-120">Boolean</span></span>|<span data-ttu-id="8f16c-121">Si la configuración de dispositivos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="8f16c-121">Whether device configuration is managed by Intune</span></span>|
|<span data-ttu-id="8f16c-122">compliancePolicy</span><span class="sxs-lookup"><span data-stu-id="8f16c-122">compliancePolicy</span></span>|<span data-ttu-id="8f16c-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="8f16c-123">Boolean</span></span>|<span data-ttu-id="8f16c-124">Si la directiva de cumplimiento se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="8f16c-124">Whether compliance policy is managed by Intune</span></span>|
|<span data-ttu-id="8f16c-125">windowsUpdateForBusiness</span><span class="sxs-lookup"><span data-stu-id="8f16c-125">windowsUpdateForBusiness</span></span>|<span data-ttu-id="8f16c-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="8f16c-126">Boolean</span></span>|<span data-ttu-id="8f16c-127">Si Windows Update para empresas se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="8f16c-127">Whether Windows Update for Business is managed by Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="8f16c-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8f16c-128">Relationships</span></span>
<span data-ttu-id="8f16c-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8f16c-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8f16c-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8f16c-130">JSON Representation</span></span>
<span data-ttu-id="8f16c-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8f16c-131">Here is a JSON representation of the resource.</span></span>
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



