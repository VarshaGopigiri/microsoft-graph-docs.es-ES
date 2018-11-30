---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharedDriveItem
ms.openlocfilehash: 3b4497c1a15704388dbb4bb4ba181d3985d65a69
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="shareddriveitem-resource-type"></a><span data-ttu-id="25647-102">Tipo de recurso de SharedDriveItem</span><span class="sxs-lookup"><span data-stu-id="25647-102">SharedDriveItem resource type</span></span>

<span data-ttu-id="25647-103">El recurso **sharedDriveItem** se devuelve al usar la API [Shares](../api/shares_get.md) para obtener acceso a un objeto [driveItem](driveitem.md) compartido.</span><span class="sxs-lookup"><span data-stu-id="25647-103">The **sharedDriveItem** resource is returned when using the [Shares](../api/shares_get.md) API to access a shared [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="25647-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25647-104">JSON representation</span></span>

<span data-ttu-id="25647-105">A continuación se incluye una representación JSON del recurso **sharedDriveItem**.</span><span class="sxs-lookup"><span data-stu-id="25647-105">Here is a JSON representation of the **sharedDriveItem** resource.</span></span>

<span data-ttu-id="25647-106">El recurso **sharedDriveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="25647-106">The **sharedDriveItem** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.sharedDriveItem"
}-->

```json
{
  "id": "string",
  "name": "string",
  "owner": { "@odata.type": "microsoft.graph.identitySet" },

  "driveItem": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "items": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "list": { "@odata.type": "microsoft.graph.list" },
  "listItem": { "@odata.type": "microsoft.graph.listItem" },
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "site": { "@odata.type": "microsoft.graph.site" }
}
```

## <a name="properties"></a><span data-ttu-id="25647-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25647-107">Properties</span></span>

| <span data-ttu-id="25647-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25647-108">Property</span></span> | <span data-ttu-id="25647-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="25647-109">Type</span></span>                          | <span data-ttu-id="25647-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="25647-110">Description</span></span>                                                      |
| :------- | :---------------------------- | :--------------------------------------------------------------- |
| <span data-ttu-id="25647-111">id</span><span class="sxs-lookup"><span data-stu-id="25647-111">id</span></span>       | <span data-ttu-id="25647-112">String</span><span class="sxs-lookup"><span data-stu-id="25647-112">String</span></span>                        | <span data-ttu-id="25647-113">El identificador único del recurso compartido al que se accede.</span><span class="sxs-lookup"><span data-stu-id="25647-113">The unique identifier for the share being accessed.</span></span>              |
| <span data-ttu-id="25647-114">name</span><span class="sxs-lookup"><span data-stu-id="25647-114">name</span></span>     | <span data-ttu-id="25647-115">String</span><span class="sxs-lookup"><span data-stu-id="25647-115">String</span></span>                        | <span data-ttu-id="25647-116">El nombre para mostrar del elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="25647-116">The display name of the shared item.</span></span>                             |
| <span data-ttu-id="25647-117">owner</span><span class="sxs-lookup"><span data-stu-id="25647-117">owner</span></span>    | [<span data-ttu-id="25647-118">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="25647-118">IdentitySet</span></span>](identityset.md) | <span data-ttu-id="25647-119">Información sobre el propietario del elemento compartido al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="25647-119">Information about the owner of the shared item being referenced.</span></span> |

## <a name="relationships"></a><span data-ttu-id="25647-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="25647-120">Relationships</span></span>

