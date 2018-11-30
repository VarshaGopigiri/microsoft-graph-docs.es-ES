---
title: Obtener privilegedRoleAssignment
description: Recuperar las propiedades y relaciones del objeto privilegedRoleAssignment.
ms.openlocfilehash: ad8815842698be0ef6a3eef37dc3e26f7dc11dbd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085371"
---
# <a name="get-privilegedroleassignment"></a><span data-ttu-id="6031a-103">Obtener privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6031a-103">Get privilegedRoleAssignment</span></span>

> <span data-ttu-id="6031a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6031a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6031a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6031a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6031a-106">Recuperar las propiedades y relaciones del objeto privilegedRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="6031a-106">Retrieve the properties and relationships of privilegedRoleAssignment object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6031a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6031a-107">Permissions</span></span>
<span data-ttu-id="6031a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6031a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="6031a-110">El solicitante debe tener uno de los siguientes roles: _Administrador de roles con privilegios_, _Administrador Global_, _Administrador de seguridad_o _Lector de seguridad_.</span><span class="sxs-lookup"><span data-stu-id="6031a-110">The requestor needs to have one of the following roles: _Privileged Role Administrator_, _Global Administrator_, _Security Administrator_, or _Security Reader_.</span></span> 

|<span data-ttu-id="6031a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6031a-111">Permission type</span></span>      | <span data-ttu-id="6031a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6031a-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6031a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6031a-113">Delegated (work or school account)</span></span> | <span data-ttu-id="6031a-114">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6031a-114">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="6031a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6031a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6031a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6031a-116">Not supported.</span></span>    |
|<span data-ttu-id="6031a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6031a-117">Application</span></span> | <span data-ttu-id="6031a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6031a-118">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6031a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6031a-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoleAssignments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6031a-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6031a-120">Optional query parameters</span></span>
<span data-ttu-id="6031a-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6031a-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6031a-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6031a-122">Request headers</span></span>
| <span data-ttu-id="6031a-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="6031a-123">Name</span></span>      |<span data-ttu-id="6031a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6031a-124">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="6031a-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="6031a-125">Authorization</span></span>  | <span data-ttu-id="6031a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6031a-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6031a-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6031a-128">Request body</span></span>
<span data-ttu-id="6031a-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6031a-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6031a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6031a-130">Response</span></span>

<span data-ttu-id="6031a-131">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [privilegedRoleAssignment](../resources/privilegedroleassignment.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6031a-131">If successful, this method returns a `200 OK` response code and [privilegedRoleAssignment](../resources/privilegedroleassignment.md) object in the response body.</span></span>

<span data-ttu-id="6031a-132">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="6031a-132">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="6031a-133">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="6031a-133">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="6031a-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6031a-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6031a-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6031a-135">Request</span></span>
<span data-ttu-id="6031a-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6031a-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedroleassignment"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoleAssignments/{id}
```
##### <a name="response"></a><span data-ttu-id="6031a-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6031a-137">Response</span></span>
<span data-ttu-id="6031a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6031a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 184

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "isElevated": true,
  "expirationDateTime": "2016-10-19T10:37:00Z",
  "resultMessage": "resultMessage-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get privilegedRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->