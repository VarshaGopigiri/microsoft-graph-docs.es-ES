---
title: Tipo de recurso resourceAction
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f1db2a1db2c76829ddd39438ed40cd1086fe4e17
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932718"
---
# <a name="resourceaction-resource-type"></a><span data-ttu-id="c92d9-103">Tipo de recurso resourceAction</span><span class="sxs-lookup"><span data-stu-id="c92d9-103">resourceAction resource type</span></span>

> <span data-ttu-id="c92d9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c92d9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c92d9-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c92d9-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="c92d9-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c92d9-106">Properties</span></span>
|<span data-ttu-id="c92d9-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c92d9-107">Property</span></span>|<span data-ttu-id="c92d9-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c92d9-108">Type</span></span>|<span data-ttu-id="c92d9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c92d9-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c92d9-110">allowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="c92d9-110">allowedResourceActions</span></span>|<span data-ttu-id="c92d9-111">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="c92d9-111">String collection</span></span>|<span data-ttu-id="c92d9-112">Acciones permitidas</span><span class="sxs-lookup"><span data-stu-id="c92d9-112">Allowed Actions</span></span>|
|<span data-ttu-id="c92d9-113">notAllowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="c92d9-113">notAllowedResourceActions</span></span>|<span data-ttu-id="c92d9-114">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="c92d9-114">String collection</span></span>|<span data-ttu-id="c92d9-115">Acciones no permitidas</span><span class="sxs-lookup"><span data-stu-id="c92d9-115">Not Allowed Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="c92d9-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c92d9-116">Relationships</span></span>
<span data-ttu-id="c92d9-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c92d9-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c92d9-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c92d9-118">JSON Representation</span></span>
<span data-ttu-id="c92d9-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c92d9-119">Here is a JSON representation of the resource.</span></span>
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



