---
title: Lista privilegedOperationEvents
description: filtro '' expresión.
ms.openlocfilehash: c18e00086ae92610cdc05e31d9f04ecf7e5d5c48
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088721"
---
# <a name="list-privilegedoperationevents"></a><span data-ttu-id="f3943-103">Lista privilegedOperationEvents</span><span class="sxs-lookup"><span data-stu-id="f3943-103">List privilegedOperationEvents</span></span>

> <span data-ttu-id="f3943-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3943-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3943-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3943-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f3943-106">Recuperar una lista de objetos de [privilegedOperationEvent](../resources/privilegedoperationevent.md) , que representan los eventos de auditoría que se generan mediante la administración de identidades con privilegios para las operaciones de función.</span><span class="sxs-lookup"><span data-stu-id="f3943-106">Retrieve a list of [privilegedOperationEvent](../resources/privilegedoperationevent.md) objects, which represent the audit events that are generated by Privileged Identity Management for the role operations.</span></span> <span data-ttu-id="f3943-107">Para obtener detalles sobre el evento de auditoría, consulte [privilegedOperationEvent](../resources/privilegedoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="f3943-107">For the details about the audit event, refer [privilegedOperationEvent](../resources/privilegedoperationevent.md).</span></span> <span data-ttu-id="f3943-108">Para filtrar los resultados de consulta, usar el estándar de OData ``$filter`` expresión.</span><span class="sxs-lookup"><span data-stu-id="f3943-108">To filter the query results, use the standard OData ``$filter`` expression.</span></span>


## <a name="permissions"></a><span data-ttu-id="f3943-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="f3943-109">Permissions</span></span>
<span data-ttu-id="f3943-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3943-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="f3943-112">El solicitante debe tener uno de los siguientes roles: _Administrador de roles con privilegios_, _Administrador Global_, _Administrador de seguridad_o _Lector de seguridad_.</span><span class="sxs-lookup"><span data-stu-id="f3943-112">The requestor needs to have one of the following roles: _Privileged Role Administrator_, _Global Administrator_, _Security Administrator_, or _Security Reader_.</span></span>

 

|<span data-ttu-id="f3943-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3943-113">Permission type</span></span>      | <span data-ttu-id="f3943-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3943-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f3943-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3943-115">Delegated (work or school account)</span></span> | <span data-ttu-id="f3943-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f3943-116">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f3943-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3943-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3943-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3943-118">Not supported.</span></span>    |
|<span data-ttu-id="f3943-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3943-119">Application</span></span> | <span data-ttu-id="f3943-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3943-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f3943-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3943-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedOperationEvents
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f3943-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f3943-122">Optional query parameters</span></span>
<span data-ttu-id="f3943-123">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3943-123">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f3943-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3943-124">Request headers</span></span>
| <span data-ttu-id="f3943-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3943-125">Name</span></span>      |<span data-ttu-id="f3943-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3943-126">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f3943-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="f3943-127">Authorization</span></span>  | <span data-ttu-id="f3943-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3943-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f3943-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f3943-130">Request body</span></span>
<span data-ttu-id="f3943-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f3943-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f3943-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3943-132">Response</span></span>

<span data-ttu-id="f3943-133">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [privilegedOperationEvent](../resources/privilegedoperationevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3943-133">If successful, this method returns a `200 OK` response code and collection of [privilegedOperationEvent](../resources/privilegedoperationevent.md) objects in the response body.</span></span>

<span data-ttu-id="f3943-134">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="f3943-134">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="f3943-135">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="f3943-135">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="examples"></a><span data-ttu-id="f3943-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3943-136">Examples</span></span>

### <a name="get-audit-events-for-role-assignment-operations"></a><span data-ttu-id="f3943-137">Obtener eventos de auditoría para las operaciones de asignación de rol</span><span class="sxs-lookup"><span data-stu-id="f3943-137">Get audit events for role assignment operations</span></span>
##### <a name="request"></a><span data-ttu-id="f3943-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3943-138">Request</span></span>
<span data-ttu-id="f3943-139">En el ejemplo siguiente se muestra una solicitud para obtener los eventos de auditoría para las operaciones de asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="f3943-139">The following example shows a request to get the audit events for the role assignment operations.</span></span> <span data-ttu-id="f3943-140">En este caso, ``requestType`` valor es ``Assign``.</span><span class="sxs-lookup"><span data-stu-id="f3943-140">In this case, ``requestType`` value is ``Assign``.</span></span>

<!-- { "blockType": "request" } -->
```http
GET https://graph.microsoft.com/beta/privilegedOperationEvents?$filter=requestType%20eq%20'Assign'
```
##### <a name="response"></a><span data-ttu-id="f3943-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3943-141">Response</span></span>
<span data-ttu-id="f3943-142">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3943-142">The following example shows the response.</span></span> <span data-ttu-id="f3943-143">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f3943-143">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f3943-144">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3943-144">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedOperationEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 547

{
    "value": [
        {
            "id": "201707240003469369",
            "userId": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f80",
            "userName": "admin1",
            "userMail": "admin1@contoso.onmicrosoft.com",
            "roleId": "9360feb5-f418-4baa-8175-e2a00bac4301",
            "roleName": "Directory Writers",
            "expirationDateTime": "0001-01-01T00:00:00Z",
            "creationDateTime": "2017-07-24T18:32:38.7589078Z",
            "requestorId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "requestorName": "admin",
            "tenantId": "ef73ae8b-cc96-4325-9bd1-dc82594b0b40",
            "requestType": "Assign",
            "additionalInformation": null,
            "referenceKey": null,
            "referenceSystem": null
        },
        {
            "id": "201707240003469372",
            "userId": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f80",
            "userName": "admin",
            "userMail": "admin1@contoso.onmicrosoft.com",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "roleName": "Guest Inviter",
            "expirationDateTime": "0001-01-01T00:00:00Z",
            "creationDateTime": "2017-07-24T18:33:00.7607701Z",
            "requestorId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "requestorName": "admin",
            "tenantId": "ef73ae8b-cc96-4325-9bd1-dc82594b0b40",
            "requestType": "Assign",
            "additionalInformation": null,
            "referenceKey": null,
            "referenceSystem": null
        }
    ]
}
```
### <a name="get-audit-events-for-the-operations-of-self-role-activation-and-makepermanent"></a><span data-ttu-id="f3943-145">Obtener eventos de auditoría para las operaciones de la activación de la función y makePermanent</span><span class="sxs-lookup"><span data-stu-id="f3943-145">Get audit events for the operations of self role activation and makePermanent</span></span>
##### <a name="request"></a><span data-ttu-id="f3943-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3943-146">Request</span></span>
<span data-ttu-id="f3943-147">En el ejemplo siguiente se muestra una solicitud para obtener los eventos de auditoría para las operaciones de la activación de la función y makePermanent.</span><span class="sxs-lookup"><span data-stu-id="f3943-147">The following example shows a request to get the audit events for the operations of self role activation and makePermanent.</span></span> <span data-ttu-id="f3943-148">En este caso, ``requestType`` valor es ``Activate``.</span><span class="sxs-lookup"><span data-stu-id="f3943-148">In this case, ``requestType`` value is ``Activate``.</span></span>

<!-- { "blockType": "request" } -->
```http
GET https://graph.microsoft.com/beta/privilegedOperationEvents?$filter=requestType%20eq%20'Activate'
```
##### <a name="response"></a><span data-ttu-id="f3943-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3943-149">Response</span></span>
<span data-ttu-id="f3943-150">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3943-150">The following example shows the response.</span></span> <span data-ttu-id="f3943-151">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f3943-151">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f3943-152">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3943-152">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedOperationEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 547

{
    "value": [
        {
            "id": "201707240003469811",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "userName": "admin1",
            "userMail": "admin1@contoso.onmicrosoft.com",
            "roleId": "44367163-eba1-44c3-98af-f5787879f96a",
            "roleName": "CRM Service Administrator",
            "expirationDateTime": "0001-01-01T00:00:00Z",
            "creationDateTime": "2017-07-24T23:34:41.9661094Z",
            "requestorId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "requestorName": "admin1",
            "tenantId": "ef73ae8b-cc96-4325-9bd1-dc82594b0b40",
            "requestType": "Activate",
            "additionalInformation": "Make permanent admin",
            "referenceKey": null,
            "referenceSystem": null
        },
        {
            "id": "201707240003469814",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "userName": "admin1",
            "userMail": "admin1@contoso.onmicrosoft.com",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "roleName": "Guest Inviter",
            "expirationDateTime": "2017-07-25T00:37:07.3402169Z",
            "creationDateTime": "2017-07-24T23:37:08.0052112Z",
            "requestorId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "requestorName": "admin1",
            "tenantId": "ef73ae8b-cc96-4325-9bd1-dc82594b0b40",
            "requestType": "Activate",
            "additionalInformation": "self activate",
            "referenceKey": "",
            "referenceSystem": ""
        }
    ]
}
```

### <a name="get-audit-events-for-role-assignment-deactivation"></a><span data-ttu-id="f3943-153">Obtener eventos de auditoría para la desactivación de la asignación de rol</span><span class="sxs-lookup"><span data-stu-id="f3943-153">Get audit events for role assignment deactivation</span></span>
##### <a name="request"></a><span data-ttu-id="f3943-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3943-154">Request</span></span>
<span data-ttu-id="f3943-155">En el ejemplo siguiente se muestra una solicitud para obtener los eventos de auditoría de desactivación de la asignación de rol.</span><span class="sxs-lookup"><span data-stu-id="f3943-155">The following example shows a request to get the audit events for role assignment deactivation.</span></span> <span data-ttu-id="f3943-156">En este caso, ``requestType`` valor es ``Deactivate``.</span><span class="sxs-lookup"><span data-stu-id="f3943-156">In this case, ``requestType`` value is ``Deactivate``.</span></span>

<!-- { "blockType": "request" } -->
```http
GET https://graph.microsoft.com/beta/privilegedOperationEvents?$filter=requestType%20eq%20'Deactivate'
```
##### <a name="response"></a><span data-ttu-id="f3943-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3943-157">Response</span></span>
<span data-ttu-id="f3943-158">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3943-158">The following example shows the response.</span></span> <span data-ttu-id="f3943-159">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f3943-159">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f3943-160">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3943-160">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedOperationEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 547

{
    "value": [
        {
            "id": "201707240003469375",
            "userId": "2cf9eef8-bc67-4aa4-bb65-75cc9e5c3f80",
            "userName": "admin1",
            "userMail": "admin1@contoso.onmicrosoft.com",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "roleName": "Guest Inviter",
            "expirationDateTime": "0001-01-01T00:00:00Z",
            "creationDateTime": "2017-07-24T18:33:28.3408971Z",
            "requestorId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "requestorName": "admin1",
            "tenantId": "ef73ae8b-cc96-4325-9bd1-dc82594b0b40",
            "requestType": "Deactivate",
            "additionalInformation": "Make eligible admin",
            "referenceKey": null,
            "referenceSystem": null
        }
    ]
}
```
### <a name="get-audit-events-created-in-a-time-range"></a><span data-ttu-id="f3943-161">Obtener eventos de auditoría creados en un intervalo de tiempo</span><span class="sxs-lookup"><span data-stu-id="f3943-161">Get audit events created in a time range</span></span>
##### <a name="request"></a><span data-ttu-id="f3943-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3943-162">Request</span></span> 
<span data-ttu-id="f3943-163">En el ejemplo siguiente se muestra una solicitud para obtener los eventos de auditoría creados en un intervalo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f3943-163">The following example shows a request to get the audit events created in a time range.</span></span>

<!-- { "blockType": "request" } -->
```http
GET https://graph.microsoft.com/beta/privilegedOperationEvents?$filter=(creationDateTime%20ge%202017-06-25T07:00:00Z)%20and%20(creationDateTime%20le%202017-07-25T17:30:17Z)&$count=true&$orderby=creationDateTime%20desc
```
##### <a name="response"></a><span data-ttu-id="f3943-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3943-164">Response</span></span>
<span data-ttu-id="f3943-165">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3943-165">The following example shows the response.</span></span> <span data-ttu-id="f3943-166">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f3943-166">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f3943-167">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3943-167">All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedOperationEvent",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 547

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#privilegedOperationEvents",
    "@odata.count": 2,
    "value": [
        {
            "id": "201707250003471056",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "userName": "admin",
            "userMail": "admin@contoso.onmicrosoft.com",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "roleName": "Guest Inviter",
            "expirationDateTime": "2017-07-25T17:38:49.5640383Z",
            "creationDateTime": "2017-07-25T16:38:50.3681771Z",
            "requestorId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "requestorName": "admin",
            "tenantId": "ef73ae8b-cc96-4325-9bd1-dc82594b0b40",
            "requestType": "Activate",
            "additionalInformation": "activate test",
            "referenceKey": "",
            "referenceSystem": ""
        },
        {
            "id": "201707250003469896",
            "userId": "0f693614-c255-4cf5-92fa-74e770c656d8",
            "userName": "admin",
            "userMail": "admin@contoso.onmicrosoft.com",
            "roleId": "95e79109-95c0-4d8e-aee3-d01accf2d47b",
            "roleName": "Guest Inviter",
            "expirationDateTime": "0001-01-01T00:00:00Z",
            "creationDateTime": "2017-07-25T00:37:08.6172407Z",
            "requestorId": "6b61baec-bb80-4a8a-b8bd-fa5ba1f12386",
            "requestorName": "Azure AD PIM",
            "tenantId": "ef73ae8b-cc96-4325-9bd1-dc82594b0b40",
            "requestType": "Deactivate",
            "additionalInformation": "Expired",
            "referenceKey": "",
            "referenceSystem": ""
        }
    ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List privilegedOperationEvents",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->