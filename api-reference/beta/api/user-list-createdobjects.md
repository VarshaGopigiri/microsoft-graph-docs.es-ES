---
title: List createdObjects
description: Obtiene una lista de objetos de directorio creados por el usuario.
author: dkershaw10
ms.openlocfilehash: a7067926e5104c08d65a1753fc716787bed52fd5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27342108"
---
# <a name="list-createdobjects"></a><span data-ttu-id="3aff6-103">List createdObjects</span><span class="sxs-lookup"><span data-stu-id="3aff6-103">List createdObjects</span></span>

> <span data-ttu-id="3aff6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3aff6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3aff6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3aff6-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3aff6-106">Obtiene una lista de objetos de directorio creados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3aff6-106">Get a list of directory objects that were created by the user.</span></span>
## <a name="permissions"></a><span data-ttu-id="3aff6-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3aff6-107">Permissions</span></span>
<span data-ttu-id="3aff6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3aff6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3aff6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3aff6-110">Permission type</span></span>      | <span data-ttu-id="3aff6-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3aff6-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3aff6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3aff6-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3aff6-113">User.Read, User.ReadWrite, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3aff6-113">User.Read, User.ReadWrite, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="3aff6-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3aff6-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3aff6-115">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3aff6-115">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="3aff6-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3aff6-116">Application</span></span> | <span data-ttu-id="3aff6-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3aff6-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3aff6-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3aff6-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/createdObjects
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3aff6-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3aff6-119">Optional query parameters</span></span>
<span data-ttu-id="3aff6-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3aff6-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3aff6-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3aff6-121">Request headers</span></span>
| <span data-ttu-id="3aff6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3aff6-122">Header</span></span>       | <span data-ttu-id="3aff6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3aff6-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3aff6-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="3aff6-124">Authorization</span></span>  | <span data-ttu-id="3aff6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3aff6-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3aff6-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3aff6-127">Content-Type</span></span>  | <span data-ttu-id="3aff6-128">application/json</span><span class="sxs-lookup"><span data-stu-id="3aff6-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3aff6-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3aff6-129">Request body</span></span>
<span data-ttu-id="3aff6-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3aff6-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3aff6-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3aff6-131">Response</span></span>

<span data-ttu-id="3aff6-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3aff6-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3aff6-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3aff6-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3aff6-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3aff6-134">Request</span></span>
<span data-ttu-id="3aff6-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3aff6-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_createdobjects"
}-->
```http
GET https://graph.microsoft.com/beta/me/createdObjects
```
##### <a name="response"></a><span data-ttu-id="3aff6-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3aff6-136">Response</span></span>
<span data-ttu-id="3aff6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3aff6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List createdObjects",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->