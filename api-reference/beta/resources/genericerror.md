---
title: tipo de recurso de error genérico
description: Un error de propósito general.
ms.openlocfilehash: caf3fbb99ad521fd807138ab230f6a1b8ae7bb16
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083834"
---
# <a name="genericerror-resource-type"></a><span data-ttu-id="4a62d-103">tipo de recurso de error genérico</span><span class="sxs-lookup"><span data-stu-id="4a62d-103">genericError resource type</span></span>

> <span data-ttu-id="4a62d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4a62d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4a62d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4a62d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4a62d-106">Un error de propósito general.</span><span class="sxs-lookup"><span data-stu-id="4a62d-106">A general-purpose error.</span></span>

## <a name="properties"></a><span data-ttu-id="4a62d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a62d-107">Properties</span></span>

| <span data-ttu-id="4a62d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a62d-108">Property</span></span> | <span data-ttu-id="4a62d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a62d-109">Type</span></span> | <span data-ttu-id="4a62d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a62d-110">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="4a62d-111">message</span><span class="sxs-lookup"><span data-stu-id="4a62d-111">message</span></span> | <span data-ttu-id="4a62d-112">String</span><span class="sxs-lookup"><span data-stu-id="4a62d-112">String</span></span> | <span data-ttu-id="4a62d-113">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="4a62d-113">The error message.</span></span> |
| <span data-ttu-id="4a62d-114">código</span><span class="sxs-lookup"><span data-stu-id="4a62d-114">code</span></span> | <span data-ttu-id="4a62d-115">String</span><span class="sxs-lookup"><span data-stu-id="4a62d-115">String</span></span> | <span data-ttu-id="4a62d-116">Código de error.</span><span class="sxs-lookup"><span data-stu-id="4a62d-116">The error code.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4a62d-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a62d-117">JSON representation</span></span>

<span data-ttu-id="4a62d-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4a62d-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.genericError"
}-->

```json
{
  "message": "String",
  "code": "String"
}
```