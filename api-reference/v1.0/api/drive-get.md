---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener unidad
ms.openlocfilehash: 6ff71104c18a5a9354d18689c62a96be72b7fe12
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029877"
---
# <a name="get-drive"></a><span data-ttu-id="4fe9d-102">Obtener unidad</span><span class="sxs-lookup"><span data-stu-id="4fe9d-102">Get Drive</span></span>

<span data-ttu-id="4fe9d-103">Recupere las propiedades y relaciones de un recurso [Drive](../resources/drive.md).</span><span class="sxs-lookup"><span data-stu-id="4fe9d-103">Retrieve the properties and relationships of a [Drive](../resources/drive.md) resource.</span></span>

<span data-ttu-id="4fe9d-104">Un recurso Drive es el contenedor de nivel superior de un sistema de archivos, como bibliotecas de documentos de OneDrive o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-104">A Drive is the top-level container for a file system, such as OneDrive or SharePoint document libraries.</span></span>

## <a name="permissions"></a><span data-ttu-id="4fe9d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4fe9d-105">Permissions</span></span>

<span data-ttu-id="4fe9d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4fe9d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4fe9d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4fe9d-108">Permission type</span></span>      | <span data-ttu-id="4fe9d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4fe9d-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4fe9d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4fe9d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="4fe9d-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4fe9d-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="4fe9d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4fe9d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4fe9d-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4fe9d-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="4fe9d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4fe9d-114">Application</span></span> | <span data-ttu-id="4fe9d-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4fe9d-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="get-current-users-onedrive"></a><span data-ttu-id="4fe9d-116">Obtener el OneDrive del usuario actual</span><span class="sxs-lookup"><span data-stu-id="4fe9d-116">Get current user's OneDrive</span></span>

<span data-ttu-id="4fe9d-117">Se puede tener acceso a la unidad del usuario que ha iniciado sesión (si se usa la autenticación delegada) desde el singleton `me`.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-117">The signed in user's drive (when using delegated authentication) can be accessed from the `me` singleton.</span></span>

<span data-ttu-id="4fe9d-118">Si no se ha aprovisionado el OneDrive de un usuario pero este tiene una licencia para usar OneDrive, esta solicitud aprovisionará de forma automática la unidad del usuario, cuando se usa la autenticación delegada.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-118">If a user's OneDrive is not provisioned but the user has a license to use OneDrive, this request will automatically provision the user's drive, when using delegated authentication.</span></span>

