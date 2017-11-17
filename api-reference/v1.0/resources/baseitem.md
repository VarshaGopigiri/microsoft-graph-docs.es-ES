---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: BaseItem
ms.openlocfilehash: bbfebd734407259c391cdb1ce74beb96dc74d8bf
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="baseitem-resource-type"></a><span data-ttu-id="41762-102">Tipo de recurso BaseItem</span><span class="sxs-lookup"><span data-stu-id="41762-102">BaseItem resource type</span></span>

<span data-ttu-id="41762-p101">El recurso **baseItem** es un recurso abstracto que contiene un conjunto común de propiedades compartidas entre varios tipos de recursos. Recursos derivados de **baseItem**:</span><span class="sxs-lookup"><span data-stu-id="41762-p101">The **baseItem** resource is an abstract resource that contains a common set of properties shared among several other resources types. Resources that derive from **baseItem** include:</span></span>

* [<span data-ttu-id="41762-105">drive</span><span class="sxs-lookup"><span data-stu-id="41762-105">drive</span></span>](drive.md)
* [<span data-ttu-id="41762-106">driveItem</span><span class="sxs-lookup"><span data-stu-id="41762-106">DriveItem</span></span>](driveitem.md)
* [<span data-ttu-id="41762-107">site</span><span class="sxs-lookup"><span data-stu-id="41762-107">site</span></span>](site.md)
* [<span data-ttu-id="41762-108">sharedDriveItem</span><span class="sxs-lookup"><span data-stu-id="41762-108">sharedDriveItem</span></span>](shareddriveitem.md)

## <a name="json-representation"></a><span data-ttu-id="41762-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41762-109">JSON representation</span></span>

<span data-ttu-id="41762-110">A continuación se incluye una representación JSON del recurso **baseItem**.</span><span class="sxs-lookup"><span data-stu-id="41762-110">Here is a JSON representation of a **baseItem** resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "createdBy", "lastModifiedBy", "description", "parentReference", "webUrl" ],
  "keyProperty": "id",
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

## <a name="properties"></a><span data-ttu-id="41762-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41762-111">Properties</span></span>

| <span data-ttu-id="41762-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41762-112">Property</span></span>             | <span data-ttu-id="41762-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="41762-113">Type</span></span>              | <span data-ttu-id="41762-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="41762-114">Description</span></span>                                                                            |
| :------------------- | :---------------- | :------------------------------------------------------------------------------------- |
| <span data-ttu-id="41762-115">id</span><span class="sxs-lookup"><span data-stu-id="41762-115">id</span></span>                   | <span data-ttu-id="41762-116">string</span><span class="sxs-lookup"><span data-stu-id="41762-116">string</span></span>            | <span data-ttu-id="41762-p102">El identificador único de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41762-p102">The unique identifier of the drive. Read-only.</span></span>                                         |
| <span data-ttu-id="41762-119">createdBy</span><span class="sxs-lookup"><span data-stu-id="41762-119">createdBy</span></span>            | <span data-ttu-id="41762-120">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="41762-120">[identitySet][]</span></span>   | <span data-ttu-id="41762-p103">Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41762-p103">Identity of the user, device, or application which created the item. Read-only.</span></span>        |
| <span data-ttu-id="41762-123">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="41762-123">createdDateTime</span></span>      | <span data-ttu-id="41762-124">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41762-124">dateTimeOffset</span></span>    | <span data-ttu-id="41762-p104">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41762-p104">Date and time of item creation. Read-only.</span></span>                                             |
| <span data-ttu-id="41762-127">eTag</span><span class="sxs-lookup"><span data-stu-id="41762-127">eTag</span></span>                 | <span data-ttu-id="41762-128">string</span><span class="sxs-lookup"><span data-stu-id="41762-128">string</span></span>            | <span data-ttu-id="41762-p105">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41762-p105">ETag for the item. Read-only.</span></span>                                                          |
| <span data-ttu-id="41762-131">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="41762-131">lastModifiedBy</span></span>       | <span data-ttu-id="41762-132">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="41762-132">[identitySet][]</span></span>   | <span data-ttu-id="41762-p106">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41762-p106">Identity of the user, device, and application which last modified the item. Read-only.</span></span> |
| <span data-ttu-id="41762-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="41762-135">lastModifiedDateTime</span></span> | <span data-ttu-id="41762-136">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41762-136">dateTimeOffset</span></span>    | <span data-ttu-id="41762-p107">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41762-p107">Date and time the item was last modified. Read-only.</span></span>                                   |
| <span data-ttu-id="41762-139">name</span><span class="sxs-lookup"><span data-stu-id="41762-139">name</span></span>                 | <span data-ttu-id="41762-140">string</span><span class="sxs-lookup"><span data-stu-id="41762-140">string</span></span>            | <span data-ttu-id="41762-p108">Nombre del elemento. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="41762-p108">The name of the item. Read-write.</span></span>                                                      |
| <span data-ttu-id="41762-143">parentReference</span><span class="sxs-lookup"><span data-stu-id="41762-143">parentReference</span></span>      | <span data-ttu-id="41762-144">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="41762-144">[itemReference][]</span></span> | <span data-ttu-id="41762-p109">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="41762-p109">Parent information, if the item has a parent. Read-write.</span></span>                              |
| <span data-ttu-id="41762-147">webUrl</span><span class="sxs-lookup"><span data-stu-id="41762-147">webUrl</span></span>               | <span data-ttu-id="41762-148">string (url)</span><span class="sxs-lookup"><span data-stu-id="41762-148">string (url)</span></span>      | <span data-ttu-id="41762-p110">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41762-p110">URL that displays the resource in the browser. Read-only.</span></span>                              |

[identitySet]: identityset.md
[itemReference]: itemreference.md

## <a name="remarks"></a><span data-ttu-id="41762-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41762-153">Remarks</span></span>

<span data-ttu-id="41762-154">El tipo `baseItem` no debe utilizarse directamente.</span><span class="sxs-lookup"><span data-stu-id="41762-154">The `baseItem` type is not expected to be used directly.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/BaseItem"
} -->
