---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: BaseItem
ms.openlocfilehash: eaf73cf54671393b61cc37b5a5d1922060640882
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029837"
---
# <a name="baseitem-resource-type"></a><span data-ttu-id="2501d-102">Tipo de recurso BaseItem</span><span class="sxs-lookup"><span data-stu-id="2501d-102">BaseItem resource type</span></span>

<span data-ttu-id="2501d-p101">El recurso **baseItem** es un recurso abstracto que contiene un conjunto común de propiedades compartidas entre varios tipos de recursos. Recursos derivados de **baseItem**:</span><span class="sxs-lookup"><span data-stu-id="2501d-p101">The **baseItem** resource is an abstract resource that contains a common set of properties shared among several other resources types. Resources that derive from **baseItem** include:</span></span>

* [<span data-ttu-id="2501d-105">drive</span><span class="sxs-lookup"><span data-stu-id="2501d-105">drive</span></span>](drive.md)
* [<span data-ttu-id="2501d-106">driveItem</span><span class="sxs-lookup"><span data-stu-id="2501d-106">driveItem</span></span>](driveitem.md)
* [<span data-ttu-id="2501d-107">site</span><span class="sxs-lookup"><span data-stu-id="2501d-107">site</span></span>](site.md)
* [<span data-ttu-id="2501d-108">sharedDriveItem</span><span class="sxs-lookup"><span data-stu-id="2501d-108">sharedDriveItem</span></span>](shareddriveitem.md)

## <a name="json-representation"></a><span data-ttu-id="2501d-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2501d-109">JSON representation</span></span>

<span data-ttu-id="2501d-110">A continuación se incluye una representación JSON del recurso **baseItem**.</span><span class="sxs-lookup"><span data-stu-id="2501d-110">Here is a JSON representation of a **baseItem** resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "createdBy", "lastModifiedBy", "description", "parentReference", "webUrl" ],
  "keyProperty": "id",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.baseItem"
}-->

