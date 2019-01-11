---
title: Lista privilegedRoleAssignmentRequests
description: 'Recuperar una colección de privilegedRoleAssignmentRequest. '
localization_priority: Normal
ms.openlocfilehash: 4bae072caeb54c513e9146fe36dfd100ce1b4360
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838706"
---
# <a name="list-privilegedroleassignmentrequests"></a><span data-ttu-id="9dac3-103">Lista privilegedRoleAssignmentRequests</span><span class="sxs-lookup"><span data-stu-id="9dac3-103">List privilegedRoleAssignmentRequests</span></span>

> <span data-ttu-id="9dac3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9dac3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9dac3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9dac3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9dac3-106">Recuperar una colección de [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md).</span><span class="sxs-lookup"><span data-stu-id="9dac3-106">Retrieve a collection of [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md).</span></span> 

<span data-ttu-id="9dac3-107">**Nota:** Este solicitante debe tener al menos una asignación de funciones en el recurso.</span><span class="sxs-lookup"><span data-stu-id="9dac3-107">**Note:** This requester must have at least one role assignment on the resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="9dac3-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="9dac3-108">Permissions</span></span>
<span data-ttu-id="9dac3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9dac3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9dac3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9dac3-111">Permission type</span></span>                        | <span data-ttu-id="9dac3-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9dac3-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="9dac3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9dac3-113">Delegated (work or school account)</span></span> | <span data-ttu-id="9dac3-114">PrivilegedAccess.ReadWrite.AzureAD, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9dac3-114">PrivilegedAccess.ReadWrite.AzureAD, Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="9dac3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9dac3-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9dac3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9dac3-116">Not supported.</span></span> |
|<span data-ttu-id="9dac3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9dac3-117">Application</span></span>                            | <span data-ttu-id="9dac3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9dac3-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9dac3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9dac3-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoleAssignmentRequests
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9dac3-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9dac3-120">Optional query parameters</span></span>
<span data-ttu-id="9dac3-121">Este método es compatible con los [parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9dac3-121">This method supports the [OData query parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9dac3-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9dac3-122">Request headers</span></span>
| <span data-ttu-id="9dac3-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="9dac3-123">Name</span></span>      |<span data-ttu-id="9dac3-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dac3-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="9dac3-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="9dac3-125">Authorization</span></span>  | <span data-ttu-id="9dac3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9dac3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9dac3-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9dac3-128">Request body</span></span>
<span data-ttu-id="9dac3-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9dac3-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9dac3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9dac3-130">Response</span></span>
<span data-ttu-id="9dac3-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9dac3-131">If successful, this method returns a `200 OK` response code and a collection of [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9dac3-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9dac3-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9dac3-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9dac3-133">Request</span></span>
<span data-ttu-id="9dac3-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9dac3-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedroleassignmentrequest"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignmentRequests
```
##### <a name="response"></a><span data-ttu-id="9dac3-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9dac3-135">Response</span></span>
<span data-ttu-id="9dac3-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9dac3-136">The following is an example of the response.</span></span> <span data-ttu-id="9dac3-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="9dac3-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="9dac3-138">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9dac3-138">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequest",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 304

{
  "@odata.context":"https://https://graph.microsoft.com/beta/$metadata#privilegedRoleAssignmentRequests",
  "value":[
    {
      "schedule":{
        "type":"activation","startDateTime":"2018-02-07T22:55:00Z","endDateTime":null,"duration" : null
      },"id":"03ea0c3d-90a0-42d4-b220-11c049c506fb","userId": "Self"，"roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b","evaluateOnly":false,"type":"UserAdd","assignmentState":"Active","requestedDateTime":"2018-02-07T22:17:37.2215343Z","status":"ApprovalAborted","duration":"1","reason":"Activate for testing","ticketNumber":"222","ticketSystem":"222"
    },{
      "schedule":{
        "type":"assignment","startDateTime":"2018-01-23T02:43:15.258242Z","endDateTime":null,"duration" : null
      },"id":"fe4450bb-6d28-4583-8fc4-25b0ea91daf5","userId": "Self"，"roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b","evaluateOnly":false,"type":"UserAdd","assignmentState":"Active","requestedDateTime":"2018-01-23T02:42:55.628338Z","status":"Completed","duration":"1","reason":"asdf","ticketNumber":null,"ticketSystem":null
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List privilegedRoleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
