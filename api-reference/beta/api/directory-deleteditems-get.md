---
title: Obtener elemento eliminado
description: Recuperar las propiedades de un elemento eliminado recientemente en elementos eliminados.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 09996c27aec0183ded5b09b490c95fb95d57893a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926431"
---
# <a name="get-deleted-item"></a><span data-ttu-id="2a2c3-103">Obtener elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="2a2c3-103">Get deleted item</span></span>

> <span data-ttu-id="2a2c3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a2c3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a2c3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a2c3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2a2c3-106">Recuperar las propiedades de un elemento eliminado recientemente en [elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="2a2c3-106">Retrieve the properties of a recently deleted item in [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="2a2c3-107">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="2a2c3-107">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span>

## <a name="permissions"></a><span data-ttu-id="2a2c3-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="2a2c3-108">Permissions</span></span>
<span data-ttu-id="2a2c3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2a2c3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="2a2c3-111">Para los usuarios: User.Read.All, User.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="2a2c3-111">For users: User.Read.All, User.ReadWrite.All, Directory.Read.All</span></span>
* <span data-ttu-id="2a2c3-112">Para los grupos: Group.Read.All, Group.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="2a2c3-112">For groups: Group.Read.All, Group.ReadWrite.All, Directory.Read.All</span></span>

## <a name="http-request"></a><span data-ttu-id="2a2c3-113">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a2c3-113">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directory/deleteditems/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2a2c3-114">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2a2c3-114">Optional query parameters</span></span>
<span data-ttu-id="2a2c3-115">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a2c3-115">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2a2c3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a2c3-116">Request headers</span></span>
| <span data-ttu-id="2a2c3-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="2a2c3-117">Name</span></span>      |<span data-ttu-id="2a2c3-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a2c3-118">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="2a2c3-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2a2c3-119">Authorization</span></span>  | <span data-ttu-id="2a2c3-120">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="2a2c3-120">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="2a2c3-121">Accept</span><span class="sxs-lookup"><span data-stu-id="2a2c3-121">Accept</span></span>  | <span data-ttu-id="2a2c3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2a2c3-122">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="2a2c3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a2c3-123">Request body</span></span>
<span data-ttu-id="2a2c3-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2a2c3-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2a2c3-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a2c3-125">Response</span></span>

<span data-ttu-id="2a2c3-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a2c3-126">If successful, this method returns a `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2a2c3-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a2c3-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2a2c3-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a2c3-128">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_directory"
}-->
```http
GET https://graph.microsoft.com/beta/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb
```
##### <a name="response"></a><span data-ttu-id="2a2c3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a2c3-129">Response</span></span>
<span data-ttu-id="2a2c3-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a2c3-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directory"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects/$entity",
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
