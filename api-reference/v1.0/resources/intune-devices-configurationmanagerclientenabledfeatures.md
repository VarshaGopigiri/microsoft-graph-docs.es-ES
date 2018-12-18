---
title: Tipo de recurso configurationManagerClientEnabledFeatures
description: Características habilitadas del cliente de Configuration Manager
author: tfitzmac
ms.openlocfilehash: fe975f2e8d537d1231a89eb9f2a44cdd8258fd1a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27325147"
---
# <a name="configurationmanagerclientenabledfeatures-resource-type"></a><span data-ttu-id="11323-103">Tipo de recurso configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="11323-103">configurationManagerClientEnabledFeatures resource type</span></span>

> <span data-ttu-id="11323-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="11323-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="11323-105">Características habilitadas del cliente de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="11323-105">configuration Manager client enabled features</span></span>
## <a name="properties"></a><span data-ttu-id="11323-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11323-106">Properties</span></span>
|<span data-ttu-id="11323-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11323-107">Property</span></span>|<span data-ttu-id="11323-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="11323-108">Type</span></span>|<span data-ttu-id="11323-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="11323-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="11323-110">inventario</span><span class="sxs-lookup"><span data-stu-id="11323-110">inventory</span></span>|<span data-ttu-id="11323-111">Booleano</span><span class="sxs-lookup"><span data-stu-id="11323-111">Boolean</span></span>|<span data-ttu-id="11323-112">Si el inventario se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="11323-112">Whether inventory is managed by Intune</span></span>|
|<span data-ttu-id="11323-113">modernApps</span><span class="sxs-lookup"><span data-stu-id="11323-113">modernApps</span></span>|<span data-ttu-id="11323-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="11323-114">Boolean</span></span>|<span data-ttu-id="11323-115">Si la aplicación moderna se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="11323-115">Whether modern application is managed by Intune</span></span>|
|<span data-ttu-id="11323-116">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="11323-116">resourceAccess</span></span>|<span data-ttu-id="11323-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="11323-117">Boolean</span></span>|<span data-ttu-id="11323-118">Si el acceso a los recursos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="11323-118">Whether resource access is managed by Intune</span></span>|
|<span data-ttu-id="11323-119">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="11323-119">deviceConfiguration</span></span>|<span data-ttu-id="11323-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="11323-120">Boolean</span></span>|<span data-ttu-id="11323-121">Si la configuración de dispositivos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="11323-121">Whether device configuration is managed by Intune</span></span>|
|<span data-ttu-id="11323-122">compliancePolicy</span><span class="sxs-lookup"><span data-stu-id="11323-122">compliancePolicy</span></span>|<span data-ttu-id="11323-123">Booleano</span><span class="sxs-lookup"><span data-stu-id="11323-123">Boolean</span></span>|<span data-ttu-id="11323-124">Si la directiva de cumplimiento se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="11323-124">Whether compliance policy is managed by Intune</span></span>|
|<span data-ttu-id="11323-125">windowsUpdateForBusiness</span><span class="sxs-lookup"><span data-stu-id="11323-125">windowsUpdateForBusiness</span></span>|<span data-ttu-id="11323-126">Booleano</span><span class="sxs-lookup"><span data-stu-id="11323-126">Boolean</span></span>|<span data-ttu-id="11323-127">Si Windows Update para empresas se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="11323-127">Whether Windows Update for Business is managed by Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="11323-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11323-128">Relationships</span></span>
<span data-ttu-id="11323-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11323-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="11323-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11323-130">JSON Representation</span></span>
<span data-ttu-id="11323-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11323-131">Here is a JSON representation of the resource.</span></span>
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



