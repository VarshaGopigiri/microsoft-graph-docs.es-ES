---
title: tipo de recurso synchronizationJobRestartCriteria
description: 'Define el ámbito de la [synchronizationJob: reinicie](../api/synchronization_synchronizationjob_restart.md) acción.'
ms.openlocfilehash: edf5cf258750df72dda2c9754d3543e07fc32e39
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083551"
---
# <a name="synchronizationjobrestartcriteria-resource-type"></a><span data-ttu-id="0bb3b-103">tipo de recurso synchronizationJobRestartCriteria</span><span class="sxs-lookup"><span data-stu-id="0bb3b-103">synchronizationJobRestartCriteria resource type</span></span>

> <span data-ttu-id="0bb3b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0bb3b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0bb3b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0bb3b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0bb3b-106">Define el ámbito de la [synchronizationJob: reinicie](../api/synchronization_synchronizationjob_restart.md) acción.</span><span class="sxs-lookup"><span data-stu-id="0bb3b-106">Defines the scope of the [synchronizationJob: restart](../api/synchronization_synchronizationjob_restart.md) action.</span></span>

## <a name="properties"></a><span data-ttu-id="0bb3b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0bb3b-107">Properties</span></span>
| <span data-ttu-id="0bb3b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0bb3b-108">Property</span></span>     | <span data-ttu-id="0bb3b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0bb3b-109">Type</span></span>   |<span data-ttu-id="0bb3b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bb3b-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0bb3b-111">resetScope</span><span class="sxs-lookup"><span data-stu-id="0bb3b-111">resetScope</span></span>|<span data-ttu-id="0bb3b-112">String</span><span class="sxs-lookup"><span data-stu-id="0bb3b-112">String</span></span>| <span data-ttu-id="0bb3b-113">Combinación de separados por comas de los valores siguientes: `Full`, `QuarantineState`, `Watermark`, `Escrows`, `ConnectorDataStore`.</span><span class="sxs-lookup"><span data-stu-id="0bb3b-113">Comma-separated combination of the following values: `Full`, `QuarantineState`, `Watermark`, `Escrows`, `ConnectorDataStore`.</span></span> <span data-ttu-id="0bb3b-114">Uso `Full` si desea que todas las opciones.</span><span class="sxs-lookup"><span data-stu-id="0bb3b-114">Use `Full` if you want all of the options.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0bb3b-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0bb3b-115">JSON representation</span></span>

<span data-ttu-id="0bb3b-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0bb3b-116">The following is a JSON representation of the resource.</span></span>

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