---
title: tipo de recurso bulkManagedDeviceActionResult
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: adc2b2a6b139ad428cb191fe45a3ca7f4192092a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981780"
---
# <a name="bulkmanageddeviceactionresult-resource-type"></a><span data-ttu-id="2becb-103">tipo de recurso bulkManagedDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="2becb-103">bulkManagedDeviceActionResult resource type</span></span>

> <span data-ttu-id="2becb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2becb-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2becb-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2becb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2becb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2becb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2becb-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2becb-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="2becb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2becb-108">Properties</span></span>
|<span data-ttu-id="2becb-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2becb-109">Property</span></span>|<span data-ttu-id="2becb-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2becb-110">Type</span></span>|<span data-ttu-id="2becb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2becb-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2becb-112">successfulDeviceIds</span><span class="sxs-lookup"><span data-stu-id="2becb-112">successfulDeviceIds</span></span>|<span data-ttu-id="2becb-113">Colección String</span><span class="sxs-lookup"><span data-stu-id="2becb-113">String collection</span></span>|<span data-ttu-id="2becb-114">Dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="2becb-114">Successful devices</span></span>|
|<span data-ttu-id="2becb-115">failedDeviceIds</span><span class="sxs-lookup"><span data-stu-id="2becb-115">failedDeviceIds</span></span>|<span data-ttu-id="2becb-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="2becb-116">String collection</span></span>|<span data-ttu-id="2becb-117">Dispositivos con errores</span><span class="sxs-lookup"><span data-stu-id="2becb-117">Failed devices</span></span>|
|<span data-ttu-id="2becb-118">notFoundDeviceIds</span><span class="sxs-lookup"><span data-stu-id="2becb-118">notFoundDeviceIds</span></span>|<span data-ttu-id="2becb-119">Colección String</span><span class="sxs-lookup"><span data-stu-id="2becb-119">String collection</span></span>|<span data-ttu-id="2becb-120">No se encontraron dispositivos</span><span class="sxs-lookup"><span data-stu-id="2becb-120">Not found devices</span></span>|
|<span data-ttu-id="2becb-121">notSupportedDeviceIds</span><span class="sxs-lookup"><span data-stu-id="2becb-121">notSupportedDeviceIds</span></span>|<span data-ttu-id="2becb-122">Colección String</span><span class="sxs-lookup"><span data-stu-id="2becb-122">String collection</span></span>|<span data-ttu-id="2becb-123">Dispositivos no admitidos</span><span class="sxs-lookup"><span data-stu-id="2becb-123">Not supported devices</span></span>|

## <a name="relationships"></a><span data-ttu-id="2becb-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2becb-124">Relationships</span></span>
<span data-ttu-id="2becb-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2becb-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2becb-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2becb-126">JSON Representation</span></span>
<span data-ttu-id="2becb-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2becb-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.bulkManagedDeviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.bulkManagedDeviceActionResult",
  "successfulDeviceIds": [
    "String"
  ],
  "failedDeviceIds": [
    "String"
  ],
  "notFoundDeviceIds": [
    "String"
  ],
  "notSupportedDeviceIds": [
    "String"
  ]
}
```





