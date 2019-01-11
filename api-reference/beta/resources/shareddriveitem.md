---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharedDriveItem
localization_priority: Normal
ms.openlocfilehash: d20656351725f23d4fd4c00b65fdc88fe2f449b8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853070"
---
# <a name="shareddriveitem-resource-type"></a><span data-ttu-id="19f4f-102">Tipo de recurso SharedDriveItem</span><span class="sxs-lookup"><span data-stu-id="19f4f-102">SharedDriveItem resource type</span></span>

> <span data-ttu-id="19f4f-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="19f4f-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="19f4f-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="19f4f-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="19f4f-105">El recurso **sharedDriveItem** se devuelve al usar la API [Shares](../api/shares-get.md) para obtener acceso a un objeto [driveItem](driveitem.md) compartido.</span><span class="sxs-lookup"><span data-stu-id="19f4f-105">The **sharedDriveItem** resource is returned when using the [Shares](../api/shares-get.md) API to access a shared [driveItem](driveitem.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="19f4f-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="19f4f-106">JSON representation</span></span>

<span data-ttu-id="19f4f-107">A continuación se incluye una representación JSON del recurso **sharedDriveItem**.</span><span class="sxs-lookup"><span data-stu-id="19f4f-107">Here is a JSON representation of the **sharedDriveItem** resource.</span></span>

<span data-ttu-id="19f4f-108">El recurso **sharedDriveItem** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="19f4f-108">The **sharedDriveItem** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

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
  "permission": { "@odata.type": "microsoft.graph.permission" },
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "site": { "@odata.type": "microsoft.graph.site" }
}
```

## <a name="properties"></a><span data-ttu-id="19f4f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19f4f-109">Properties</span></span>

| <span data-ttu-id="19f4f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19f4f-110">Property</span></span> | <span data-ttu-id="19f4f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="19f4f-111">Type</span></span>                          | <span data-ttu-id="19f4f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="19f4f-112">Description</span></span>                                                      |
| :------- | :---------------------------- | :--------------------------------------------------------------- |
| <span data-ttu-id="19f4f-113">id</span><span class="sxs-lookup"><span data-stu-id="19f4f-113">id</span></span>       | <span data-ttu-id="19f4f-114">String</span><span class="sxs-lookup"><span data-stu-id="19f4f-114">String</span></span>                        | <span data-ttu-id="19f4f-115">El identificador único del recurso compartido al que se accede.</span><span class="sxs-lookup"><span data-stu-id="19f4f-115">The unique identifier for the share being accessed.</span></span>              |
| <span data-ttu-id="19f4f-116">name</span><span class="sxs-lookup"><span data-stu-id="19f4f-116">name</span></span>     | <span data-ttu-id="19f4f-117">String</span><span class="sxs-lookup"><span data-stu-id="19f4f-117">String</span></span>                        | <span data-ttu-id="19f4f-118">El nombre para mostrar del elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="19f4f-118">The display name of the shared item.</span></span>                             |
| <span data-ttu-id="19f4f-119">owner</span><span class="sxs-lookup"><span data-stu-id="19f4f-119">owner</span></span>    | [<span data-ttu-id="19f4f-120">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="19f4f-120">IdentitySet</span></span>](identityset.md) | <span data-ttu-id="19f4f-121">Información sobre el propietario del elemento compartido al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="19f4f-121">Information about the owner of the shared item being referenced.</span></span> |

## <a name="relationships"></a><span data-ttu-id="19f4f-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="19f4f-122">Relationships</span></span>

| <span data-ttu-id="19f4f-123">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="19f4f-123">Relationship name</span></span> | <span data-ttu-id="19f4f-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="19f4f-124">Type</span></span>                | <span data-ttu-id="19f4f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="19f4f-125">Description</span></span>
| ------------------|:--------------------|:-----------------------------------
| <span data-ttu-id="19f4f-126">**driveItem**</span><span class="sxs-lookup"><span data-stu-id="19f4f-126">**driveItem**</span></span>     | <span data-ttu-id="19f4f-127">[**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="19f4f-127">[**driveItem**][driveItem]</span></span> | <span data-ttu-id="19f4f-128">Usado para obtener acceso al recurso **driveItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="19f4f-128">Used to access the underlying **driveItem**</span></span>
| <span data-ttu-id="19f4f-129">**list**</span><span class="sxs-lookup"><span data-stu-id="19f4f-129">**list**</span></span>          | <span data-ttu-id="19f4f-130">[**list**][list]</span><span class="sxs-lookup"><span data-stu-id="19f4f-130">[**list**][list]</span></span>           | <span data-ttu-id="19f4f-131">Usado para obtener acceso al recurso **list** subyacente.</span><span class="sxs-lookup"><span data-stu-id="19f4f-131">Used to access the underlying **list**</span></span>
| <span data-ttu-id="19f4f-132">**listItem**</span><span class="sxs-lookup"><span data-stu-id="19f4f-132">**listItem**</span></span>      | <span data-ttu-id="19f4f-133">[**listItem**][listItem]</span><span class="sxs-lookup"><span data-stu-id="19f4f-133">[**listItem**][listItem]</span></span>   | <span data-ttu-id="19f4f-134">Usado para obtener acceso al recurso **listItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="19f4f-134">Used to access the underlying **listItem**</span></span>
| <span data-ttu-id="19f4f-135">**permission**</span><span class="sxs-lookup"><span data-stu-id="19f4f-135">**permission**</span></span>    | <span data-ttu-id="19f4f-136">[**permiso**][permission]</span><span class="sxs-lookup"><span data-stu-id="19f4f-136">[**permission**][permission]</span></span> | <span data-ttu-id="19f4f-137">Utilizado para tener acceso el **permiso** que representa el vínculo de uso compartido subyacente</span><span class="sxs-lookup"><span data-stu-id="19f4f-137">Used to access the **permission** representing the underlying sharing link</span></span>
| <span data-ttu-id="19f4f-138">**site**</span><span class="sxs-lookup"><span data-stu-id="19f4f-138">**site**</span></span>          | <span data-ttu-id="19f4f-139">[**site**][site]</span><span class="sxs-lookup"><span data-stu-id="19f4f-139">[**site**][site]</span></span>           | <span data-ttu-id="19f4f-140">Usado para obtener acceso al recurso **site** subyacente.</span><span class="sxs-lookup"><span data-stu-id="19f4f-140">Used to access the underlying **site**</span></span>

<span data-ttu-id="19f4f-141">O bien, para recursos **driveItem** compartidos de cuentas personales de OneDrive, también se pueden usar las siguientes relaciones.</span><span class="sxs-lookup"><span data-stu-id="19f4f-141">Alternatively, for **driveItems** shared from personal OneDrive accounts, the following relationships may also be used.</span></span>

| <span data-ttu-id="19f4f-142">Nombre de la relación</span><span class="sxs-lookup"><span data-stu-id="19f4f-142">Relationship name</span></span> | <span data-ttu-id="19f4f-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="19f4f-143">Type</span></span>                         | <span data-ttu-id="19f4f-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="19f4f-144">Description</span></span>
| ------------------|:-----------------------------|:-----------------------------------
| <span data-ttu-id="19f4f-145">**items**</span><span class="sxs-lookup"><span data-stu-id="19f4f-145">**items**</span></span>         | <span data-ttu-id="19f4f-146">Colección [**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="19f4f-146">[**driveItem**][driveItem] collection</span></span> | <span data-ttu-id="19f4f-147">Todos los recursos driveItem que se incluyen en la raíz de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="19f4f-147">All driveItems contained in the sharing root.</span></span> <span data-ttu-id="19f4f-148">Esta colección no se puede enumerar.</span><span class="sxs-lookup"><span data-stu-id="19f4f-148">This collection cannot be enumerated.</span></span>
| <span data-ttu-id="19f4f-149">**driveItem**</span><span class="sxs-lookup"><span data-stu-id="19f4f-149">**driveItem**</span></span>     | <span data-ttu-id="19f4f-150">[**driveItem**][driveItem]</span><span class="sxs-lookup"><span data-stu-id="19f4f-150">[**driveItem**][driveItem]</span></span>            | <span data-ttu-id="19f4f-151">Usado para obtener acceso al recurso **driveItem** subyacente.</span><span class="sxs-lookup"><span data-stu-id="19f4f-151">Used to access the underlying **driveItem**</span></span>

[driveItem]: driveitem.md
[list]: list.md
[listItem]: listitem.md
[permission]: permission.md
[site]: site.md

## <a name="methods"></a><span data-ttu-id="19f4f-152">Métodos</span><span class="sxs-lookup"><span data-stu-id="19f4f-152">Methods</span></span>

| <span data-ttu-id="19f4f-153">Método</span><span class="sxs-lookup"><span data-stu-id="19f4f-153">Method</span></span>                                  | <span data-ttu-id="19f4f-154">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="19f4f-154">REST Path</span></span>                |
| :-------------------------------------- | :----------------------- |
| [<span data-ttu-id="19f4f-155">Obtener el elemento compartido</span><span class="sxs-lookup"><span data-stu-id="19f4f-155">Get shared item</span></span>](../api/shares-get.md) | `GET /shares/{share-id}` |

## <a name="remarks"></a><span data-ttu-id="19f4f-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19f4f-156">Remarks</span></span>

<span data-ttu-id="19f4f-157">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="19f4f-157">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Share resource returns information about a shared item or collection of items.",
  "keywords": "share,shared,sharing root,shared files, shared items",
  "section": "documentation",
  "tocPath": "Resources/Share"
} -->
