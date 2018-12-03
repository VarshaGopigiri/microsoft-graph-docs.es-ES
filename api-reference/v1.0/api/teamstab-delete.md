---
title: Eliminar ficha de canal
description: 'Quita (libera) una ficha desde el canal especificado dentro de un equipo. '
ms.openlocfilehash: b3f35d2cc8280d440b8c834ad9443bd5bbfd6bcc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030790"
---
# <a name="delete-tab-from-channel"></a><span data-ttu-id="f5c37-103">Eliminar ficha de canal</span><span class="sxs-lookup"><span data-stu-id="f5c37-103">Delete tab from channel</span></span>



<span data-ttu-id="f5c37-104">Quita (libera) una ficha desde el [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="f5c37-104">Removes (unpins) a tab from the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="f5c37-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f5c37-105">Permissions</span></span>
<span data-ttu-id="f5c37-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5c37-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f5c37-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5c37-108">Permission type</span></span>      | <span data-ttu-id="f5c37-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5c37-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f5c37-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5c37-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f5c37-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f5c37-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="f5c37-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5c37-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f5c37-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5c37-113">Not supported.</span></span>    |
|<span data-ttu-id="f5c37-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5c37-114">Application</span></span> | <span data-ttu-id="f5c37-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f5c37-115">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="f5c37-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5c37-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="request-headers"></a><span data-ttu-id="f5c37-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5c37-117">Request headers</span></span>
| <span data-ttu-id="f5c37-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5c37-118">Header</span></span>       | <span data-ttu-id="f5c37-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f5c37-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f5c37-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5c37-120">Authorization</span></span>  | <span data-ttu-id="f5c37-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5c37-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f5c37-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5c37-123">Request body</span></span>
<span data-ttu-id="f5c37-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f5c37-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f5c37-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5c37-125">Response</span></span>

<span data-ttu-id="f5c37-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5c37-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f5c37-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5c37-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="f5c37-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5c37-129">Request</span></span>
<span data-ttu-id="f5c37-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5c37-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
DELETE https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="f5c37-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5c37-131">Response</span></span>
<span data-ttu-id="f5c37-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5c37-132">The following is an example of the response.</span></span> <span data-ttu-id="f5c37-133">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f5c37-133">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f5c37-134">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f5c37-134">All of the properties will be returned from an actual call.</span></span>
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