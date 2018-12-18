---
title: Enumerar miembros
description: Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.
author: lleonard-msft
ms.openlocfilehash: 4fdbb5fd940e9fa20adb9f2a3d3dd1c7c035dbf7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359888"
---
# <a name="list-members"></a><span data-ttu-id="bb5a2-104">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="bb5a2-104">List members</span></span>

<span data-ttu-id="bb5a2-p102">Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="bb5a2-p102">Retrieve a list of the users that are assigned to the directory role.  Only users can be assigned to a directory role.</span></span>
## <a name="permissions"></a><span data-ttu-id="bb5a2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bb5a2-107">Permissions</span></span>
<span data-ttu-id="bb5a2-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb5a2-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="bb5a2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb5a2-110">Permission type</span></span>      | <span data-ttu-id="bb5a2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb5a2-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bb5a2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb5a2-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bb5a2-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bb5a2-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="bb5a2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb5a2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bb5a2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb5a2-115">Not supported.</span></span>    |
|<span data-ttu-id="bb5a2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb5a2-116">Application</span></span> | <span data-ttu-id="bb5a2-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bb5a2-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bb5a2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb5a2-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bb5a2-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bb5a2-119">Optional query parameters</span></span>
<span data-ttu-id="bb5a2-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb5a2-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bb5a2-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb5a2-121">Request headers</span></span>
| <span data-ttu-id="bb5a2-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="bb5a2-122">Name</span></span>       | <span data-ttu-id="bb5a2-123">Type</span><span class="sxs-lookup"><span data-stu-id="bb5a2-123">Type</span></span> | <span data-ttu-id="bb5a2-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb5a2-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bb5a2-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="bb5a2-125">Authorization</span></span>  | <span data-ttu-id="bb5a2-126">string</span><span class="sxs-lookup"><span data-stu-id="bb5a2-126">string</span></span>  | <span data-ttu-id="bb5a2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bb5a2-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bb5a2-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb5a2-129">Request body</span></span>
<span data-ttu-id="bb5a2-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bb5a2-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bb5a2-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb5a2-131">Response</span></span>

<span data-ttu-id="bb5a2-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb5a2-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bb5a2-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb5a2-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bb5a2-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb5a2-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoles/{id}/members
```
##### <a name="response"></a><span data-ttu-id="bb5a2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb5a2-135">Response</span></span>
<span data-ttu-id="bb5a2-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb5a2-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "businessPhones":["000-000-0000"],
      "displayName":"First Last",
      "givenName":"First",
      "jobTitle":null,
      "mail":"first@example.com",
      "officeLocation":null,
      "preferredLanguage":"en-US",
      "surname":"Last",
      "userPrincipalName":"first@example.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->