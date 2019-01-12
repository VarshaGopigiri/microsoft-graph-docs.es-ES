---
title: Enumerar miembros
description: Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 19a820605c1a912a0f9d6c052bc36de6114c473e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937267"
---
# <a name="list-members"></a><span data-ttu-id="4e488-104">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="4e488-104">List members</span></span>

<span data-ttu-id="4e488-p102">Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="4e488-p102">Retrieve a list of the users that are assigned to the directory role.  Only users can be assigned to a directory role.</span></span>
## <a name="permissions"></a><span data-ttu-id="4e488-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4e488-107">Permissions</span></span>
<span data-ttu-id="4e488-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4e488-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4e488-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4e488-110">Permission type</span></span>      | <span data-ttu-id="4e488-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4e488-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4e488-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4e488-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4e488-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4e488-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4e488-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4e488-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4e488-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4e488-115">Not supported.</span></span>    |
|<span data-ttu-id="4e488-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4e488-116">Application</span></span> | <span data-ttu-id="4e488-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4e488-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4e488-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4e488-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4e488-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4e488-119">Optional query parameters</span></span>
<span data-ttu-id="4e488-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e488-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4e488-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4e488-121">Request headers</span></span>
| <span data-ttu-id="4e488-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="4e488-122">Name</span></span>       | <span data-ttu-id="4e488-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e488-123">Type</span></span> | <span data-ttu-id="4e488-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e488-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4e488-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="4e488-125">Authorization</span></span>  | <span data-ttu-id="4e488-126">string</span><span class="sxs-lookup"><span data-stu-id="4e488-126">string</span></span>  | <span data-ttu-id="4e488-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4e488-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4e488-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4e488-129">Request body</span></span>
<span data-ttu-id="4e488-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4e488-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4e488-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e488-131">Response</span></span>

<span data-ttu-id="4e488-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4e488-132">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4e488-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4e488-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4e488-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4e488-134">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoles/{id}/members
```
##### <a name="response"></a><span data-ttu-id="4e488-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4e488-135">Response</span></span>
<span data-ttu-id="4e488-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4e488-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
