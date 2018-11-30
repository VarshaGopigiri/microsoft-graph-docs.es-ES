---
author: psampath
ms.author: psampath
ms.date: 06/20/2018
title: StoragePlanInformation
ms.openlocfilehash: 07552f405ec8c5d6ae8345a8238cd8aec3763b11
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088151"
---
# <a name="storageplaninformation-resource-type"></a><span data-ttu-id="3c459-102">tipo de recurso storagePlanInformation</span><span class="sxs-lookup"><span data-stu-id="3c459-102">storagePlanInformation resource type</span></span>

> <span data-ttu-id="3c459-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3c459-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3c459-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3c459-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3c459-105">El recurso **storagePlanInformation** proporciona información acerca de los planes de cuota de almacenamiento de información de la unidad.</span><span class="sxs-lookup"><span data-stu-id="3c459-105">The **storagePlanInformation** resource provides information about the drive's storage quota plans.</span></span>

### <a name="json-representation"></a><span data-ttu-id="3c459-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3c459-106">JSON representation</span></span>

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
## <a name="properties"></a><span data-ttu-id="3c459-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c459-107">Properties</span></span>

| <span data-ttu-id="3c459-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="3c459-108">Property name</span></span>     | <span data-ttu-id="3c459-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c459-109">Type</span></span>      | <span data-ttu-id="3c459-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c459-110">Description</span></span>                                                             |
|:------------------|:----------|:----------------------------------------------------------------------- |
| <span data-ttu-id="3c459-111">upgradeAvailable</span><span class="sxs-lookup"><span data-stu-id="3c459-111">upgradeAvailable</span></span>  | <span data-ttu-id="3c459-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="3c459-112">Boolean</span></span>   | <span data-ttu-id="3c459-113">Indica si hay planes de cuota de almacenamiento superiores.</span><span class="sxs-lookup"><span data-stu-id="3c459-113">Indicates if there are higher storage quota plans available.</span></span> <span data-ttu-id="3c459-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3c459-114">Read-only.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "storagePlanInformation resource contains information about storage quota plans that make up the drive's storage space quota.",
  "keywords": "quota,plans,upgradeAvailable",
  "section": "documentation",
  "tocPath": "Resources/StoragePlanInformation"
} -->

