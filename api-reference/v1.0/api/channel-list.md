---
title: Canales de lista
description: Recuperar la lista de canales en este equipo.
author: nkramer
localization_priority: Priority
ms.prod: microsoft-teams
ms.openlocfilehash: 609b83032877b77923e8444926aec785e4ae84db
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932696"
---
# <a name="list-channels"></a><span data-ttu-id="514a2-103">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="514a2-103">List channels</span></span>



<span data-ttu-id="514a2-104">Recuperar la lista de [canales](../resources/channel.md) en este equipo.</span><span class="sxs-lookup"><span data-stu-id="514a2-104">Retrieve the list of [channels](../resources/channel.md) in this team.</span></span>

## <a name="permissions"></a><span data-ttu-id="514a2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="514a2-105">Permissions</span></span>
<span data-ttu-id="514a2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="514a2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="514a2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="514a2-108">Permission type</span></span>      | <span data-ttu-id="514a2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="514a2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="514a2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="514a2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="514a2-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="514a2-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="514a2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="514a2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="514a2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="514a2-113">Not supported.</span></span>    |
|<span data-ttu-id="514a2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="514a2-114">Application</span></span> | <span data-ttu-id="514a2-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="514a2-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

> <span data-ttu-id="514a2-116">**Nota**: esta API es compatible con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="514a2-116">**Note**: This API supports admin permissions.</span></span> <span data-ttu-id="514a2-117">Los administradores globales y los administradores de servicios de Microsoft Teams pueden tener acceso a los equipos que no son miembros de.</span><span class="sxs-lookup"><span data-stu-id="514a2-117">Global admins and Microsoft Teams service admins can access teams that they are not a member of.</span></span>

## <a name="http-request"></a><span data-ttu-id="514a2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="514a2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels
```

## <a name="optional-query-parameters"></a><span data-ttu-id="514a2-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="514a2-119">Optional query parameters</span></span>
<span data-ttu-id="514a2-120">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="514a2-120">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="514a2-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="514a2-121">Request headers</span></span>
| <span data-ttu-id="514a2-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="514a2-122">Header</span></span>       | <span data-ttu-id="514a2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="514a2-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="514a2-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="514a2-124">Authorization</span></span>  | <span data-ttu-id="514a2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="514a2-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="514a2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="514a2-127">Request body</span></span>
<span data-ttu-id="514a2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="514a2-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="514a2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="514a2-129">Response</span></span>

<span data-ttu-id="514a2-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="514a2-130">If successful, this method returns a `200 OK` response code and collection of [Channel](../resources/channel.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="514a2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="514a2-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="514a2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="514a2-132">Request</span></span>
<span data-ttu-id="514a2-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="514a2-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channels"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels
```
##### <a name="response"></a><span data-ttu-id="514a2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="514a2-134">Response</span></span>
<span data-ttu-id="514a2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="514a2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.channel",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 262

{
  "value": [
    {
      "description": "description-value",
      "displayName": "display-name-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List channels",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
