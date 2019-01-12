---
title: Tipo de recurso emailAddress
description: Representa el nombre y la dirección SMTP de una instancia de entidad, por ejemplo, un mensaje destinatario o el calendario de propietario.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: c06849a73f4246653b8d78dcd392c4e4f6686a46
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932794"
---
# <a name="emailaddress-resource-type"></a><span data-ttu-id="5abe8-103">Tipo de recurso emailAddress</span><span class="sxs-lookup"><span data-stu-id="5abe8-103">emailAddress resource type</span></span>

> <span data-ttu-id="5abe8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5abe8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5abe8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5abe8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5abe8-106">Representa el nombre y la dirección SMTP de una instancia de entidad, por ejemplo, un mensaje destinatario o el calendario de propietario.</span><span class="sxs-lookup"><span data-stu-id="5abe8-106">Represents the name and SMTP address of an entity instance, for example, a message recipient or calendar owner.</span></span>

## <a name="properties"></a><span data-ttu-id="5abe8-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5abe8-107">Properties</span></span>
| <span data-ttu-id="5abe8-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5abe8-108">Property</span></span>     | <span data-ttu-id="5abe8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5abe8-109">Type</span></span>   |<span data-ttu-id="5abe8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5abe8-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5abe8-111">address</span><span class="sxs-lookup"><span data-stu-id="5abe8-111">address</span></span>|<span data-ttu-id="5abe8-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="5abe8-112">String</span></span>|<span data-ttu-id="5abe8-113">La dirección de correo electrónico de una instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="5abe8-113">The email address of an entity instance.</span></span>|
|<span data-ttu-id="5abe8-114">name</span><span class="sxs-lookup"><span data-stu-id="5abe8-114">name</span></span>|<span data-ttu-id="5abe8-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="5abe8-115">String</span></span>|<span data-ttu-id="5abe8-116">El nombre para mostrar de una instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="5abe8-116">The display name of an entity instance.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5abe8-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5abe8-117">JSON representation</span></span>

<span data-ttu-id="5abe8-118">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5abe8-118">Here is a JSON representation of the resource</span></span>

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
