---
title: Tipo de recurso updateWindowsDeviceAccountActionParameter
description: Todavía no documentado
ms.openlocfilehash: f6403e4c3b106b318b7d551796911f6bcc0253c2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031011"
---
# <a name="updatewindowsdeviceaccountactionparameter-resource-type"></a><span data-ttu-id="01422-103">Tipo de recurso updateWindowsDeviceAccountActionParameter</span><span class="sxs-lookup"><span data-stu-id="01422-103">updateWindowsDeviceAccountActionParameter resource type</span></span>

> <span data-ttu-id="01422-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01422-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01422-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01422-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="01422-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01422-106">Properties</span></span>
|<span data-ttu-id="01422-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01422-107">Property</span></span>|<span data-ttu-id="01422-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="01422-108">Type</span></span>|<span data-ttu-id="01422-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="01422-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01422-110">deviceAccount</span><span class="sxs-lookup"><span data-stu-id="01422-110">deviceAccount</span></span>|[<span data-ttu-id="01422-111">windowsDeviceAccount</span><span class="sxs-lookup"><span data-stu-id="01422-111">windowsDeviceAccount</span></span>](../resources/intune-devices-windowsdeviceaccount.md)|<span data-ttu-id="01422-112">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01422-112">Not yet documented</span></span>|
|<span data-ttu-id="01422-113">passwordRotationEnabled</span><span class="sxs-lookup"><span data-stu-id="01422-113">passwordRotationEnabled</span></span>|<span data-ttu-id="01422-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="01422-114">Boolean</span></span>|<span data-ttu-id="01422-115">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01422-115">Not yet documented</span></span>|
|<span data-ttu-id="01422-116">calendarSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="01422-116">calendarSyncEnabled</span></span>|<span data-ttu-id="01422-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="01422-117">Boolean</span></span>|<span data-ttu-id="01422-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01422-118">Not yet documented</span></span>|
|<span data-ttu-id="01422-119">deviceAccountEmail</span><span class="sxs-lookup"><span data-stu-id="01422-119">deviceAccountEmail</span></span>|<span data-ttu-id="01422-120">cadena</span><span class="sxs-lookup"><span data-stu-id="01422-120">String</span></span>|<span data-ttu-id="01422-121">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01422-121">Not yet documented</span></span>|
|<span data-ttu-id="01422-122">exchangeServer</span><span class="sxs-lookup"><span data-stu-id="01422-122">exchangeServer</span></span>|<span data-ttu-id="01422-123">cadena</span><span class="sxs-lookup"><span data-stu-id="01422-123">String</span></span>|<span data-ttu-id="01422-124">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01422-124">Not yet documented</span></span>|
|<span data-ttu-id="01422-125">sessionInitiationProtocalAddress</span><span class="sxs-lookup"><span data-stu-id="01422-125">sessionInitiationProtocalAddress</span></span>|<span data-ttu-id="01422-126">cadena</span><span class="sxs-lookup"><span data-stu-id="01422-126">String</span></span>|<span data-ttu-id="01422-127">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01422-127">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="01422-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="01422-128">Relationships</span></span>
<span data-ttu-id="01422-129">Ninguna</span><span class="sxs-lookup"><span data-stu-id="01422-129">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="01422-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="01422-130">JSON Representation</span></span>
<span data-ttu-id="01422-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="01422-131">Here is a JSON representation of the resource.</span></span>
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



