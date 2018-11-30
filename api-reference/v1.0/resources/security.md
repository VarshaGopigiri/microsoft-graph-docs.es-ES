---
title: tipo de recurso de seguridad
description: El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad. Devuelve un recurso de seguridad singleton. No contiene todas las propiedades utilizables.
ms.openlocfilehash: ddf00e46135733ef18c18918c0c365134138671f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029528"
---
# <a name="security-resource-type"></a><span data-ttu-id="f7b36-105">tipo de recurso de seguridad</span><span class="sxs-lookup"><span data-stu-id="f7b36-105">security resource type</span></span>

<span data-ttu-id="f7b36-106">El recurso de seguridad es el punto de entrada para el modelo de objetos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f7b36-106">The security resource is the entry point for the Security object model.</span></span> <span data-ttu-id="f7b36-107">Devuelve un recurso de seguridad singleton.</span><span class="sxs-lookup"><span data-stu-id="f7b36-107">It returns a singleton security resource.</span></span> <span data-ttu-id="f7b36-108">No contiene todas las propiedades utilizables.</span><span class="sxs-lookup"><span data-stu-id="f7b36-108">It doesn't contain any usable properties.</span></span>

## <a name="methods"></a><span data-ttu-id="f7b36-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f7b36-109">Methods</span></span>

| <span data-ttu-id="f7b36-110">Método</span><span class="sxs-lookup"><span data-stu-id="f7b36-110">Method</span></span>       | <span data-ttu-id="f7b36-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7b36-111">Return Type</span></span> | <span data-ttu-id="f7b36-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7b36-112">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="f7b36-113">List alerts</span><span class="sxs-lookup"><span data-stu-id="f7b36-113">List alerts</span></span>](../api/alert-list.md) | <span data-ttu-id="f7b36-114">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="f7b36-114">[alert](alert.md) collection</span></span> | <span data-ttu-id="f7b36-115">Obtener una colección de objetos de alerta.</span><span class="sxs-lookup"><span data-stu-id="f7b36-115">Get a alert object collection.</span></span> |
| [<span data-ttu-id="f7b36-116">obtener alertas</span><span class="sxs-lookup"><span data-stu-id="f7b36-116">get alerts</span></span>](../api/alert-get.md) | <span data-ttu-id="f7b36-117">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="f7b36-117">[alert](alert.md) collection</span></span> | <span data-ttu-id="f7b36-118">Obtener un objeto de alerta.</span><span class="sxs-lookup"><span data-stu-id="f7b36-118">Get a alert object.</span></span> |
| [<span data-ttu-id="f7b36-119">Actualización de alertas</span><span class="sxs-lookup"><span data-stu-id="f7b36-119">Update alerts</span></span>](../api/alert-update.md) | <span data-ttu-id="f7b36-120">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="f7b36-120">[alert](alert.md) collection</span></span> | <span data-ttu-id="f7b36-121">Obtener un objeto de alerta.</span><span class="sxs-lookup"><span data-stu-id="f7b36-121">Get a alert object.</span></span> |

## <a name="properties"></a><span data-ttu-id="f7b36-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f7b36-122">Properties</span></span>
<span data-ttu-id="f7b36-123">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f7b36-123">None</span></span>

## <a name="relationships"></a><span data-ttu-id="f7b36-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f7b36-124">Relationships</span></span>
| <span data-ttu-id="f7b36-125">Relación</span><span class="sxs-lookup"><span data-stu-id="f7b36-125">Relationship</span></span> | <span data-ttu-id="f7b36-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7b36-126">Type</span></span>        | <span data-ttu-id="f7b36-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7b36-127">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="f7b36-128">alerts</span><span class="sxs-lookup"><span data-stu-id="f7b36-128">alerts</span></span>|<span data-ttu-id="f7b36-129">colección de [alerta](alert.md)</span><span class="sxs-lookup"><span data-stu-id="f7b36-129">[alert](alert.md) collection</span></span>| <span data-ttu-id="f7b36-p103">Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="f7b36-p103">Read-only. Nullable.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="f7b36-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f7b36-132">JSON representation</span></span>
<span data-ttu-id="f7b36-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f7b36-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.security"
}-->

```json
{
}
```

## <a name="example"></a><span data-ttu-id="f7b36-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7b36-134">Example</span></span>

<span data-ttu-id="f7b36-135">El recurso de **seguridad** está disponible en la raíz del gráfico.</span><span class="sxs-lookup"><span data-stu-id="f7b36-135">The **security** resource is available at the root of the graph.</span></span>

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