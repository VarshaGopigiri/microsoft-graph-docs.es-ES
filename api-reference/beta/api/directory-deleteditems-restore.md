---
title: Restaurar elemento eliminado
description: 'Restaura un elemento eliminado recientemente de la carpeta Elementos eliminados. '
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: 6206b850df7e808df05e191b6e0485f617a7e1ab
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27843879"
---
# <a name="restore-deleted-item"></a><span data-ttu-id="1618c-103">Restaurar elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="1618c-103">Restore deleted item</span></span>

> <span data-ttu-id="1618c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1618c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1618c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1618c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1618c-106">Restaura un elemento eliminado recientemente de la carpeta [Elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="1618c-106">Restores a recently deleted item from [deleted items](../resources/directory.md).</span></span> 

<span data-ttu-id="1618c-107">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="1618c-107">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span> <span data-ttu-id="1618c-108">Si un elemento se ha eliminado accidentalmente, puede restaurarlo por completo.</span><span class="sxs-lookup"><span data-stu-id="1618c-108">If an item was accidentally deleted, you can fully restore the item.</span></span>

<span data-ttu-id="1618c-109">Un elemento eliminado recientemente seguirá estando disponible durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="1618c-109">A recently deleted item will remain available for up to 30 days.</span></span> <span data-ttu-id="1618c-110">Después de 30 días, el elemento se elimina permanentemente.</span><span class="sxs-lookup"><span data-stu-id="1618c-110">After 30 days, the item is permanently deleted.</span></span>

## <a name="permissions"></a><span data-ttu-id="1618c-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="1618c-111">Permissions</span></span>
<span data-ttu-id="1618c-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1618c-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

* <span data-ttu-id="1618c-114">Para los usuarios: User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="1618c-114">For users: User.ReadWrite.All, Directory.AccessAsUser.All</span></span>
* <span data-ttu-id="1618c-115">Para los grupos: Group.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="1618c-115">For groups: Group.ReadWrite.All, Directory.AccessAsUser.All</span></span>

## <a name="http-request"></a><span data-ttu-id="1618c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1618c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directory/deleteditems/{id}/restore
```

## <a name="request-headers"></a><span data-ttu-id="1618c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1618c-117">Request headers</span></span>
| <span data-ttu-id="1618c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1618c-118">Name</span></span>       | <span data-ttu-id="1618c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="1618c-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1618c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="1618c-120">Authorization</span></span>  | <span data-ttu-id="1618c-121">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="1618c-121">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="1618c-122">Accept</span><span class="sxs-lookup"><span data-stu-id="1618c-122">Accept</span></span> | <span data-ttu-id="1618c-123">application/json</span><span class="sxs-lookup"><span data-stu-id="1618c-123">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="1618c-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1618c-124">Request body</span></span>
<span data-ttu-id="1618c-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1618c-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1618c-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1618c-126">Response</span></span>

<span data-ttu-id="1618c-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1618c-127">If successful, this method returns `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1618c-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1618c-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1618c-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1618c-129">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directory"
}-->
```http
POST https://graph.microsoft.com/beta/directory/deleteditems/46cc6179-19d0-473e-97ad-6ff84347bbbb/restore
```
<span data-ttu-id="1618c-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="1618c-130">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="1618c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1618c-131">Response</span></span>
<span data-ttu-id="1618c-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1618c-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#directoryObjects/$entity",
  "@odata.type":"#microsoft.graph.group",
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
  "description": "Create deletedItem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
