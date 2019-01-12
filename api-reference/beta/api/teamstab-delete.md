---
title: Eliminar ficha de canal
description: 'Quita (libera) una ficha desde el canal especificado dentro de un equipo. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 2103d63e6919e40b868071a44fb3f0a99e95049b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945177"
---
# <a name="delete-tab-from-channel"></a><span data-ttu-id="220f8-103">Eliminar ficha de canal</span><span class="sxs-lookup"><span data-stu-id="220f8-103">Delete tab from channel</span></span>

> <span data-ttu-id="220f8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="220f8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="220f8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="220f8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="220f8-106">Quita (libera) una ficha desde el [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="220f8-106">Removes (unpins) a tab from the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="220f8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="220f8-107">Permissions</span></span>
<span data-ttu-id="220f8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="220f8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="220f8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="220f8-110">Permission type</span></span>      | <span data-ttu-id="220f8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="220f8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="220f8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="220f8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="220f8-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="220f8-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="220f8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="220f8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="220f8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="220f8-115">Not supported.</span></span>    |
|<span data-ttu-id="220f8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="220f8-116">Application</span></span> | <span data-ttu-id="220f8-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="220f8-117">Group.ReadWrite.All</span></span> |

> <span data-ttu-id="220f8-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="220f8-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="220f8-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="220f8-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="220f8-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="220f8-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="request-headers"></a><span data-ttu-id="220f8-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="220f8-121">Request headers</span></span>
| <span data-ttu-id="220f8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="220f8-122">Header</span></span>       | <span data-ttu-id="220f8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="220f8-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="220f8-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="220f8-124">Authorization</span></span>  | <span data-ttu-id="220f8-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="220f8-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="220f8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="220f8-127">Request body</span></span>
<span data-ttu-id="220f8-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="220f8-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="220f8-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="220f8-129">Response</span></span>

<span data-ttu-id="220f8-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="220f8-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="220f8-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="220f8-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="220f8-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="220f8-133">Request</span></span>
<span data-ttu-id="220f8-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="220f8-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="220f8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="220f8-135">Response</span></span>
<span data-ttu-id="220f8-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="220f8-136">The following is an example of the response.</span></span> <span data-ttu-id="220f8-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="220f8-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="220f8-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="220f8-138">All of the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete tab from channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
