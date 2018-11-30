---
title: tipo de recurso numberRange
description: Definición del intervalo de números.
ms.openlocfilehash: ef4b24e3034414221365d81c40b453e7ca66a94b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083482"
---
# <a name="numberrange-resource-type"></a><span data-ttu-id="f8e86-103">tipo de recurso numberRange</span><span class="sxs-lookup"><span data-stu-id="f8e86-103">numberRange resource type</span></span>

> <span data-ttu-id="f8e86-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f8e86-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f8e86-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f8e86-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f8e86-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f8e86-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f8e86-107">Definición del intervalo de números.</span><span class="sxs-lookup"><span data-stu-id="f8e86-107">Number Range definition.</span></span>
## <a name="properties"></a><span data-ttu-id="f8e86-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f8e86-108">Properties</span></span>
|<span data-ttu-id="f8e86-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f8e86-109">Property</span></span>|<span data-ttu-id="f8e86-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f8e86-110">Type</span></span>|<span data-ttu-id="f8e86-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8e86-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f8e86-112">lowerNumber</span><span class="sxs-lookup"><span data-stu-id="f8e86-112">lowerNumber</span></span>|<span data-ttu-id="f8e86-113">Int32</span><span class="sxs-lookup"><span data-stu-id="f8e86-113">Int32</span></span>|<span data-ttu-id="f8e86-114">Número inferior.</span><span class="sxs-lookup"><span data-stu-id="f8e86-114">Lower number.</span></span>|
|<span data-ttu-id="f8e86-115">upperNumber</span><span class="sxs-lookup"><span data-stu-id="f8e86-115">upperNumber</span></span>|<span data-ttu-id="f8e86-116">Int32</span><span class="sxs-lookup"><span data-stu-id="f8e86-116">Int32</span></span>|<span data-ttu-id="f8e86-117">Número superior.</span><span class="sxs-lookup"><span data-stu-id="f8e86-117">Upper number.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f8e86-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f8e86-118">Relationships</span></span>
<span data-ttu-id="f8e86-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f8e86-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f8e86-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f8e86-120">JSON Representation</span></span>
<span data-ttu-id="f8e86-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f8e86-121">Here is a JSON representation of the resource.</span></span>
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





