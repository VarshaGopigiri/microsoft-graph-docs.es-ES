---
title: Canal de revisión
description: Actualizar las propiedades del canal especificado.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 4c3a03aaab52da62f56ca376035e56a9b8584832
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984342"
---
# <a name="patch-channel"></a><span data-ttu-id="710ed-103">Canal de revisión</span><span class="sxs-lookup"><span data-stu-id="710ed-103">Patch channel</span></span>



<span data-ttu-id="710ed-104">Actualizar las propiedades del [canal](../resources/channel.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="710ed-104">Update the properties of the specified [channel](../resources/channel.md).</span></span>

> <span data-ttu-id="710ed-105">**Nota**: hay un problema conocido con permisos de la aplicación y esta API.</span><span class="sxs-lookup"><span data-stu-id="710ed-105">**Note**: There is a known issue with application permissions and this API.</span></span> <span data-ttu-id="710ed-106">Para obtener información detallada, vea el [conocido lista de problemas](/graph/known-issues#application-permissions).</span><span class="sxs-lookup"><span data-stu-id="710ed-106">For details, see the [known issues list](/graph/known-issues#application-permissions).</span></span>

## <a name="permissions"></a><span data-ttu-id="710ed-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="710ed-107">Permissions</span></span>
<span data-ttu-id="710ed-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="710ed-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="710ed-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="710ed-110">Permission type</span></span>      | <span data-ttu-id="710ed-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="710ed-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="710ed-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="710ed-112">Delegated (work or school account)</span></span> | <span data-ttu-id="710ed-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="710ed-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="710ed-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="710ed-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="710ed-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="710ed-115">Not supported.</span></span>    |
|<span data-ttu-id="710ed-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="710ed-116">Application</span></span> | <span data-ttu-id="710ed-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="710ed-117">Group.ReadWrite.All</span></span> |

> <span data-ttu-id="710ed-118">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="710ed-118">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="710ed-119">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="710ed-119">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="710ed-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="710ed-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /teams/{id}/channels/{id}
```
## <a name="request-headers"></a><span data-ttu-id="710ed-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="710ed-121">Request headers</span></span>
| <span data-ttu-id="710ed-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="710ed-122">Header</span></span>       | <span data-ttu-id="710ed-123">Valor</span><span class="sxs-lookup"><span data-stu-id="710ed-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="710ed-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="710ed-124">Authorization</span></span>  | <span data-ttu-id="710ed-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="710ed-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="710ed-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="710ed-127">Content-Type</span></span>  | <span data-ttu-id="710ed-128">application/json</span><span class="sxs-lookup"><span data-stu-id="710ed-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="710ed-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="710ed-129">Request body</span></span>
<span data-ttu-id="710ed-130">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [canal](../resources/channel.md) .</span><span class="sxs-lookup"><span data-stu-id="710ed-130">In the request body, supply a JSON representation of [channel](../resources/channel.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="710ed-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="710ed-131">Response</span></span>

<span data-ttu-id="710ed-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="710ed-132">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="710ed-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="710ed-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="710ed-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="710ed-134">Request</span></span>
<span data-ttu-id="710ed-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="710ed-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "patch_channel"
}-->
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="710ed-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="710ed-136">Response</span></span>
<span data-ttu-id="710ed-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="710ed-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