### <a name="http-request"></a><span data-ttu-id="4fe9d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fe9d-119">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-default", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive
```

## <a name="get-a-users-onedrive"></a><span data-ttu-id="4fe9d-120">Obtener la cuenta de OneDrive de un usuario</span><span class="sxs-lookup"><span data-stu-id="4fe9d-120">Get a user's OneDrive</span></span>

<span data-ttu-id="4fe9d-121">Para obtener acceso al OneDrive o OneDrive para la Empresa de un usuario, la aplicación debe solicitar la relación **drive** en el recurso User.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-121">To access a user's OneDrive or OneDrive for Business, your app must request the **drive** relationship on the User resource.</span></span>

<span data-ttu-id="4fe9d-122">Si no se ha aprovisionado el OneDrive de un usuario pero este tiene una licencia para usar OneDrive, esta solicitud aprovisionará de forma automática la unidad del usuario, cuando se usa la autenticación delegada.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-122">If a user's OneDrive is not provisioned but the user has a license to use OneDrive, this request will automatically provision the user's drive, when using delegated authentication.</span></span>

### <a name="http-request"></a><span data-ttu-id="4fe9d-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fe9d-123">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-by-user", "scopes": "files.read.all", "tags": "service.graph" } -->

```http
GET /users/{idOrUserPrincipalName}/drive
```

### <a name="path-parameters"></a><span data-ttu-id="4fe9d-124">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="4fe9d-124">Path parameters</span></span>

| <span data-ttu-id="4fe9d-125">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="4fe9d-125">Parameter name</span></span> | <span data-ttu-id="4fe9d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4fe9d-126">Value</span></span>  | <span data-ttu-id="4fe9d-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fe9d-127">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="4fe9d-128">_idOrUserPrincipalName_</span><span class="sxs-lookup"><span data-stu-id="4fe9d-128">_idOrUserPrincipalName_</span></span>     | <span data-ttu-id="4fe9d-129">string</span><span class="sxs-lookup"><span data-stu-id="4fe9d-129">string</span></span> | <span data-ttu-id="4fe9d-130">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-130">Required.</span></span> <span data-ttu-id="4fe9d-131">El identificador del objeto de usuario que es el propietario del OneDrive.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-131">The identifier for the user object who owns the OneDrive.</span></span> |

## <a name="get-the-document-library-associated-with-a-group"></a><span data-ttu-id="4fe9d-132">Obtener la biblioteca de documentos asociada a un grupo</span><span class="sxs-lookup"><span data-stu-id="4fe9d-132">Get the document library associated with a group</span></span>

<span data-ttu-id="4fe9d-133">Para obtener acceso a la biblioteca de documentos predeterminada de un grupo, la aplicación solicita la relación **drive** en el grupo.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-133">To access a Group's default document library, your app requests the **drive** relationship on the Group.</span></span>

### <a name="http-request"></a><span data-ttu-id="4fe9d-134">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fe9d-134">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-by-group", "scopes": "group.read.all", "tags": "service.graph" } -->

```http
GET /groups/{groupId}/drive
```

### <a name="path-parameters"></a><span data-ttu-id="4fe9d-135">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="4fe9d-135">Path parameters</span></span>

| <span data-ttu-id="4fe9d-136">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="4fe9d-136">Parameter name</span></span> | <span data-ttu-id="4fe9d-137">Valor</span><span class="sxs-lookup"><span data-stu-id="4fe9d-137">Value</span></span>  | <span data-ttu-id="4fe9d-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fe9d-138">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="4fe9d-139">_groupId_</span><span class="sxs-lookup"><span data-stu-id="4fe9d-139">_groupId_</span></span>      | <span data-ttu-id="4fe9d-140">string</span><span class="sxs-lookup"><span data-stu-id="4fe9d-140">string</span></span> | <span data-ttu-id="4fe9d-141">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-141">Required.</span></span> <span data-ttu-id="4fe9d-142">El identificador del grupo que es el propietario de la biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-142">The identifier for the group which owns the document library.</span></span> |

## <a name="get-the-document-library-for-a-site"></a><span data-ttu-id="4fe9d-143">Obtener la biblioteca de documentos de un sitio</span><span class="sxs-lookup"><span data-stu-id="4fe9d-143">Get the document library for a site</span></span>

<span data-ttu-id="4fe9d-144">Para obtener acceso a la biblioteca de documentos predeterminada de un [sitio](../resources/site.md), la aplicación solicita la relación **drive** en el sitio.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-144">To access a [Site's](../resources/site.md) default document library, your app requests the **drive** relationship on the Site.</span></span>

### <a name="http-request"></a><span data-ttu-id="4fe9d-145">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fe9d-145">HTTP request</span></span>

```http
GET /sites/{siteId}/drive
```

### <a name="path-parameters"></a><span data-ttu-id="4fe9d-146">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="4fe9d-146">Path parameters</span></span>

| <span data-ttu-id="4fe9d-147">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="4fe9d-147">Parameter name</span></span> | <span data-ttu-id="4fe9d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="4fe9d-148">Value</span></span>  | <span data-ttu-id="4fe9d-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fe9d-149">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="4fe9d-150">_siteId_</span><span class="sxs-lookup"><span data-stu-id="4fe9d-150">_siteId_</span></span>       | <span data-ttu-id="4fe9d-151">string</span><span class="sxs-lookup"><span data-stu-id="4fe9d-151">string</span></span> | <span data-ttu-id="4fe9d-152">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-152">Required.</span></span> <span data-ttu-id="4fe9d-153">El identificador del sitio que contiene la biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-153">The identifier for the site that contains the document library.</span></span> |

## <a name="get-a-drive-by-id"></a><span data-ttu-id="4fe9d-154">Obtener una unidad por su identificador</span><span class="sxs-lookup"><span data-stu-id="4fe9d-154">Get a drive by ID</span></span>

<span data-ttu-id="4fe9d-155">Si tiene el identificador único de una unidad, puede tener acceso a ella directamente desde la colección de unidades de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-155">If you have the unique identifier for a drive, you can access it directly from the top-level drives collection.</span></span>

### <a name="http-request"></a><span data-ttu-id="4fe9d-156">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4fe9d-156">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-by-id", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}
```

