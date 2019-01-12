---
title: Remove owner
description: Use esta API para quitar un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación owners.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: f07eb16e2e7f70c3f503a5f182c015c6862ce5e2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986757"
---
# <a name="remove-owner"></a><span data-ttu-id="c36bd-103">Remove owner</span><span class="sxs-lookup"><span data-stu-id="c36bd-103">Remove owner</span></span>
<span data-ttu-id="c36bd-104">Use esta API para quitar un propietario de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación owners.</span><span class="sxs-lookup"><span data-stu-id="c36bd-104">Use this API to remove an owner from an Office 365 group, a security group, or a mail-enabled security group through the owners navigation property.</span></span>

## <a name="permissions"></a><span data-ttu-id="c36bd-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c36bd-105">Permissions</span></span>
<span data-ttu-id="c36bd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c36bd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c36bd-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c36bd-108">Permission type</span></span>      | <span data-ttu-id="c36bd-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c36bd-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c36bd-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c36bd-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c36bd-111">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c36bd-111">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c36bd-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c36bd-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c36bd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c36bd-113">Not supported.</span></span>    |
|<span data-ttu-id="c36bd-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c36bd-114">Application</span></span> | <span data-ttu-id="c36bd-115">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c36bd-115">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c36bd-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c36bd-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/owners/{id}/$ref
```

## <a name="request-headers"></a><span data-ttu-id="c36bd-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c36bd-117">Request headers</span></span>
| <span data-ttu-id="c36bd-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c36bd-118">Name</span></span>       | <span data-ttu-id="c36bd-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c36bd-119">Type</span></span> | <span data-ttu-id="c36bd-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c36bd-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c36bd-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c36bd-121">Authorization</span></span>  | <span data-ttu-id="c36bd-122">string</span><span class="sxs-lookup"><span data-stu-id="c36bd-122">string</span></span>  | <span data-ttu-id="c36bd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c36bd-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c36bd-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c36bd-125">Request body</span></span>
<span data-ttu-id="c36bd-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c36bd-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c36bd-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c36bd-127">Response</span></span>
<span data-ttu-id="c36bd-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c36bd-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c36bd-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c36bd-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="c36bd-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c36bd-131">Request</span></span>
<span data-ttu-id="c36bd-132">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c36bd-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_owner_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/owners/{id}/$ref
```
<span data-ttu-id="c36bd-133">En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.</span><span class="sxs-lookup"><span data-stu-id="c36bd-133">In the request, specify the `id` of the directory object you want to remove after the $ref segment.</span></span>

#### <a name="response"></a><span data-ttu-id="c36bd-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c36bd-134">Response</span></span>
<span data-ttu-id="c36bd-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c36bd-135">The following is an example of the response.</span></span>
><span data-ttu-id="c36bd-136">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c36bd-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c36bd-137">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c36bd-137">All the properties will be returned from an actual call.</span></span>
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
  "description": "Delete owner",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
