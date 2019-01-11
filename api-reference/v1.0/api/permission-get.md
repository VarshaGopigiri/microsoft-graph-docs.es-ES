---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener permisos
localization_priority: Normal
ms.openlocfilehash: 4d893724af2c695597f0d81d5ceb0649c30ad7b0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864137"
---
# <a name="get-sharing-permission-for-a-file-or-folder"></a><span data-ttu-id="39635-102">Obtener permiso de uso compartido de un archivo o una carpeta</span><span class="sxs-lookup"><span data-stu-id="39635-102">Get sharing permission for a file or folder</span></span>

<span data-ttu-id="39635-103">Devuelva el permiso efectivo de uso compartido para un recurso de permiso en concreto.</span><span class="sxs-lookup"><span data-stu-id="39635-103">Return the effective sharing permission for a particular permission resource.</span></span>

<span data-ttu-id="39635-104">Los permisos efectivos de un elemento pueden provenir de dos orígenes: permisos que se establecen directamente en el propio elemento o permisos que se heredan de los antecesores del elemento.</span><span class="sxs-lookup"><span data-stu-id="39635-104">Effective permissions of an item can come from two sources: permissions set directly on the item itself or permissions that are inherited from the item's ancestors.</span></span>

<span data-ttu-id="39635-p101">Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad `inheritedFrom`. Esta propiedad es un recurso [ItemReference](../resources/itemreference.md) que hace referencia al antecesor del que se hereda el permiso.</span><span class="sxs-lookup"><span data-stu-id="39635-p101">Callers can differentiate if the permission is inherited or not by checking the `inheritedFrom` property. This property is an [ItemReference](../resources/itemreference.md) resource referencing the ancestor that the permission is inherited from.</span></span>

<span data-ttu-id="39635-107">Los niveles de permiso de SharePoint establecidos en un elemento se devuelven con un prefijo "SP".</span><span class="sxs-lookup"><span data-stu-id="39635-107">SharePoint permission levels set on an item are returned with an 'SP' prefix.</span></span> <span data-ttu-id="39635-108">Por ejemplo, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span><span class="sxs-lookup"><span data-stu-id="39635-108">For example, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span></span> <span data-ttu-id="39635-109">Vea [Lista completa de roles de SharePoint](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span><span class="sxs-lookup"><span data-stu-id="39635-109">See [Full list of SharePoint roles](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span></span>

## <a name="permissions"></a><span data-ttu-id="39635-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="39635-110">Permissions</span></span>

<span data-ttu-id="39635-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39635-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39635-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39635-113">Permission type</span></span>      | <span data-ttu-id="39635-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39635-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="39635-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39635-115">Delegated (work or school account)</span></span> | <span data-ttu-id="39635-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39635-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="39635-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39635-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="39635-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39635-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="39635-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39635-119">Application</span></span> | <span data-ttu-id="39635-120">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39635-120">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="39635-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39635-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/permissions/{perm-id}
GET /groups/{group-id}/drive/items/{item-id}/permissions/{perm-id}
GET /me/drive/items/{item-id}/permissions/{perm-id}
GET /sites/{site-id}/drive/items/{item-id}/permissions/{perm-id}
GET /users/{user-id}/drive/items/{item-id}/permissions/{perm-id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="39635-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="39635-122">Optional query parameters</span></span>

<span data-ttu-id="39635-123">Este método admite el [parámetro de consulta $select](/graph/query-parameters) para dar forma a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39635-123">This method support the [$select query parameter](/graph/query-parameters) to shape the response.</span></span>

## <a name="response"></a><span data-ttu-id="39635-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39635-124">Response</span></span>

<span data-ttu-id="39635-125">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [Permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39635-125">If successful, this method returns a `200 OK` response code and [Permission](../resources/permission.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39635-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39635-126">Example</span></span>

### <a name="request"></a><span data-ttu-id="39635-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39635-127">Request</span></span>

<span data-ttu-id="39635-128">Aquí tiene un ejemplo de la solicitud para obtener acceso a un permiso en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="39635-128">Here is an example of the request to access a permission on a folder.</span></span>

<!-- { "blockType": "request", "name": "get-item-permission", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/permissions/{perm-id}
```

### <a name="response"></a><span data-ttu-id="39635-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39635-129">Response</span></span>

<span data-ttu-id="39635-130">Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="39635-130">If successful, this method returns a [Permission](../resources/permission.md) resource for the specified ID.</span></span> 

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

## <a name="remarks"></a><span data-ttu-id="39635-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="39635-131">Remarks</span></span>

<span data-ttu-id="39635-132">El recurso [Permission](../resources/permission.md) usa _facetas_ para proporcionar información sobre el tipo de permiso que representa el recurso.</span><span class="sxs-lookup"><span data-stu-id="39635-132">The [Permission](../resources/permission.md) resource uses _facets_ to provide information about the kind of permission represented by the resource.</span></span>

<span data-ttu-id="39635-p104">Los permisos con una faceta [**link**](../resources/sharinglink.md) representan vínculos para compartir creados en el elemento. Los vínculos para compartir contienen un token único que proporciona acceso al elemento a cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="39635-p104">Permissions with a [**link**](../resources/sharinglink.md) facet represent sharing links created on the item. Sharing links contain a unique token that provides access to the item for anyone with the link.</span></span>

<span data-ttu-id="39635-135">Los permisos con una faceta [**invitation**](../resources/sharinginvitation.md) representan los permisos agregados al invitar a usuarios o grupos específicos para que tengan acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="39635-135">Permissions with a [**invitation**](../resources/sharinginvitation.md) facet represent permissions added by inviting specific users or groups to have access to the file.</span></span>

### <a name="error-responses"></a><span data-ttu-id="39635-136">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="39635-136">Error responses</span></span>

<span data-ttu-id="39635-137">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="39635-137">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Get a DriveItem's sharing permissions",
  "keywords": "permission, permissions, sharing",
  "section": "documentation",
  "tocPath": "Sharing/Permissions"
} -->
