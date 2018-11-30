---
title: List rejectedSenders
description: 'Obtiene una lista de usuarios o grupos que se encuentran en la lista de rejectedSenders de este grupo. '
ms.openlocfilehash: c3142f205442b6c14cb45e0d0706dd111e2ec2f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085839"
---
# <a name="list-rejectedsenders"></a><span data-ttu-id="1106b-103">List rejectedSenders</span><span class="sxs-lookup"><span data-stu-id="1106b-103">List rejectedSenders</span></span>

> <span data-ttu-id="1106b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1106b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1106b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1106b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1106b-106">Obtiene una lista de usuarios o grupos que se encuentran en la lista de rejectedSenders de este grupo.</span><span class="sxs-lookup"><span data-stu-id="1106b-106">Get a list of users or groups that are in the rejectedSenders list for this group.</span></span> 

<span data-ttu-id="1106b-p102">Los usuarios de la lista de remitentes rechazados no pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud GET). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes rechazados y de remitentes aceptados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="1106b-p102">Users in the rejected senders list cannot post to conversations of the group (identified in the GET request URL). Make sure you do not specify the same user or group in the rejected senders and accepted senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="1106b-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="1106b-109">Permissions</span></span>
<span data-ttu-id="1106b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1106b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1106b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1106b-112">Permission type</span></span>      | <span data-ttu-id="1106b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1106b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1106b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1106b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="1106b-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1106b-115">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="1106b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1106b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1106b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1106b-117">Not supported.</span></span>    |
|<span data-ttu-id="1106b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1106b-118">Application</span></span> | <span data-ttu-id="1106b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1106b-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="1106b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1106b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/rejectedSenders
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1106b-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1106b-121">Optional query parameters</span></span>
<span data-ttu-id="1106b-122">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1106b-122">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1106b-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1106b-123">Request headers</span></span>
| <span data-ttu-id="1106b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1106b-124">Header</span></span>       | <span data-ttu-id="1106b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1106b-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1106b-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="1106b-126">Authorization</span></span>  | <span data-ttu-id="1106b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1106b-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1106b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1106b-129">Request body</span></span>
<span data-ttu-id="1106b-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1106b-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1106b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1106b-131">Response</span></span>
<span data-ttu-id="1106b-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1106b-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1106b-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1106b-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="1106b-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1106b-134">Request</span></span>
<span data-ttu-id="1106b-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1106b-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_rejectedsenders"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/rejectedSenders
```

#### <a name="response"></a><span data-ttu-id="1106b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1106b-136">Response</span></span>
<span data-ttu-id="1106b-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1106b-137">The following is an example of the response.</span></span>
><span data-ttu-id="1106b-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="1106b-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="1106b-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1106b-139">All the properties will be returned from an actual call.</span></span>
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
  "description": "List rejectedSenders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->