---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener permisos
ms.openlocfilehash: 1964d291b6243ac286d5ac08a6bc48f3e576bbd3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090852"
---
# <a name="get-sharing-permission-for-a-file-or-folder"></a><span data-ttu-id="27cff-102">Obtener permiso de uso compartido de un archivo o una carpeta</span><span class="sxs-lookup"><span data-stu-id="27cff-102">Get sharing permission for a file or folder</span></span>

> <span data-ttu-id="27cff-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27cff-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27cff-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27cff-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="27cff-105">Devuelva el permiso efectivo de uso compartido para un recurso de permiso en concreto.</span><span class="sxs-lookup"><span data-stu-id="27cff-105">Return the effective sharing permission for a particular permission resource.</span></span>

<span data-ttu-id="27cff-106">Los permisos efectivos de un elemento pueden provenir de dos orígenes: permisos que se establecen directamente en el propio elemento o permisos que se heredan de los antecesores del elemento.</span><span class="sxs-lookup"><span data-stu-id="27cff-106">Effective permissions of an item can come from two sources: permissions set directly on the item itself or permissions that are inherited from the item's ancestors.</span></span>

<span data-ttu-id="27cff-p102">Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad `inheritedFrom`. Esta propiedad es un recurso [ItemReference](../resources/itemreference.md) que hace referencia al antecesor del que se hereda el permiso.</span><span class="sxs-lookup"><span data-stu-id="27cff-p102">Callers can differentiate if the permission is inherited or not by checking the `inheritedFrom` property. This property is an [ItemReference](../resources/itemreference.md) resource referencing the ancestor that the permission is inherited from.</span></span>

<span data-ttu-id="27cff-109">Los niveles de permiso de SharePoint establecidos en un elemento se devuelven con un prefijo "SP".</span><span class="sxs-lookup"><span data-stu-id="27cff-109">SharePoint permission levels set on an item are returned with an 'SP' prefix.</span></span> <span data-ttu-id="27cff-110">Por ejemplo, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span><span class="sxs-lookup"><span data-stu-id="27cff-110">For example, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span></span> <span data-ttu-id="27cff-111">Vea [Lista completa de roles de SharePoint](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span><span class="sxs-lookup"><span data-stu-id="27cff-111">See [Full list of SharePoint roles](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span></span>

## <a name="permissions"></a><span data-ttu-id="27cff-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="27cff-112">Permissions</span></span>

<span data-ttu-id="27cff-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="27cff-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="27cff-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="27cff-115">Permission type</span></span>      | <span data-ttu-id="27cff-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="27cff-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="27cff-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="27cff-117">Delegated (work or school account)</span></span> | <span data-ttu-id="27cff-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27cff-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="27cff-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="27cff-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="27cff-120">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27cff-120">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="27cff-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="27cff-121">Application</span></span> | <span data-ttu-id="27cff-122">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27cff-122">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="27cff-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="27cff-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
GET /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
GET /me/drive/items/{item-id}/permissions/{perm-id}
GET /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
GET /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="27cff-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="27cff-124">Optional query parameters</span></span>

<span data-ttu-id="27cff-125">Este método admite el [parámetro de consulta $select](/graph/query-parameters) para dar forma a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27cff-125">This method support the [$select query parameter](/graph/query-parameters) to shape the response.</span></span>

## <a name="response"></a><span data-ttu-id="27cff-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27cff-126">Response</span></span>

<span data-ttu-id="27cff-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [Permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="27cff-127">If successful, this method returns a `200 OK` response code and [Permission](../resources/permission.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="27cff-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="27cff-128">Example</span></span>

### <a name="request"></a><span data-ttu-id="27cff-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="27cff-129">Request</span></span>

<span data-ttu-id="27cff-130">Aquí tiene un ejemplo de la solicitud para obtener acceso a un permiso en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="27cff-130">Here is an example of the request to access a permission on a folder.</span></span>

<!-- { "blockType": "request", "name": "get-item-permission", "scopes": "files.read" } -->

```http
GET https://graph.microsoft.com/beta/me/drive/items/{item-id}/permissions/{perm-id}
```
### <a name="response"></a><span data-ttu-id="27cff-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="27cff-131">Response</span></span>

<span data-ttu-id="27cff-132">Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="27cff-132">If successful, this method returns a [Permission](../resources/permission.md) resource for the specified ID.</span></span> 

<!-- {"blockType": "response", "@odata.type": "microsoft.graph.permission", "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "grantedTo": {
    "user": {
      "displayName": "Ryan Gregg",
      "id": "efee1b77-fb3b-4f65-99d6-274c11914d12"
    }
  },
  "id": "1",
  "roles": [ "write" ]
}
```

## <a name="remarks"></a><span data-ttu-id="27cff-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="27cff-133">Remarks</span></span>

<span data-ttu-id="27cff-134">El recurso [Permission](../resources/permission.md) usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.</span><span class="sxs-lookup"><span data-stu-id="27cff-134">The [Permission](../resources/permission.md) resource uses _facets_ to provide information about the kind of permission represented by the resource.</span></span>

<span data-ttu-id="27cff-p105">Los permisos con una faceta [**link**](../resources/sharinglink.md) representan vínculos para compartir creados en el elemento. Los vínculos para compartir contienen un token único que proporciona acceso al elemento a cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="27cff-p105">Permissions with a [**link**](../resources/sharinglink.md) facet represent sharing links created on the item. Sharing links contain a unique token that provides access to the item for anyone with the link.</span></span>

<span data-ttu-id="27cff-137">Los permisos con una faceta [**invitation**](../resources/sharinginvitation.md) representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="27cff-137">Permissions with a [**invitation**](../resources/sharinginvitation.md) facet represent permissions added by inviting specific users or groups to have access to the file.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get a DriveItem's sharing permissions",
  "keywords": "permission, permissions, sharing",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Get permission"
}-->
