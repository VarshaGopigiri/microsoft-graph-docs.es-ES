---
title: Tipo de recurso inferenceClassificationOverride
description: Representa el reemplazo de un usuario sobre cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado.
localization_priority: Normal
ms.openlocfilehash: 8df0f1e5fa34c630c51de7c73234e6092448f867
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885067"
---
# <a name="inferenceclassificationoverride-resource-type"></a><span data-ttu-id="54f8d-103">Tipo de recurso inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="54f8d-103">inferenceClassificationOverride resource type</span></span>

<span data-ttu-id="54f8d-104">Representa el reemplazo de un usuario sobre cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado.</span><span class="sxs-lookup"><span data-stu-id="54f8d-104">Represents a user's override for how incoming messages from a specific sender should always be classified as.</span></span>


## <a name="methods"></a><span data-ttu-id="54f8d-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="54f8d-105">Methods</span></span>

| <span data-ttu-id="54f8d-106">Método</span><span class="sxs-lookup"><span data-stu-id="54f8d-106">Method</span></span>           | <span data-ttu-id="54f8d-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54f8d-107">Return Type</span></span>    |<span data-ttu-id="54f8d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="54f8d-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="54f8d-109">Update</span><span class="sxs-lookup"><span data-stu-id="54f8d-109">Update</span></span>](../api/inferenceclassificationoverride-update.md) | [<span data-ttu-id="54f8d-110">inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="54f8d-110">inferenceClassificationOverride</span></span>](inferenceclassificationoverride.md) |<span data-ttu-id="54f8d-111">Cambie el campo **ClassifyAs** de una invalidación tal como se especifica.</span><span class="sxs-lookup"><span data-stu-id="54f8d-111">Change the **ClassifyAs** field of an override as specified.</span></span> |
|[<span data-ttu-id="54f8d-112">Delete</span><span class="sxs-lookup"><span data-stu-id="54f8d-112">Delete</span></span>](../api/inferenceclassificationoverride-delete.md) | <span data-ttu-id="54f8d-113">None</span><span class="sxs-lookup"><span data-stu-id="54f8d-113">None</span></span> |<span data-ttu-id="54f8d-114">Elimina un reemplazo especificado por su identificador.</span><span class="sxs-lookup"><span data-stu-id="54f8d-114">Delete an override specified by its ID.</span></span> |

## <a name="properties"></a><span data-ttu-id="54f8d-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54f8d-115">Properties</span></span>
| <span data-ttu-id="54f8d-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54f8d-116">Property</span></span>     | <span data-ttu-id="54f8d-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="54f8d-117">Type</span></span>   |<span data-ttu-id="54f8d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="54f8d-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="54f8d-119">classifyAs</span><span class="sxs-lookup"><span data-stu-id="54f8d-119">classifyAs</span></span>|<span data-ttu-id="54f8d-120">inferenceClassificationType</span><span class="sxs-lookup"><span data-stu-id="54f8d-120">inferenceClassificationType</span></span>| <span data-ttu-id="54f8d-121">Especifica cómo los mensajes entrantes de una determinada siempre debe clasificarse como remitente.</span><span class="sxs-lookup"><span data-stu-id="54f8d-121">Specifies how incoming messages from a specific sender should always be classified as.</span></span> <span data-ttu-id="54f8d-122">Los valores posibles son: `focused`, `other`.</span><span class="sxs-lookup"><span data-stu-id="54f8d-122">The possible values are: `focused`, `other`.</span></span>|
|<span data-ttu-id="54f8d-123">id</span><span class="sxs-lookup"><span data-stu-id="54f8d-123">id</span></span>|<span data-ttu-id="54f8d-124">string</span><span class="sxs-lookup"><span data-stu-id="54f8d-124">string</span></span>| <span data-ttu-id="54f8d-p102">Identificador único del reemplazo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="54f8d-p102">The unique identifier of the override. Read-only.</span></span>|
|<span data-ttu-id="54f8d-127">senderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="54f8d-127">senderEmailAddress</span></span>|[<span data-ttu-id="54f8d-128">emailAddress</span><span class="sxs-lookup"><span data-stu-id="54f8d-128">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="54f8d-129">Información de la dirección de correo del remitente para el que se creó el reemplazo.</span><span class="sxs-lookup"><span data-stu-id="54f8d-129">The email address information of the sender for whom the override is created.</span></span>|

## <a name="relationships"></a><span data-ttu-id="54f8d-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="54f8d-130">Relationships</span></span>
<span data-ttu-id="54f8d-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="54f8d-131">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="54f8d-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="54f8d-132">JSON representation</span></span>

<span data-ttu-id="54f8d-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="54f8d-133">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
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
