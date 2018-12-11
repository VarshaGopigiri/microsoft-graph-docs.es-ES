---
title: tipo de recurso directoryObjectPartnerReference
description: Representa una referencia a un objeto de directorio en un inquilino de socio. Se hereda de directoryObject.
ms.openlocfilehash: ebdd7380eaa6b59488aca46120339f7175b640fa
ms.sourcegitcommit: 72d4da2a6bfaf99fa4edaf6ce3b97b1a6d96d874
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2018
ms.locfileid: "27224130"
---
# <a name="directoryobjectpartnerreference-resource-type"></a><span data-ttu-id="75679-104">tipo de recurso directoryObjectPartnerReference</span><span class="sxs-lookup"><span data-stu-id="75679-104">directoryObjectPartnerReference resource type</span></span>

> <span data-ttu-id="75679-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75679-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75679-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75679-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="75679-107">Representa una referencia a un objeto de Active directory en una organización asociada.</span><span class="sxs-lookup"><span data-stu-id="75679-107">Represents a reference to a directory object in a partner organization.</span></span> <span data-ttu-id="75679-108">Se hereda de [directoryObject](directoryobject.md?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="75679-108">Inherits from [directoryObject](directoryobject.md?view=graph-rest-beta).</span></span>

## <a name="properties"></a><span data-ttu-id="75679-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75679-109">Properties</span></span>

| <span data-ttu-id="75679-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75679-110">Property</span></span> | <span data-ttu-id="75679-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="75679-111">Type</span></span> | <span data-ttu-id="75679-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="75679-112">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="75679-113">description</span><span class="sxs-lookup"><span data-stu-id="75679-113">description</span></span>|<span data-ttu-id="75679-114">String</span><span class="sxs-lookup"><span data-stu-id="75679-114">String</span></span>| <span data-ttu-id="75679-115">Descripción del objeto devuelto.</span><span class="sxs-lookup"><span data-stu-id="75679-115">Description of the object returned.</span></span> <span data-ttu-id="75679-116">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75679-116">Read-only.</span></span> |
|<span data-ttu-id="75679-117">displayName</span><span class="sxs-lookup"><span data-stu-id="75679-117">displayName</span></span>|<span data-ttu-id="75679-118">String</span><span class="sxs-lookup"><span data-stu-id="75679-118">String</span></span>| <span data-ttu-id="75679-119">Nombre del objeto de Active directory que se devuelve, al igual que el grupo o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75679-119">Name of directory object being returned, like group or application.</span></span> <span data-ttu-id="75679-120">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75679-120">Read-only.</span></span> |
|<span data-ttu-id="75679-121">externalPartnerTenantId</span><span class="sxs-lookup"><span data-stu-id="75679-121">externalPartnerTenantId</span></span>|<span data-ttu-id="75679-122">Guid</span><span class="sxs-lookup"><span data-stu-id="75679-122">Guid</span></span>| <span data-ttu-id="75679-123">El identificador de inquilino para el inquilino de socio.</span><span class="sxs-lookup"><span data-stu-id="75679-123">The tenant identifier for the partner tenant.</span></span> <span data-ttu-id="75679-124">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75679-124">Read-only.</span></span> |
|<span data-ttu-id="75679-125">id</span><span class="sxs-lookup"><span data-stu-id="75679-125">id</span></span>|<span data-ttu-id="75679-126">String</span><span class="sxs-lookup"><span data-stu-id="75679-126">String</span></span>| <span data-ttu-id="75679-127">El identificador único para el recurso.</span><span class="sxs-lookup"><span data-stu-id="75679-127">The unique identifier for the resource.</span></span> <span data-ttu-id="75679-128">Heredado de [directoryObject](directoryobject.md?view=graph-rest-beta).</span><span class="sxs-lookup"><span data-stu-id="75679-128">Inherited from [directoryObject](directoryobject.md?view=graph-rest-beta).</span></span> <span data-ttu-id="75679-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75679-129">Read-only.</span></span> |
|<span data-ttu-id="75679-130">objectType</span><span class="sxs-lookup"><span data-stu-id="75679-130">objectType</span></span>|<span data-ttu-id="75679-131">String</span><span class="sxs-lookup"><span data-stu-id="75679-131">String</span></span>| <span data-ttu-id="75679-132">El tipo del objeto que se hace referencia en el inquilino de socio.</span><span class="sxs-lookup"><span data-stu-id="75679-132">The type of the referenced object in the partner tenant.</span></span> <span data-ttu-id="75679-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75679-133">Read-only.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="75679-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75679-134">JSON representation</span></span>

<span data-ttu-id="75679-135">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="75679-135">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryObjectPartnerReference"
}-->

```json
{
  "description": "string ",
  "displayName": "string",
  "externalPartnerTenantId": "string (identifier)",
  "id": "string (identifier)",
  "objectType": "string"
}
```

## <a name="see-also"></a><span data-ttu-id="75679-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="75679-136">See also</span></span>

- [<span data-ttu-id="75679-137">Obtener objetos de directorio a partir de una lista de identificadores</span><span class="sxs-lookup"><span data-stu-id="75679-137">Get directory objects from a list of ids</span></span>](/graph/api/directoryobject-getbyids?view=graph-rest-beta)

<!-- uuid: fbec8cd7-cfe4-431d-87fc-d102cd2841a4
2018-12-06 02:01:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObjectPartnerReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
