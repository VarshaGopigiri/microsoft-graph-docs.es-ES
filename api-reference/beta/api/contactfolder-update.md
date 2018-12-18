---
title: Actualizar contactfolder
description: Actualiza las propiedades del objeto contactfolder.
author: angelgolfer-ms
ms.openlocfilehash: 5b61758309e8489312d2f8360625d6d12566fae0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330996"
---
# <a name="update-contactfolder"></a><span data-ttu-id="53ffe-103">Actualizar contactfolder</span><span class="sxs-lookup"><span data-stu-id="53ffe-103">Update contactfolder</span></span>

> <span data-ttu-id="53ffe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53ffe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53ffe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53ffe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="53ffe-106">Actualiza las propiedades del objeto contactfolder.</span><span class="sxs-lookup"><span data-stu-id="53ffe-106">Update the properties of contactfolder object.</span></span>
## <a name="permissions"></a><span data-ttu-id="53ffe-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="53ffe-107">Permissions</span></span>
<span data-ttu-id="53ffe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="53ffe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="53ffe-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53ffe-110">Permission type</span></span>      | <span data-ttu-id="53ffe-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53ffe-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="53ffe-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53ffe-112">Delegated (work or school account)</span></span> | <span data-ttu-id="53ffe-113">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="53ffe-113">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="53ffe-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53ffe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="53ffe-115">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="53ffe-115">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="53ffe-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53ffe-116">Application</span></span> | <span data-ttu-id="53ffe-117">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="53ffe-117">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="53ffe-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53ffe-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/contactFolders/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="53ffe-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53ffe-119">Request headers</span></span>
| <span data-ttu-id="53ffe-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53ffe-120">Header</span></span>       | <span data-ttu-id="53ffe-121">Valor</span><span class="sxs-lookup"><span data-stu-id="53ffe-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="53ffe-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="53ffe-122">Authorization</span></span>  | <span data-ttu-id="53ffe-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53ffe-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="53ffe-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="53ffe-125">Content-Type</span></span>  | <span data-ttu-id="53ffe-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53ffe-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="53ffe-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53ffe-128">Request body</span></span>
<span data-ttu-id="53ffe-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="53ffe-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="53ffe-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53ffe-132">Property</span></span>     | <span data-ttu-id="53ffe-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="53ffe-133">Type</span></span>   |<span data-ttu-id="53ffe-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="53ffe-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="53ffe-135">displayName</span><span class="sxs-lookup"><span data-stu-id="53ffe-135">displayName</span></span>|<span data-ttu-id="53ffe-136">String</span><span class="sxs-lookup"><span data-stu-id="53ffe-136">String</span></span>|<span data-ttu-id="53ffe-137">Nombre para mostrar de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="53ffe-137">The folder's display name.</span></span>|
|<span data-ttu-id="53ffe-138">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="53ffe-138">parentFolderId</span></span>|<span data-ttu-id="53ffe-139">String</span><span class="sxs-lookup"><span data-stu-id="53ffe-139">String</span></span>|<span data-ttu-id="53ffe-140">El identificador de la carpeta principal de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="53ffe-140">The ID of the folder's parent folder.</span></span>|
|<span data-ttu-id="53ffe-141">wellKnownName</span><span class="sxs-lookup"><span data-stu-id="53ffe-141">wellKnownName</span></span>|<span data-ttu-id="53ffe-142">string</span><span class="sxs-lookup"><span data-stu-id="53ffe-142">string</span></span>|<span data-ttu-id="53ffe-143">El nombre de la carpeta si la carpeta es una carpeta reconocida.</span><span class="sxs-lookup"><span data-stu-id="53ffe-143">The name of the folder if the folder is a recognized folder.</span></span> <span data-ttu-id="53ffe-144">Actualmente `contacts` es la única carpeta Contactos reconocida.</span><span class="sxs-lookup"><span data-stu-id="53ffe-144">Currently `contacts` is the only recognized contacts folder.</span></span>|

## <a name="response"></a><span data-ttu-id="53ffe-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53ffe-145">Response</span></span>

<span data-ttu-id="53ffe-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53ffe-146">If successful, this method returns a `200 OK` response code and updated [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="53ffe-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53ffe-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="53ffe-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53ffe-148">Request</span></span>
<span data-ttu-id="53ffe-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53ffe-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_contactfolder"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/contactFolders/{id}
Content-type: application/json
Content-length: 84

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value"
}
```
##### <a name="response"></a><span data-ttu-id="53ffe-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53ffe-150">Response</span></span>
<span data-ttu-id="53ffe-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53ffe-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "wellKnownName": "wellKnownName-value",
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
