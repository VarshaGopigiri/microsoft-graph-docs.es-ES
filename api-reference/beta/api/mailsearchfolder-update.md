---
title: Actualizar mailSearchFolder
description: Actualizar las propiedades modificables del objeto mailSearchFolder.
ms.openlocfilehash: abe32817c45ee1e05fbb251bd46a31941eb4218b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091181"
---
# <a name="update-mailsearchfolder"></a><span data-ttu-id="d831c-103">Actualizar mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="d831c-103">Update mailSearchFolder</span></span>

> <span data-ttu-id="d831c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d831c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d831c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d831c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d831c-106">Actualizar las propiedades modificables del objeto [mailSearchFolder](../resources/mailsearchfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="d831c-106">Update the writable properties of [mailSearchFolder](../resources/mailsearchfolder.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="d831c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d831c-107">Permissions</span></span>
<span data-ttu-id="d831c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d831c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d831c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d831c-110">Permission type</span></span>      | <span data-ttu-id="d831c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d831c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d831c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d831c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d831c-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d831c-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d831c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d831c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d831c-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d831c-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d831c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d831c-116">Application</span></span> | <span data-ttu-id="d831c-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d831c-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d831c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d831c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d831c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d831c-119">Request headers</span></span>
| <span data-ttu-id="d831c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d831c-120">Header</span></span>       | <span data-ttu-id="d831c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d831c-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d831c-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="d831c-122">Authorization</span></span>  | <span data-ttu-id="d831c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d831c-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d831c-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d831c-125">Content-Type</span></span>  | <span data-ttu-id="d831c-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d831c-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d831c-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d831c-128">Request body</span></span>
<span data-ttu-id="d831c-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="d831c-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="d831c-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d831c-132">Property</span></span>     | <span data-ttu-id="d831c-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="d831c-133">Type</span></span>   |<span data-ttu-id="d831c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="d831c-134">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d831c-135">displayName</span><span class="sxs-lookup"><span data-stu-id="d831c-135">displayName</span></span> | <span data-ttu-id="d831c-136">String</span><span class="sxs-lookup"><span data-stu-id="d831c-136">String</span></span> | <span data-ttu-id="d831c-137">El nombre para mostrar de la [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="d831c-137">The display name of the [mailFolder](../resources/mailfolder.md).</span></span>|
| <span data-ttu-id="d831c-138">includeNestedFolders</span><span class="sxs-lookup"><span data-stu-id="d831c-138">includeNestedFolders</span></span> | <span data-ttu-id="d831c-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="d831c-139">Boolean</span></span> | <span data-ttu-id="d831c-140">¿Cómo se debe recorrer la jerarquía de carpetas de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d831c-140">How the mailbox folder hierarchy should be traversed.</span></span> <span data-ttu-id="d831c-141">`true`significa que debe ser una búsqueda en profundidad mientras `false` significa que se debe realizar una búsqueda no exhaustivos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d831c-141">`true` means that a deep search should be done while `false` means a shallow search should be done instead.</span></span> |
| <span data-ttu-id="d831c-142">sourceFolderIDs</span><span class="sxs-lookup"><span data-stu-id="d831c-142">sourceFolderIDs</span></span> | <span data-ttu-id="d831c-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="d831c-143">String collection</span></span> | <span data-ttu-id="d831c-144">Las carpetas de buzón de correo que deben ser extraídas.</span><span class="sxs-lookup"><span data-stu-id="d831c-144">The mailbox folders that should be mined.</span></span> |
| <span data-ttu-id="d831c-145">filterQuery</span><span class="sxs-lookup"><span data-stu-id="d831c-145">filterQuery</span></span> | <span data-ttu-id="d831c-146">String</span><span class="sxs-lookup"><span data-stu-id="d831c-146">String</span></span> | <span data-ttu-id="d831c-147">La consulta de OData para filtrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="d831c-147">The OData query to filter the messages.</span></span> |

## <a name="response"></a><span data-ttu-id="d831c-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d831c-148">Response</span></span>
<span data-ttu-id="d831c-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d831c-149">If successful, this method returns a `200 OK` response code and updated [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d831c-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d831c-150">Example</span></span>
#### <a name="request"></a><span data-ttu-id="d831c-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d831c-151">Request</span></span>
<span data-ttu-id="d831c-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d831c-152">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_mailsearchfolder"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM
Content-type: application/json
Content-length: 159

{
  "@odata.type": "microsoft.graph.mailSearchFolder",
  "filterQuery": "contains(subject, 'Analytics')))"
}
```

#### <a name="response"></a><span data-ttu-id="d831c-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d831c-153">Response</span></span>
<span data-ttu-id="d831c-154">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d831c-154">The following is an example of the response.</span></span>
><span data-ttu-id="d831c-155">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="d831c-155">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="d831c-156">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d831c-156">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailSearchFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "@odata.type": "#microsoft.graph.mailSearchFolder",
  "id": "AAMkAGVmMDEzMx",
  "displayName": "Get MyAnalytics",
  "parentFolderId": "AAMkAGVmMDEzMy",
  "childFolderCount": 0,
  "unreadItemCount": 0,
  "totalItemCount": 0,
  "wellKnownName": null,
  "isSupported": true,
  "includeNestedFolders": true,
  "sourceFolderIDs": [
      "AAMkAGVmMDEzMi"
  ],
  "filterQuery": "contains(subject, 'Analytics')"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update mailSearchFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
