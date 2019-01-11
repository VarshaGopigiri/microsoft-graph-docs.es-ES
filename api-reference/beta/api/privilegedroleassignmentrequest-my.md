---
title: 'privilegedRoleAssignmentRequest: Mi'
description: Obtenga las solicitudes de asignación de roles con privilegios del solicitante.
localization_priority: Normal
ms.openlocfilehash: 8f37224dd47be060f1ffc8a3551c537289edf966
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27872166"
---
# <a name="privilegedroleassignmentrequest-my"></a><span data-ttu-id="138e6-103">privilegedRoleAssignmentRequest: Mi</span><span class="sxs-lookup"><span data-stu-id="138e6-103">privilegedRoleAssignmentRequest: my</span></span>

> <span data-ttu-id="138e6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="138e6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="138e6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="138e6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="138e6-106">Obtenga las solicitudes de asignación de roles con privilegios del solicitante.</span><span class="sxs-lookup"><span data-stu-id="138e6-106">Get the requester's privileged role assignment requests.</span></span>

## <a name="permissions"></a><span data-ttu-id="138e6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="138e6-107">Permissions</span></span>
<span data-ttu-id="138e6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="138e6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="138e6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="138e6-110">Permission type</span></span>                        | <span data-ttu-id="138e6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="138e6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------------------------|:---------------------------------------------------------|
|<span data-ttu-id="138e6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="138e6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="138e6-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="138e6-113">PrivilegedAccess.ReadWrite.AzureAD, Directory.Read.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="138e6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="138e6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="138e6-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="138e6-115">Not supported.</span></span> |
|<span data-ttu-id="138e6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="138e6-116">Application</span></span>                            | <span data-ttu-id="138e6-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="138e6-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="138e6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="138e6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignmentRequests/my
```
## <a name="optional-query-parameters"></a><span data-ttu-id="138e6-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="138e6-119">Optional query parameters</span></span>
<span data-ttu-id="138e6-120">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="138e6-120">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="138e6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="138e6-121">Request headers</span></span>
| <span data-ttu-id="138e6-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="138e6-122">Name</span></span>      |<span data-ttu-id="138e6-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="138e6-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="138e6-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="138e6-124">Authorization</span></span>  | <span data-ttu-id="138e6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="138e6-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="138e6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="138e6-127">Request body</span></span>
<span data-ttu-id="138e6-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="138e6-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="138e6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="138e6-129">Response</span></span>
<span data-ttu-id="138e6-130">Si tiene éxito, este método devuelve `200 OK` objeto de colección de respuesta código y [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="138e6-130">If successful, this method returns `200 OK` response code and [privilegedRoleAssignmentRequest](../resources/privilegedroleassignmentrequest.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="138e6-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="138e6-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="138e6-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="138e6-132">Request</span></span>
<span data-ttu-id="138e6-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="138e6-133">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "privilegedroleassignmentrequest_my)"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignmentRequests/my
```

##### <a name="response"></a><span data-ttu-id="138e6-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="138e6-134">Response</span></span>
<span data-ttu-id="138e6-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="138e6-135">The following is an example of the response.</span></span> <span data-ttu-id="138e6-136">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="138e6-136">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="138e6-137">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="138e6-137">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequest"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 304

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#privilegedRoleAssignmentRequests",
    "@odata.count": 4,
    "value": [{
        "schedule": {
            "type": "activation",
            "startDateTime": "2018-02-08T02:35:17.903Z",
            "endDateTime": null,
            "duration" : null
        },
        "id": "e13ef8a0-c1cb-4d03-aaae-9cd1c8ede2d1",
         "userId": "Self"，
         "roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b",
        "evaluateOnly": false,
        "type": "UserAdd",
        "assignmentState": "Active",
        "requestedDateTime": "2018-02-08T02:35:42.9137335Z",
        "status": "RequestedApproval",
        "duration": "2",
        "reason": "Activate the role for business purpose",
        "ticketNumber": "234",
        "ticketSystem": "system",
        "roleInfo@odata.context": "https://graph.microsoft.com/beta/$metadata#privilegedRoleAssignmentRequests('e13ef8a0-c1cb-4d03-aaae-9cd1c8ede2d1')/roleInfo/$entity",
        "roleInfo": {
            "id": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b",
            "name": "Directory Readers"
        }
    }, {
        "schedule": {
            "type": "activation",
            "startDateTime": "2018-02-07T22:55:00Z",
            "endDateTime": null,
            "duration" : null
        },
        "id": "03ea0c3d-90a0-42d4-b220-11c049c506fb",
        "userId": "Self"，
        "roleId": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b",
        "evaluateOnly": false,
        "type": "UserAdd",
        "assignmentState": "Active",
        "requestedDateTime": "2018-02-07T22:17:37.2215343Z",
        "status": "ApprovalAborted",
        "duration": "1",
        "reason": "Activate for testing",
        "ticketNumber": "222",
        "ticketSystem": "222",
        "roleInfo@odata.context": "https://graph.microsoft.com/beta/$metadata#privilegedRoleAssignmentRequests('03ea0c3d-90a0-42d4-b220-11c049c506fb')/roleInfo/$entity",
        "roleInfo": {
            "id": "88d8e3e3-8f55-4a1e-953a-9b9898b8876b",
            "name": "Directory Readers"
        }
    }]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleAssignmentRequest: my",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
