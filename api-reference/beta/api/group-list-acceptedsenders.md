---
title: List acceptedSenders
description: Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.
ms.openlocfilehash: a4a4970abe0a6a866ed26fa04ebe3f7a0cee1f8c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090416"
---
# <a name="list-acceptedsenders"></a><span data-ttu-id="fc07d-103">List acceptedSenders</span><span class="sxs-lookup"><span data-stu-id="fc07d-103">List acceptedSenders</span></span>

> <span data-ttu-id="fc07d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fc07d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fc07d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fc07d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fc07d-106">Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.</span><span class="sxs-lookup"><span data-stu-id="fc07d-106">Get a list of users or groups that are in the acceptedSenders list for this group.</span></span>

<span data-ttu-id="fc07d-p102">Los usuarios de la lista de remitentes aceptados pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud GET). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes aceptados y de remitentes rechazados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="fc07d-p102">Users in the accepted senders list can post to conversations of the group (identified in the GET request URL). Make sure you do not specify the same user or group in the accepted senders and rejected senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="fc07d-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc07d-109">Permissions</span></span>
<span data-ttu-id="fc07d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc07d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc07d-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc07d-112">Permission type</span></span>      | <span data-ttu-id="fc07d-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc07d-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fc07d-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc07d-114">Delegated (work or school account)</span></span> | <span data-ttu-id="fc07d-115">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc07d-115">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="fc07d-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc07d-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fc07d-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc07d-117">Not supported.</span></span>    |
|<span data-ttu-id="fc07d-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc07d-118">Application</span></span> | <span data-ttu-id="fc07d-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc07d-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fc07d-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc07d-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/acceptedSenders
```

## <a name="optional-query-parameters"></a><span data-ttu-id="fc07d-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fc07d-121">Optional query parameters</span></span>
<span data-ttu-id="fc07d-122">Este método admite los [parámetros de consulta de OData](/graph/query-parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc07d-122">This method supports the [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="fc07d-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc07d-123">Request headers</span></span>
| <span data-ttu-id="fc07d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc07d-124">Header</span></span>       | <span data-ttu-id="fc07d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fc07d-125">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="fc07d-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc07d-126">Authorization</span></span>  | <span data-ttu-id="fc07d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc07d-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="fc07d-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc07d-129">Request body</span></span>
<span data-ttu-id="fc07d-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fc07d-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fc07d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc07d-131">Response</span></span>
<span data-ttu-id="fc07d-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc07d-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc07d-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc07d-133">Example</span></span>
#### <a name="request"></a><span data-ttu-id="fc07d-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc07d-134">Request</span></span>
<span data-ttu-id="fc07d-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc07d-135">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_acceptedsenders"
}-->
```http
GET https://graph.microsoft.com/beta/groups/{id}/acceptedSenders
```

#### <a name="response"></a><span data-ttu-id="fc07d-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc07d-136">Response</span></span>
<span data-ttu-id="fc07d-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc07d-137">The following is an example of the response.</span></span>
><span data-ttu-id="fc07d-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="fc07d-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="fc07d-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc07d-139">All the properties will be returned from an actual call.</span></span>
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