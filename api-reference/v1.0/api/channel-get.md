---
title: Obtener el canal
description: Recuperar las propiedades y relaciones de un canal.
ms.openlocfilehash: 42f25d0866af9000cfb6f96952ac19e32af0e87c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029389"
---
# <a name="get-channel"></a><span data-ttu-id="48cba-103">Obtener el canal</span><span class="sxs-lookup"><span data-stu-id="48cba-103">Get channel</span></span>



<span data-ttu-id="48cba-104">Recuperar las propiedades y relaciones de un [canal](../resources/channel.md).</span><span class="sxs-lookup"><span data-stu-id="48cba-104">Retrieve the properties and relationships of a [channel](../resources/channel.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="48cba-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="48cba-105">Permissions</span></span>
<span data-ttu-id="48cba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="48cba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="48cba-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="48cba-108">Permission type</span></span>      | <span data-ttu-id="48cba-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="48cba-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="48cba-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="48cba-110">Delegated (work or school account)</span></span> | <span data-ttu-id="48cba-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48cba-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="48cba-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48cba-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="48cba-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="48cba-113">Not supported.</span></span>    |
|<span data-ttu-id="48cba-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48cba-114">Application</span></span> | <span data-ttu-id="48cba-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48cba-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="48cba-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="48cba-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels/{id}

```

## <a name="optional-query-parameters"></a><span data-ttu-id="48cba-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="48cba-117">Optional query parameters</span></span>

<span data-ttu-id="48cba-118">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48cba-118">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="48cba-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="48cba-119">Request headers</span></span>
| <span data-ttu-id="48cba-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48cba-120">Header</span></span>       | <span data-ttu-id="48cba-121">Valor</span><span class="sxs-lookup"><span data-stu-id="48cba-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="48cba-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="48cba-122">Authorization</span></span>  | <span data-ttu-id="48cba-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="48cba-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="48cba-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="48cba-125">Request body</span></span>
<span data-ttu-id="48cba-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="48cba-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="48cba-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48cba-127">Response</span></span>

<span data-ttu-id="48cba-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48cba-128">If successful, this method returns a `200 OK` response code and a [channel](../resources/channel.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="48cba-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48cba-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="48cba-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48cba-130">Request</span></span>
<span data-ttu-id="48cba-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48cba-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channel"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}
```
##### <a name="response"></a><span data-ttu-id="48cba-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48cba-132">Response</span></span>
<span data-ttu-id="48cba-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48cba-133">Here is an example of the response.</span></span> 

><span data-ttu-id="48cba-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="48cba-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
    "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
