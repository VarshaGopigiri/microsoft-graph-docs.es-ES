---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enumerar quién tiene acceso a un archivo
localization_priority: Normal
ms.openlocfilehash: 2db8e7b59e75dc0ab70fe95b79919c6d86ea07be
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844512"
---
# <a name="list-sharing-permissions-on-a-driveitem"></a><span data-ttu-id="76fee-102">Mostrar permisos de uso compartido en un objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="76fee-102">List sharing permissions on a DriveItem</span></span>

> <span data-ttu-id="76fee-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="76fee-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="76fee-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="76fee-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="76fee-105">Muestre los permisos de uso compartido efectivos de un objeto [DriveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="76fee-105">List the effective sharing permissions of on a [DriveItem](../resources/driveitem.md).</span></span>

## <a name="access-to-sharing-permissions"></a><span data-ttu-id="76fee-106">Acceso a permisos de uso compartido</span><span class="sxs-lookup"><span data-stu-id="76fee-106">Access to sharing permissions</span></span>

<span data-ttu-id="76fee-107">La colección de permisos incluye información potencialmente confidencial y puede no estar disponible para todos los autores de llamadas.</span><span class="sxs-lookup"><span data-stu-id="76fee-107">The permissions collection includes potentially sensitive information and may not be available for every caller.</span></span>

* <span data-ttu-id="76fee-108">Para el propietario del elemento, se devolverán todos los permisos de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="76fee-108">For the owner of the item, all sharing permissions will be returned.</span></span> <span data-ttu-id="76fee-109">Esto incluye los copropietarios.</span><span class="sxs-lookup"><span data-stu-id="76fee-109">This includes co-owners.</span></span>
* <span data-ttu-id="76fee-110">Para un autor de llamada que no sea el propietario, se devuelven solo los permisos de uso compartido que se aplican al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="76fee-110">For a non-owner caller, only the sharing permissions that apply to the caller are returned.</span></span>
* <span data-ttu-id="76fee-111">Las propiedades de permisos de uso compartido que contienen información confidencial (por ejemplo, `shareId` y `webUrl`) se devuelven solo a los autores de llamadas que pueden crear el permiso de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="76fee-111">Sharing permission properties that contain secrets (e.g. `shareId` and `webUrl`) are only returned for callers that are able to create the sharing permission.</span></span>

## <a name="permissions"></a><span data-ttu-id="76fee-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="76fee-112">Permissions</span></span>

<span data-ttu-id="76fee-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="76fee-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="76fee-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76fee-115">Permission type</span></span>      | <span data-ttu-id="76fee-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76fee-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76fee-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76fee-117">Delegated (work or school account)</span></span> | <span data-ttu-id="76fee-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76fee-118">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="76fee-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76fee-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76fee-120">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76fee-120">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="76fee-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76fee-121">Application</span></span> | <span data-ttu-id="76fee-122">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76fee-122">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="76fee-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76fee-123">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/permissions
GET /groups/{group-id}/drive/items/{item-id}/permissions
GET /me/drive/items/{item-id}/permissions
GET /me/drive/root:/{path}:/permissions
GET /sites/{siteId}/drive/items/{itemId}/permissions
GET /users/{userId}/drive/items/{itemId}/permissions
```

## <a name="optional-query-parameters"></a><span data-ttu-id="76fee-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="76fee-124">Optional query parameters</span></span>

<span data-ttu-id="76fee-125">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$select` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76fee-125">This method supports the `$select` [OData Query Parameters](/graph/query-parameters) to customize the response.</span></span>

## <a name="optional-request-headers"></a><span data-ttu-id="76fee-126">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="76fee-126">Optional request headers</span></span>

| <span data-ttu-id="76fee-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="76fee-127">Name</span></span>          | <span data-ttu-id="76fee-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="76fee-128">Type</span></span>   | <span data-ttu-id="76fee-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="76fee-129">Description</span></span>                                                                                                                                     |
|:--------------|:-------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76fee-130">if-none-match</span><span class="sxs-lookup"><span data-stu-id="76fee-130">if-none-match</span></span> | <span data-ttu-id="76fee-131">string</span><span class="sxs-lookup"><span data-stu-id="76fee-131">string</span></span> | <span data-ttu-id="76fee-132">Si se incluye este encabezado de la solicitud y el ETag proporcionado coincide con el ETag actual del elemento, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="76fee-132">If this request header is included and the etag provided matches the current etag on the item, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="response"></a><span data-ttu-id="76fee-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76fee-133">Response</span></span>

<span data-ttu-id="76fee-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de recursos [Permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76fee-134">If successful, this method returns a `200 OK` response code and collection of [Permission](../resources/permission.md) resources in the response body.</span></span>

<span data-ttu-id="76fee-135">Los permisos de uso compartido efectivos de un objeto DriveItem pueden provenir de dos orígenes:</span><span class="sxs-lookup"><span data-stu-id="76fee-135">Effective sharing permissions of a DriveItem can come from two sources:</span></span>

* <span data-ttu-id="76fee-136">Permisos de uso compartido que se aplican directamente en el propio objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="76fee-136">Sharing permissions applied directly on the DriveItem itself</span></span>
* <span data-ttu-id="76fee-137">Permisos de uso compartido heredados de los antecesores del objeto DriveItem</span><span class="sxs-lookup"><span data-stu-id="76fee-137">Sharing permissions inherited from the DriveItem's ancestors</span></span>

<span data-ttu-id="76fee-p104">Los autores de llamadas pueden distinguir si el permiso se hereda o no comprobando la propiedad **inheritedFrom**. Esta propiedad es un recurso [**itemReference**](../resources/itemreference.md) que hace referencia al antecesor del que se hereda el permiso.</span><span class="sxs-lookup"><span data-stu-id="76fee-p104">Callers can differentiate if the permission is inherited or not by checking the **inheritedFrom** property. This property is an [**itemReference**](../resources/itemreference.md) resource referencing the ancestor that the permission is inherited from.</span></span>

<span data-ttu-id="76fee-140">Los niveles de permiso de SharePoint establecidos en un elemento se devuelven con un prefijo "SP".</span><span class="sxs-lookup"><span data-stu-id="76fee-140">SharePoint permission levels set on an item are returned with an 'SP' prefix.</span></span> <span data-ttu-id="76fee-141">Por ejemplo, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span><span class="sxs-lookup"><span data-stu-id="76fee-141">For example, SP.View Only, SP.Limited Access, SP.View Web Analytics Data.</span></span> <span data-ttu-id="76fee-142">Vea [Lista completa de roles de SharePoint](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span><span class="sxs-lookup"><span data-stu-id="76fee-142">See [Full list of SharePoint roles](https://technet.microsoft.com/en-us/library/cc721640.aspx#section1).</span></span>

## <a name="example"></a><span data-ttu-id="76fee-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76fee-143">Example</span></span>

<span data-ttu-id="76fee-144">En este ejemplo, se recupera la colección de permisos en un elemento de la unidad del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="76fee-144">This example retrieves the collection of permissions on an item in the signed in user's drive.</span></span>

<!-- { "blockType": "request", "name": "get-item-permissions", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/permissions
```

### <a name="response"></a><span data-ttu-id="76fee-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76fee-145">Response</span></span>

<span data-ttu-id="76fee-146">Esta respuesta de ejemplo incluye tres permisos, el primero es un vínculo para compartir con permisos de edición, el segundo es un permiso explícito para un usuario llamado John, que se ha heredado de una carpeta principal, y el tercero es un vínculo para compartir de lectura y escritura creado por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="76fee-146">This example response includes three permissions, the first is a sharing link with edit permissions, the second is an explicit permission for a user named John, which was inherited from a parent folder, and the third is a read-write sharing link created by an application.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="76fee-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="76fee-147">Remarks</span></span>

<span data-ttu-id="76fee-p106">La relación **permisos** del objeto DriveItem no se puede expandir como parte de una llamada a [get DriveItem](driveitem-get.md) o una colección de objetos DriveItem. Debe tener acceso a la propiedad de permisos directamente.</span><span class="sxs-lookup"><span data-stu-id="76fee-p106">The **permissions** relationship of DriveItem cannot be expanded as part of a call to [get DriveItem](driveitem-get.md) or a collection of DriveItems. You must access the permissions property directly.</span></span>

## <a name="error-responses"></a><span data-ttu-id="76fee-150">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="76fee-150">Error responses</span></span>

<span data-ttu-id="76fee-151">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="76fee-151">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "List an item's permissions",
  "keywords": "permission, permissions, sharing",
  "section": "documentation",
  "tocPath": "Sharing/Permissions"
} -->
