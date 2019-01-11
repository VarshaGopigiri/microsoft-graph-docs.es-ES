---
title: tipo de recurso synchronizationJobRestartCriteria
description: 'Define el ámbito de la [synchronizationJob: reinicie](../api/synchronization_synchronizationjob_restart.md) acción.'
localization_priority: Normal
ms.openlocfilehash: e26bae2e418da22a2b56e3acb973e4111066df23
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867882"
---
# <a name="synchronizationjobrestartcriteria-resource-type"></a><span data-ttu-id="a2226-103">tipo de recurso synchronizationJobRestartCriteria</span><span class="sxs-lookup"><span data-stu-id="a2226-103">synchronizationJobRestartCriteria resource type</span></span>

> <span data-ttu-id="a2226-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a2226-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a2226-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a2226-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a2226-106">Define el ámbito de la [synchronizationJob: reinicie](../api/synchronization_synchronizationjob_restart.md) acción.</span><span class="sxs-lookup"><span data-stu-id="a2226-106">Defines the scope of the [synchronizationJob: restart](../api/synchronization_synchronizationjob_restart.md) action.</span></span>

## <a name="properties"></a><span data-ttu-id="a2226-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2226-107">Properties</span></span>
| <span data-ttu-id="a2226-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2226-108">Property</span></span>     | <span data-ttu-id="a2226-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2226-109">Type</span></span>   |<span data-ttu-id="a2226-110">Description</span><span class="sxs-lookup"><span data-stu-id="a2226-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a2226-111">resetScope</span><span class="sxs-lookup"><span data-stu-id="a2226-111">resetScope</span></span>|<span data-ttu-id="a2226-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="a2226-112">String</span></span>| <span data-ttu-id="a2226-113">Combinación de separados por comas de los valores siguientes: `Full`, `QuarantineState`, `Watermark`, `Escrows`, `ConnectorDataStore`.</span><span class="sxs-lookup"><span data-stu-id="a2226-113">Comma-separated combination of the following values: `Full`, `QuarantineState`, `Watermark`, `Escrows`, `ConnectorDataStore`.</span></span> <span data-ttu-id="a2226-114">Uso `Full` si desea que todas las opciones.</span><span class="sxs-lookup"><span data-stu-id="a2226-114">Use `Full` if you want all of the options.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a2226-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a2226-115">JSON representation</span></span>

<span data-ttu-id="a2226-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a2226-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationJobRestartCriteria"
}-->

```json
{
  "resetScope": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationJobRestartCriteria resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
