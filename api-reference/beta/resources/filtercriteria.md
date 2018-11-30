---
title: Tipo de recurso FilterCriteria
description: Representa los criterios de filtrado que se aplican a una columna.
ms.openlocfilehash: dbcc57ff940fec525b712eb11ac44209f5f8a4d2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083840"
---
# <a name="filtercriteria-resource-type"></a><span data-ttu-id="8aad4-103">Tipo de recurso FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="8aad4-103">FilterCriteria resource type</span></span>

> <span data-ttu-id="8aad4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8aad4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8aad4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8aad4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8aad4-106">Representa los criterios de filtrado que se aplican a una columna.</span><span class="sxs-lookup"><span data-stu-id="8aad4-106">Represents the filtering criteria applied to a column.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8aad4-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8aad4-107">JSON representation</span></span>

<span data-ttu-id="8aad4-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8aad4-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.filterCriteria"
}-->

```json
{
  "color": "string",
  "criterion1": "string",
  "criterion2": "string",
  "dynamicCriteria": "string",
  "filterOn": "string",
  "values": "string"
}

```