### <a name="path-parameters"></a><span data-ttu-id="4fe9d-157">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="4fe9d-157">Path parameters</span></span>

| <span data-ttu-id="4fe9d-158">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="4fe9d-158">Parameter name</span></span> | <span data-ttu-id="4fe9d-159">Valor</span><span class="sxs-lookup"><span data-stu-id="4fe9d-159">Value</span></span>  | <span data-ttu-id="4fe9d-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fe9d-160">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="4fe9d-161">_driveId_</span><span class="sxs-lookup"><span data-stu-id="4fe9d-161">_driveId_</span></span>      | <span data-ttu-id="4fe9d-162">string</span><span class="sxs-lookup"><span data-stu-id="4fe9d-162">string</span></span> | <span data-ttu-id="4fe9d-163">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-163">Required.</span></span> <span data-ttu-id="4fe9d-164">El identificador de la unidad que se ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-164">The identifier for the drive requested.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="4fe9d-165">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4fe9d-165">Optional query parameters</span></span>

<span data-ttu-id="4fe9d-166">Este método admite el [parámetro de consulta $select][odata-query-parameters] para dar forma a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-166">These method support the [$select query parameter][odata-query-parameters] to shape the response.</span></span>

## <a name="http-response"></a><span data-ttu-id="4fe9d-167">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="4fe9d-167">HTTP response</span></span>

<span data-ttu-id="4fe9d-168">Cada uno de estos métodos devuelve un [recurso Drive][drive-resource] para la unidad coincidente en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-168">Each of these methods returns a [Drive resource][drive-resource] for the matching drive in the response body.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.drive", "truncated": true, "name": ["get-drive-by-id", "get-drive-by-group", "get-drive-by-user", "get-drive-default"] } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "b!t18F8ybsHUq1z3LTz8xvZqP8zaSWjkFNhsME-Fepo75dTf9vQKfeRblBZjoSQrd7",
    "driveType": "business",
    "owner": {
        "user": {
            "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
            "displayName": "Ryan Gregg"
        }
    },
    "quota": {
        "deleted": 256938,
        "remaining": 1099447353539,
        "state": "normal",
        "total": 1099511627776
    }
}
```

### <a name="error-response-codes"></a><span data-ttu-id="4fe9d-169">Códigos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="4fe9d-169">Error response codes</span></span>

<span data-ttu-id="4fe9d-170">Si la unidad no existe y no se puede aprovisionar automáticamente (al usar la autenticación delegada) se devolverá una respuesta `HTTP 404`.</span><span class="sxs-lookup"><span data-stu-id="4fe9d-170">If the drive does not exist and cannot be provisioned automatically (when using delegated authentication) an `HTTP 404` response will be returned.</span></span>

[drive-resource]: ../resources/drive.md
[odata-query-parameters]: /graph/query-parameters

<!-- {
  "type": "#page.annotation",
  "description": "Get metadata for a OneDrive, OneDrive for Business, or Office 365 group drive",
  "keywords": "drive,onedrive,default drive,group drive",
  "section": "documentation",
  "suppressions": [
      "Warning: /api-reference/v1.0/api/drive-get.md:
        Unable to map some markdown elements into schema.
            Unmapped methods:
        get-drive-default, get-drive-by-user, get-drive-by-group, get-drive-by-id
            Unmapped tables:
        Permissions - AuthScopes, Path parameters - PathParameters, Path parameters - PathParameters, Path parameters - PathParameters, Path parameters - PathParameters"
  ],
  "tocPath": "Drives/Get drive"
} -->