---
title: Lista privilegedRoles
description: Recuperar una lista de objetos de privilegedRole.
localization_priority: Normal
ms.openlocfilehash: c36ea34cc6d7ee1999e37f15eff543f48bbfc2bd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826050"
---
# <a name="list-privilegedroles"></a><span data-ttu-id="a463b-103">Lista privilegedRoles</span><span class="sxs-lookup"><span data-stu-id="a463b-103">List privilegedRoles</span></span>

> <span data-ttu-id="a463b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a463b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a463b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a463b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a463b-106">Recuperar una lista de objetos de [privilegedRole](../resources/privilegedrole.md) .</span><span class="sxs-lookup"><span data-stu-id="a463b-106">Retrieve a list of [privilegedRole](../resources/privilegedrole.md) objects.</span></span>

<span data-ttu-id="a463b-107">Para filtrar los resultados de la consulta, use el estándar OData ``$filter`` expresiones en los URI.</span><span class="sxs-lookup"><span data-stu-id="a463b-107">To filter the results from the query, use the standard OData ``$filter`` expressions in the URIs.</span></span>
## <a name="permissions"></a><span data-ttu-id="a463b-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a463b-108">Permissions</span></span>
<span data-ttu-id="a463b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a463b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

<span data-ttu-id="a463b-111">El solicitante debe tener uno de los siguientes roles: _Administrador de roles con privilegios_, _Administrador Global_, _Administrador de seguridad_o _Lector de seguridad_.</span><span class="sxs-lookup"><span data-stu-id="a463b-111">The requestor needs to have one of the following roles: _Privileged Role Administrator_, _Global Administrator_, _Security Administrator_, or _Security Reader_.</span></span>
 

|<span data-ttu-id="a463b-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a463b-112">Permission type</span></span>      | <span data-ttu-id="a463b-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a463b-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a463b-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a463b-114">Delegated (work or school account)</span></span> | <span data-ttu-id="a463b-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a463b-115">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a463b-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a463b-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a463b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a463b-117">Not supported.</span></span>    |
|<span data-ttu-id="a463b-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a463b-118">Application</span></span> | <span data-ttu-id="a463b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a463b-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a463b-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a463b-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /privilegedRoles
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a463b-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a463b-121">Optional query parameters</span></span>
<span data-ttu-id="a463b-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a463b-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a463b-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a463b-123">Request headers</span></span>
| <span data-ttu-id="a463b-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="a463b-124">Name</span></span>      |<span data-ttu-id="a463b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a463b-125">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a463b-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="a463b-126">Authorization</span></span>  | <span data-ttu-id="a463b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a463b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a463b-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a463b-129">Request body</span></span>
<span data-ttu-id="a463b-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a463b-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a463b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a463b-131">Response</span></span>

<span data-ttu-id="a463b-132">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [privilegedRole](../resources/privilegedrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a463b-132">If successful, this method returns a `200 OK` response code and collection of [privilegedRole](../resources/privilegedrole.md) objects in the response body.</span></span>

<span data-ttu-id="a463b-133">Tenga en cuenta que el inquilino debe estar registrado en PIM.</span><span class="sxs-lookup"><span data-stu-id="a463b-133">Note that the tenant needs to be registered to PIM.</span></span> <span data-ttu-id="a463b-134">De lo contrario, se devolverá el código de estado HTTP 403 Prohibido.</span><span class="sxs-lookup"><span data-stu-id="a463b-134">Otherwise, the HTTP 403 Forbidden status code will be returned.</span></span>
## <a name="example"></a><span data-ttu-id="a463b-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a463b-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a463b-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a463b-136">Request</span></span>
<span data-ttu-id="a463b-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a463b-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_privilegedroles"
}-->
```http
GET https://graph.microsoft.com/beta/privilegedRoles
```
##### <a name="response"></a><span data-ttu-id="a463b-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a463b-138">Response</span></span>
<span data-ttu-id="a463b-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a463b-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRole",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 83

{
  "value": [
    {
      "id": "id-value",
      "name": "name-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List privilegedRoles",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
