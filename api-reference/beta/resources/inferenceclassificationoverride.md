---
title: Tipo de recurso inferenceClassificationOverride
description: Representa el reemplazo de un usuario para cómo los mensajes entrantes de un remitente específico siempre se debe clasificar como
localization_priority: Normal
ms.openlocfilehash: 9124f773a26c9edf1238276c3d0017dcc46e7ad8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876275"
---
# <a name="inferenceclassificationoverride-resource-type"></a><span data-ttu-id="b3ca0-103">Tipo de recurso inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="b3ca0-103">inferenceClassificationOverride resource type</span></span>

> <span data-ttu-id="b3ca0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b3ca0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b3ca0-106">Representa el reemplazo de un usuario de cómo los mensajes entrantes de un remitente específico siempre deben clasificarse como un [Dirigidos a Bandeja de entrada](manage-focused-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="b3ca0-106">Represents a user's override for how incoming messages from a specific sender should always be classified as in a [Focused Inbox](manage-focused-inbox.md).</span></span>


## <a name="methods"></a><span data-ttu-id="b3ca0-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="b3ca0-107">Methods</span></span>

| <span data-ttu-id="b3ca0-108">Método</span><span class="sxs-lookup"><span data-stu-id="b3ca0-108">Method</span></span>           | <span data-ttu-id="b3ca0-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3ca0-109">Return Type</span></span>    |<span data-ttu-id="b3ca0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3ca0-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b3ca0-111">Update</span><span class="sxs-lookup"><span data-stu-id="b3ca0-111">Update</span></span>](../api/inferenceclassificationoverride-update.md) | [<span data-ttu-id="b3ca0-112">inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="b3ca0-112">inferenceClassificationOverride</span></span>](inferenceclassificationoverride.md) |<span data-ttu-id="b3ca0-113">Cambie el campo **ClassifyAs** de una invalidación tal como se especifica.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-113">Change the **ClassifyAs** field of an override as specified.</span></span> |
|[<span data-ttu-id="b3ca0-114">Delete</span><span class="sxs-lookup"><span data-stu-id="b3ca0-114">Delete</span></span>](../api/inferenceclassificationoverride-delete.md) | <span data-ttu-id="b3ca0-115">None</span><span class="sxs-lookup"><span data-stu-id="b3ca0-115">None</span></span> |<span data-ttu-id="b3ca0-116">Elimina un reemplazo especificado por su identificador.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-116">Delete an override specified by its ID.</span></span> |

## <a name="properties"></a><span data-ttu-id="b3ca0-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3ca0-117">Properties</span></span>
| <span data-ttu-id="b3ca0-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3ca0-118">Property</span></span>     | <span data-ttu-id="b3ca0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3ca0-119">Type</span></span>   |<span data-ttu-id="b3ca0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3ca0-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b3ca0-121">classifyAs</span><span class="sxs-lookup"><span data-stu-id="b3ca0-121">classifyAs</span></span>|<span data-ttu-id="b3ca0-122">string</span><span class="sxs-lookup"><span data-stu-id="b3ca0-122">string</span></span>| <span data-ttu-id="b3ca0-p102">Especifica cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado. Los valores posibles son: `focused`, `other`.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-p102">Specifies how incoming messages from a specific sender should always be classified as. Possible values are: `focused`, `other`.</span></span>|
|<span data-ttu-id="b3ca0-125">id</span><span class="sxs-lookup"><span data-stu-id="b3ca0-125">id</span></span>|<span data-ttu-id="b3ca0-126">string</span><span class="sxs-lookup"><span data-stu-id="b3ca0-126">string</span></span>| <span data-ttu-id="b3ca0-p103">Identificador único del reemplazo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-p103">The unique identifier of the override. Read-only.</span></span>|
|<span data-ttu-id="b3ca0-129">senderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b3ca0-129">senderEmailAddress</span></span>|[<span data-ttu-id="b3ca0-130">emailAddress</span><span class="sxs-lookup"><span data-stu-id="b3ca0-130">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="b3ca0-131">Información de la dirección de correo del remitente para el que se creó el reemplazo.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-131">The email address information of the sender for whom the override is created.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b3ca0-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b3ca0-132">Relationships</span></span>
<span data-ttu-id="b3ca0-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b3ca0-133">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="b3ca0-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b3ca0-134">JSON representation</span></span>

<span data-ttu-id="b3ca0-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b3ca0-135">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
}-->

```json
{
  "classifyAs": "string",
  "id": "string (identifier)",
  "senderEmailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "inferenceClassificationOverride resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
