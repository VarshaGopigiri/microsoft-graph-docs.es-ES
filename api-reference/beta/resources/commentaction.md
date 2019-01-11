---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: CommentAction
localization_priority: Normal
ms.openlocfilehash: 952a86161047ab869238feaba50b8ad4d8ce0658
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845601"
---
# <a name="commentaction-resource-type"></a><span data-ttu-id="84eaa-102">Tipo de recurso CommentAction</span><span class="sxs-lookup"><span data-stu-id="84eaa-102">CommentAction resource type</span></span>

> <span data-ttu-id="84eaa-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="84eaa-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="84eaa-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="84eaa-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="84eaa-105">El recurso **CommentAction** proporciona información sobre un comentario [activity][] realizado en un elemento.</span><span class="sxs-lookup"><span data-stu-id="84eaa-105">The **CommentAction** resource provides information about a comment [activity][] made on an item.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="84eaa-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="84eaa-107">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.commentAction"
}-->

```json
{
  "isReply": false,
  "parentAuthor": {"@odata.type": "microsoft.graph.identitySet"},
  "participants": [{"@odata.type": "microsoft.graph.identitySet"}]
}
```

## <a name="properties"></a><span data-ttu-id="84eaa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84eaa-108">Properties</span></span>

| <span data-ttu-id="84eaa-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="84eaa-109">Property name</span></span>    | <span data-ttu-id="84eaa-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="84eaa-110">Type</span></span>                       | <span data-ttu-id="84eaa-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="84eaa-111">Description</span></span>
|:-----------------|:---------------------------|:-----------------------------
| <span data-ttu-id="84eaa-112">isReply</span><span class="sxs-lookup"><span data-stu-id="84eaa-112">isReply</span></span>          | <span data-ttu-id="84eaa-113">boolean</span><span class="sxs-lookup"><span data-stu-id="84eaa-113">boolean</span></span>                    | <span data-ttu-id="84eaa-114">Si es true, esta actividad fue una respuesta a un hilo de comentarios existente.</span><span class="sxs-lookup"><span data-stu-id="84eaa-114">If true, this activity was a reply to an existing comment thread.</span></span>
| <span data-ttu-id="84eaa-115">parentAuthor</span><span class="sxs-lookup"><span data-stu-id="84eaa-115">parentAuthor</span></span>     | <span data-ttu-id="84eaa-116">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="84eaa-116">[identitySet][]</span></span>            | <span data-ttu-id="84eaa-117">La identidad del usuario que inició el hilo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="84eaa-117">The identity of the user who started the comment thread.</span></span>
| <span data-ttu-id="84eaa-118">participants</span><span class="sxs-lookup"><span data-stu-id="84eaa-118">participants</span></span>     | <span data-ttu-id="84eaa-119">Colección [identitySet][]</span><span class="sxs-lookup"><span data-stu-id="84eaa-119">[identitySet][] collection</span></span> | <span data-ttu-id="84eaa-120">Las identidades de los usuarios que participan en este hilo de comentarios.</span><span class="sxs-lookup"><span data-stu-id="84eaa-120">The identities of the users participating in this comment thread.</span></span>

[identitySet]: identityset.md

## <a name="remarks"></a><span data-ttu-id="84eaa-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="84eaa-122">Remarks</span></span>

<span data-ttu-id="84eaa-123">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="84eaa-123">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The CommentAction object provides information about a comment that was made on an item.",
  "keywords": "activities,activity,action,comment",
  "section": "documentation",
  "tocPath": "Resources/CommentAction"
} -->
