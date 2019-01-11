---
title: Tipo de recurso resourceAction
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 94a0ce30dc6e9607aa1531e7421af6b7a5500939
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870738"
---
# <a name="resourceaction-resource-type"></a><span data-ttu-id="fee24-103">Tipo de recurso resourceAction</span><span class="sxs-lookup"><span data-stu-id="fee24-103">resourceAction resource type</span></span>

> <span data-ttu-id="fee24-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fee24-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fee24-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fee24-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="fee24-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fee24-106">Properties</span></span>
|<span data-ttu-id="fee24-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fee24-107">Property</span></span>|<span data-ttu-id="fee24-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="fee24-108">Type</span></span>|<span data-ttu-id="fee24-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fee24-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fee24-110">allowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="fee24-110">allowedResourceActions</span></span>|<span data-ttu-id="fee24-111">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="fee24-111">String collection</span></span>|<span data-ttu-id="fee24-112">Acciones permitidas</span><span class="sxs-lookup"><span data-stu-id="fee24-112">Allowed Actions</span></span>|
|<span data-ttu-id="fee24-113">notAllowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="fee24-113">notAllowedResourceActions</span></span>|<span data-ttu-id="fee24-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="fee24-114">String collection</span></span>|<span data-ttu-id="fee24-115">Acciones no permitidas</span><span class="sxs-lookup"><span data-stu-id="fee24-115">Not Allowed Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="fee24-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fee24-116">Relationships</span></span>
<span data-ttu-id="fee24-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="fee24-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="fee24-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fee24-118">JSON Representation</span></span>
<span data-ttu-id="fee24-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fee24-119">Here is a JSON representation of the resource.</span></span>
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



