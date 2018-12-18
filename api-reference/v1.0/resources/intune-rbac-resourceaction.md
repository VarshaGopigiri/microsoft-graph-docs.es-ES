---
title: Tipo de recurso resourceAction
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: b64c1fb0ef49c2d7c47c88137bcca8ef89f6ad67
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343921"
---
# <a name="resourceaction-resource-type"></a><span data-ttu-id="cd56e-103">Tipo de recurso resourceAction</span><span class="sxs-lookup"><span data-stu-id="cd56e-103">resourceAction resource type</span></span>

> <span data-ttu-id="cd56e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cd56e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cd56e-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cd56e-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="cd56e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd56e-106">Properties</span></span>
|<span data-ttu-id="cd56e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd56e-107">Property</span></span>|<span data-ttu-id="cd56e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd56e-108">Type</span></span>|<span data-ttu-id="cd56e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd56e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cd56e-110">allowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="cd56e-110">allowedResourceActions</span></span>|<span data-ttu-id="cd56e-111">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="cd56e-111">String collection</span></span>|<span data-ttu-id="cd56e-112">Acciones permitidas</span><span class="sxs-lookup"><span data-stu-id="cd56e-112">Allowed Actions</span></span>|
|<span data-ttu-id="cd56e-113">notAllowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="cd56e-113">notAllowedResourceActions</span></span>|<span data-ttu-id="cd56e-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="cd56e-114">String collection</span></span>|<span data-ttu-id="cd56e-115">Acciones no permitidas</span><span class="sxs-lookup"><span data-stu-id="cd56e-115">Not Allowed Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="cd56e-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cd56e-116">Relationships</span></span>
<span data-ttu-id="cd56e-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cd56e-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cd56e-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd56e-118">JSON Representation</span></span>
<span data-ttu-id="cd56e-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cd56e-119">Here is a JSON representation of the resource.</span></span>
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



