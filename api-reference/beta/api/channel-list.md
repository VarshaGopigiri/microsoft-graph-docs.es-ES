---
title: Canales de lista
description: Recuperar la lista de canales en este equipo.
ms.openlocfilehash: a37ca4e6012dd287b1b637fe3ddb3cfc2aaf5518
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084008"
---
# <a name="list-channels"></a><span data-ttu-id="ee415-103">Canales de lista</span><span class="sxs-lookup"><span data-stu-id="ee415-103">List channels</span></span>

> <span data-ttu-id="ee415-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee415-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee415-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee415-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ee415-106">Recuperar la lista de [canales](../resources/channel.md) en este equipo.</span><span class="sxs-lookup"><span data-stu-id="ee415-106">Retrieve the list of [channels](../resources/channel.md) in this team.</span></span>

## <a name="permissions"></a><span data-ttu-id="ee415-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ee415-107">Permissions</span></span>
<span data-ttu-id="ee415-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee415-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="ee415-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee415-110">Permission type</span></span>      | <span data-ttu-id="ee415-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee415-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ee415-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee415-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ee415-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ee415-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ee415-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee415-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ee415-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee415-115">Not supported.</span></span>    |
|<span data-ttu-id="ee415-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee415-116">Application</span></span> | <span data-ttu-id="ee415-117">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ee415-117">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="ee415-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee415-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}/channels
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ee415-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ee415-119">Optional query parameters</span></span>
<span data-ttu-id="ee415-120">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee415-120">This method supports the $filter, $select, and $expand [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ee415-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee415-121">Request headers</span></span>
| <span data-ttu-id="ee415-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee415-122">Header</span></span>       | <span data-ttu-id="ee415-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ee415-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ee415-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee415-124">Authorization</span></span>  | <span data-ttu-id="ee415-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee415-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ee415-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ee415-127">Request body</span></span>
<span data-ttu-id="ee415-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ee415-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ee415-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee415-129">Response</span></span>

<span data-ttu-id="ee415-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [canal](../resources/channel.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee415-130">If successful, this method returns a `200 OK` response code and collection of [Channel](../resources/channel.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee415-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee415-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ee415-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee415-132">Request</span></span>
<span data-ttu-id="ee415-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee415-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_channels"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels
```
##### <a name="response"></a><span data-ttu-id="ee415-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee415-134">Response</span></span>
<span data-ttu-id="ee415-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee415-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
