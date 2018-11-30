---
author: daspek
ms.author: dspektor
ms.date: 10/06/2017
title: IncompleteData
ms.openlocfilehash: 4319ab0f36e12ddd28ca9bb6c7bfd48043228504
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084186"
---
# <a name="incompletedata-resource-type"></a><span data-ttu-id="be804-102">tipo de recurso incompleteData</span><span class="sxs-lookup"><span data-stu-id="be804-102">incompleteData resource type</span></span>

 > <span data-ttu-id="be804-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="be804-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="be804-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="be804-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="be804-105">El aspecto de **incompleteData** indica que se ha generado un recurso con datos incompletos.</span><span class="sxs-lookup"><span data-stu-id="be804-105">The **incompleteData** facet indicates that a resource was generated with incomplete data.</span></span>
<span data-ttu-id="be804-106">Las propiedades dentro de pueden proporcionar información acerca de por qué hay datos incompletos.</span><span class="sxs-lookup"><span data-stu-id="be804-106">The properties within may provide information about why there is incomplete data.</span></span>

## <a name="json-representation"></a><span data-ttu-id="be804-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="be804-107">JSON representation</span></span>

<!-- { "blockType": "resource", "@type": "microsoft.graph.incompleteData" } -->

```json
{
  "missingDataBeforeDateTime": "String (timestamp)",
  "wasThrottled": false
}
```

## <a name="properties"></a><span data-ttu-id="be804-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be804-108">Properties</span></span>

| <span data-ttu-id="be804-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be804-109">Property</span></span>                  | <span data-ttu-id="be804-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="be804-110">Type</span></span>           | <span data-ttu-id="be804-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="be804-111">Description</span></span>
|:--------------------------|:---------------|:--------------------------------
| <span data-ttu-id="be804-112">missingDataBeforeDateTime</span><span class="sxs-lookup"><span data-stu-id="be804-112">missingDataBeforeDateTime</span></span> | <span data-ttu-id="be804-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be804-113">DateTimeOffset</span></span> | <span data-ttu-id="be804-114">El servicio no tiene datos de origen antes de la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="be804-114">The service does not have source data before the specified time.</span></span>
| <span data-ttu-id="be804-115">wasThrottled</span><span class="sxs-lookup"><span data-stu-id="be804-115">wasThrottled</span></span>              | <span data-ttu-id="be804-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="be804-116">Boolean</span></span>        | <span data-ttu-id="be804-117">Algunos datos no se grabó debido a una actividad excesiva.</span><span class="sxs-lookup"><span data-stu-id="be804-117">Some data was not recorded due to excessive activity.</span></span>

<!-- {
  "type": "#page.annotation",
  "section": "documentation",
  "tocPath": "Facets/IncompleteData"
} -->
