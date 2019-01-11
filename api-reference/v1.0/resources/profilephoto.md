---
title: Tipo de recurso profilePhoto
description: Foto de perfil de un usuario, grupo o un contacto de Outlook al que se accede desde Exchange Online. Son datos binarios no codificados en base 64.
localization_priority: Priority
ms.openlocfilehash: b1901928a97356b2a9808a446d34981fd74bf456
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876569"
---
# <a name="profilephoto-resource-type"></a><span data-ttu-id="64dda-104">Tipo de recurso profilePhoto</span><span class="sxs-lookup"><span data-stu-id="64dda-104">profilePhoto resource type</span></span>
<span data-ttu-id="64dda-p102">Foto de perfil de un usuario, grupo o un contacto de Outlook al que se accede desde Exchange Online. Son datos binarios no codificados en base 64.</span><span class="sxs-lookup"><span data-stu-id="64dda-p102">A profile photo of a user, group or an Outlook contact accessed from Exchange Online. It's binary data not encoded in base-64.</span></span>

<span data-ttu-id="64dda-107">Los tamaños de fotos HD admitidos en Exchange Online son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'.</span><span class="sxs-lookup"><span data-stu-id="64dda-107">The supported sizes of HD photos on Exchange Online are as follows: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504', and '648x648'.</span></span> 

## <a name="methods"></a><span data-ttu-id="64dda-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="64dda-108">Methods</span></span>

| <span data-ttu-id="64dda-109">Método</span><span class="sxs-lookup"><span data-stu-id="64dda-109">Method</span></span>       | <span data-ttu-id="64dda-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64dda-110">Return Type</span></span>  |<span data-ttu-id="64dda-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="64dda-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="64dda-112">Get profilePhoto</span><span class="sxs-lookup"><span data-stu-id="64dda-112">Get profilePhoto</span></span>](../api/profilephoto-get.md) | [<span data-ttu-id="64dda-113">profilePhoto</span><span class="sxs-lookup"><span data-stu-id="64dda-113">profilePhoto</span></span>](profilephoto.md) |<span data-ttu-id="64dda-114">Obtiene el **profilePhoto** especificado o sus metadatos (propiedades profilePhoto).</span><span class="sxs-lookup"><span data-stu-id="64dda-114">Get the specified **profilePhoto** or its metadata (profilePhoto properties).</span></span>|
|[<span data-ttu-id="64dda-115">Update</span><span class="sxs-lookup"><span data-stu-id="64dda-115">Update</span></span>](../api/profilephoto-update.md) | [<span data-ttu-id="64dda-116">profilePhoto</span><span class="sxs-lookup"><span data-stu-id="64dda-116">profilePhoto</span></span>](profilephoto.md)  |<span data-ttu-id="64dda-p103">Asigna una foto al usuario, grupo o contacto que se especifique. La foto debe estar en formato binario. Reemplaza la foto existente, si existe.</span><span class="sxs-lookup"><span data-stu-id="64dda-p103">Assign a photo to the specified user, group, or contact. The photo should be in binary. It replaces the existing photo, if any.</span></span>|

## <a name="properties"></a><span data-ttu-id="64dda-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="64dda-120">Properties</span></span>
| <span data-ttu-id="64dda-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="64dda-121">Property</span></span>     | <span data-ttu-id="64dda-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="64dda-122">Type</span></span>   |<span data-ttu-id="64dda-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="64dda-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="64dda-124">id</span><span class="sxs-lookup"><span data-stu-id="64dda-124">id</span></span>|<span data-ttu-id="64dda-125">string</span><span class="sxs-lookup"><span data-stu-id="64dda-125">string</span></span>|<span data-ttu-id="64dda-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="64dda-126">Read-only.</span></span>|
|<span data-ttu-id="64dda-127">height</span><span class="sxs-lookup"><span data-stu-id="64dda-127">height</span></span>|<span data-ttu-id="64dda-128">int32</span><span class="sxs-lookup"><span data-stu-id="64dda-128">int32</span></span>|<span data-ttu-id="64dda-p104">Alto de la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="64dda-p104">The height of the photo. Read-only.</span></span>|
|<span data-ttu-id="64dda-131">width</span><span class="sxs-lookup"><span data-stu-id="64dda-131">width</span></span>|<span data-ttu-id="64dda-132">int32</span><span class="sxs-lookup"><span data-stu-id="64dda-132">int32</span></span>|<span data-ttu-id="64dda-p105">Ancho de la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="64dda-p105">The width of the photo. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="64dda-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="64dda-135">Relationships</span></span>
<span data-ttu-id="64dda-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="64dda-136">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="64dda-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="64dda-137">JSON representation</span></span>

<span data-ttu-id="64dda-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="64dda-138">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "isMediaEntity": true,
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.profilePhoto"
}-->

```json
{
  "id": "240X240",
  "height": 240,
  "width": 240
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "profilePhoto resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
