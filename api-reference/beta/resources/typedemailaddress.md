---
title: tipo de recurso typedEmailAddress
description: Representa el nombre, direcciones de correo electrónico y su correspondiente tipo de dirección de correo electrónico de un contacto.
localization_priority: Normal
ms.openlocfilehash: c77d3dddc3e2bfcac47e6ed245dad9223fe7f08c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871270"
---
# <a name="typedemailaddress-resource-type"></a><span data-ttu-id="e9d91-103">tipo de recurso typedEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e9d91-103">typedEmailAddress resource type</span></span>

> <span data-ttu-id="e9d91-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9d91-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9d91-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9d91-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e9d91-106">Representa el nombre, direcciones de correo electrónico y su correspondiente tipo de dirección de correo electrónico de un [contacto](contact.md).</span><span class="sxs-lookup"><span data-stu-id="e9d91-106">Represents the name, email addresses, and their corresponding email address type of a [contact](contact.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e9d91-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9d91-107">Properties</span></span>
| <span data-ttu-id="e9d91-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9d91-108">Property</span></span>     | <span data-ttu-id="e9d91-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9d91-109">Type</span></span>   |<span data-ttu-id="e9d91-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9d91-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e9d91-111">address</span><span class="sxs-lookup"><span data-stu-id="e9d91-111">address</span></span>|<span data-ttu-id="e9d91-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9d91-112">String</span></span>|<span data-ttu-id="e9d91-113">La dirección de correo electrónico de un contacto.</span><span class="sxs-lookup"><span data-stu-id="e9d91-113">The email address of a contact.</span></span>|
|<span data-ttu-id="e9d91-114">name</span><span class="sxs-lookup"><span data-stu-id="e9d91-114">name</span></span>|<span data-ttu-id="e9d91-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9d91-115">String</span></span>|<span data-ttu-id="e9d91-116">El nombre para mostrar de un contacto.</span><span class="sxs-lookup"><span data-stu-id="e9d91-116">The display name of a contact.</span></span>|
|<span data-ttu-id="e9d91-117">type</span><span class="sxs-lookup"><span data-stu-id="e9d91-117">type</span></span> |<span data-ttu-id="e9d91-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9d91-118">String</span></span> |<span data-ttu-id="e9d91-119">El tipo de dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e9d91-119">The type of email address.</span></span> <span data-ttu-id="e9d91-120">Los valores posibles son: `unknown`, `work`, `personal`, `main` y `other`.</span><span class="sxs-lookup"><span data-stu-id="e9d91-120">Possible values are: `unknown`, `work`, `personal`, `main`, `other`.</span></span> <span data-ttu-id="e9d91-121">El valor predeterminado es `unknown`, lo que significa **dirección** no se ha establecido como un tipo específico.</span><span class="sxs-lookup"><span data-stu-id="e9d91-121">The default value is `unknown`, which means **address** has not been set as a specific type.</span></span> |
|<span data-ttu-id="e9d91-122">otherLabel</span><span class="sxs-lookup"><span data-stu-id="e9d91-122">otherLabel</span></span> |<span data-ttu-id="e9d91-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="e9d91-123">String</span></span>  |<span data-ttu-id="e9d91-124">Para especificar un tipo de dirección de correo electrónico personalizado, establezca el **tipo** en `other`y asignar **otherLabel** en una cadena personalizada.</span><span class="sxs-lookup"><span data-stu-id="e9d91-124">To specify a custom type of email address, set **type** to `other`, and assign **otherLabel** to a custom string.</span></span> <span data-ttu-id="e9d91-125">Por ejemplo, puede usar una dirección de correo electrónico específica para las actividades de voluntarias.</span><span class="sxs-lookup"><span data-stu-id="e9d91-125">For example, you may use a specific email address for your volunteer activities.</span></span> <span data-ttu-id="e9d91-126">Establecer **tipo de** `other`y establecer **otherLabel** en una cadena personalizada como `Volunteer work`.</span><span class="sxs-lookup"><span data-stu-id="e9d91-126">Set **type** to `other`, and set **otherLabel** to a custom string such as `Volunteer work`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e9d91-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e9d91-127">JSON representation</span></span>

<span data-ttu-id="e9d91-128">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e9d91-128">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.typedEmailAddress"
}-->

```json
{
  "address": "string",
  "name": "string",
  "type": "string",
  "otherLabel": "string"
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
