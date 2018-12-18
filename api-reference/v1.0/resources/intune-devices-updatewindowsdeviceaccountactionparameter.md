---
title: Tipo de recurso updateWindowsDeviceAccountActionParameter
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: cd69ffa01473a40228d53ad2f68f793cadf838d5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335465"
---
# <a name="updatewindowsdeviceaccountactionparameter-resource-type"></a><span data-ttu-id="22f42-103">Tipo de recurso updateWindowsDeviceAccountActionParameter</span><span class="sxs-lookup"><span data-stu-id="22f42-103">updateWindowsDeviceAccountActionParameter resource type</span></span>

> <span data-ttu-id="22f42-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="22f42-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="22f42-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="22f42-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="22f42-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22f42-106">Properties</span></span>
|<span data-ttu-id="22f42-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="22f42-107">Property</span></span>|<span data-ttu-id="22f42-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="22f42-108">Type</span></span>|<span data-ttu-id="22f42-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="22f42-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="22f42-110">deviceAccount</span><span class="sxs-lookup"><span data-stu-id="22f42-110">deviceAccount</span></span>|[<span data-ttu-id="22f42-111">windowsDeviceAccount</span><span class="sxs-lookup"><span data-stu-id="22f42-111">windowsDeviceAccount</span></span>](../resources/intune-devices-windowsdeviceaccount.md)|<span data-ttu-id="22f42-112">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="22f42-112">Not yet documented</span></span>|
|<span data-ttu-id="22f42-113">passwordRotationEnabled</span><span class="sxs-lookup"><span data-stu-id="22f42-113">passwordRotationEnabled</span></span>|<span data-ttu-id="22f42-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="22f42-114">Boolean</span></span>|<span data-ttu-id="22f42-115">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="22f42-115">Not yet documented</span></span>|
|<span data-ttu-id="22f42-116">calendarSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="22f42-116">calendarSyncEnabled</span></span>|<span data-ttu-id="22f42-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="22f42-117">Boolean</span></span>|<span data-ttu-id="22f42-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="22f42-118">Not yet documented</span></span>|
|<span data-ttu-id="22f42-119">deviceAccountEmail</span><span class="sxs-lookup"><span data-stu-id="22f42-119">deviceAccountEmail</span></span>|<span data-ttu-id="22f42-120">cadena</span><span class="sxs-lookup"><span data-stu-id="22f42-120">String</span></span>|<span data-ttu-id="22f42-121">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="22f42-121">Not yet documented</span></span>|
|<span data-ttu-id="22f42-122">exchangeServer</span><span class="sxs-lookup"><span data-stu-id="22f42-122">exchangeServer</span></span>|<span data-ttu-id="22f42-123">cadena</span><span class="sxs-lookup"><span data-stu-id="22f42-123">String</span></span>|<span data-ttu-id="22f42-124">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="22f42-124">Not yet documented</span></span>|
|<span data-ttu-id="22f42-125">sessionInitiationProtocalAddress</span><span class="sxs-lookup"><span data-stu-id="22f42-125">sessionInitiationProtocalAddress</span></span>|<span data-ttu-id="22f42-126">cadena</span><span class="sxs-lookup"><span data-stu-id="22f42-126">String</span></span>|<span data-ttu-id="22f42-127">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="22f42-127">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="22f42-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="22f42-128">Relationships</span></span>
<span data-ttu-id="22f42-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="22f42-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="22f42-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="22f42-130">JSON Representation</span></span>
<span data-ttu-id="22f42-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="22f42-131">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.updateWindowsDeviceAccountActionParameter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.updateWindowsDeviceAccountActionParameter",
  "deviceAccount": {
    "@odata.type": "microsoft.graph.windowsDeviceAccount",
    "password": "String"
  },
  "passwordRotationEnabled": true,
  "calendarSyncEnabled": true,
  "deviceAccountEmail": "String",
  "exchangeServer": "String",
  "sessionInitiationProtocalAddress": "String"
}
```



