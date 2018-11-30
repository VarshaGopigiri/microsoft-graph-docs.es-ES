---
title: Lista privilegedRoleAssignments
description: Recuperar una lista de objetos de privilegedRoleAssignment, que corresponden a todas las asignaciones de roles para la organización.
ms.openlocfilehash: 7642768348e2fff43f52c6865cabf85aa16ef893
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089159"
---
# <a name="list-privilegedroleassignments"></a><span data-ttu-id="7ae73-103">Lista privilegedRoleAssignments</span><span class="sxs-lookup"><span data-stu-id="7ae73-103">List privilegedRoleAssignments</span></span>

> <span data-ttu-id="7ae73-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7ae73-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7ae73-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7ae73-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7ae73-106">Recuperar una lista de objetos de [privilegedRoleAssignment](../resources/privilegedroleassignment.md) , que corresponden a todas las asignaciones de roles para la organización.</span><span class="sxs-lookup"><span data-stu-id="7ae73-106">Retrieve a list of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) objects, which correspond to all role assignments for the organization.</span></span>
## <a name="permissions"></a><span data-ttu-id="7ae73-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7ae73-107">Permissions</span></span>
<span data-ttu-id="7ae73-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7ae73-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="7ae73-110">El solicitante debe tener uno de los siguientes roles: _Administrador de roles con privilegios_, _Administrador Global_, _Administrador de seguridad_o _Lector de seguridad_.</span><span class="sxs-lookup"><span data-stu-id="7ae73-110">The requestor needs to have one of the following roles: _Privileged Role Administrator_, _Global Administrator_, _Security Administrator_, or _Security Reader_.</span></span> 

|<span data-ttu-id="7ae73-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7ae73-111">Permission type</span></span>      | <span data-ttu-id="7ae73-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7ae73-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7ae73-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7ae73-113">Delegated (work or school account)</span></span> | <span data-ttu-id="7ae73-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7ae73-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7ae73-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7ae73-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7ae73-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ae73-116">Not supported.</span></span>    |
|<span data-ttu-id="7ae73-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7ae73-117">Application</span></span> | <span data-ttu-id="7ae73-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ae73-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7ae73-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7ae73-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoleAssignments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7ae73-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7ae73-120">Optional query parameters</span></span>
<span data-ttu-id="7ae73-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ae73-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7ae73-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ae73-122">Request headers</span></span>
| <span data-ttu-id="7ae73-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="7ae73-123">Name</span></span>      |<span data-ttu-id="7ae73-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ae73-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="7ae73-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="7ae73-125">Authorization</span></span>  | <span data-ttu-id="7ae73-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7ae73-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7ae73-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7ae73-128">Request body</span></span>
<span data-ttu-id="7ae73-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7ae73-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7ae73-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ae73-130">Response</span></span>

<span data-ttu-id="7ae73-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [privilegedRoleAssignment](../resources/privilegedroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ae73-131">If successful, this method returns a `200 OK` response code and collection of [privilegedRoleAssignment](../resources/privilegedroleassignment.md) objects in the response body.</span></span>

