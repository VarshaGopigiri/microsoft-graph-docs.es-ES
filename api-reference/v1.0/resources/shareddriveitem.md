---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharedDriveItem
localization_priority: Normal
ms.openlocfilehash: 6e20df0cf50a7fc2648f5df97fcfe84e83992d99
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826197"
---
# <a name="shareddriveitem-resource-type"></a><span data-ttu-id="f67a5-102">Tipo de recurso SharedDriveItem</span><span class="sxs-lookup"><span data-stu-id="f67a5-102">SharedDriveItem resource type</span></span>

<span data-ttu-id="f67a5-103">El recurso **sharedDriveItem** se devuelve al usar la API [Shares](../api/shares-get.md) para obtener acceso a un objeto [driveItem](driveitem.md) compartido.</span><span class="sxs-lookup"><span data-stu-id="f67a5-103">The **sharedDriveItem** resource is returned when using the [Shares](../api/shares-get.md) API to access a shared [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="f67a5-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f67a5-104">JSON representation</span></span>

<span data-ttu-id="f67a5-105">A continuación se incluye una representación JSON del recurso **sharedDriveItem**.</span><span class="sxs-lookup"><span data-stu-id="f67a5-105">Here is a JSON representation of the **sharedDriveItem** resource.</span></span>

<span data-ttu-id="f67a5-106">El recurso **sharedDriveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="f67a5-106">The **sharedDriveItem** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItem",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.sharedDriveItem"
}-->

```json
{
  "id": "string",
  "name": "string",
  "owner": { "@odata.type": "microsoft.graph.identitySet" },

  "driveItem": { "@odata.type": "microsoft.graph.driveItem" },
  "items": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "list": { "@odata.type": "microsoft.graph.list" },
  "listItem": { "@odata.type": "microsoft.graph.listItem" },
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "site": { "@odata.type": "microsoft.graph.site" }
}
```

## <a name="properties"></a><span data-ttu-id="f67a5-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f67a5-107">Properties</span></span>

| <span data-ttu-id="f67a5-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f67a5-108">Property</span></span> | <span data-ttu-id="f67a5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f67a5-109">Type</span></span>                          | <span data-ttu-id="f67a5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f67a5-110">Description</span></span>                                                      |
| :------- | :---------------------------- | :--------------------------------------------------------------- |
| <span data-ttu-id="f67a5-111">id</span><span class="sxs-lookup"><span data-stu-id="f67a5-111">id</span></span>       | <span data-ttu-id="f67a5-112">String</span><span class="sxs-lookup"><span data-stu-id="f67a5-112">String</span></span>                        | <span data-ttu-id="f67a5-113">El identificador único del recurso compartido al que se accede.</span><span class="sxs-lookup"><span data-stu-id="f67a5-113">The unique identifier for the share being accessed.</span></span>              |
| <span data-ttu-id="f67a5-114">name</span><span class="sxs-lookup"><span data-stu-id="f67a5-114">name</span></span>     | <span data-ttu-id="f67a5-115">String</span><span class="sxs-lookup"><span data-stu-id="f67a5-115">String</span></span>                        | <span data-ttu-id="f67a5-116">El nombre para mostrar del elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="f67a5-116">The display name of the shared item.</span></span>                             |
| <span data-ttu-id="f67a5-117">owner</span><span class="sxs-lookup"><span data-stu-id="f67a5-117">owner</span></span>    | [<span data-ttu-id="f67a5-118">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="f67a5-118">IdentitySet</span></span>](identityset.md) | <span data-ttu-id="f67a5-119">Información sobre el propietario del elemento compartido al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="f67a5-119">Information about the owner of the shared item being referenced.</span></span> |

## <a name="relationships"></a><span data-ttu-id="f67a5-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f67a5-120">Relationships</span></span>

