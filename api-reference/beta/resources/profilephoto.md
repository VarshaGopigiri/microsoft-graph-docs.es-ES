---
title: Tipo de recurso profilePhoto
description: Una imagen de perfil de un usuario, grupo o un contacto de Outlook tiene acceso desde Exchange Online o Azure Active Directory (AAD). Es datos binarios no codificados en base-64.
localization_priority: Normal
ms.openlocfilehash: 7754d70c4e59b13b1b0003022ddc0f185cc18ae2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837074"
---
# <a name="profilephoto-resource-type"></a><span data-ttu-id="dc64e-104">Tipo de recurso profilePhoto</span><span class="sxs-lookup"><span data-stu-id="dc64e-104">profilePhoto resource type</span></span>

> <span data-ttu-id="dc64e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dc64e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dc64e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dc64e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dc64e-107">Una imagen de perfil de un usuario, grupo o un contacto de Outlook tiene acceso desde Exchange Online o Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="dc64e-107">A profile photo of a user, group or an Outlook contact accessed from Exchange Online or Azure Active Directory (AAD).</span></span> <span data-ttu-id="dc64e-108">Es datos binarios no codificados en base-64.</span><span class="sxs-lookup"><span data-stu-id="dc64e-108">It's binary data not encoded in base-64.</span></span>

<span data-ttu-id="dc64e-109">Los tamaños de fotos HD admitidos en Exchange Online son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'.</span><span class="sxs-lookup"><span data-stu-id="dc64e-109">The supported sizes of HD photos on Exchange Online are as follows: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504', and '648x648'.</span></span> <span data-ttu-id="dc64e-110">En AAD, fotos pueden ser cualquier dimensión.</span><span class="sxs-lookup"><span data-stu-id="dc64e-110">On AAD, photos can be any dimension.</span></span>

## <a name="methods"></a><span data-ttu-id="dc64e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc64e-111">Methods</span></span>

| <span data-ttu-id="dc64e-112">Método</span><span class="sxs-lookup"><span data-stu-id="dc64e-112">Method</span></span>       | <span data-ttu-id="dc64e-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc64e-113">Return Type</span></span>  |<span data-ttu-id="dc64e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc64e-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="dc64e-115">Get profilePhoto</span><span class="sxs-lookup"><span data-stu-id="dc64e-115">Get profilePhoto</span></span>](../api/profilephoto-get.md) | [<span data-ttu-id="dc64e-116">profilePhoto</span><span class="sxs-lookup"><span data-stu-id="dc64e-116">profilePhoto</span></span>](profilephoto.md) |<span data-ttu-id="dc64e-117">Obtenga el especificado **profilePhoto** o sus metadatos (propiedades de**profilePhoto** ).</span><span class="sxs-lookup"><span data-stu-id="dc64e-117">Get the specified **profilePhoto** or its metadata (**profilePhoto** properties).</span></span> |
|[<span data-ttu-id="dc64e-118">Update</span><span class="sxs-lookup"><span data-stu-id="dc64e-118">Update</span></span>](../api/profilephoto-update.md) | [<span data-ttu-id="dc64e-119">profilePhoto</span><span class="sxs-lookup"><span data-stu-id="dc64e-119">profilePhoto</span></span>](profilephoto.md)  |<span data-ttu-id="dc64e-p105">Asigna una foto al usuario, grupo o contacto que se especifique. La foto debe estar en formato binario. Reemplaza la foto existente, si existe.</span><span class="sxs-lookup"><span data-stu-id="dc64e-p105">Assign a photo to the specified user, group, or contact. The photo should be in binary. It replaces the existing photo, if any.</span></span> |

## <a name="properties"></a><span data-ttu-id="dc64e-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dc64e-123">Properties</span></span>
| <span data-ttu-id="dc64e-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dc64e-124">Property</span></span>     | <span data-ttu-id="dc64e-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc64e-125">Type</span></span>   |<span data-ttu-id="dc64e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc64e-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dc64e-127">id</span><span class="sxs-lookup"><span data-stu-id="dc64e-127">id</span></span>|<span data-ttu-id="dc64e-128">string</span><span class="sxs-lookup"><span data-stu-id="dc64e-128">string</span></span>|<span data-ttu-id="dc64e-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dc64e-129">Read-only.</span></span>|
|<span data-ttu-id="dc64e-130">height</span><span class="sxs-lookup"><span data-stu-id="dc64e-130">height</span></span>|<span data-ttu-id="dc64e-131">int32</span><span class="sxs-lookup"><span data-stu-id="dc64e-131">int32</span></span>|<span data-ttu-id="dc64e-p106">Alto de la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dc64e-p106">The height of the photo. Read-only.</span></span>|
|<span data-ttu-id="dc64e-134">width</span><span class="sxs-lookup"><span data-stu-id="dc64e-134">width</span></span>|<span data-ttu-id="dc64e-135">int32</span><span class="sxs-lookup"><span data-stu-id="dc64e-135">int32</span></span>|<span data-ttu-id="dc64e-p107">Ancho de la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dc64e-p107">The width of the photo. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="dc64e-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dc64e-138">Relationships</span></span>
<span data-ttu-id="dc64e-139">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dc64e-139">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="dc64e-140">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dc64e-140">JSON representation</span></span>

<span data-ttu-id="dc64e-141">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="dc64e-141">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
