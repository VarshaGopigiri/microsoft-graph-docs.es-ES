---
author: daspek
ms.author: dspektor
ms.date: 10/06/2017
title: IncompleteData
localization_priority: Normal
ms.openlocfilehash: add1e3612f65e203f2437419cbb105b78025aa0a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27807514"
---
# <a name="incompletedata-resource-type"></a><span data-ttu-id="fd934-102">tipo de recurso incompleteData</span><span class="sxs-lookup"><span data-stu-id="fd934-102">incompleteData resource type</span></span>

 > <span data-ttu-id="fd934-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fd934-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fd934-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fd934-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fd934-105">El aspecto de **incompleteData** indica que se ha generado un recurso con datos incompletos.</span><span class="sxs-lookup"><span data-stu-id="fd934-105">The **incompleteData** facet indicates that a resource was generated with incomplete data.</span></span>
<span data-ttu-id="fd934-106">Las propiedades dentro de pueden proporcionar información acerca de por qué hay datos incompletos.</span><span class="sxs-lookup"><span data-stu-id="fd934-106">The properties within may provide information about why there is incomplete data.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fd934-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fd934-107">JSON representation</span></span>

<!-- { "blockType": "resource", "@type": "microsoft.graph.incompleteData" } -->

```json
{
  "missingDataBeforeDateTime": "String (timestamp)",
  "wasThrottled": false
}
```

## <a name="properties"></a><span data-ttu-id="fd934-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd934-108">Properties</span></span>

| <span data-ttu-id="fd934-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd934-109">Property</span></span>                  | <span data-ttu-id="fd934-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd934-110">Type</span></span>           | <span data-ttu-id="fd934-111">Description</span><span class="sxs-lookup"><span data-stu-id="fd934-111">Description</span></span>
|:--------------------------|:---------------|:--------------------------------
| <span data-ttu-id="fd934-112">missingDataBeforeDateTime</span><span class="sxs-lookup"><span data-stu-id="fd934-112">missingDataBeforeDateTime</span></span> | <span data-ttu-id="fd934-113">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fd934-113">DateTimeOffset</span></span> | <span data-ttu-id="fd934-114">El servicio no tiene datos de origen antes de la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="fd934-114">The service does not have source data before the specified time.</span></span>
| <span data-ttu-id="fd934-115">wasThrottled</span><span class="sxs-lookup"><span data-stu-id="fd934-115">wasThrottled</span></span>              | <span data-ttu-id="fd934-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="fd934-116">Boolean</span></span>        | <span data-ttu-id="fd934-117">Algunos datos no se grabó debido a una actividad excesiva.</span><span class="sxs-lookup"><span data-stu-id="fd934-117">Some data was not recorded due to excessive activity.</span></span>

<!-- {
  "type": "#page.annotation",
  "section": "documentation",
  "tocPath": "Facets/IncompleteData"
} -->