| <span data-ttu-id="f67a5-121">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="f67a5-121">Relationship name</span></span> | <span data-ttu-id="f67a5-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="f67a5-122">Type</span></span>                | <span data-ttu-id="f67a5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="f67a5-123">Description</span></span>
| ------------------|:--------------------|:-----------------------------------
| <span data-ttu-id="f67a5-124">**driveItem**</span><span class="sxs-lookup"><span data-stu-id="f67a5-124">**driveItem**</span></span>     | <span data-ttu-id="f67a5-125">[**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="f67a5-125">[**driveItem**][driveItem]</span></span>   | <span data-ttu-id="f67a5-126">Usado para obtener acceso al recurso **driveItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="f67a5-126">Used to access the underlying **driveItem**</span></span>
| <span data-ttu-id="f67a5-127">**list**</span><span class="sxs-lookup"><span data-stu-id="f67a5-127">**list**</span></span>          | <span data-ttu-id="f67a5-128">[**list**][list]</span><span class="sxs-lookup"><span data-stu-id="f67a5-128">[**list**][list]</span></span>        | <span data-ttu-id="f67a5-129">Usado para obtener acceso al recurso **list** subyacente.</span><span class="sxs-lookup"><span data-stu-id="f67a5-129">Used to access the underlying **list**</span></span>
| <span data-ttu-id="f67a5-130">**listItem**</span><span class="sxs-lookup"><span data-stu-id="f67a5-130">**listItem**</span></span>      | <span data-ttu-id="f67a5-131">[**listItem**][listItem]</span><span class="sxs-lookup"><span data-stu-id="f67a5-131">[**listItem**][listItem]</span></span>    | <span data-ttu-id="f67a5-132">Usado para obtener acceso al recurso **listItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="f67a5-132">Used to access the underlying **listItem**</span></span>
| <span data-ttu-id="f67a5-133">**site**</span><span class="sxs-lookup"><span data-stu-id="f67a5-133">**site**</span></span>          | <span data-ttu-id="f67a5-134">[**site**][site]</span><span class="sxs-lookup"><span data-stu-id="f67a5-134">[**site**][site]</span></span>        | <span data-ttu-id="f67a5-135">Usado para obtener acceso al recurso **site** subyacente.</span><span class="sxs-lookup"><span data-stu-id="f67a5-135">Used to access the underlying **site**</span></span>

<span data-ttu-id="f67a5-136">O bien, para recursos **driveItem** compartidos de cuentas personales de OneDrive, también se pueden usar las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="f67a5-136">Alternatively, for **driveItems** shared from personal OneDrive accounts, the following relationships may also be used.</span></span>

| <span data-ttu-id="f67a5-137">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="f67a5-137">Relationship name</span></span> | <span data-ttu-id="f67a5-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="f67a5-138">Type</span></span>                         | <span data-ttu-id="f67a5-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="f67a5-139">Description</span></span>
| ------------------|:-----------------------------|:-----------------------------------
| <span data-ttu-id="f67a5-140">**items**</span><span class="sxs-lookup"><span data-stu-id="f67a5-140">**items**</span></span>         | <span data-ttu-id="f67a5-141">Colección [**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="f67a5-141">[**driveItem**][driveItem] collection</span></span> | <span data-ttu-id="f67a5-142">Todos los recursos driveItem que se incluyen en la raíz de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="f67a5-142">All driveItems contained in the sharing root.</span></span> <span data-ttu-id="f67a5-143">Esta colección no se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="f67a5-143">This collection cannot be enumerated.</span></span>
| <span data-ttu-id="f67a5-144">**root**</span><span class="sxs-lookup"><span data-stu-id="f67a5-144">**root**</span></span>          | <span data-ttu-id="f67a5-145">[**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="f67a5-145">[**driveItem**][driveItem]</span></span>   | <span data-ttu-id="f67a5-146">Se usa para tener acceso a la **driveItem**de subyacente.</span><span class="sxs-lookup"><span data-stu-id="f67a5-146">Used to access the underlying **driveItem**.</span></span> <span data-ttu-id="f67a5-147">En desuso--usar `driveItem` en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f67a5-147">Deprecated -- use `driveItem` instead.</span></span>

[driveItem]: driveitem.md
[list]: list.md
[listItem]: listitem.md
[site]: site.md

## <a name="methods"></a><span data-ttu-id="f67a5-148">Métodos</span><span class="sxs-lookup"><span data-stu-id="f67a5-148">Methods</span></span>

| <span data-ttu-id="f67a5-149">Método</span><span class="sxs-lookup"><span data-stu-id="f67a5-149">Method</span></span>                                  | <span data-ttu-id="f67a5-150">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="f67a5-150">REST Path</span></span>                |
| :-------------------------------------- | :----------------------- |
| [<span data-ttu-id="f67a5-151">Obtener el elemento compartido</span><span class="sxs-lookup"><span data-stu-id="f67a5-151">Get shared item</span></span>](../api/shares-get.md) | `GET /shares/{share-id}` |

## <a name="remarks"></a><span data-ttu-id="f67a5-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f67a5-152">Remarks</span></span>

<span data-ttu-id="f67a5-153">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="f67a5-153">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Share resource returns information about a shared item or collection of items.",
  "keywords": "share,shared,sharing root,shared files, shared items",
  "section": "documentation",
  "tocPath": "Resources/Share"
} -->
