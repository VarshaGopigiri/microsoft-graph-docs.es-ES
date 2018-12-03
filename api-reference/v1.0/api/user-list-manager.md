---
title: List manager
description: Obtiene el administrador del usuario. Devuelve el usuario o el contacto asignado como administrador del usuario.
ms.openlocfilehash: eb25449970311ceb7790b54c64191c669daeb004
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028614"
---
# <a name="list-manager"></a><span data-ttu-id="ce145-104">List manager</span><span class="sxs-lookup"><span data-stu-id="ce145-104">List manager</span></span>

<span data-ttu-id="ce145-p102">Obtiene el administrador del usuario. Devuelve el usuario o el contacto asignado como administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="ce145-p102">Get user's manager. Returns the user or contact assigned as the user's manager.</span></span>
## <a name="permissions"></a><span data-ttu-id="ce145-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ce145-107">Permissions</span></span>
<span data-ttu-id="ce145-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ce145-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce145-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce145-110">Permission type</span></span>      | <span data-ttu-id="ce145-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce145-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ce145-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce145-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ce145-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ce145-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ce145-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce145-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ce145-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce145-115">Not supported.</span></span>    |
|<span data-ttu-id="ce145-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce145-116">Application</span></span> | <span data-ttu-id="ce145-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce145-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ce145-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce145-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/manager
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ce145-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ce145-119">Optional query parameters</span></span>
<span data-ttu-id="ce145-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce145-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ce145-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce145-121">Request headers</span></span>
| <span data-ttu-id="ce145-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce145-122">Header</span></span>       | <span data-ttu-id="ce145-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ce145-123">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="ce145-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce145-124">Authorization</span></span>  | <span data-ttu-id="ce145-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ce145-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ce145-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ce145-127">Content-Type</span></span>   | <span data-ttu-id="ce145-128">application/json</span><span class="sxs-lookup"><span data-stu-id="ce145-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ce145-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce145-129">Request body</span></span>
<span data-ttu-id="ce145-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ce145-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ce145-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce145-131">Response</span></span>

<span data-ttu-id="ce145-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce145-132">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ce145-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce145-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ce145-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce145-134">Request</span></span>
<span data-ttu-id="ce145-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce145-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_manager"
}-->
```http
GET https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/manager
```
##### <a name="response"></a><span data-ttu-id="ce145-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce145-136">Response</span></span>
<span data-ttu-id="ce145-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce145-137">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "objectType": "User",
  "id": "111048d2-2761-4347-b978-07354283363b",
  "accountEnabled": true,
  "city": "San Diego",
  "country": "United States",
  "department": "Sales & Marketing",
  "displayName": "Sara Davis",
  "givenName": "Sara",
  "jobTitle": "Finance VP",
  "mail": "SaraD@contoso.onmicrosoft.com",
  "mailNickname": "SaraD",
  "state": "CA",
  "streetAddress": "9256 Towne Center Dr., Suite 400",
  "surname": "Davis",
  "usageLocation": "US",
  "userPrincipalName": "SaraD@contoso.onmicrosoft.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List directReports",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->