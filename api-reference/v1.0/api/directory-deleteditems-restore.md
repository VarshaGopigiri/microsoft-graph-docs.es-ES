---
title: Restaurar elemento eliminado
description: 'Restaura un elemento eliminado recientemente de la carpeta Elementos eliminados. '
ms.openlocfilehash: 3fa47d269cefaf54994b57f8f06a92a8ac8fc4b7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030982"
---
# <a name="restore-deleted-item"></a><span data-ttu-id="6d97c-103">Restaurar elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="6d97c-103">Restore deleted item</span></span>

<span data-ttu-id="6d97c-104">Restaura un elemento eliminado recientemente de la carpeta [Elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="6d97c-104">Restores a recently deleted item from [deleted items](../resources/directory.md).</span></span> 

<span data-ttu-id="6d97c-105">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="6d97c-105">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span> <span data-ttu-id="6d97c-106">Si un elemento se ha eliminado accidentalmente, puede restaurarlo por completo.</span><span class="sxs-lookup"><span data-stu-id="6d97c-106">If an item was accidentally deleted, you can fully restore the item.</span></span>

<span data-ttu-id="6d97c-107">Un elemento eliminado recientemente seguirá estando disponible durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="6d97c-107">A recently deleted item will remain available for up to 30 days.</span></span> <span data-ttu-id="6d97c-108">Después de 30 días, el elemento se elimina permanentemente.</span><span class="sxs-lookup"><span data-stu-id="6d97c-108">After 30 days, the item is permanently deleted.</span></span>

## <a name="permissions"></a><span data-ttu-id="6d97c-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="6d97c-109">Permissions</span></span>
<span data-ttu-id="6d97c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6d97c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

### <a name="for-users"></a><span data-ttu-id="6d97c-112">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="6d97c-112">For users:</span></span>

|<span data-ttu-id="6d97c-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d97c-113">Permission type</span></span>      | <span data-ttu-id="6d97c-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d97c-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d97c-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d97c-115">Delegated (work or school account)</span></span> | <span data-ttu-id="6d97c-116">User.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6d97c-116">User.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="6d97c-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d97c-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d97c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d97c-118">Not supported.</span></span> |
|<span data-ttu-id="6d97c-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d97c-119">Application</span></span> | <span data-ttu-id="6d97c-120">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d97c-120">User.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="6d97c-121">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="6d97c-121">For groups:</span></span>

|<span data-ttu-id="6d97c-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6d97c-122">Permission type</span></span>      | <span data-ttu-id="6d97c-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6d97c-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6d97c-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6d97c-124">Delegated (work or school account)</span></span> | <span data-ttu-id="6d97c-125">Group.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6d97c-125">Group.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="6d97c-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6d97c-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6d97c-127">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6d97c-127">Not supported.</span></span>    |
|<span data-ttu-id="6d97c-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6d97c-128">Application</span></span> | <span data-ttu-id="6d97c-129">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6d97c-129">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6d97c-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6d97c-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directory/deletedItems/{id}/restore
```

## <a name="request-headers"></a><span data-ttu-id="6d97c-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6d97c-131">Request headers</span></span>
| <span data-ttu-id="6d97c-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="6d97c-132">Name</span></span>       | <span data-ttu-id="6d97c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d97c-133">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6d97c-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="6d97c-134">Authorization</span></span>  | <span data-ttu-id="6d97c-135">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="6d97c-135">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="6d97c-136">Accept</span><span class="sxs-lookup"><span data-stu-id="6d97c-136">Accept</span></span> | <span data-ttu-id="6d97c-137">application/json</span><span class="sxs-lookup"><span data-stu-id="6d97c-137">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="6d97c-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6d97c-138">Request body</span></span>
<span data-ttu-id="6d97c-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6d97c-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6d97c-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d97c-140">Response</span></span>

<span data-ttu-id="6d97c-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6d97c-141">If successful, this method returns `200 OK` response code and [directoryObject](../resources/directoryobject.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6d97c-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6d97c-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6d97c-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6d97c-143">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directory"
}-->
```http
POST https://graph.microsoft.com/v1.0/directory/deletedItems/{object-id}/restore
```
<span data-ttu-id="6d97c-144">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryObject](../resources/directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="6d97c-144">In the request body, supply a JSON representation of [directoryObject](../resources/directoryobject.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="6d97c-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6d97c-145">Response</span></span>
<span data-ttu-id="6d97c-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6d97c-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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