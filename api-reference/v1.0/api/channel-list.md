---
title: Canales de lista
description: Recuperar la lista de canales en este equipo.
ms.openlocfilehash: 5f96d4c47a787839626a9d90733d087906407b01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030054"
---
# <a name="list-channels"></a><span data-ttu-id="c6894-103">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="c6894-103">List channels</span></span>



<span data-ttu-id="c6894-104">Recuperar la lista de [canales](../resources/channel.md) en este equipo.</span><span class="sxs-lookup"><span data-stu-id="c6894-104">Retrieve the list of [channels](../resources/channel.md) in this team.</span></span>

## <a name="permissions"></a><span data-ttu-id="c6894-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6894-105">Permissions</span></span>
<span data-ttu-id="c6894-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6894-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c6894-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6894-108">Permission type</span></span>      | <span data-ttu-id="c6894-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6894-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6894-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6894-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c6894-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6894-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c6894-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6894-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6894-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6894-113">Not supported.</span></span>    |
|<span data-ttu-id="c6894-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6894-114">Application</span></span> | <span data-ttu-id="c6894-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6894-115">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="c6894-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6894-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c6894-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c6894-117">Optional query parameters</span></span>
<span data-ttu-id="c6894-118">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6894-118">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c6894-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6894-119">Request headers</span></span>
| <span data-ttu-id="c6894-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6894-120">Header</span></span>       | <span data-ttu-id="c6894-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c6894-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c6894-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c6894-122">Authorization</span></span>  | <span data-ttu-id="c6894-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6894-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c6894-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6894-125">Request body</span></span>
<span data-ttu-id="c6894-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c6894-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c6894-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6894-127">Response</span></span>

<span data-ttu-id="c6894-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6894-128">If successful, this method returns a `200 OK` response code and collection of [Channel](../resources/channel.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6894-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6894-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c6894-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6894-130">Request</span></span>
<span data-ttu-id="c6894-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6894-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channels"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels
```
##### <a name="response"></a><span data-ttu-id="c6894-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6894-132">Response</span></span>
<span data-ttu-id="c6894-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6894-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
