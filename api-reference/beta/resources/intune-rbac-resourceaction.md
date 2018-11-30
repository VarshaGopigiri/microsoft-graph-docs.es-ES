---
title: Tipo de recurso resourceAction
description: Todavía no documentado
ms.openlocfilehash: d4f585ec52096cc9bd6d1430825d61426df644fe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087568"
---
# <a name="resourceaction-resource-type"></a><span data-ttu-id="2a2b5-103">Tipo de recurso resourceAction</span><span class="sxs-lookup"><span data-stu-id="2a2b5-103">resourceAction resource type</span></span>

> <span data-ttu-id="2a2b5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a2b5-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a2b5-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a2b5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2a2b5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a2b5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a2b5-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2a2b5-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="2a2b5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a2b5-108">Properties</span></span>
|<span data-ttu-id="2a2b5-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2a2b5-109">Property</span></span>|<span data-ttu-id="2a2b5-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a2b5-110">Type</span></span>|<span data-ttu-id="2a2b5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a2b5-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a2b5-112">allowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="2a2b5-112">allowedResourceActions</span></span>|<span data-ttu-id="2a2b5-113">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="2a2b5-113">String collection</span></span>|<span data-ttu-id="2a2b5-114">Acciones permitidas</span><span class="sxs-lookup"><span data-stu-id="2a2b5-114">Allowed Actions</span></span>|
|<span data-ttu-id="2a2b5-115">notAllowedResourceActions</span><span class="sxs-lookup"><span data-stu-id="2a2b5-115">notAllowedResourceActions</span></span>|<span data-ttu-id="2a2b5-116">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="2a2b5-116">String collection</span></span>|<span data-ttu-id="2a2b5-117">Acciones no permitidas</span><span class="sxs-lookup"><span data-stu-id="2a2b5-117">Not Allowed Actions</span></span>|

## <a name="relationships"></a><span data-ttu-id="2a2b5-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2a2b5-118">Relationships</span></span>
<span data-ttu-id="2a2b5-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2a2b5-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2a2b5-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2a2b5-120">JSON Representation</span></span>
<span data-ttu-id="2a2b5-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2a2b5-121">Here is a JSON representation of the resource.</span></span>
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





