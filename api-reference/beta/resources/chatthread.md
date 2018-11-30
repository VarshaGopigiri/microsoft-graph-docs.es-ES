---
title: tipo de recurso chatThread
description: Una chatThread es una colección de chatMessages en Microsoft Teams.
ms.openlocfilehash: ef8f118ae4354a5e4197802708aecfa1fb6f8cb8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089968"
---
# <a name="chatthread-resource-type"></a><span data-ttu-id="38545-103">tipo de recurso chatThread</span><span class="sxs-lookup"><span data-stu-id="38545-103">chatThread resource type</span></span>

> <span data-ttu-id="38545-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38545-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38545-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38545-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="38545-106">Una chatThread es una colección de [chatMessages](chatmessage.md) en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="38545-106">A chatThread is a collection of [chatMessages](chatmessage.md) in Microsoft Teams.</span></span>

> <span data-ttu-id="38545-107">En la actualidad, chatThreads puede ser [creado en los canales](../api/channel-post-chatthreads.md).</span><span class="sxs-lookup"><span data-stu-id="38545-107">Currently, chatThreads can be [created in channels](../api/channel-post-chatthreads.md).</span></span>  <span data-ttu-id="38545-108">API de futuras versiones admitirá chatThreads existente, así como lectura/escritura de chats directas entre los usuarios que están fuera del ámbito de un equipo o un canal de lectura.</span><span class="sxs-lookup"><span data-stu-id="38545-108">Future API releases will support reading existing chatThreads, as well as reading/writing direct chats between users that are outside the scope of a team or channel.</span></span>

## <a name="methods"></a><span data-ttu-id="38545-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="38545-109">Methods</span></span>

| <span data-ttu-id="38545-110">Método</span><span class="sxs-lookup"><span data-stu-id="38545-110">Method</span></span>       | <span data-ttu-id="38545-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38545-111">Return Type</span></span>  |<span data-ttu-id="38545-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="38545-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="38545-113">Crear hilo</span><span class="sxs-lookup"><span data-stu-id="38545-113">Create thread</span></span>](../api/channel-post-chatthreads.md) | [<span data-ttu-id="38545-114">chatThread</span><span class="sxs-lookup"><span data-stu-id="38545-114">chatThread</span></span>](chatthread.md) |<span data-ttu-id="38545-115">Iniciar un nuevo subproceso en el canal especificado, que proporciona el primer mensaje.</span><span class="sxs-lookup"><span data-stu-id="38545-115">Start a new thread in the specified channel, providing the first message.</span></span>|

## <a name="properties"></a><span data-ttu-id="38545-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38545-116">Properties</span></span>
| <span data-ttu-id="38545-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38545-117">Property</span></span>     | <span data-ttu-id="38545-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="38545-118">Type</span></span>   |<span data-ttu-id="38545-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="38545-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38545-120">id</span><span class="sxs-lookup"><span data-stu-id="38545-120">id</span></span>|<span data-ttu-id="38545-121">String</span><span class="sxs-lookup"><span data-stu-id="38545-121">String</span></span>| <span data-ttu-id="38545-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="38545-122">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="38545-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="38545-123">Relationships</span></span>
| <span data-ttu-id="38545-124">Relación</span><span class="sxs-lookup"><span data-stu-id="38545-124">Relationship</span></span> | <span data-ttu-id="38545-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="38545-125">Type</span></span>   |<span data-ttu-id="38545-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="38545-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="38545-127">rootMessage</span><span class="sxs-lookup"><span data-stu-id="38545-127">rootMessage</span></span>|[<span data-ttu-id="38545-128">chatMessage</span><span class="sxs-lookup"><span data-stu-id="38545-128">chatMessage</span></span>](chatmessage.md)| <span data-ttu-id="38545-129">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="38545-129">Nullable.</span></span>|
|<span data-ttu-id="38545-130">chatMessages</span><span class="sxs-lookup"><span data-stu-id="38545-130">chatMessages</span></span>|<span data-ttu-id="38545-131">colección de [chatMessage](chatmessage.md)</span><span class="sxs-lookup"><span data-stu-id="38545-131">[chatMessage](chatmessage.md) collection</span></span>| <span data-ttu-id="38545-132">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="38545-132">Nullable.</span></span>|

> <span data-ttu-id="38545-133">Actualmente estas relaciones existe implícitamente, pero no se puede leer o escribir.</span><span class="sxs-lookup"><span data-stu-id="38545-133">Currently these relationships exist implicitly, but cannot read or written.</span></span>  <span data-ttu-id="38545-134">Versiones beta futuras API admitirá esto.</span><span class="sxs-lookup"><span data-stu-id="38545-134">Future beta API releases will support this.</span></span>

## <a name="json-representation"></a><span data-ttu-id="38545-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="38545-135">JSON representation</span></span>

<span data-ttu-id="38545-136">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="38545-136">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "posts"
  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatThread"
}-->

```json
{
  "id": "string (identifier)",
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chatThread resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
