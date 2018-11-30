---
title: List acceptedSenders
description: Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.
ms.openlocfilehash: d06919f67a4d4afe917e87571f403970825f66ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032506"
---
# <a name="list-acceptedsenders"></a><span data-ttu-id="5392a-103">List acceptedSenders</span><span class="sxs-lookup"><span data-stu-id="5392a-103">List acceptedSenders</span></span>
<span data-ttu-id="5392a-104">Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.</span><span class="sxs-lookup"><span data-stu-id="5392a-104">Get a list of users or groups that are in the acceptedSenders list for this group.</span></span>

<span data-ttu-id="5392a-p101">Los usuarios de la lista de remitentes aceptados pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud GET). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes aceptados y de remitentes rechazados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="5392a-p101">Users in the accepted senders list can post to conversations of the group (identified in the GET request URL). Make sure you do not specify the same user or group in the accepted senders and rejected senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="5392a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5392a-107">Permissions</span></span>
<span data-ttu-id="5392a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5392a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5392a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5392a-110">Permission type</span></span>      | <span data-ttu-id="5392a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5392a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5392a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5392a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5392a-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5392a-113">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5392a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5392a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5392a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5392a-115">Not supported.</span></span>    |
|<span data-ttu-id="5392a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5392a-116">Application</span></span> | <span data-ttu-id="5392a-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5392a-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5392a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5392a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/acceptedSenders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5392a-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5392a-119">Optional query parameters</span></span>
<span data-ttu-id="5392a-120">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5392a-120">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5392a-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5392a-121">Request headers</span></span>
| <span data-ttu-id="5392a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5392a-122">Header</span></span>       | <span data-ttu-id="5392a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5392a-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5392a-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="5392a-124">Authorization</span></span>  | <span data-ttu-id="5392a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5392a-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5392a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5392a-127">Request body</span></span>
<span data-ttu-id="5392a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5392a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5392a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5392a-129">Response</span></span>
<span data-ttu-id="5392a-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5392a-130">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5392a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5392a-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="5392a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5392a-132">Request</span></span>
<span data-ttu-id="5392a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5392a-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_acceptedsenders"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders
```

#### <a name="response"></a><span data-ttu-id="5392a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5392a-134">Response</span></span>
<span data-ttu-id="5392a-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5392a-135">The following is an example of the response.</span></span>
><span data-ttu-id="5392a-136">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="5392a-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="5392a-137">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5392a-137">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List acceptedSenders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->