---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar quién tiene acceso a un archivo
ms.openlocfilehash: d7090939fb2b950ed92fd9574cf9dd5b80ec8a6c
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23266635"
---
# <a name="list-sharing-permissions-on-a-driveitem"></a><span data-ttu-id="5699b-102">Mostrar permisos de uso compartido en un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="5699b-102">List sharing permissions on a DriveItem</span></span>

<span data-ttu-id="5699b-103">Muestre los permisos de uso compartido efectivos de un objeto [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="5699b-103">List the effective sharing permissions of on a [DriveItem](../resources/driveitem.md).</span></span>

## <a name="access-to-sharing-permissions"></a><span data-ttu-id="5699b-104">Acceso a permisos de uso compartido</span><span class="sxs-lookup"><span data-stu-id="5699b-104">Access to sharing permissions</span></span>

<span data-ttu-id="5699b-105">La colección de permisos incluye información potencialmente confidencial y puede no estar disponible para todos los autores de llamadas.</span><span class="sxs-lookup"><span data-stu-id="5699b-105">The permissions collection includes potentially sensitive information and may not be available for every caller.</span></span>

* <span data-ttu-id="5699b-106">Para el propietario del elemento, se devolverán todos los permisos de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="5699b-106">For the owner of the item, all sharing permissions will be returned.</span></span> <span data-ttu-id="5699b-107">Esto incluye los copropietarios.</span><span class="sxs-lookup"><span data-stu-id="5699b-107">This includes co-owners.</span></span>
* <span data-ttu-id="5699b-108">Para un autor de llamada que no sea el propietario, se devuelven solo los permisos de uso compartido que se aplican al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5699b-108">For a non-owner caller, only the sharing permissions that apply to the caller are returned.</span></span>
* <span data-ttu-id="5699b-109">Las propiedades de permisos de uso compartido que contienen información confidencial (por ejemplo, `shareId` y `webUrl`) se devuelven solo a los autores de llamadas que pueden crear el permiso de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="5699b-109">Sharing permission properties that contain secrets (e.g. `shareId` and `webUrl`) are only returned for callers that are able to create the sharing permission.</span></span>

## <a name="permissions"></a><span data-ttu-id="5699b-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="5699b-110">Permissions</span></span>

<span data-ttu-id="5699b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5699b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5699b-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5699b-113">Permission type</span></span>      | <span data-ttu-id="5699b-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5699b-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5699b-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5699b-115">Delegated (work or school account)</span></span> | <span data-ttu-id="5699b-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5699b-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="5699b-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5699b-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5699b-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5699b-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="5699b-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5699b-119">Application</span></span> | <span data-ttu-id="5699b-120">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5699b-120">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5699b-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5699b-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/permissions
GET /groups/{group-id}/drive/items/{item-id}/permissions
GET /me/drive/items/{item-id}/permissions
GET /me/drive/root:/{path}:/permissions
GET /sites/{siteId}/drive/items/{itemId}/permissions
GET /users/{userId}/drive/items/{itemId}/permissions
```

## <a name="optional-query-parameters"></a><span data-ttu-id="5699b-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5699b-122">Optional query parameters</span></span>

<span data-ttu-id="5699b-123">Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5699b-123">This method supports the `$select` [OData Query Parameters](../../../concepts/query_parameters.md) to customize the response.</span></span>

## <a name="optional-request-headers"></a><span data-ttu-id="5699b-124">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="5699b-124">Optional request headers</span></span>

| <span data-ttu-id="5699b-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="5699b-125">Name</span></span>          | <span data-ttu-id="5699b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="5699b-126">Type</span></span>   | <span data-ttu-id="5699b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5699b-127">Description</span></span>                                                                                                                                     |
|:--------------|:-------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5699b-128">if-none-match</span><span class="sxs-lookup"><span data-stu-id="5699b-128">if-none-match</span></span> | <span data-ttu-id="5699b-129">string</span><span class="sxs-lookup"><span data-stu-id="5699b-129">string</span></span> | <span data-ttu-id="5699b-130">Si se incluye este encabezado de la solicitud y el ETag proporcionado coincide con el ETag actual del elemento, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="5699b-130">If this request header is included and the etag provided matches the current etag on the item, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="response"></a><span data-ttu-id="5699b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5699b-131">Response</span></span>

<span data-ttu-id="5699b-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos [Permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5699b-132">If successful, this method returns a `200 OK` response code and collection of [Permission](../resources/permission.md) resources in the response body.</span></span>

<span data-ttu-id="5699b-133">Los permisos de uso compartido efectivos de un objeto DriveItem pueden provenir de dos orígenes:</span><span class="sxs-lookup"><span data-stu-id="5699b-133">Effective sharing permissions of a DriveItem can come from two sources:</span></span>

* <span data-ttu-id="5699b-134">Permisos de uso compartido que se aplican directamente en el propio objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="5699b-134">Sharing permissions applied directly on the DriveItem itself</span></span>
* <span data-ttu-id="5699b-135">Permisos de uso compartido heredados de los antecesores del objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="5699b-135">Sharing permissions inherited from the DriveItem's ancestors</span></span>

<span data-ttu-id="5699b-p103">Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad **inheritedFrom**. Esta propiedad es un recurso [**itemReference**](../resources/itemreference.md) que hace referencia al antecesor del que se hereda el permiso.</span><span class="sxs-lookup"><span data-stu-id="5699b-p103">Callers can differentiate if the permission is inherited or not by checking the **inheritedFrom** property. This property is an [**itemReference**](../resources/itemreference.md) resource referencing the ancestor that the permission is inherited from.</span></span>

<span data-ttu-id="5699b-138">Los niveles de permiso de SharePoint establecidos en un elemento se devuelven con un prefijo "SP".</span><span class="sxs-lookup"><span data-stu-id="5699b-138">SharePoint permission levels set on an item are returned with an 'SP' prefix.</span></span> <span data-ttu-id="5699b-139">Por ejemplo, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span><span class="sxs-lookup"><span data-stu-id="5699b-139">For example, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span></span> <span data-ttu-id="5699b-140">Vea [Lista completa de roles de SharePoint](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span><span class="sxs-lookup"><span data-stu-id="5699b-140">See [Full list of SharePoint roles](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span></span>

## <a name="example"></a><span data-ttu-id="5699b-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5699b-141">Example</span></span>

<span data-ttu-id="5699b-142">En este ejemplo, se recupera la colección de permisos en un elemento de la unidad del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="5699b-142">This example retrieves the collection of permissions on an item in the signed in user's drive.</span></span>

<!-- { "blockType": "request", "name": "get-item-permissions", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/permissions
```

### <a name="response"></a><span data-ttu-id="5699b-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5699b-143">Response</span></span>

<span data-ttu-id="5699b-144">Esta respuesta de ejemplo incluye tres permisos, el primero es un vínculo para compartir con permisos de edición, el segundo es un permiso explícito para un usuario llamado John, que se ha heredado de una carpeta principal, y el tercero es un vínculo para compartir de lectura y escritura creado por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5699b-144">This example response includes three permissions, the first is a sharing link with edit permissions, the second is an explicit permission for a user named John, which was inherited from a parent folder, and the third is a read-write sharing link created by an application.</span></span>

<!-- {"blockType": "response", "@odata.type": "Collection(microsoft.graph.permission)", "truncated": true} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "1",
      "roles": ["write"],
      "link": {
        "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
        "type": "edit"
      }
    },
    {
      "id": "2",
      "roles": ["write"],
      "grantedTo": {
        "user": {
          "id": "5D33DD65C6932946",
          "displayName": "John Doe"
        }
      },
      "inheritedFrom": {
        "driveId": "1234567890ABD",
        "id": "1234567890ABC!123",
        "path": "/drive/root:/Documents" }
    },
    {
      "id": "3",
      "roles": ["write"],
      "link": {
        "webUrl": "https://onedrive.live.com/redir?resid=5D33DD65C6932946!70859&authkey=!AL7N1QAfSWcjNU8&ithint=folder%2cgif",
        "type": "edit",
        "application": {
          "id": "12345",
          "displayName": "Contoso Time Manager"
        }
      }
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="5699b-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5699b-145">Remarks</span></span>

<span data-ttu-id="5699b-p105">La relación **permisos** del objeto DriveItem no se puede expandir como parte de una llamada a [get DriveItem](driveitem_get.md) o una colección de objetos DriveItem. Debe tener acceso a la propiedad de permisos directamente.</span><span class="sxs-lookup"><span data-stu-id="5699b-p105">The **permissions** relationship of DriveItem cannot be expanded as part of a call to [get DriveItem](driveitem_get.md) or a collection of DriveItems. You must access the permissions property directly.</span></span>

## <a name="error-responses"></a><span data-ttu-id="5699b-148">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="5699b-148">Error responses</span></span>

<span data-ttu-id="5699b-149">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="5699b-149">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>

[error-response]: ../../../concepts/errors.md

<!-- {
  "type": "#page.annotation",
  "description": "List an item's permissions",
  "keywords": "permission, permissions, sharing",
  "section": "documentation",
  "tocPath": "Sharing/Permissions"
} -->
