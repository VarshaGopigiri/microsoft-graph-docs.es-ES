---
title: Tipo de recurso resourceAction
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8d607ca2b250e9d2af55b74ef568a82c522bf761
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876387"
---
# <a name="resourceaction-resource-type"></a><span data-ttu-id="7389f-103">Tipo de recurso resourceAction</span><span class="sxs-lookup"><span data-stu-id="7389f-103">resourceAction resource type</span></span>

> <span data-ttu-id="7389f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7389f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7389f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7389f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7389f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7389f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7389f-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7389f-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="7389f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7389f-108">Properties</span></span>
|<span data-ttu-id="7389f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7389f-109">Property</span></span>|<span data-ttu-id="7389f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7389f-110">Type</span></span>|<span data-ttu-id="7389f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7389f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7389f-112">allowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="7389f-112">allowedResourceActions</span></span>|<span data-ttu-id="7389f-113">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="7389f-113">String collection</span></span>|<span data-ttu-id="7389f-114">Acciones permitidas</span><span class="sxs-lookup"><span data-stu-id="7389f-114">Allowed Actions</span></span>|
|<span data-ttu-id="7389f-115">notAllowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="7389f-115">notAllowedResourceActions</span></span>|<span data-ttu-id="7389f-116">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="7389f-116">String collection</span></span>|<span data-ttu-id="7389f-117">Acciones no permitidas</span><span class="sxs-lookup"><span data-stu-id="7389f-117">Not Allowed Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="7389f-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7389f-118">Relationships</span></span>
<span data-ttu-id="7389f-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7389f-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7389f-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7389f-120">JSON Representation</span></span>
<span data-ttu-id="7389f-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7389f-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.resourceAction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.resourceAction",
  "allowedResourceActions": [
    "String"
  ],
  "notAllowedResourceActions": [
    "String"
  ]
}
```





