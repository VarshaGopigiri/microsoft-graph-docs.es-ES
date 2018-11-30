---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: BaseItem
ms.openlocfilehash: d70a75be0be4d7ecbd010288cb313b8394736932
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091082"
---
# <a name="baseitem-resource-type"></a><span data-ttu-id="53b22-102">Tipo de recurso BaseItem</span><span class="sxs-lookup"><span data-stu-id="53b22-102">BaseItem resource type</span></span>

> <span data-ttu-id="53b22-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53b22-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53b22-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53b22-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53b22-p102">El recurso **baseItem** es un recurso abstracto que contiene un conjunto común de propiedades compartidas entre varios tipos de recursos. Recursos derivados de **baseItem**:</span><span class="sxs-lookup"><span data-stu-id="53b22-p102">The **baseItem** resource is an abstract resource that contains a common set of properties shared among several other resources types. Resources that derive from **baseItem** include:</span></span>

* [<span data-ttu-id="53b22-107">drive</span><span class="sxs-lookup"><span data-stu-id="53b22-107">drive</span></span>](drive.md)
* [<span data-ttu-id="53b22-108">driveItem</span><span class="sxs-lookup"><span data-stu-id="53b22-108">driveItem</span></span>](driveitem.md)
* [<span data-ttu-id="53b22-109">site</span><span class="sxs-lookup"><span data-stu-id="53b22-109">site</span></span>](site.md)
* [<span data-ttu-id="53b22-110">sharedDriveItem</span><span class="sxs-lookup"><span data-stu-id="53b22-110">sharedDriveItem</span></span>](shareddriveitem.md)

## <a name="json-representation"></a><span data-ttu-id="53b22-111">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53b22-111">JSON representation</span></span>

<span data-ttu-id="53b22-112">A continuación se incluye una representación JSON del recurso **baseItem**.</span><span class="sxs-lookup"><span data-stu-id="53b22-112">Here is a JSON representation of a **baseItem** resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="53b22-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53b22-113">Properties</span></span>

| <span data-ttu-id="53b22-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53b22-114">Property</span></span>             | <span data-ttu-id="53b22-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="53b22-115">Type</span></span>              | <span data-ttu-id="53b22-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="53b22-116">Description</span></span>                                                                            |
| :------------------- | :---------------- | :------------------------------------------------------------------------------------- |
| <span data-ttu-id="53b22-117">id</span><span class="sxs-lookup"><span data-stu-id="53b22-117">id</span></span>                   | <span data-ttu-id="53b22-118">string</span><span class="sxs-lookup"><span data-stu-id="53b22-118">string</span></span>            | <span data-ttu-id="53b22-p103">El identificador único de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p103">The unique identifier of the drive. Read-only.</span></span>                                         |
| <span data-ttu-id="53b22-121">createdBy</span><span class="sxs-lookup"><span data-stu-id="53b22-121">createdBy</span></span>            | <span data-ttu-id="53b22-122">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="53b22-122">[identitySet][]</span></span>   | <span data-ttu-id="53b22-p104">Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p104">Identity of the user, device, or application which created the item. Read-only.</span></span>        |
| <span data-ttu-id="53b22-125">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="53b22-125">createdDateTime</span></span>      | <span data-ttu-id="53b22-126">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53b22-126">dateTimeOffset</span></span>    | <span data-ttu-id="53b22-p105">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p105">Date and time of item creation. Read-only.</span></span>                                             |
| <span data-ttu-id="53b22-129">eTag</span><span class="sxs-lookup"><span data-stu-id="53b22-129">eTag</span></span>                 | <span data-ttu-id="53b22-130">string</span><span class="sxs-lookup"><span data-stu-id="53b22-130">string</span></span>            | <span data-ttu-id="53b22-p106">ETag para el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p106">ETag for the item. Read-only.</span></span>                                                          |
| <span data-ttu-id="53b22-133">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="53b22-133">lastModifiedBy</span></span>       | <span data-ttu-id="53b22-134">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="53b22-134">[identitySet][]</span></span>   | <span data-ttu-id="53b22-p107">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p107">Identity of the user, device, and application which last modified the item. Read-only.</span></span> |
| <span data-ttu-id="53b22-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="53b22-137">lastModifiedDateTime</span></span> | <span data-ttu-id="53b22-138">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53b22-138">dateTimeOffset</span></span>    | <span data-ttu-id="53b22-p108">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p108">Date and time the item was last modified. Read-only.</span></span>                                   |
| <span data-ttu-id="53b22-141">name</span><span class="sxs-lookup"><span data-stu-id="53b22-141">name</span></span>                 | <span data-ttu-id="53b22-142">string</span><span class="sxs-lookup"><span data-stu-id="53b22-142">string</span></span>            | <span data-ttu-id="53b22-p109">Nombre del elemento. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p109">The name of the item. Read-write.</span></span>                                                      |
| <span data-ttu-id="53b22-145">parentReference</span><span class="sxs-lookup"><span data-stu-id="53b22-145">parentReference</span></span>      | <span data-ttu-id="53b22-146">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="53b22-146">[itemReference][]</span></span> | <span data-ttu-id="53b22-p110">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p110">Parent information, if the item has a parent. Read-write.</span></span>                              |
| <span data-ttu-id="53b22-149">webUrl</span><span class="sxs-lookup"><span data-stu-id="53b22-149">webUrl</span></span>               | <span data-ttu-id="53b22-150">string (url)</span><span class="sxs-lookup"><span data-stu-id="53b22-150">string (url)</span></span>      | <span data-ttu-id="53b22-p111">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53b22-p111">URL that displays the resource in the browser. Read-only.</span></span>                              |

[identitySet]: identityset.md
[itemReference]: itemreference.md

## <a name="remarks"></a><span data-ttu-id="53b22-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53b22-155">Remarks</span></span>

<span data-ttu-id="53b22-156">El tipo `baseItem` no debe utilizarse directamente.</span><span class="sxs-lookup"><span data-stu-id="53b22-156">The `baseItem` type is not expected to be used directly.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/BaseItem"
} -->