| <span data-ttu-id="25647-121">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="25647-121">Relationship name</span></span> | <span data-ttu-id="25647-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="25647-122">Type</span></span>                | <span data-ttu-id="25647-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="25647-123">Description</span></span>
| ------------------|:--------------------|:-----------------------------------
| <span data-ttu-id="25647-124">**driveItem**</span><span class="sxs-lookup"><span data-stu-id="25647-124">**DriveItem**</span></span>     | <span data-ttu-id="25647-125">[**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="25647-125">DriveItem</span></span>   | <span data-ttu-id="25647-126">Usado para obtener acceso al recurso **driveItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="25647-126">Used to access the underlying **driveItem**</span></span>
| <span data-ttu-id="25647-127">**list**</span><span class="sxs-lookup"><span data-stu-id="25647-127">**list**</span></span>          | <span data-ttu-id="25647-128">[**list**][list]</span><span class="sxs-lookup"><span data-stu-id="25647-128">List</span></span>        | <span data-ttu-id="25647-129">Usado para obtener acceso al recurso **list** subyacente.</span><span class="sxs-lookup"><span data-stu-id="25647-129">Used to access the underlying **list**</span></span>
| <span data-ttu-id="25647-130">**listItem**</span><span class="sxs-lookup"><span data-stu-id="25647-130">**listItem**</span></span>      | <span data-ttu-id="25647-131">[**listItem**][listItem]</span><span class="sxs-lookup"><span data-stu-id="25647-131">**ListItem**</span></span>    | <span data-ttu-id="25647-132">Usado para obtener acceso al recurso **listItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="25647-132">Used to access the underlying **listItem**</span></span>
| <span data-ttu-id="25647-133">**site**</span><span class="sxs-lookup"><span data-stu-id="25647-133">**site**</span></span>          | <span data-ttu-id="25647-134">[**site**][site]</span><span class="sxs-lookup"><span data-stu-id="25647-134">**Site**</span></span>        | <span data-ttu-id="25647-135">Usado para obtener acceso al recurso **site** subyacente.</span><span class="sxs-lookup"><span data-stu-id="25647-135">Used to access the underlying **site**</span></span>


<span data-ttu-id="25647-136">O bien, para recursos **driveItem** compartidos de cuentas personales de OneDrive, también se pueden usar las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="25647-136">Alternatively, for **driveItems** shared from personal OneDrive accounts, the following relationships may also be used.</span></span>

| <span data-ttu-id="25647-137">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="25647-137">Relationship name</span></span> | <span data-ttu-id="25647-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="25647-138">Type</span></span>                         | <span data-ttu-id="25647-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="25647-139">Description</span></span>
| ------------------|:-----------------------------|:-----------------------------------
| <span data-ttu-id="25647-140">**items**</span><span class="sxs-lookup"><span data-stu-id="25647-140">**items**</span></span>         | <span data-ttu-id="25647-141">Colección [**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="25647-141">**driveItem** collection</span></span> | <span data-ttu-id="25647-142">Todos los recursos driveItem que se incluyen en la raíz de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="25647-142">All items contained in the sharing root.</span></span> <span data-ttu-id="25647-143">Esta colección no se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="25647-143">This collection cannot be enumerated.</span></span>
| <span data-ttu-id="25647-144">**driveItem**</span><span class="sxs-lookup"><span data-stu-id="25647-144">**DriveItem**</span></span>     | <span data-ttu-id="25647-145">[**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="25647-145">DriveItem</span></span>            | <span data-ttu-id="25647-146">Usado para obtener acceso al recurso **driveItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="25647-146">Used to access the underlying **driveItem**</span></span>

[driveItem]: driveItem.md
[list]: list.md
[listItem]: listItem.md
[site]: site.md

## <a name="methods"></a><span data-ttu-id="25647-147">Métodos</span><span class="sxs-lookup"><span data-stu-id="25647-147">Methods</span></span>

| <span data-ttu-id="25647-148">Método</span><span class="sxs-lookup"><span data-stu-id="25647-148">Method</span></span>                                  | <span data-ttu-id="25647-149">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="25647-149">REST Path</span></span>                |
| :-------------------------------------- | :----------------------- |
| [<span data-ttu-id="25647-150">Obtener el elemento compartido</span><span class="sxs-lookup"><span data-stu-id="25647-150">Get shared item</span></span>](../api/shares_get.md) | `GET /shares/{share-id}` |

## <a name="remarks"></a><span data-ttu-id="25647-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25647-151">Remarks</span></span>

<span data-ttu-id="25647-152">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="25647-152">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Share resource returns information about a shared item or collection of items.",
  "keywords": "share,shared,sharing root,shared files, shared items",
  "section": "documentation",
  "tocPath": "Resources/Share"
} -->
