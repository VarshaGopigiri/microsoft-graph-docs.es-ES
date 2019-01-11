---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Cuota
localization_priority: Normal
ms.openlocfilehash: a63b41253569dbb3d666a76b0a7495839ef61b12
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882414"
---
# <a name="quota-resource-type"></a><span data-ttu-id="5a8e8-102">tipo de recurso de cuota</span><span class="sxs-lookup"><span data-stu-id="5a8e8-102">quota resource type</span></span>

> <span data-ttu-id="5a8e8-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5a8e8-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5a8e8-105">El recurso de **cuota** proporciona detalles acerca del espacio restringe en un recurso de [unidad](drive.md) .</span><span class="sxs-lookup"><span data-stu-id="5a8e8-105">The **quota** resource provides details about space constrains on a [drive](drive.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5a8e8-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5a8e8-106">JSON representation</span></span>

<span data-ttu-id="5a8e8-107">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-107">Here is a JSON representation of the resource.</span></span>

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
  "storagePlanInformation": {
    "upgradeAvailable": true
  },
  "total": 1024,
  "used": 1024
}
```

## <a name="properties"></a><span data-ttu-id="5a8e8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a8e8-108">Properties</span></span>

| <span data-ttu-id="5a8e8-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="5a8e8-109">Property name</span></span> | <span data-ttu-id="5a8e8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a8e8-110">Type</span></span>   | <span data-ttu-id="5a8e8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a8e8-111">Description</span></span>                                                                 |
|:--------------|:-------|:----------------------------------------------------------------------------|
| <span data-ttu-id="5a8e8-112">total</span><span class="sxs-lookup"><span data-stu-id="5a8e8-112">total</span></span>         | <span data-ttu-id="5a8e8-113">Int64</span><span class="sxs-lookup"><span data-stu-id="5a8e8-113">Int64</span></span>  | <span data-ttu-id="5a8e8-p102">Espacio total de almacenamiento permitido, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-p102">Total allowed storage space, in bytes. Read-only.</span></span>                           |
| <span data-ttu-id="5a8e8-116">used</span><span class="sxs-lookup"><span data-stu-id="5a8e8-116">used</span></span>          | <span data-ttu-id="5a8e8-117">Int64</span><span class="sxs-lookup"><span data-stu-id="5a8e8-117">Int64</span></span>  | <span data-ttu-id="5a8e8-p103">Espacio total usado, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-p103">Total space used, in bytes. Read-only.</span></span>                                      |
| <span data-ttu-id="5a8e8-120">remaining</span><span class="sxs-lookup"><span data-stu-id="5a8e8-120">remaining</span></span>     | <span data-ttu-id="5a8e8-121">Int64</span><span class="sxs-lookup"><span data-stu-id="5a8e8-121">Int64</span></span>  | <span data-ttu-id="5a8e8-p104">Espacio total restante antes de alcanzar el límite de cuota, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-p104">Total space remaining before reaching the quota limit, in bytes. Read-only.</span></span> |
| <span data-ttu-id="5a8e8-124">deleted</span><span class="sxs-lookup"><span data-stu-id="5a8e8-124">deleted</span></span>       | <span data-ttu-id="5a8e8-125">Int64</span><span class="sxs-lookup"><span data-stu-id="5a8e8-125">Int64</span></span>  | <span data-ttu-id="5a8e8-p105">Espacio total consumido por los archivos de la Papelera de reciclaje, en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-p105">Total space consumed by files in the recycle bin, in bytes. Read-only.</span></span>      |
| <span data-ttu-id="5a8e8-128">state</span><span class="sxs-lookup"><span data-stu-id="5a8e8-128">state</span></span>         | <span data-ttu-id="5a8e8-129">string</span><span class="sxs-lookup"><span data-stu-id="5a8e8-129">string</span></span> | <span data-ttu-id="5a8e8-p106">Valor de enumeración que indica el estado del espacio de almacenamiento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-p106">Enumeration value that indicates the state of the storage space. Read-only.</span></span> |
| <span data-ttu-id="5a8e8-132">storagePlanInformation</span><span class="sxs-lookup"><span data-stu-id="5a8e8-132">storagePlanInformation</span></span>  | [<span data-ttu-id="5a8e8-133">storagePlanInformation</span><span class="sxs-lookup"><span data-stu-id="5a8e8-133">storagePlanInformation</span></span>](storageplaninformation.md) | <span data-ttu-id="5a8e8-134">Información acerca de los planes de cuota de almacenamiento de información de la unidad.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-134">Information about the drive's storage quota plans.</span></span> <span data-ttu-id="5a8e8-135">Sólo en OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-135">Only in Personal OneDrive.</span></span>|

### <a name="state-enumeration-values"></a><span data-ttu-id="5a8e8-136">Valores de estado (enumeración)</span><span class="sxs-lookup"><span data-stu-id="5a8e8-136">State enumeration values</span></span>

| <span data-ttu-id="5a8e8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5a8e8-137">Value</span></span>      | <span data-ttu-id="5a8e8-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a8e8-138">Description</span></span>                                                                                                                                                                 |
|:-----------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `normal`   | <span data-ttu-id="5a8e8-139">A la unidad le queda mucha cuota restante.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-139">The drive has plenty of remaining quota left.</span></span>                                                                                                                               |
| `nearing`  | <span data-ttu-id="5a8e8-140">La cuota restante es inferior al 10 % del espacio total de cuota.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-140">Remaining quota is less than 10% of total quota space.</span></span>                                                                                                                      |
| `critical` | <span data-ttu-id="5a8e8-141">La cuota restante es inferior al 1 % del espacio total de cuota.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-141">Remaining quota is less than 1% of total quota space.</span></span>                                                                                                                       |
| `exceeded` | <span data-ttu-id="5a8e8-p108">La cuota usada ha superado la cuota total. No se pueden agregar nuevos archivos ni carpetas en la unidad hasta que esté por debajo de la cantidad total de cuota o se adquiera más espacio de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5a8e8-p108">The used quota has exceeded the total quota. New files or folders cannot be added to the drive until it is under the total quota amount or more storage space is purchased.</span></span> |

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "tocPath": "Facets/Quota"
} -->
