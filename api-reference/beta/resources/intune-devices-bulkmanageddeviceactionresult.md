---
title: tipo de recurso bulkManagedDeviceActionResult
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c7aa0d49182908a960130e202fd4cf096c2c16c9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27872250"
---
# <a name="bulkmanageddeviceactionresult-resource-type"></a><span data-ttu-id="ffaca-103">tipo de recurso bulkManagedDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="ffaca-103">bulkManagedDeviceActionResult resource type</span></span>

> <span data-ttu-id="ffaca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ffaca-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ffaca-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ffaca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ffaca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ffaca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ffaca-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ffaca-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="ffaca-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffaca-108">Properties</span></span>
|<span data-ttu-id="ffaca-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffaca-109">Property</span></span>|<span data-ttu-id="ffaca-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffaca-110">Type</span></span>|<span data-ttu-id="ffaca-111">Description</span><span class="sxs-lookup"><span data-stu-id="ffaca-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ffaca-112">successfulDeviceIds</span><span class="sxs-lookup"><span data-stu-id="ffaca-112">successfulDeviceIds</span></span>|<span data-ttu-id="ffaca-113">Colección String</span><span class="sxs-lookup"><span data-stu-id="ffaca-113">String collection</span></span>|<span data-ttu-id="ffaca-114">Dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="ffaca-114">Successful devices</span></span>|
|<span data-ttu-id="ffaca-115">failedDeviceIds</span><span class="sxs-lookup"><span data-stu-id="ffaca-115">failedDeviceIds</span></span>|<span data-ttu-id="ffaca-116">Colección String</span><span class="sxs-lookup"><span data-stu-id="ffaca-116">String collection</span></span>|<span data-ttu-id="ffaca-117">Dispositivos con errores</span><span class="sxs-lookup"><span data-stu-id="ffaca-117">Failed devices</span></span>|
|<span data-ttu-id="ffaca-118">notFoundDeviceIds</span><span class="sxs-lookup"><span data-stu-id="ffaca-118">notFoundDeviceIds</span></span>|<span data-ttu-id="ffaca-119">Colección String</span><span class="sxs-lookup"><span data-stu-id="ffaca-119">String collection</span></span>|<span data-ttu-id="ffaca-120">No se encontraron dispositivos</span><span class="sxs-lookup"><span data-stu-id="ffaca-120">Not found devices</span></span>|
|<span data-ttu-id="ffaca-121">notSupportedDeviceIds</span><span class="sxs-lookup"><span data-stu-id="ffaca-121">notSupportedDeviceIds</span></span>|<span data-ttu-id="ffaca-122">Colección String</span><span class="sxs-lookup"><span data-stu-id="ffaca-122">String collection</span></span>|<span data-ttu-id="ffaca-123">Dispositivos no admitidos</span><span class="sxs-lookup"><span data-stu-id="ffaca-123">Not supported devices</span></span>|

## <a name="relationships"></a><span data-ttu-id="ffaca-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ffaca-124">Relationships</span></span>
<span data-ttu-id="ffaca-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ffaca-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ffaca-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ffaca-126">JSON Representation</span></span>
<span data-ttu-id="ffaca-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ffaca-127">Here is a JSON representation of the resource.</span></span>
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





