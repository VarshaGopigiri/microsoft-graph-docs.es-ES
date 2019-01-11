---
title: tipo de recurso de error genérico
description: Un error de propósito general.
localization_priority: Normal
ms.openlocfilehash: 744266ef8ffb17c4af4168d6239e5a5a30561936
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823572"
---
# <a name="genericerror-resource-type"></a><span data-ttu-id="1dc76-103">tipo de recurso de error genérico</span><span class="sxs-lookup"><span data-stu-id="1dc76-103">genericError resource type</span></span>

> <span data-ttu-id="1dc76-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1dc76-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1dc76-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1dc76-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1dc76-106">Un error de propósito general.</span><span class="sxs-lookup"><span data-stu-id="1dc76-106">A general-purpose error.</span></span>

## <a name="properties"></a><span data-ttu-id="1dc76-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1dc76-107">Properties</span></span>

| <span data-ttu-id="1dc76-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1dc76-108">Property</span></span> | <span data-ttu-id="1dc76-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1dc76-109">Type</span></span> | <span data-ttu-id="1dc76-110">Description</span><span class="sxs-lookup"><span data-stu-id="1dc76-110">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="1dc76-111">message</span><span class="sxs-lookup"><span data-stu-id="1dc76-111">message</span></span> | <span data-ttu-id="1dc76-112">String</span><span class="sxs-lookup"><span data-stu-id="1dc76-112">String</span></span> | <span data-ttu-id="1dc76-113">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="1dc76-113">The error message.</span></span> |
| <span data-ttu-id="1dc76-114">código</span><span class="sxs-lookup"><span data-stu-id="1dc76-114">code</span></span> | <span data-ttu-id="1dc76-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="1dc76-115">String</span></span> | <span data-ttu-id="1dc76-116">Código de error.</span><span class="sxs-lookup"><span data-stu-id="1dc76-116">The error code.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="1dc76-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1dc76-117">JSON representation</span></span>

<span data-ttu-id="1dc76-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1dc76-118">Here is a JSON representation of the resource.</span></span>

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
