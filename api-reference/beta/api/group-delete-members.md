---
title: Quitar miembro
description: Use esta API para quitar un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede quitar usuarios u otros grupos.
localization_priority: Normal
ms.openlocfilehash: 917e662158785111847d5d74821bfedbb61205dc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864480"
---
# <a name="remove-member"></a><span data-ttu-id="c2164-104">Quitar miembro</span><span class="sxs-lookup"><span data-stu-id="c2164-104">Remove member</span></span>

> <span data-ttu-id="c2164-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2164-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2164-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2164-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c2164-p103">Use esta API para quitar un miembro de un grupo de Office 365, un grupo de seguridad o un grupo de seguridad habilitado para correo a través de la propiedad de navegación **members**. Puede quitar usuarios u otros grupos.</span><span class="sxs-lookup"><span data-stu-id="c2164-p103">Use this API to remove a member from an Office 365 group, a security group, or a mail-enabled security group through the **members** navigation property. You can remove users or other groups.</span></span>

## <a name="permissions"></a><span data-ttu-id="c2164-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2164-109">Permissions</span></span>
<span data-ttu-id="c2164-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2164-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2164-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2164-112">Permission type</span></span>      | <span data-ttu-id="c2164-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2164-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2164-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2164-114">Delegated (work or school account)</span></span> | <span data-ttu-id="c2164-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="c2164-115">Group.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="c2164-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2164-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2164-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2164-117">Not supported.</span></span>    |
|<span data-ttu-id="c2164-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2164-118">Application</span></span> | <span data-ttu-id="c2164-119">Group.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2164-119">Group.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2164-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2164-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/members/{id}/$ref
```

## <a name="request-headers"></a><span data-ttu-id="c2164-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2164-121">Request headers</span></span>
| <span data-ttu-id="c2164-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2164-122">Name</span></span>       | <span data-ttu-id="c2164-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2164-123">Type</span></span> | <span data-ttu-id="c2164-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2164-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c2164-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="c2164-125">Authorization</span></span>  | <span data-ttu-id="c2164-126">string</span><span class="sxs-lookup"><span data-stu-id="c2164-126">string</span></span>  | <span data-ttu-id="c2164-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2164-p105">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c2164-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2164-129">Request body</span></span>
<span data-ttu-id="c2164-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c2164-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c2164-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2164-131">Response</span></span>
<span data-ttu-id="c2164-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2164-p106">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2164-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2164-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="c2164-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2164-135">Request</span></span>
<span data-ttu-id="c2164-136">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2164-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_group"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/{id}/members/{id}/$ref
```
<span data-ttu-id="c2164-137">En la solicitud, especifique la `id` del objeto de directorio que quiere quitar después del segmento de $ref.</span><span class="sxs-lookup"><span data-stu-id="c2164-137">In the request, specify the `id` of the directory object you want to remove after the $ref segment.</span></span>

#### <a name="response"></a><span data-ttu-id="c2164-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2164-138">Response</span></span>
<span data-ttu-id="c2164-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2164-139">The following is an example of the response.</span></span>
><span data-ttu-id="c2164-140">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c2164-140">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c2164-141">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2164-141">All the properties will be returned from an actual call.</span></span>
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
