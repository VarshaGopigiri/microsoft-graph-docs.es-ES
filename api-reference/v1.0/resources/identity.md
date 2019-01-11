---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Identidad
localization_priority: Normal
ms.openlocfilehash: 0d4e7284da7353e7c6902d7ae1958d41f9eafd8f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816019"
---
# <a name="identity-resource-type"></a><span data-ttu-id="9bc07-102">Tipo de recurso Identity</span><span class="sxs-lookup"><span data-stu-id="9bc07-102">Identity resource type</span></span>

<span data-ttu-id="9bc07-p101">El recurso **Identity** representa una identidad de un _actor_. Por ejemplo, un actor puede ser un usuario, un dispositivo o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9bc07-p101">The **Identity** resource represents an identity of an _actor_. For example, an actor can be a user, device, or application.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9bc07-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9bc07-105">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.identity",
  "openType": true,
 "optionalProperties": ["displayName", "thumbnails"] } -->
```json
{
  "displayName": "string",
  "id": "string",
  "thumbnails": { "@odata.type": "microsoft.graph.thumbnailSet" }
}
```

## <a name="properties"></a><span data-ttu-id="9bc07-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9bc07-106">Properties</span></span>

| <span data-ttu-id="9bc07-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9bc07-107">Property</span></span>    | <span data-ttu-id="9bc07-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9bc07-108">Type</span></span>   | <span data-ttu-id="9bc07-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9bc07-109">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:------------|:-------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc07-110">displayName</span><span class="sxs-lookup"><span data-stu-id="9bc07-110">displayName</span></span> | <span data-ttu-id="9bc07-111">String</span><span class="sxs-lookup"><span data-stu-id="9bc07-111">String</span></span> | <span data-ttu-id="9bc07-p102">El nombre para mostrar de la identidad. Tenga en cuenta que puede que no esté siempre disponible o actualizado. Por ejemplo, si un usuario cambia su nombre para mostrar, la API puede mostrar el nuevo valor en una respuesta futura, pero los elementos asociados con el usuario no estarán modificados al usar [delta](../api/driveitem-delta.md).</span><span class="sxs-lookup"><span data-stu-id="9bc07-p102">The identity's display name. Note that this may not always be available or up to date. For example, if a user changes their display name, the API may show the new value in a future response, but the items associated with the user won't show up as having changed when using [delta](../api/driveitem-delta.md).</span></span>     |
| <span data-ttu-id="9bc07-115">id</span><span class="sxs-lookup"><span data-stu-id="9bc07-115">id</span></span>          | <span data-ttu-id="9bc07-116">String</span><span class="sxs-lookup"><span data-stu-id="9bc07-116">String</span></span> | <span data-ttu-id="9bc07-117">Identificador único de la identidad.</span><span class="sxs-lookup"><span data-stu-id="9bc07-117">Unique identifier for the identity.</span></span>                                                                                                                                                                                                                                                                                   |

## <a name="remarks"></a><span data-ttu-id="9bc07-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bc07-118">Remarks</span></span>

<span data-ttu-id="9bc07-p103">En algunas circunstancias, puede que el identificador único del actor no esté disponible. En este caso, se devuelve la propiedad **displayName** de la identidad, pero faltará la propiedad **id** del recurso.</span><span class="sxs-lookup"><span data-stu-id="9bc07-p103">In some circumstances, the unique identifier for the actor may not be available. In this case, the **displayName** property for the identity will be returned, but the **id** property will be missing from the resource.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity contains information about an app, user, or group.",
  "keywords": "identity,owner,modifier,app,user,group",
  "section": "documentation",
  "tocPath": "Resources/Identity"

} -->
