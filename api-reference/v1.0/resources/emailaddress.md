---
title: Tipo de recurso emailAddress
description: Nombre y dirección de correo de un contacto o destinatario del mensaje.
localization_priority: Normal
ms.openlocfilehash: 5ea1919e5c5f389c9b7fece508e8339f722b725a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826890"
---
# <a name="emailaddress-resource-type"></a><span data-ttu-id="224e4-103">Tipo de recurso emailAddress</span><span class="sxs-lookup"><span data-stu-id="224e4-103">emailAddress resource type</span></span>

<span data-ttu-id="224e4-104">Nombre y dirección de correo de un contacto o destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="224e4-104">The name and email address of a contact or message recipient.</span></span>

## <a name="properties"></a><span data-ttu-id="224e4-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="224e4-105">Properties</span></span>
| <span data-ttu-id="224e4-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="224e4-106">Property</span></span>     | <span data-ttu-id="224e4-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="224e4-107">Type</span></span>   |<span data-ttu-id="224e4-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="224e4-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="224e4-109">address</span><span class="sxs-lookup"><span data-stu-id="224e4-109">address</span></span>|<span data-ttu-id="224e4-110">String</span><span class="sxs-lookup"><span data-stu-id="224e4-110">String</span></span>|<span data-ttu-id="224e4-111">Dirección de correo de la persona o entidad.</span><span class="sxs-lookup"><span data-stu-id="224e4-111">The email address of the person or entity.</span></span>|
|<span data-ttu-id="224e4-112">name</span><span class="sxs-lookup"><span data-stu-id="224e4-112">name</span></span>|<span data-ttu-id="224e4-113">String</span><span class="sxs-lookup"><span data-stu-id="224e4-113">String</span></span>|<span data-ttu-id="224e4-114">Nombre para mostrar de la persona o entidad.</span><span class="sxs-lookup"><span data-stu-id="224e4-114">The display name of the person or entity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="224e4-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="224e4-115">JSON representation</span></span>

<span data-ttu-id="224e4-116">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="224e4-116">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.emailAddress"
}-->

```json
{
  "address": "string",
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "emailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