<span data-ttu-id="7ae73-132">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="7ae73-132">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="7ae73-133">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="7ae73-133">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="examples"></a><span data-ttu-id="7ae73-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7ae73-134">Examples</span></span>
### <a name="get-all-role-assignments"></a><span data-ttu-id="7ae73-135">Obtener todas las asignaciones de roles</span><span class="sxs-lookup"><span data-stu-id="7ae73-135">Get all role assignments</span></span>
##### <a name="request"></a><span data-ttu-id="7ae73-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ae73-136">Request</span></span>
<span data-ttu-id="7ae73-137">En el ejemplo siguiente se muestra una solicitud para obtener todas las asignaciones de roles:</span><span class="sxs-lookup"><span data-stu-id="7ae73-137">The following example shows a request to get all role assignments:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedroleassignments"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignments
```
##### <a name="response"></a><span data-ttu-id="7ae73-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ae73-138">Response</span></span>
<span data-ttu-id="7ae73-139">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ae73-139">The following example shows the response.</span></span> <span data-ttu-id="7ae73-140">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="7ae73-140">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="7ae73-141">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ae73-141">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "value": [
    {
      "id": "id-value",
      "userId": "userId-value",
      "roleId": "roleId-value",
      "isElevated": true,
      "expirationDateTime": "2016-10-19T10:37:00Z",
      "resultMessage": "resultMessage-value"
    }
  ]
}
```
### <a name="get-active-role-assignments"></a><span data-ttu-id="7ae73-142">Obtener las asignaciones de rol activo</span><span class="sxs-lookup"><span data-stu-id="7ae73-142">Get active role assignments</span></span>
##### <a name="request"></a><span data-ttu-id="7ae73-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ae73-143">Request</span></span> 
<span data-ttu-id="7ae73-144">En el ejemplo siguiente se muestra una solicitud para las asignaciones de rol activo de consulta:</span><span class="sxs-lookup"><span data-stu-id="7ae73-144">The following example shows a request to query active role assignments:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedroleassignments"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignments?$filter=isElevated%20eq%20true
```
##### <a name="response"></a><span data-ttu-id="7ae73-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ae73-145">Response</span></span>
<span data-ttu-id="7ae73-146">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ae73-146">The following example shows the response.</span></span> <span data-ttu-id="7ae73-147">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="7ae73-147">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="7ae73-148">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ae73-148">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "value": [
        {
            "id": "0f693614-c255-4cf5-92fa-74e770c656d8_62e90394-69f5-4237-9190-012177145e10",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "roleId": "62e90394-69f5-4237-9190-012177145e10",
            "isElevated": true,
            "expirationDateTime": null,
            "resultMessage": null
        },
        {
            "id": "0f693614-c255-4cf5-92fa-74e770c656d8_95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "isElevated": true,
            "expirationDateTime": "2017-07-25T17:38:49.563Z",
            "resultMessage": null
        }
  ]
}
```
### <a name="get-permanent-role-assignments"></a><span data-ttu-id="7ae73-149">Obtener las asignaciones de roles permanente</span><span class="sxs-lookup"><span data-stu-id="7ae73-149">Get permanent role assignments</span></span>
##### <a name="request"></a><span data-ttu-id="7ae73-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ae73-150">Request</span></span> 
<span data-ttu-id="7ae73-151">En el ejemplo siguiente se muestra una solicitud para asignaciones de roles permanente de consulta, donde ``expirationDateTime`` valor es ``null``:</span><span class="sxs-lookup"><span data-stu-id="7ae73-151">The following example shows a request to query permanent role assignments, where ``expirationDateTime`` value is ``null``:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedroleassignments"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignments?$filter=isElevated%20eq%20true%20and%20expirationDateTime%20eq%20null
```
##### <a name="response"></a><span data-ttu-id="7ae73-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ae73-152">Response</span></span>
<span data-ttu-id="7ae73-153">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ae73-153">The following example shows the response.</span></span> <span data-ttu-id="7ae73-154">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="7ae73-154">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="7ae73-155">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ae73-155">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "value": [
        {
            "id": "0f693614-c255-4cf5-92fa-74e770c656d8_194ae4cb-b126-40b2-bd5b-6091b380977d",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "roleId": "194ae4cb-b126-40b2-bd5b-6091b380977d",
            "isElevated": true,
            "expirationDateTime": null,
            "resultMessage": null
        },
        {
            "id": "0f693614-c255-4cf5-92fa-74e770c656d8_44367163-eba1-44c3-98af-f5787879f96a",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "roleId": "44367163-eba1-44c3-98af-f5787879f96a",
            "isElevated": true,
            "expirationDateTime": null,
            "resultMessage": null
        }
  ]
}
```
### <a name="get-eligible-role-assignments"></a><span data-ttu-id="7ae73-156">Obtener las asignaciones de roles optan</span><span class="sxs-lookup"><span data-stu-id="7ae73-156">Get eligible role assignments</span></span>
##### <a name="request"></a><span data-ttu-id="7ae73-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ae73-157">Request</span></span> 
<span data-ttu-id="7ae73-158">En el ejemplo siguiente se muestra una solicitud para las asignaciones de funciones optan de consulta, incluidos los que no está activo y active:</span><span class="sxs-lookup"><span data-stu-id="7ae73-158">The following example shows a request to query eligible role assignments, including the active and non-active ones:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedroleassignments"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignments?$filter=isElevated%20eq%20true%20and%20expirationDateTime%20ne%20null%20or%20isElevated%20eq%20false
```
##### <a name="response"></a><span data-ttu-id="7ae73-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ae73-159">Response</span></span> 
<span data-ttu-id="7ae73-160">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ae73-160">The following example shows the response.</span></span> <span data-ttu-id="7ae73-161">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="7ae73-161">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="7ae73-162">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ae73-162">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 237

{
  "value": [
        {
            "id": "0f693614-c255-4cf5-92fa-74e770c656d8_95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "isElevated": true,
            "expirationDateTime": "2017-07-25T18:42:26.823Z",
            "resultMessage": null
        },
        {
            "id": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f81_194ae4cb-b126-40b2-bd5b-6091b380977d",
            "userId": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f81",
            "roleId": "194ae4cb-b126-40b2-bd5b-6091b380977d",
            "isElevated": false,
            "expirationDateTime": null,
            "resultMessage": null
        },
        {
            "id": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f81_9360feb5-f418-4baa-8175-e2a00bac4301",
            "userId": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f81",
            "roleId": "9360feb5-f418-4baa-8175-e2a00bac4301",
            "isElevated": false,
            "expirationDateTime": null,
            "resultMessage": null
        },
        {
            "id": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f81_95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "userId": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f81",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "isElevated": false,
            "expirationDateTime": null,
            "resultMessage": null
        }
  ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List privilegedRoleAssignments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
