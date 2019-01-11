---
title: Tipo de recurso extensionSchemaProperty
description: Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición schemaExtension.
localization_priority: Normal
ms.openlocfilehash: 384f60c323ca6c6fb23d2f4811a6d2cb918bf844
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880573"
---
# <a name="extensionschemaproperty-resource-type"></a><span data-ttu-id="548f6-103">Tipo de recurso extensionSchemaProperty</span><span class="sxs-lookup"><span data-stu-id="548f6-103">extensionSchemaProperty resource type</span></span>

<span data-ttu-id="548f6-104">Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición [schemaExtension](schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="548f6-104">Use the **extensionSchemaProperty** resource to define a property's name and its type, as part of a [schemaExtension](schemaextension.md) definition.</span></span>


## <a name="properties"></a><span data-ttu-id="548f6-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="548f6-105">Properties</span></span>
| <span data-ttu-id="548f6-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="548f6-106">Property</span></span>     | <span data-ttu-id="548f6-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="548f6-107">Type</span></span>   |<span data-ttu-id="548f6-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="548f6-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="548f6-109">name</span><span class="sxs-lookup"><span data-stu-id="548f6-109">name</span></span>|<span data-ttu-id="548f6-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="548f6-110">String</span></span>| <span data-ttu-id="548f6-111">El nombre de la propiedad fuertemente tipada definida como parte de una extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="548f6-111">The name of the strongly-typed property defined as part of a schema extension.</span></span>|
|<span data-ttu-id="548f6-112">tipo</span><span class="sxs-lookup"><span data-stu-id="548f6-112">type</span></span>|<span data-ttu-id="548f6-113">String</span><span class="sxs-lookup"><span data-stu-id="548f6-113">String</span></span>| <span data-ttu-id="548f6-p101">Tipo de la propiedad que se define como parte de una extensión de esquema.  Los valores permitidos son *Binary, Boolean, DateTime, Integer* y *String*.  Consulte la tabla siguiente para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="548f6-p101">The type of the property that is defined as part of a schema extension.  Allowed values are *Binary, Boolean, DateTime, Integer* or *String*.  See the table below for more details.</span></span>|

#### <a name="supported-property-data-types"></a><span data-ttu-id="548f6-117">Tipos de datos de propiedad admitidos</span><span class="sxs-lookup"><span data-stu-id="548f6-117">Supported property data types</span></span> 
<span data-ttu-id="548f6-118">Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:</span><span class="sxs-lookup"><span data-stu-id="548f6-118">The following data types are supported when defining a property in a schema extension:</span></span>

| <span data-ttu-id="548f6-119">Tipo de propiedad</span><span class="sxs-lookup"><span data-stu-id="548f6-119">Property Type</span></span> | <span data-ttu-id="548f6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="548f6-120">Remarks</span></span> |
|-------------|------------|
| <span data-ttu-id="548f6-121">Binario</span><span class="sxs-lookup"><span data-stu-id="548f6-121">Binary</span></span> | <span data-ttu-id="548f6-122">Máximo de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="548f6-122">256 bytes maximum.</span></span> |
| <span data-ttu-id="548f6-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="548f6-123">Boolean</span></span> | <span data-ttu-id="548f6-124">No se admite para contactos, mensajes, eventos y publicaciones.</span><span class="sxs-lookup"><span data-stu-id="548f6-124">Not supported for contacts, messages, events and posts.</span></span> |
| <span data-ttu-id="548f6-125">DateTime</span><span class="sxs-lookup"><span data-stu-id="548f6-125">DateTime</span></span> | <span data-ttu-id="548f6-p102">Debe especificarse en el formato ISO 8601. Se almacenarán en UTC.</span><span class="sxs-lookup"><span data-stu-id="548f6-p102">Must be specified in ISO 8601 format. Will be stored in UTC.</span></span> |
| <span data-ttu-id="548f6-128">Integer</span><span class="sxs-lookup"><span data-stu-id="548f6-128">Integer</span></span> | <span data-ttu-id="548f6-129">Valor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="548f6-129">32-bit value.</span></span> <span data-ttu-id="548f6-130">No se admite para contactos, mensajes, eventos y publicaciones.</span><span class="sxs-lookup"><span data-stu-id="548f6-130">Not supported for contacts, messages, events and posts.</span></span> |
| <span data-ttu-id="548f6-131">String</span><span class="sxs-lookup"><span data-stu-id="548f6-131">String</span></span> | <span data-ttu-id="548f6-132">256 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="548f6-132">256 characters maximum.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="548f6-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="548f6-133">JSON representation</span></span>
<span data-ttu-id="548f6-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="548f6-134">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.extensionSchemaProperty"
}-->

```json
{
  "name": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "extensionSchemaProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
