---
title: Eliminar ficha de canal
description: 'Quita (libera) una ficha desde el canal especificado dentro de un equipo. '
author: nkramer
ms.openlocfilehash: 7d8465f650d63f22625c1da2c56b3de4e065374b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349290"
---
# <a name="delete-tab-from-channel"></a><span data-ttu-id="ed329-103">Eliminar ficha de canal</span><span class="sxs-lookup"><span data-stu-id="ed329-103">Delete tab from channel</span></span>

> <span data-ttu-id="ed329-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed329-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed329-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed329-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ed329-106">Quita (libera) una ficha desde el [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="ed329-106">Removes (unpins) a tab from the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="ed329-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ed329-107">Permissions</span></span>
<span data-ttu-id="ed329-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed329-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed329-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed329-110">Permission type</span></span>      | <span data-ttu-id="ed329-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed329-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ed329-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed329-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ed329-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed329-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ed329-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed329-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ed329-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed329-115">Not supported.</span></span>    |
|<span data-ttu-id="ed329-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed329-116">Application</span></span> | <span data-ttu-id="ed329-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed329-117">Group.ReadWrite.All</span></span> |

> <span data-ttu-id="ed329-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="ed329-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="ed329-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="ed329-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="ed329-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed329-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="request-headers"></a><span data-ttu-id="ed329-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed329-121">Request headers</span></span>
| <span data-ttu-id="ed329-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed329-122">Header</span></span>       | <span data-ttu-id="ed329-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ed329-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ed329-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ed329-124">Authorization</span></span>  | <span data-ttu-id="ed329-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ed329-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ed329-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed329-127">Request body</span></span>
<span data-ttu-id="ed329-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ed329-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ed329-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed329-129">Response</span></span>

<span data-ttu-id="ed329-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed329-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ed329-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed329-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ed329-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed329-133">Request</span></span>
<span data-ttu-id="ed329-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed329-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="ed329-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed329-135">Response</span></span>
<span data-ttu-id="ed329-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed329-136">The following is an example of the response.</span></span> <span data-ttu-id="ed329-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="ed329-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="ed329-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed329-138">All of the properties will be returned from an actual call.</span></span>
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
