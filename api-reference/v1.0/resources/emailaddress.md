---
title: Tipo de recurso emailAddress
description: Nombre y dirección de correo de un contacto o destinatario del mensaje.
ms.openlocfilehash: 962b2f36af9e292125edc3da8606cd532b8c2ec0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028927"
---
# <a name="emailaddress-resource-type"></a><span data-ttu-id="a384a-103">Tipo de recurso emailAddress</span><span class="sxs-lookup"><span data-stu-id="a384a-103">emailAddress resource type</span></span>

<span data-ttu-id="a384a-104">Nombre y dirección de correo de un contacto o destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="a384a-104">The name and email address of a contact or message recipient.</span></span>

## <a name="properties"></a><span data-ttu-id="a384a-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a384a-105">Properties</span></span>
| <span data-ttu-id="a384a-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a384a-106">Property</span></span>     | <span data-ttu-id="a384a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a384a-107">Type</span></span>   |<span data-ttu-id="a384a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a384a-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a384a-109">address</span><span class="sxs-lookup"><span data-stu-id="a384a-109">address</span></span>|<span data-ttu-id="a384a-110">String</span><span class="sxs-lookup"><span data-stu-id="a384a-110">String</span></span>|<span data-ttu-id="a384a-111">Dirección de correo de la persona o entidad.</span><span class="sxs-lookup"><span data-stu-id="a384a-111">The email address of the person or entity.</span></span>|
|<span data-ttu-id="a384a-112">name</span><span class="sxs-lookup"><span data-stu-id="a384a-112">name</span></span>|<span data-ttu-id="a384a-113">String</span><span class="sxs-lookup"><span data-stu-id="a384a-113">String</span></span>|<span data-ttu-id="a384a-114">Nombre para mostrar de la persona o entidad.</span><span class="sxs-lookup"><span data-stu-id="a384a-114">The display name of the person or entity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a384a-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a384a-115">JSON representation</span></span>

<span data-ttu-id="a384a-116">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a384a-116">Here is a JSON representation of the resource</span></span>

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
