---
title: Quitar miembro
description: Use esta API para quitar un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede quitar usuarios u otros grupos.
localization_priority: Priority
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 0f93449f5fdebfce3388f20418174b03b91615d6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966744"
---
# <a name="remove-member"></a><span data-ttu-id="88405-104">Quitar miembro</span><span class="sxs-lookup"><span data-stu-id="88405-104">Remove member</span></span>
<span data-ttu-id="88405-p102">Use esta API para quitar un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede quitar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="88405-p102">Use this API to remove a member from an Office 365 group, a security group, or a mail-enabled security group through the **members** navigation property. You can remove users or other groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="88405-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="88405-107">Permissions</span></span>
<span data-ttu-id="88405-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88405-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88405-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88405-110">Permission type</span></span>      | <span data-ttu-id="88405-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88405-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88405-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88405-112">Delegated (work or school account)</span></span> | <span data-ttu-id="88405-113">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="88405-113">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="88405-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88405-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88405-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88405-115">Not supported.</span></span>    |
|<span data-ttu-id="88405-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88405-116">Application</span></span> | <span data-ttu-id="88405-117">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88405-117">Group.ReadWrite.All, Directory.ReadWrite.All</span></span>  |

## <a name="http-request"></a><span data-ttu-id="88405-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88405-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/members/{id}/$ref
```

## <a name="request-headers"></a><span data-ttu-id="88405-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88405-119">Request headers</span></span>
| <span data-ttu-id="88405-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="88405-120">Name</span></span>       | <span data-ttu-id="88405-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="88405-121">Type</span></span> | <span data-ttu-id="88405-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="88405-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="88405-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="88405-123">Authorization</span></span>  | <span data-ttu-id="88405-124">string</span><span class="sxs-lookup"><span data-stu-id="88405-124">string</span></span>  | <span data-ttu-id="88405-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88405-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="88405-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88405-127">Request body</span></span>
<span data-ttu-id="88405-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="88405-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="88405-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88405-129">Response</span></span>
<span data-ttu-id="88405-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88405-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88405-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88405-132">Example</span></span>
#### <a name="request"></a><span data-ttu-id="88405-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88405-133">Request</span></span>
<span data-ttu-id="88405-134">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88405-134">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/members/{id}/$ref
```
<span data-ttu-id="88405-135">En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.</span><span class="sxs-lookup"><span data-stu-id="88405-135">In the request, specify the `id` of the directory object you want to remove after the $ref segment.</span></span>

#### <a name="response"></a><span data-ttu-id="88405-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88405-136">Response</span></span>
<span data-ttu-id="88405-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88405-137">The following is an example of the response.</span></span>
><span data-ttu-id="88405-138">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="88405-138">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="88405-139">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88405-139">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