```json
{
  "id": "string (identifier)",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "datetime",
  "name": "string",
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="2501d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2501d-111">Properties</span></span>

| <span data-ttu-id="2501d-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2501d-112">Property</span></span>             | <span data-ttu-id="2501d-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="2501d-113">Type</span></span>              | <span data-ttu-id="2501d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2501d-114">Description</span></span>                                                                            |
| :------------------- | :---------------- | :------------------------------------------------------------------------------------- |
| <span data-ttu-id="2501d-115">id</span><span class="sxs-lookup"><span data-stu-id="2501d-115">id</span></span>                   | <span data-ttu-id="2501d-116">string</span><span class="sxs-lookup"><span data-stu-id="2501d-116">string</span></span>            | <span data-ttu-id="2501d-p102">El identificador único de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p102">The unique identifier of the drive. Read-only.</span></span>                                         |
| <span data-ttu-id="2501d-119">createdBy</span><span class="sxs-lookup"><span data-stu-id="2501d-119">createdBy</span></span>            | <span data-ttu-id="2501d-120">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="2501d-120">[identitySet][]</span></span>   | <span data-ttu-id="2501d-p103">Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p103">Identity of the user, device, or application which created the item. Read-only.</span></span>        |
| <span data-ttu-id="2501d-123">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2501d-123">createdDateTime</span></span>      | <span data-ttu-id="2501d-124">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2501d-124">dateTimeOffset</span></span>    | <span data-ttu-id="2501d-p104">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p104">Date and time of item creation. Read-only.</span></span>                                             |
| <span data-ttu-id="2501d-127">description</span><span class="sxs-lookup"><span data-stu-id="2501d-127">description</span></span>          | <span data-ttu-id="2501d-128">String</span><span class="sxs-lookup"><span data-stu-id="2501d-128">String</span></span>            | <span data-ttu-id="2501d-129">Proporciona una descripción del elemento visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="2501d-129">Provides a user-visible description of the item.</span></span> <span data-ttu-id="2501d-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2501d-130">Optional.</span></span>                             |
| <span data-ttu-id="2501d-131">eTag</span><span class="sxs-lookup"><span data-stu-id="2501d-131">eTag</span></span>                 | <span data-ttu-id="2501d-132">string</span><span class="sxs-lookup"><span data-stu-id="2501d-132">string</span></span>            | <span data-ttu-id="2501d-p106">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p106">ETag for the item. Read-only.</span></span>                                                          |
| <span data-ttu-id="2501d-135">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="2501d-135">lastModifiedBy</span></span>       | <span data-ttu-id="2501d-136">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="2501d-136">[identitySet][]</span></span>   | <span data-ttu-id="2501d-p107">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p107">Identity of the user, device, and application which last modified the item. Read-only.</span></span> |
| <span data-ttu-id="2501d-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2501d-139">lastModifiedDateTime</span></span> | <span data-ttu-id="2501d-140">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2501d-140">dateTimeOffset</span></span>    | <span data-ttu-id="2501d-p108">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p108">Date and time the item was last modified. Read-only.</span></span>                                   |
| <span data-ttu-id="2501d-143">name</span><span class="sxs-lookup"><span data-stu-id="2501d-143">name</span></span>                 | <span data-ttu-id="2501d-144">string</span><span class="sxs-lookup"><span data-stu-id="2501d-144">string</span></span>            | <span data-ttu-id="2501d-p109">Nombre del elemento. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p109">The name of the item. Read-write.</span></span>                                                      |
| <span data-ttu-id="2501d-147">parentReference</span><span class="sxs-lookup"><span data-stu-id="2501d-147">parentReference</span></span>      | <span data-ttu-id="2501d-148">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="2501d-148">[itemReference][]</span></span> | <span data-ttu-id="2501d-p110">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p110">Parent information, if the item has a parent. Read-write.</span></span>                              |
| <span data-ttu-id="2501d-151">webUrl</span><span class="sxs-lookup"><span data-stu-id="2501d-151">webUrl</span></span>               | <span data-ttu-id="2501d-152">string (url)</span><span class="sxs-lookup"><span data-stu-id="2501d-152">string (url)</span></span>      | <span data-ttu-id="2501d-p111">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-p111">URL that displays the resource in the browser. Read-only.</span></span>                              |

## <a name="relationships"></a><span data-ttu-id="2501d-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2501d-155">Relationships</span></span>

| <span data-ttu-id="2501d-156">Relación</span><span class="sxs-lookup"><span data-stu-id="2501d-156">Relationship</span></span>       | <span data-ttu-id="2501d-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="2501d-157">Type</span></span>     | <span data-ttu-id="2501d-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="2501d-158">Description</span></span>
|:-------------------|:---------|:---------------------------------------------
| <span data-ttu-id="2501d-159">createdByUser</span><span class="sxs-lookup"><span data-stu-id="2501d-159">createdByUser</span></span>      | <span data-ttu-id="2501d-160">[user][]</span><span class="sxs-lookup"><span data-stu-id="2501d-160">[user][]</span></span> | <span data-ttu-id="2501d-161">Identidad del usuario que ha creado el elemento.</span><span class="sxs-lookup"><span data-stu-id="2501d-161">Identity of the user who created the item.</span></span> <span data-ttu-id="2501d-162">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-162">Read-only.</span></span>
| <span data-ttu-id="2501d-163">lastModifiedByUser</span><span class="sxs-lookup"><span data-stu-id="2501d-163">lastModifiedByUser</span></span> | <span data-ttu-id="2501d-164">[user][]</span><span class="sxs-lookup"><span data-stu-id="2501d-164">[user][]</span></span> | <span data-ttu-id="2501d-165">Identidad del usuario que ha modificado por última vez el elemento.</span><span class="sxs-lookup"><span data-stu-id="2501d-165">Identity of the user who last modified the item.</span></span> <span data-ttu-id="2501d-166">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2501d-166">Read-only.</span></span>

[identitySet]: identityset.md
[itemReference]: itemreference.md
[user]: user.md

## <a name="remarks"></a><span data-ttu-id="2501d-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2501d-170">Remarks</span></span>

<span data-ttu-id="2501d-171">El tipo `baseItem` no debe utilizarse directamente.</span><span class="sxs-lookup"><span data-stu-id="2501d-171">The `baseItem` type is not expected to be used directly.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/BaseItem"
} -->
