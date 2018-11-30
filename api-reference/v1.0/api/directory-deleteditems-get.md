---
title: Obtener elemento eliminado
description: Recuperar las propiedades de un elemento eliminado recientemente en elementos eliminados.
ms.openlocfilehash: 513b9d8e48cbf4474024b61b7274aa9943daa025
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028771"
---
# <a name="get-deleted-item"></a><span data-ttu-id="926e4-103">Obtener elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="926e4-103">Get deleted item</span></span>

<span data-ttu-id="926e4-104">Recuperar las propiedades de un elemento eliminado recientemente en [elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="926e4-104">Retrieve the properties of a recently deleted item in [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="926e4-105">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="926e4-105">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span>

## <a name="permissions"></a><span data-ttu-id="926e4-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="926e4-106">Permissions</span></span>
<span data-ttu-id="926e4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="926e4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

### <a name="for-users"></a><span data-ttu-id="926e4-109">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="926e4-109">For users:</span></span>

|<span data-ttu-id="926e4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="926e4-110">Permission type</span></span>      | <span data-ttu-id="926e4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="926e4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="926e4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="926e4-112">Delegated (work or school account)</span></span> | <span data-ttu-id="926e4-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="926e4-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory AccessAsUser.All</span></span> |
|<span data-ttu-id="926e4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="926e4-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="926e4-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="926e4-115">Not supported.</span></span> |
|<span data-ttu-id="926e4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="926e4-116">Application</span></span> | <span data-ttu-id="926e4-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="926e4-117">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="926e4-118">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="926e4-118">For groups:</span></span>

|<span data-ttu-id="926e4-119">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="926e4-119">Permission type</span></span>      | <span data-ttu-id="926e4-120">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="926e4-120">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="926e4-121">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="926e4-121">Delegated (work or school account)</span></span> | <span data-ttu-id="926e4-122">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="926e4-122">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="926e4-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="926e4-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="926e4-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="926e4-124">Not supported.</span></span>    |
|<span data-ttu-id="926e4-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="926e4-125">Application</span></span> | <span data-ttu-id="926e4-126">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="926e4-126">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="926e4-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="926e4-127">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directory/deletedItems/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="926e4-128">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="926e4-128">Optional query parameters</span></span>
<span data-ttu-id="926e4-129">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="926e4-129">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="926e4-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="926e4-130">Request headers</span></span>
| <span data-ttu-id="926e4-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="926e4-131">Name</span></span>      |<span data-ttu-id="926e4-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="926e4-132">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="926e4-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="926e4-133">Authorization</span></span>  | <span data-ttu-id="926e4-134">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="926e4-134">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="926e4-135">Accept</span><span class="sxs-lookup"><span data-stu-id="926e4-135">Accept</span></span>  | <span data-ttu-id="926e4-136">application/json</span><span class="sxs-lookup"><span data-stu-id="926e4-136">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="926e4-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="926e4-137">Request body</span></span>
<span data-ttu-id="926e4-138">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="926e4-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="926e4-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="926e4-139">Response</span></span>

<span data-ttu-id="926e4-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="926e4-140">If successful, this method returns a `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="926e4-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="926e4-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="926e4-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="926e4-142">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directory"
}-->
```http
GET https://graph.microsoft.com/v1.0/directory/deletedItems/{object-id}
```
##### <a name="response"></a><span data-ttu-id="926e4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="926e4-143">Response</span></span>
<span data-ttu-id="926e4-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="926e4-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#directoryObjects/$entity",
  "id":"46cc6179-19d0-473e-97ad-6ff84347bbbb",
  "displayName":"SampleGroup",
  "groupTypes":["Unified"],
  "mail":"example@contoso.com",
  "mailEnabled":true,
  "mailNickname":"Example",
  "securityEnabled":false,
  "visibility":"Public"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get directory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->