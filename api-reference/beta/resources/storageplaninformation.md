---
author: psampath
ms.author: psampath
ms.date: 06/20/2018
title: StoragePlanInformation
localization_priority: Normal
ms.openlocfilehash: bbe4faaffbf53c24d4d0f5b8ea1f5ee1e1966a2c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860126"
---
# <a name="storageplaninformation-resource-type"></a><span data-ttu-id="07279-102">tipo de recurso storagePlanInformation</span><span class="sxs-lookup"><span data-stu-id="07279-102">storagePlanInformation resource type</span></span>

> <span data-ttu-id="07279-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="07279-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="07279-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="07279-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="07279-105">El recurso **storagePlanInformation** proporciona información acerca de los planes de cuota de almacenamiento de información de la unidad.</span><span class="sxs-lookup"><span data-stu-id="07279-105">The **storagePlanInformation** resource provides information about the drive's storage quota plans.</span></span>

### <a name="json-representation"></a><span data-ttu-id="07279-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="07279-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
   "@odata.type": "microsoft.graph.storagePlanInformation",
} -->

```json
{
  "upgradeAvailable": true
}

```
## <a name="properties"></a><span data-ttu-id="07279-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="07279-107">Properties</span></span>

| <span data-ttu-id="07279-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="07279-108">Property name</span></span>     | <span data-ttu-id="07279-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="07279-109">Type</span></span>      | <span data-ttu-id="07279-110">Description</span><span class="sxs-lookup"><span data-stu-id="07279-110">Description</span></span>                                                             |
|:------------------|:----------|:----------------------------------------------------------------------- |
| <span data-ttu-id="07279-111">upgradeAvailable</span><span class="sxs-lookup"><span data-stu-id="07279-111">upgradeAvailable</span></span>  | <span data-ttu-id="07279-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="07279-112">Boolean</span></span>   | <span data-ttu-id="07279-113">Indica si hay planes de cuota de almacenamiento superiores.</span><span class="sxs-lookup"><span data-stu-id="07279-113">Indicates if there are higher storage quota plans available.</span></span> <span data-ttu-id="07279-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="07279-114">Read-only.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "storagePlanInformation resource contains information about storage quota plans that make up the drive's storage space quota.",
  "keywords": "quota,plans,upgradeAvailable",
  "section": "documentation",
  "tocPath": "Resources/StoragePlanInformation"
} -->

