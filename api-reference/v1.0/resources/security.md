---
title: tipo de recurso de seguridad
description: El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad. Devuelve un recurso de seguridad singleton. No contiene todas las propiedades utilizables.
localization_priority: Normal
author: preetikr
ms.prod: security
ms.openlocfilehash: c7bf3f279e50efb451188426d030e356d55ad6be
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983257"
---
# <a name="security-resource-type"></a><span data-ttu-id="38a5b-105">tipo de recurso de seguridad</span><span class="sxs-lookup"><span data-stu-id="38a5b-105">security resource type</span></span>

<span data-ttu-id="38a5b-106">El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="38a5b-106">The security resource is the entry point for the Security object model.</span></span> <span data-ttu-id="38a5b-107">Devuelve un recurso de seguridad singleton.</span><span class="sxs-lookup"><span data-stu-id="38a5b-107">It returns a singleton security resource.</span></span> <span data-ttu-id="38a5b-108">No contiene todas las propiedades utilizables.</span><span class="sxs-lookup"><span data-stu-id="38a5b-108">It doesn't contain any usable properties.</span></span>

## <a name="methods"></a><span data-ttu-id="38a5b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="38a5b-109">Methods</span></span>

| <span data-ttu-id="38a5b-110">Método</span><span class="sxs-lookup"><span data-stu-id="38a5b-110">Method</span></span>       | <span data-ttu-id="38a5b-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38a5b-111">Return Type</span></span> | <span data-ttu-id="38a5b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="38a5b-112">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="38a5b-113">List alerts</span><span class="sxs-lookup"><span data-stu-id="38a5b-113">List alerts</span></span>](../api/alert-list.md) | <span data-ttu-id="38a5b-114">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="38a5b-114">[alert](alert.md) collection</span></span> | <span data-ttu-id="38a5b-115">Obtener una colección de objetos de alerta.</span><span class="sxs-lookup"><span data-stu-id="38a5b-115">Get a alert object collection.</span></span> |
| [<span data-ttu-id="38a5b-116">obtener alertas</span><span class="sxs-lookup"><span data-stu-id="38a5b-116">get alerts</span></span>](../api/alert-get.md) | <span data-ttu-id="38a5b-117">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="38a5b-117">[alert](alert.md) collection</span></span> | <span data-ttu-id="38a5b-118">Obtener un objeto de alerta.</span><span class="sxs-lookup"><span data-stu-id="38a5b-118">Get a alert object.</span></span> |
| [<span data-ttu-id="38a5b-119">Actualización de alertas</span><span class="sxs-lookup"><span data-stu-id="38a5b-119">Update alerts</span></span>](../api/alert-update.md) | <span data-ttu-id="38a5b-120">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="38a5b-120">[alert](alert.md) collection</span></span> | <span data-ttu-id="38a5b-121">Obtener un objeto de alerta.</span><span class="sxs-lookup"><span data-stu-id="38a5b-121">Get a alert object.</span></span> |

## <a name="properties"></a><span data-ttu-id="38a5b-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38a5b-122">Properties</span></span>
<span data-ttu-id="38a5b-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="38a5b-123">None</span></span>

## <a name="relationships"></a><span data-ttu-id="38a5b-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="38a5b-124">Relationships</span></span>
| <span data-ttu-id="38a5b-125">Relación</span><span class="sxs-lookup"><span data-stu-id="38a5b-125">Relationship</span></span> | <span data-ttu-id="38a5b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="38a5b-126">Type</span></span>        | <span data-ttu-id="38a5b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="38a5b-127">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="38a5b-128">alerts</span><span class="sxs-lookup"><span data-stu-id="38a5b-128">alerts</span></span>|<span data-ttu-id="38a5b-129">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="38a5b-129">[alert](alert.md) collection</span></span>| <span data-ttu-id="38a5b-p103">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="38a5b-p103">Read-only. Nullable.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="38a5b-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="38a5b-132">JSON representation</span></span>
<span data-ttu-id="38a5b-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="38a5b-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.security"
}-->

```json
{
}
```

## <a name="example"></a><span data-ttu-id="38a5b-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38a5b-134">Example</span></span>

<span data-ttu-id="38a5b-135">El recurso de **seguridad** está disponible en la raíz del gráfico.</span><span class="sxs-lookup"><span data-stu-id="38a5b-135">The **security** resource is available at the root of the graph.</span></span>

<!--{
  "blockType": "request"
}-->
```http
GET https://graph.microsoft.com/v1.0/security
```

<!--{
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security"
}-->
```json
HTTP/1.1 200 OK
Content-type: application/json

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "security resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
