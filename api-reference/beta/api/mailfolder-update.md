---
title: Actualizar mailFolder
description: Actualizar las propiedades del objeto mailFolder.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: f9b0af67b4fdedbf6ecbbcfe591057a4aeb86351
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873902"
---
# <a name="update-mailfolder"></a><span data-ttu-id="c6d36-103">Actualizar mailFolder</span><span class="sxs-lookup"><span data-stu-id="c6d36-103">Update mailFolder</span></span>

> <span data-ttu-id="c6d36-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c6d36-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c6d36-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c6d36-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c6d36-106">Actualizar las propiedades del objeto [mailFolder](../resources/mailfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="c6d36-106">Update the properties of [mailFolder](../resources/mailfolder.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="c6d36-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6d36-107">Permissions</span></span>
<span data-ttu-id="c6d36-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6d36-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c6d36-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6d36-110">Permission type</span></span>      | <span data-ttu-id="c6d36-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6d36-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6d36-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6d36-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c6d36-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6d36-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c6d36-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6d36-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6d36-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6d36-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c6d36-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6d36-116">Application</span></span> | <span data-ttu-id="c6d36-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6d36-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6d36-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6d36-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}
```

## <a name="request-headers"></a><span data-ttu-id="c6d36-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6d36-119">Request headers</span></span>
| <span data-ttu-id="c6d36-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6d36-120">Header</span></span>       | <span data-ttu-id="c6d36-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c6d36-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c6d36-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c6d36-122">Authorization</span></span>  | <span data-ttu-id="c6d36-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6d36-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c6d36-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c6d36-125">Content-Type</span></span>  | <span data-ttu-id="c6d36-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6d36-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c6d36-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6d36-128">Request body</span></span>
<span data-ttu-id="c6d36-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c6d36-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c6d36-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c6d36-132">Property</span></span>     | <span data-ttu-id="c6d36-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6d36-133">Type</span></span>   |<span data-ttu-id="c6d36-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6d36-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6d36-135">displayName</span><span class="sxs-lookup"><span data-stu-id="c6d36-135">displayName</span></span>|<span data-ttu-id="c6d36-136">String</span><span class="sxs-lookup"><span data-stu-id="c6d36-136">String</span></span>|<span data-ttu-id="c6d36-137">Nombre para mostrar del objeto mailFolder.</span><span class="sxs-lookup"><span data-stu-id="c6d36-137">The mailFolder's display name.</span></span>|

## <a name="response"></a><span data-ttu-id="c6d36-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6d36-138">Response</span></span>
<span data-ttu-id="c6d36-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6d36-139">If successful, this method returns a `200 OK` response code and updated [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6d36-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6d36-140">Example</span></span>
#### <a name="request"></a><span data-ttu-id="c6d36-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6d36-141">Request</span></span>
<span data-ttu-id="c6d36-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6d36-142">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_mailfolder"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```

#### <a name="response"></a><span data-ttu-id="c6d36-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6d36-143">Response</span></span>
<span data-ttu-id="c6d36-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6d36-144">The following is an example of the response.</span></span>
><span data-ttu-id="c6d36-145">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c6d36-145">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c6d36-146">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c6d36-146">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
    "id": "AAMkAGVmMDEzM",
    "displayName": "displayName-value",
    "parentFolderId": "AAMkAGVmMDEzI",
    "childFolderCount": 2,
    "unreadItemCount": 59,
    "totalItemCount": 60,
    "wellKnownName": "inbox"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update mailfolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
