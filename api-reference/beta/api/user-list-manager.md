---
title: List manager
description: Obtiene el administrador del usuario. Devuelve el usuario o el contacto asignado como administrador del usuario.
ms.openlocfilehash: 3601b7c13eb97b288cc65e927432bd420105970a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085796"
---
# <a name="list-manager"></a><span data-ttu-id="2befd-104">List manager</span><span class="sxs-lookup"><span data-stu-id="2befd-104">List manager</span></span>

> <span data-ttu-id="2befd-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2befd-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2befd-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2befd-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2befd-p103">Obtiene el administrador del usuario. Devuelve el usuario o el contacto asignado como administrador del usuario.</span><span class="sxs-lookup"><span data-stu-id="2befd-p103">Get user's manager. Returns the user or contact assigned as the user's manager.</span></span>
## <a name="permissions"></a><span data-ttu-id="2befd-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="2befd-109">Permissions</span></span>
<span data-ttu-id="2befd-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2befd-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2befd-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2befd-112">Permission type</span></span>      | <span data-ttu-id="2befd-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2befd-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2befd-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2befd-114">Delegated (work or school account)</span></span> | <span data-ttu-id="2befd-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="2befd-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="2befd-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2befd-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2befd-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2befd-117">Not supported.</span></span>    |
|<span data-ttu-id="2befd-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2befd-118">Application</span></span> | <span data-ttu-id="2befd-119">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2befd-119">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2befd-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2befd-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/manager
```
## <a name="optional-query-parameters"></a><span data-ttu-id="2befd-121">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2befd-121">Optional query parameters</span></span>
<span data-ttu-id="2befd-122">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2befd-122">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="2befd-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2befd-123">Request headers</span></span>
| <span data-ttu-id="2befd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2befd-124">Header</span></span>       | <span data-ttu-id="2befd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2befd-125">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="2befd-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="2befd-126">Authorization</span></span>  | <span data-ttu-id="2befd-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2befd-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2befd-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2befd-129">Content-Type</span></span>   | <span data-ttu-id="2befd-130">application/json</span><span class="sxs-lookup"><span data-stu-id="2befd-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2befd-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2befd-131">Request body</span></span>
<span data-ttu-id="2befd-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2befd-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2befd-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2befd-133">Response</span></span>

<span data-ttu-id="2befd-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2befd-134">If successful, this method returns a `200 OK` response code and a [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2befd-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2befd-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2befd-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2befd-136">Request</span></span>
<span data-ttu-id="2befd-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2befd-137">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/beta/users/{id|userPrincipalName}/manager
```
##### <a name="response"></a><span data-ttu-id="2befd-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2befd-138">Response</span></span>
<span data-ttu-id="2befd-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2befd-139">Here is an example of the response.</span></span>
<!-- { "blockType": "ignored" } -->
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