---
title: Enumerar elementos eliminados
description: Recuperar una lista de elementos eliminados recientemente de elementos eliminados.
author: lleonard-msft
ms.openlocfilehash: 205052402f4402b9895cca6cc46b6ab656a51ed8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358726"
---
# <a name="list-deleted-items"></a><span data-ttu-id="befc4-103">Enumerar elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="befc4-103">List deleted items</span></span>

> <span data-ttu-id="befc4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="befc4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="befc4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="befc4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="befc4-106">Recuperar una lista de elementos eliminados recientemente de [elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="befc4-106">Retrieve a list of recently deleted items from [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="befc4-107">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="befc4-107">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span>

## <a name="permissions"></a><span data-ttu-id="befc4-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="befc4-108">Permissions</span></span>
<span data-ttu-id="befc4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="befc4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="befc4-111">Para los usuarios: User.Read.All, Directory.Read.All, User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="befc4-111">For users: User.Read.All, Directory.Read.All, User.ReadWrite.All, Directory.AccessAsUser.All</span></span>
* <span data-ttu-id="befc4-112">Para los grupos: Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="befc4-112">For groups: Group.Read.All, Directory.Read.All, Group.ReadWrite.All, Directory.AccessAsUser.All</span></span>

## <a name="http-request"></a><span data-ttu-id="befc4-113">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="befc4-113">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http 
GET /directory/deleteditems/microsoft.graph.group
GET /directory/deletedItems/microsoft.graph.user
```

<span data-ttu-id="befc4-114">Actualmente, esta API admite la recuperación de tipos de objeto de grupos (microsoft.graph.group) o de usuarios (microsoft.graph.user) de los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="befc4-114">This API currently supports retrieving object types of groups (microsoft.graph.group) or users (microsoft.graph.user) from deleted items.</span></span> <span data-ttu-id="befc4-115">El tipo se especifica como parte necesaria del URI.</span><span class="sxs-lookup"><span data-stu-id="befc4-115">The type is specified as a required part of the URI.</span></span> <span data-ttu-id="befc4-116">No se admite realizar llamadas GET /directory/deleteditems sin un tipo.</span><span class="sxs-lookup"><span data-stu-id="befc4-116">Calling GET /directory/deleteditems without a type is not supported.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="befc4-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="befc4-117">Optional query parameters</span></span>
<span data-ttu-id="befc4-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="befc4-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="befc4-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="befc4-119">Request headers</span></span>
| <span data-ttu-id="befc4-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="befc4-120">Name</span></span>      |<span data-ttu-id="befc4-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="befc4-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="befc4-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="befc4-122">Authorization</span></span>  | <span data-ttu-id="befc4-123">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="befc4-123">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="befc4-124">Accept</span><span class="sxs-lookup"><span data-stu-id="befc4-124">Accept</span></span>  | <span data-ttu-id="befc4-125">application/json</span><span class="sxs-lookup"><span data-stu-id="befc4-125">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="befc4-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="befc4-126">Request body</span></span>
<span data-ttu-id="befc4-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="befc4-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="befc4-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="befc4-128">Response</span></span>

<span data-ttu-id="befc4-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="befc4-129">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="befc4-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="befc4-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="befc4-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="befc4-131">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_deleteditems"
}-->
```http
GET https://graph.microsoft.com/beta/directory/deleteditems/microsoft.graph.group
```
##### <a name="response"></a><span data-ttu-id="befc4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="befc4-132">Response</span></span>
<span data-ttu-id="befc4-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="befc4-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#groups",
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