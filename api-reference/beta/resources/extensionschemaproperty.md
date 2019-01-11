---
title: Tipo de recurso extensionSchemaProperty
description: Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición schemaExtension.
localization_priority: Normal
ms.openlocfilehash: 44769bab4a4f4b40a80d896bed2311554ea5e8ad
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889862"
---
# <a name="extensionschemaproperty-resource-type"></a><span data-ttu-id="95b3a-103">Tipo de recurso extensionSchemaProperty</span><span class="sxs-lookup"><span data-stu-id="95b3a-103">extensionSchemaProperty resource type</span></span>

> <span data-ttu-id="95b3a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="95b3a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="95b3a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="95b3a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="95b3a-106">Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición [schemaExtension](schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="95b3a-106">Use the **extensionSchemaProperty** resource to define a property's name and its type, as part of a [schemaExtension](schemaextension.md) definition.</span></span>


## <a name="properties"></a><span data-ttu-id="95b3a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95b3a-107">Properties</span></span>
| <span data-ttu-id="95b3a-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95b3a-108">Property</span></span>     | <span data-ttu-id="95b3a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="95b3a-109">Type</span></span>   |<span data-ttu-id="95b3a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="95b3a-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="95b3a-111">name</span><span class="sxs-lookup"><span data-stu-id="95b3a-111">name</span></span>|<span data-ttu-id="95b3a-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="95b3a-112">String</span></span>| <span data-ttu-id="95b3a-113">El nombre de la propiedad fuertemente tipada definido como parte de una extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="95b3a-113">The name of the strongly typed property defined as part of a schema extension.</span></span>|
|<span data-ttu-id="95b3a-114">type</span><span class="sxs-lookup"><span data-stu-id="95b3a-114">type</span></span>|<span data-ttu-id="95b3a-115">String</span><span class="sxs-lookup"><span data-stu-id="95b3a-115">String</span></span>| <span data-ttu-id="95b3a-p102">Tipo de la propiedad que se define como parte de una extensión de esquema.  Los valores permitidos son *Binary, Boolean, DateTime, Integer* y *String*.  Consulte la tabla siguiente para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="95b3a-p102">The type of the property that is defined as part of a schema extension.  Allowed values are *Binary, Boolean, DateTime, Integer* or *String*.  See the table below for more details.</span></span>|

#### <a name="supported-property-data-types"></a><span data-ttu-id="95b3a-119">Tipos de datos de propiedad admitidos</span><span class="sxs-lookup"><span data-stu-id="95b3a-119">Supported property data types</span></span> 
<span data-ttu-id="95b3a-120">Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:</span><span class="sxs-lookup"><span data-stu-id="95b3a-120">The following data types are supported when defining a property in a schema extension:</span></span>

| <span data-ttu-id="95b3a-121">Tipo de propiedad</span><span class="sxs-lookup"><span data-stu-id="95b3a-121">Property Type</span></span> | <span data-ttu-id="95b3a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95b3a-122">Remarks</span></span> |
|-------------|------------|
| <span data-ttu-id="95b3a-123">Binario</span><span class="sxs-lookup"><span data-stu-id="95b3a-123">Binary</span></span> | <span data-ttu-id="95b3a-124">Máximo de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="95b3a-124">256 bytes maximum.</span></span> |
| <span data-ttu-id="95b3a-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="95b3a-125">Boolean</span></span> | <span data-ttu-id="95b3a-126">No se admite para los mensajes, eventos y publicaciones.</span><span class="sxs-lookup"><span data-stu-id="95b3a-126">Not supported for messages, events and posts.</span></span> |
| <span data-ttu-id="95b3a-127">DateTime</span><span class="sxs-lookup"><span data-stu-id="95b3a-127">DateTime</span></span> | <span data-ttu-id="95b3a-p103">Debe especificarse en el formato ISO 8601. Se almacenarán en UTC.</span><span class="sxs-lookup"><span data-stu-id="95b3a-p103">Must be specified in ISO 8601 format. Will be stored in UTC.</span></span> |
| <span data-ttu-id="95b3a-130">Entero</span><span class="sxs-lookup"><span data-stu-id="95b3a-130">Integer</span></span> | <span data-ttu-id="95b3a-p104">Valor de 32 bits. No se admite para los mensajes, eventos y publicaciones.</span><span class="sxs-lookup"><span data-stu-id="95b3a-p104">32-bit value. Not supported for messages, events and posts.</span></span> |
| <span data-ttu-id="95b3a-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="95b3a-133">String</span></span> | <span data-ttu-id="95b3a-134">256 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="95b3a-134">256 characters maximum.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="95b3a-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="95b3a-135">JSON representation</span></span>
<span data-ttu-id="95b3a-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="95b3a-136">Here is a JSON representation of the resource.</span></span>

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
