---
author: rgregg
ms.author: rgregg
ms.date: 09/14/2017
title: Identidad
ms.openlocfilehash: 66dcd979718665af650edbfc50a46ece7c2c4c06
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084773"
---
# <a name="identity-resource-type"></a><span data-ttu-id="b0c9e-102">tipo de recurso de identidad</span><span class="sxs-lookup"><span data-stu-id="b0c9e-102">identity resource type</span></span>

> <span data-ttu-id="b0c9e-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b0c9e-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b0c9e-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b0c9e-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b0c9e-p102">El recurso **Identity** representa una identidad de un _actor_. Por ejemplo, un actor puede ser un usuario, un dispositivo o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="b0c9e-p102">The **Identity** resource represents an identity of an _actor_. For example, an actor can be a user, device, or application.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b0c9e-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b0c9e-107">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.identity", "optionalProperties": ["displayName", "tenantId", "thumbnails"], "openType": true } -->

```json
{
  "displayName": "string",
  "id": "string",
  "tenantId": "string",
  "thumbnails": { "@odata.type": "microsoft.graph.thumbnailSet" }
}
```

## <a name="properties"></a><span data-ttu-id="b0c9e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0c9e-108">Properties</span></span>

| <span data-ttu-id="b0c9e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b0c9e-109">Property</span></span>            | <span data-ttu-id="b0c9e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0c9e-110">Type</span></span>   | <span data-ttu-id="b0c9e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0c9e-111">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:--------------------|:-------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c9e-112">displayName</span><span class="sxs-lookup"><span data-stu-id="b0c9e-112">displayName</span></span>         | <span data-ttu-id="b0c9e-113">String</span><span class="sxs-lookup"><span data-stu-id="b0c9e-113">String</span></span> | <span data-ttu-id="b0c9e-p103">El nombre para mostrar de la identidad. Tenga en cuenta que puede que no esté siempre disponible o actualizado. Por ejemplo, si un usuario cambia su nombre para mostrar, la API puede mostrar el nuevo valor en una respuesta futura, pero los elementos asociados con el usuario no estarán modificados al usar [delta](../api/driveitem-delta.md).</span><span class="sxs-lookup"><span data-stu-id="b0c9e-p103">The identity's display name. Note that this may not always be available or up to date. For example, if a user changes their display name, the API may show the new value in a future response, but the items associated with the user won't show up as having changed when using [delta](../api/driveitem-delta.md).</span></span>  |
| <span data-ttu-id="b0c9e-117">id</span><span class="sxs-lookup"><span data-stu-id="b0c9e-117">id</span></span>                  | <span data-ttu-id="b0c9e-118">String</span><span class="sxs-lookup"><span data-stu-id="b0c9e-118">String</span></span> | <span data-ttu-id="b0c9e-119">Identificador único de la identidad.</span><span class="sxs-lookup"><span data-stu-id="b0c9e-119">Unique identifier for the identity.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b0c9e-120">tenantId</span><span class="sxs-lookup"><span data-stu-id="b0c9e-120">tenantId</span></span>            | <span data-ttu-id="b0c9e-121">String</span><span class="sxs-lookup"><span data-stu-id="b0c9e-121">String</span></span> | <span data-ttu-id="b0c9e-122">Identidad única del inquilino (opcional).</span><span class="sxs-lookup"><span data-stu-id="b0c9e-122">Unique identity of the tenant (optional).</span></span>                                                                                                                                                                                                                                                                             |

## <a name="remarks"></a><span data-ttu-id="b0c9e-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0c9e-123">Remarks</span></span>

<span data-ttu-id="b0c9e-p104">En algunas circunstancias, puede que el identificador único del actor no esté disponible. En este caso, se devuelve la propiedad **displayName** de la identidad, pero faltará la propiedad **id** del recurso.</span><span class="sxs-lookup"><span data-stu-id="b0c9e-p104">In some circumstances, the unique identifier for the actor may not be available. In this case, the **displayName** property for the identity will be returned, but the **id** property will be missing from the resource.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Identity contains information about an app, user, or group.",
  "keywords": "identity,owner,modifier,app,user,group",
  "section": "documentation",
  "tocPath": "Resources/Identity"
} -->