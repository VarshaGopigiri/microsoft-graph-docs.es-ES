---
title: Enumerar elementos eliminados
description: Recuperar una lista de elementos eliminados recientemente de elementos eliminados.
author: lleonard-msft
ms.openlocfilehash: 4c972ca554f7a073ddfb5b3472784240c691c973
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314283"
---
# <a name="list-deleted-items"></a><span data-ttu-id="72b97-103">Enumerar elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="72b97-103">List deleted items</span></span>

<span data-ttu-id="72b97-104">Recuperar una lista de elementos eliminados recientemente de [elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="72b97-104">Retrieve a list of recently deleted items from [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="72b97-105">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="72b97-105">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span>

## <a name="permissions"></a><span data-ttu-id="72b97-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="72b97-106">Permissions</span></span>
<span data-ttu-id="72b97-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="72b97-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

### <a name="for-users"></a><span data-ttu-id="72b97-109">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="72b97-109">For users:</span></span>

|<span data-ttu-id="72b97-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72b97-110">Permission type</span></span>      | <span data-ttu-id="72b97-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72b97-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="72b97-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72b97-112">Delegated (work or school account)</span></span> | <span data-ttu-id="72b97-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="72b97-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="72b97-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72b97-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="72b97-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72b97-115">Not supported.</span></span> |
|<span data-ttu-id="72b97-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72b97-116">Application</span></span> | <span data-ttu-id="72b97-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="72b97-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="72b97-118">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="72b97-118">For groups:</span></span>

|<span data-ttu-id="72b97-119">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72b97-119">Permission type</span></span>      | <span data-ttu-id="72b97-120">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72b97-120">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="72b97-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72b97-121">Delegated (work or school account)</span></span> | <span data-ttu-id="72b97-122">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="72b97-122">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="72b97-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72b97-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="72b97-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="72b97-124">Not supported.</span></span>    |
|<span data-ttu-id="72b97-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72b97-125">Application</span></span> | <span data-ttu-id="72b97-126">Group.Read.All, Group.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="72b97-126">Group.Read.All, Group.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="72b97-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72b97-127">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http 
GET /directory/deletedItems/microsoft.graph.group
GET /directory/deletedItems/microsoft.graph.user
```

<span data-ttu-id="72b97-128">Actualmente, esta API admite la recuperación de tipos de objeto de grupos (microsoft.graph.group) o de usuarios (microsoft.graph.user) de los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="72b97-128">This API currently supports retrieving object types of groups (microsoft.graph.group) or users (microsoft.graph.user) from deleted items.</span></span> <span data-ttu-id="72b97-129">El tipo se especifica como parte necesaria del URI.</span><span class="sxs-lookup"><span data-stu-id="72b97-129">The type is specified as a required part of the URI.</span></span> <span data-ttu-id="72b97-130">Llamar a GET/directory/deletedItems sin un tipo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="72b97-130">Calling GET /directory/deletedItems without a type is not supported.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="72b97-131">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="72b97-131">Optional query parameters</span></span>
<span data-ttu-id="72b97-132">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72b97-132">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="72b97-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="72b97-133">Request headers</span></span>
| <span data-ttu-id="72b97-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="72b97-134">Name</span></span>      |<span data-ttu-id="72b97-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="72b97-135">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="72b97-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="72b97-136">Authorization</span></span>  | <span data-ttu-id="72b97-137">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="72b97-137">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="72b97-138">Accept</span><span class="sxs-lookup"><span data-stu-id="72b97-138">Accept</span></span>  | <span data-ttu-id="72b97-139">application/json</span><span class="sxs-lookup"><span data-stu-id="72b97-139">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="72b97-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="72b97-140">Request body</span></span>
<span data-ttu-id="72b97-141">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="72b97-141">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="72b97-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72b97-142">Response</span></span>

<span data-ttu-id="72b97-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72b97-143">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="72b97-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72b97-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="72b97-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72b97-145">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_deleteditems"
}-->
```http
GET https://graph.microsoft.com/v1.0/directory/deletedItems/microsoft.graph.group
```
##### <a name="response"></a><span data-ttu-id="72b97-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72b97-146">Response</span></span>
<span data-ttu-id="72b97-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72b97-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "value": [
    {
      "id":"46cc6179-19d0-473e-97ad-6ff84347bbbb",
      "displayName":"SampleGroup",
      "groupTypes":["Unified"],
      "mail":"example@contoso.com",
      "mailEnabled":true,
      "mailNickname":"Example",
      "securityEnabled":false,
      "visibility":"Public"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List deleteditems",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->