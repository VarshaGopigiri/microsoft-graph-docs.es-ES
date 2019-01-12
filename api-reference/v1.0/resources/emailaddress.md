---
title: Tipo de recurso emailAddress
description: Nombre y dirección de correo de un contacto o destinatario del mensaje.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 7af23418132c4d1c20097899f870c7d25be119bc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951757"
---
# <a name="emailaddress-resource-type"></a><span data-ttu-id="948ca-103">Tipo de recurso emailAddress</span><span class="sxs-lookup"><span data-stu-id="948ca-103">emailAddress resource type</span></span>

<span data-ttu-id="948ca-104">Nombre y dirección de correo de un contacto o destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="948ca-104">The name and email address of a contact or message recipient.</span></span>

## <a name="properties"></a><span data-ttu-id="948ca-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="948ca-105">Properties</span></span>
| <span data-ttu-id="948ca-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="948ca-106">Property</span></span>     | <span data-ttu-id="948ca-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="948ca-107">Type</span></span>   |<span data-ttu-id="948ca-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="948ca-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="948ca-109">address</span><span class="sxs-lookup"><span data-stu-id="948ca-109">address</span></span>|<span data-ttu-id="948ca-110">String</span><span class="sxs-lookup"><span data-stu-id="948ca-110">String</span></span>|<span data-ttu-id="948ca-111">Dirección de correo de la persona o entidad.</span><span class="sxs-lookup"><span data-stu-id="948ca-111">The email address of the person or entity.</span></span>|
|<span data-ttu-id="948ca-112">name</span><span class="sxs-lookup"><span data-stu-id="948ca-112">name</span></span>|<span data-ttu-id="948ca-113">String</span><span class="sxs-lookup"><span data-stu-id="948ca-113">String</span></span>|<span data-ttu-id="948ca-114">Nombre para mostrar de la persona o entidad.</span><span class="sxs-lookup"><span data-stu-id="948ca-114">The display name of the person or entity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="948ca-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="948ca-115">JSON representation</span></span>

<span data-ttu-id="948ca-116">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="948ca-116">Here is a JSON representation of the resource</span></span>

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
