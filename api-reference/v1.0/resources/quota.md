---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cuota
ms.openlocfilehash: 54eb88bdc048c6b63bb6f2d0a23fb05023663ca7
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267601"
---
# <a name="quota-resource-type"></a><span data-ttu-id="de3ac-102">Tipo de recurso Quota</span><span class="sxs-lookup"><span data-stu-id="de3ac-102">Quota resource type</span></span>

<span data-ttu-id="de3ac-103">El recurso **quota** proporciona detalles sobre las limitaciones de espacio en un recurso [Drive](drive.md).</span><span class="sxs-lookup"><span data-stu-id="de3ac-103">The **quota** resource provides details about space constrains on a [Drive](drive.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="de3ac-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="de3ac-104">JSON representation</span></span>

<span data-ttu-id="de3ac-105">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="de3ac-105">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@odata.type": "microsoft.graph.quota"
}-->

```json
{
  "deleted": 1024,
  "remaining": 1024,
  "state": "normal | nearing | critical | exceeded",
  "total": 1024,
  "used": 1024
}
```

## <a name="properties"></a><span data-ttu-id="de3ac-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="de3ac-106">Properties</span></span>

| <span data-ttu-id="de3ac-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="de3ac-107">Property name</span></span> | <span data-ttu-id="de3ac-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="de3ac-108">Type</span></span>   | <span data-ttu-id="de3ac-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="de3ac-109">Description</span></span>                                                                 |
|:--------------|:-------|:----------------------------------------------------------------------------|
| <span data-ttu-id="de3ac-110">total</span><span class="sxs-lookup"><span data-stu-id="de3ac-110">total</span></span>         | <span data-ttu-id="de3ac-111">Int64</span><span class="sxs-lookup"><span data-stu-id="de3ac-111">Int64</span></span>  | <span data-ttu-id="de3ac-p101">Espacio total de almacenamiento permitido, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de3ac-p101">Total allowed storage space, in bytes. Read-only.</span></span>                           |
| <span data-ttu-id="de3ac-114">used</span><span class="sxs-lookup"><span data-stu-id="de3ac-114">used</span></span>          | <span data-ttu-id="de3ac-115">Int64</span><span class="sxs-lookup"><span data-stu-id="de3ac-115">Int64</span></span>  | <span data-ttu-id="de3ac-p102">Espacio total usado, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de3ac-p102">Total space used, in bytes. Read-only.</span></span>                                      |
| <span data-ttu-id="de3ac-118">remaining</span><span class="sxs-lookup"><span data-stu-id="de3ac-118">remaining</span></span>     | <span data-ttu-id="de3ac-119">Int64</span><span class="sxs-lookup"><span data-stu-id="de3ac-119">Int64</span></span>  | <span data-ttu-id="de3ac-p103">Espacio total restante antes de alcanzar el límite de cuota, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de3ac-p103">Total space remaining before reaching the quota limit, in bytes. Read-only.</span></span> |
| <span data-ttu-id="de3ac-122">deleted</span><span class="sxs-lookup"><span data-stu-id="de3ac-122">deleted</span></span>       | <span data-ttu-id="de3ac-123">Int64</span><span class="sxs-lookup"><span data-stu-id="de3ac-123">Int64</span></span>  | <span data-ttu-id="de3ac-p104">Espacio total consumido por los archivos de la Papelera de reciclaje, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de3ac-p104">Total space consumed by files in the recycle bin, in bytes. Read-only.</span></span>      |
| <span data-ttu-id="de3ac-126">estado</span><span class="sxs-lookup"><span data-stu-id="de3ac-126">state</span></span>         | <span data-ttu-id="de3ac-127">cadena</span><span class="sxs-lookup"><span data-stu-id="de3ac-127">string</span></span> | <span data-ttu-id="de3ac-p105">Valor de enumeración que indica el estado del espacio de almacenamiento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de3ac-p105">Enumeration value that indicates the state of the storage space. Read-only.</span></span> |

## <a name="state-enumeration"></a><span data-ttu-id="de3ac-130">Enumeración de estado</span><span class="sxs-lookup"><span data-stu-id="de3ac-130">State Enumeration</span></span>

| <span data-ttu-id="de3ac-131">Valor</span><span class="sxs-lookup"><span data-stu-id="de3ac-131">Value</span></span>      | <span data-ttu-id="de3ac-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="de3ac-132">Description</span></span>                                                                                                                                                                 |
|:-----------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `normal`   | <span data-ttu-id="de3ac-133">A la unidad le queda mucha cuota restante.</span><span class="sxs-lookup"><span data-stu-id="de3ac-133">The drive has plenty of remaining quota left.</span></span>                                                                                                                               |
| `nearing`  | <span data-ttu-id="de3ac-134">La cuota restante es inferior al 10 % del espacio total de cuota.</span><span class="sxs-lookup"><span data-stu-id="de3ac-134">Remaining quota is less than 10% of total quota space.</span></span>                                                                                                                      |
| `critical` | <span data-ttu-id="de3ac-135">La cuota restante es inferior al 1 % del espacio total de cuota.</span><span class="sxs-lookup"><span data-stu-id="de3ac-135">Remaining quota is less than 1% of total quota space.</span></span>                                                                                                                       |
| `exceeded` | <span data-ttu-id="de3ac-p106">La cuota usada ha superado la cuota total. No se pueden agregar nuevos archivos ni carpetas en la unidad hasta que esté por debajo de la cantidad total de cuota o se adquiera más espacio de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="de3ac-p106">The used quota has exceeded the total quota. New files or folders cannot be added to the drive until it is under the total quota amount or more storage space is purchased.</span></span> |

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/quota.md:
      Found potential enums in resource example that weren't defined in a table:(normal, nearing,critical,exceeded) are in resource, but () are in table"
  ],
  "tocPath": "Facets/Quota"
} -->
