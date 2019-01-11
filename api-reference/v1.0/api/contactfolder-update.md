---
title: Actualizar contactfolder
description: Actualiza las propiedades del objeto contactfolder.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 01ecca2b59482c1c2c75096b711904f3054fd338
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836424"
---
# <a name="update-contactfolder"></a><span data-ttu-id="40046-103">Actualizar contactfolder</span><span class="sxs-lookup"><span data-stu-id="40046-103">Update contactfolder</span></span>

<span data-ttu-id="40046-104">Actualiza las propiedades del objeto contactfolder.</span><span class="sxs-lookup"><span data-stu-id="40046-104">Update the properties of contactfolder object.</span></span>
## <a name="permissions"></a><span data-ttu-id="40046-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="40046-105">Permissions</span></span>
<span data-ttu-id="40046-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="40046-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="40046-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="40046-108">Permission type</span></span>      | <span data-ttu-id="40046-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="40046-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="40046-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="40046-110">Delegated (work or school account)</span></span> | <span data-ttu-id="40046-111">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="40046-111">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="40046-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="40046-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="40046-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="40046-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="40046-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="40046-114">Application</span></span> | <span data-ttu-id="40046-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="40046-115">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="40046-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="40046-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/contactFolders/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="40046-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="40046-117">Request headers</span></span>
| <span data-ttu-id="40046-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40046-118">Header</span></span>       | <span data-ttu-id="40046-119">Valor</span><span class="sxs-lookup"><span data-stu-id="40046-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="40046-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="40046-120">Authorization</span></span>  | <span data-ttu-id="40046-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="40046-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="40046-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="40046-123">Content-Type</span></span>  | <span data-ttu-id="40046-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="40046-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="40046-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="40046-126">Request body</span></span>
<span data-ttu-id="40046-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="40046-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="40046-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40046-130">Property</span></span>     | <span data-ttu-id="40046-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="40046-131">Type</span></span>   |<span data-ttu-id="40046-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="40046-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="40046-133">displayName</span><span class="sxs-lookup"><span data-stu-id="40046-133">displayName</span></span>|<span data-ttu-id="40046-134">String</span><span class="sxs-lookup"><span data-stu-id="40046-134">String</span></span>|<span data-ttu-id="40046-135">Nombre para mostrar de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="40046-135">The folder's display name.</span></span>|
|<span data-ttu-id="40046-136">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="40046-136">parentFolderId</span></span>|<span data-ttu-id="40046-137">String</span><span class="sxs-lookup"><span data-stu-id="40046-137">String</span></span>|<span data-ttu-id="40046-138">Identificador de la carpeta principal de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="40046-138">The ID of the folder's parent folder.</span></span>|

## <a name="response"></a><span data-ttu-id="40046-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40046-139">Response</span></span>

<span data-ttu-id="40046-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40046-140">If successful, this method returns a `200 OK` response code and updated [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="40046-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40046-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="40046-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="40046-142">Request</span></span>
<span data-ttu-id="40046-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="40046-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_contactfolder"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/contactFolders/{id}
Content-type: application/json
Content-length: 84

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value"
}
```
##### <a name="response"></a><span data-ttu-id="40046-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40046-144">Response</span></span>
<span data-ttu-id="40046-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="40046-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 104

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update contactfolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
