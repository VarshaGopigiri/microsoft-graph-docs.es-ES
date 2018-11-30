---
title: Tipo de recurso emailAddress
description: Representa el nombre y la dirección SMTP de una instancia de entidad, por ejemplo, un mensaje destinatario o el calendario de propietario.
ms.openlocfilehash: f607fe4ce01b9a3c3f5e7af5aa1638fef3840177
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084180"
---
# <a name="emailaddress-resource-type"></a><span data-ttu-id="4fb36-103">Tipo de recurso emailAddress</span><span class="sxs-lookup"><span data-stu-id="4fb36-103">emailAddress resource type</span></span>

> <span data-ttu-id="4fb36-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4fb36-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4fb36-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4fb36-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4fb36-106">Representa el nombre y la dirección SMTP de una instancia de entidad, por ejemplo, un mensaje destinatario o el calendario de propietario.</span><span class="sxs-lookup"><span data-stu-id="4fb36-106">Represents the name and SMTP address of an entity instance, for example, a message recipient or calendar owner.</span></span>

## <a name="properties"></a><span data-ttu-id="4fb36-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4fb36-107">Properties</span></span>
| <span data-ttu-id="4fb36-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4fb36-108">Property</span></span>     | <span data-ttu-id="4fb36-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4fb36-109">Type</span></span>   |<span data-ttu-id="4fb36-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fb36-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4fb36-111">address</span><span class="sxs-lookup"><span data-stu-id="4fb36-111">address</span></span>|<span data-ttu-id="4fb36-112">String</span><span class="sxs-lookup"><span data-stu-id="4fb36-112">String</span></span>|<span data-ttu-id="4fb36-113">La dirección de correo electrónico de una instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="4fb36-113">The email address of an entity instance.</span></span>|
|<span data-ttu-id="4fb36-114">name</span><span class="sxs-lookup"><span data-stu-id="4fb36-114">name</span></span>|<span data-ttu-id="4fb36-115">String</span><span class="sxs-lookup"><span data-stu-id="4fb36-115">String</span></span>|<span data-ttu-id="4fb36-116">El nombre para mostrar de una instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="4fb36-116">The display name of an entity instance.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4fb36-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4fb36-117">JSON representation</span></span>

<span data-ttu-id="4fb36-118">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4fb36-118">Here is a JSON representation of the resource</span></span>

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
