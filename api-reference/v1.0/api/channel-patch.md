---
title: Canal de revisión
description: Actualizar las propiedades del canal especificado.
author: nkramer
ms.openlocfilehash: 8d310309ca80dcc5001276c1684ac2399c23ac28
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306597"
---
# <a name="patch-channel"></a><span data-ttu-id="7f7dd-103">Canal de revisión</span><span class="sxs-lookup"><span data-stu-id="7f7dd-103">Patch channel</span></span>



<span data-ttu-id="7f7dd-104">Actualizar las propiedades del [canal](../resources/channel.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-104">Update the properties of the specified [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="7f7dd-105">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="7f7dd-106">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="7f7dd-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="7f7dd-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7f7dd-107">Permissions</span></span>
<span data-ttu-id="7f7dd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7f7dd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7f7dd-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7f7dd-110">Permission type</span></span>      | <span data-ttu-id="7f7dd-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7f7dd-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7f7dd-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7f7dd-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7f7dd-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f7dd-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7f7dd-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7f7dd-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7f7dd-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-115">Not supported.</span></span>    |
|<span data-ttu-id="7f7dd-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7f7dd-116">Application</span></span> | <span data-ttu-id="7f7dd-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7f7dd-117">Group.ReadWrite.All</span></span> |

> <span data-ttu-id="7f7dd-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="7f7dd-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="7f7dd-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7f7dd-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="7f7dd-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7f7dd-121">Request headers</span></span>
| <span data-ttu-id="7f7dd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f7dd-122">Header</span></span>       | <span data-ttu-id="7f7dd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7f7dd-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7f7dd-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="7f7dd-124">Authorization</span></span>  | <span data-ttu-id="7f7dd-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="7f7dd-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7f7dd-127">Content-Type</span></span>  | <span data-ttu-id="7f7dd-128">application/json</span><span class="sxs-lookup"><span data-stu-id="7f7dd-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7f7dd-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7f7dd-129">Request body</span></span>
<span data-ttu-id="7f7dd-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [canal](../resources/channel.md) .</span><span class="sxs-lookup"><span data-stu-id="7f7dd-130">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="7f7dd-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f7dd-131">Response</span></span>

<span data-ttu-id="7f7dd-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-132">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7f7dd-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7f7dd-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7f7dd-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7f7dd-134">Request</span></span>
<span data-ttu-id="7f7dd-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "patch_channel"
}-->
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="7f7dd-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7f7dd-136">Response</span></span>
<span data-ttu-id="7f7dd-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
    "description": "description-value",
    "displayName": "display-name-value",
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Patch channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
