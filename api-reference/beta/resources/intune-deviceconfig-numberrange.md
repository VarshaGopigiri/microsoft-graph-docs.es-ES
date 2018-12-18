---
title: tipo de recurso numberRange
description: Definición del intervalo de números.
author: tfitzmac
ms.openlocfilehash: 7b9703524e1562a7367a3c5b9bf0212e29620429
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314661"
---
# <a name="numberrange-resource-type"></a><span data-ttu-id="2ec57-103">tipo de recurso numberRange</span><span class="sxs-lookup"><span data-stu-id="2ec57-103">numberRange resource type</span></span>

> <span data-ttu-id="2ec57-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ec57-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ec57-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ec57-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2ec57-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2ec57-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2ec57-107">Definición del intervalo de números.</span><span class="sxs-lookup"><span data-stu-id="2ec57-107">Number Range definition.</span></span>
## <a name="properties"></a><span data-ttu-id="2ec57-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ec57-108">Properties</span></span>
|<span data-ttu-id="2ec57-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ec57-109">Property</span></span>|<span data-ttu-id="2ec57-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ec57-110">Type</span></span>|<span data-ttu-id="2ec57-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ec57-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2ec57-112">lowerNumber</span><span class="sxs-lookup"><span data-stu-id="2ec57-112">lowerNumber</span></span>|<span data-ttu-id="2ec57-113">Int32</span><span class="sxs-lookup"><span data-stu-id="2ec57-113">Int32</span></span>|<span data-ttu-id="2ec57-114">Número inferior.</span><span class="sxs-lookup"><span data-stu-id="2ec57-114">Lower number.</span></span>|
|<span data-ttu-id="2ec57-115">upperNumber</span><span class="sxs-lookup"><span data-stu-id="2ec57-115">upperNumber</span></span>|<span data-ttu-id="2ec57-116">Int32</span><span class="sxs-lookup"><span data-stu-id="2ec57-116">Int32</span></span>|<span data-ttu-id="2ec57-117">Número superior.</span><span class="sxs-lookup"><span data-stu-id="2ec57-117">Upper number.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2ec57-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2ec57-118">Relationships</span></span>
<span data-ttu-id="2ec57-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2ec57-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2ec57-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2ec57-120">JSON Representation</span></span>
<span data-ttu-id="2ec57-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2ec57-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.numberRange"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.numberRange",
  "lowerNumber": 1024,
  "upperNumber": 1024
}
```





