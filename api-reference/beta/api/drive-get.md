---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Obtener unidad
ms.openlocfilehash: 620797ec453f9456f6ea6a6dcb90d396f43a7a4b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085897"
---
# <a name="get-drive"></a><span data-ttu-id="00a32-102">Obtener unidad</span><span class="sxs-lookup"><span data-stu-id="00a32-102">Get Drive</span></span>

> <span data-ttu-id="00a32-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="00a32-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="00a32-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="00a32-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="00a32-105">Recupere las propiedades y relaciones de un recurso [Drive](../resources/drive.md).</span><span class="sxs-lookup"><span data-stu-id="00a32-105">Retrieve the properties and relationships of a [Drive](../resources/drive.md) resource.</span></span>

<span data-ttu-id="00a32-106">Un recurso Drive es el contenedor de nivel superior de un sistema de archivos, como bibliotecas de documentos de OneDrive o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="00a32-106">A Drive is the top-level container for a file system, such as OneDrive or SharePoint document libraries.</span></span>

## <a name="permissions"></a><span data-ttu-id="00a32-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="00a32-107">Permissions</span></span>

<span data-ttu-id="00a32-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="00a32-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="00a32-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00a32-110">Permission type</span></span>      | <span data-ttu-id="00a32-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00a32-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="00a32-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00a32-112">Delegated (work or school account)</span></span> | <span data-ttu-id="00a32-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00a32-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="00a32-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00a32-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="00a32-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00a32-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="00a32-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00a32-116">Application</span></span> | <span data-ttu-id="00a32-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="00a32-117">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="get-current-users-onedrive"></a><span data-ttu-id="00a32-118">Obtener el OneDrive del usuario actual</span><span class="sxs-lookup"><span data-stu-id="00a32-118">Get current user's OneDrive</span></span>

<span data-ttu-id="00a32-119">Se puede tener acceso a la unidad del usuario que ha iniciado sesión (si se usa la autenticación delegada) desde el singleton `me`.</span><span class="sxs-lookup"><span data-stu-id="00a32-119">The signed in user's drive (when using delegated authentication) can be accessed from the `me` singleton.</span></span>

<span data-ttu-id="00a32-120">Si no se ha aprovisionado el OneDrive de un usuario pero este tiene una licencia para usar OneDrive, esta solicitud aprovisionará de forma automática la unidad del usuario, cuando se usa la autenticación delegada.</span><span class="sxs-lookup"><span data-stu-id="00a32-120">If a user's OneDrive is not provisioned but the user has a license to use OneDrive, this request will automatically provision the user's drive, when using delegated authentication.</span></span>

### <a name="http-request"></a><span data-ttu-id="00a32-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00a32-121">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-default", "scopes": "files.read" } -->

```http
GET /me/drive
```

## <a name="get-a-users-onedrive"></a><span data-ttu-id="00a32-122">Obtener la cuenta de OneDrive de un usuario</span><span class="sxs-lookup"><span data-stu-id="00a32-122">Get a user's OneDrive</span></span>

<span data-ttu-id="00a32-123">Para obtener acceso al OneDrive o OneDrive para la Empresa de un usuario, la aplicación debe solicitar la relación **drive** en el recurso User.</span><span class="sxs-lookup"><span data-stu-id="00a32-123">To access a user's OneDrive or OneDrive for Business, your app must request the **drive** relationship on the User resource.</span></span>

<span data-ttu-id="00a32-124">Si no se ha aprovisionado el OneDrive de un usuario pero este tiene una licencia para usar OneDrive, esta solicitud aprovisionará de forma automática la unidad del usuario, cuando se usa la autenticación delegada.</span><span class="sxs-lookup"><span data-stu-id="00a32-124">If a user's OneDrive is not provisioned but the user has a license to use OneDrive, this request will automatically provision the user's drive, when using delegated authentication.</span></span>

### <a name="http-request"></a><span data-ttu-id="00a32-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00a32-125">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-by-user", "scopes": "files.read.all" } -->

```http
GET /users/{idOrUserPrincipalName}/drive
```

### <a name="path-parameters"></a><span data-ttu-id="00a32-126">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="00a32-126">Path parameters</span></span>

| <span data-ttu-id="00a32-127">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="00a32-127">Parameter name</span></span> | <span data-ttu-id="00a32-128">Valor</span><span class="sxs-lookup"><span data-stu-id="00a32-128">Value</span></span>  | <span data-ttu-id="00a32-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="00a32-129">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="00a32-130">_idOrUserPrincipalName_</span><span class="sxs-lookup"><span data-stu-id="00a32-130">_idOrUserPrincipalName_</span></span>     | <span data-ttu-id="00a32-131">string</span><span class="sxs-lookup"><span data-stu-id="00a32-131">string</span></span> | <span data-ttu-id="00a32-132">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00a32-132">Required.</span></span> <span data-ttu-id="00a32-133">El identificador del objeto de usuario que es el propietario del OneDrive.</span><span class="sxs-lookup"><span data-stu-id="00a32-133">The identifier for the user object who owns the OneDrive.</span></span> |

## <a name="get-the-document-library-associated-with-a-group"></a><span data-ttu-id="00a32-134">Obtener la biblioteca de documentos asociada a un grupo</span><span class="sxs-lookup"><span data-stu-id="00a32-134">Get the document library associated with a group</span></span>

<span data-ttu-id="00a32-135">Para obtener acceso a la biblioteca de documentos predeterminada de un grupo, la aplicación solicita la relación **drive** en el grupo.</span><span class="sxs-lookup"><span data-stu-id="00a32-135">To access a Group's default document library, your app requests the **drive** relationship on the Group.</span></span>

### <a name="http-request"></a><span data-ttu-id="00a32-136">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00a32-136">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-by-group", "scopes": "group.read.all" } -->

```http
GET /groups/{groupId}/drive
```

### <a name="path-parameters"></a><span data-ttu-id="00a32-137">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="00a32-137">Path parameters</span></span>

| <span data-ttu-id="00a32-138">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="00a32-138">Parameter name</span></span> | <span data-ttu-id="00a32-139">Valor</span><span class="sxs-lookup"><span data-stu-id="00a32-139">Value</span></span>  | <span data-ttu-id="00a32-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="00a32-140">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="00a32-141">_groupId_</span><span class="sxs-lookup"><span data-stu-id="00a32-141">_groupId_</span></span>      | <span data-ttu-id="00a32-142">string</span><span class="sxs-lookup"><span data-stu-id="00a32-142">string</span></span> | <span data-ttu-id="00a32-143">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00a32-143">Required.</span></span> <span data-ttu-id="00a32-144">El identificador del grupo que es el propietario de la biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="00a32-144">The identifier for the group which owns the document library.</span></span> |

## <a name="get-the-document-library-for-a-site"></a><span data-ttu-id="00a32-145">Obtener la biblioteca de documentos de un sitio</span><span class="sxs-lookup"><span data-stu-id="00a32-145">Get the document library for a site</span></span>

<span data-ttu-id="00a32-146">Para obtener acceso a la biblioteca de documentos predeterminada de un [sitio](../resources/site.md), la aplicación solicita la relación **drive** en el sitio.</span><span class="sxs-lookup"><span data-stu-id="00a32-146">To access a [Site's](../resources/site.md) default document library, your app requests the **drive** relationship on the Site.</span></span>

### <a name="http-request"></a><span data-ttu-id="00a32-147">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00a32-147">HTTP request</span></span>

```http
GET /sites/{siteId}/drive
```

### <a name="path-parameters"></a><span data-ttu-id="00a32-148">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="00a32-148">Path parameters</span></span>

| <span data-ttu-id="00a32-149">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="00a32-149">Parameter name</span></span> | <span data-ttu-id="00a32-150">Valor</span><span class="sxs-lookup"><span data-stu-id="00a32-150">Value</span></span>  | <span data-ttu-id="00a32-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="00a32-151">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="00a32-152">_siteId_</span><span class="sxs-lookup"><span data-stu-id="00a32-152">_siteId_</span></span>       | <span data-ttu-id="00a32-153">string</span><span class="sxs-lookup"><span data-stu-id="00a32-153">string</span></span> | <span data-ttu-id="00a32-154">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00a32-154">Required.</span></span> <span data-ttu-id="00a32-155">El identificador del sitio que contiene la biblioteca de documentos.</span><span class="sxs-lookup"><span data-stu-id="00a32-155">The identifier for the site that contains the document library.</span></span> |

## <a name="get-a-drive-by-id"></a><span data-ttu-id="00a32-156">Obtener una unidad por su identificador</span><span class="sxs-lookup"><span data-stu-id="00a32-156">Get a drive by ID</span></span>

<span data-ttu-id="00a32-157">Si tiene el identificador único de una unidad, puede tener acceso a ella directamente desde la colección de unidades de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="00a32-157">If you have the unique identifier for a drive, you can access it directly from the top-level drives collection.</span></span>

### <a name="http-request"></a><span data-ttu-id="00a32-158">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00a32-158">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-drive-by-id", "scopes": "files.read" } -->

```http
GET /drives/{driveId}
```

### <a name="path-parameters"></a><span data-ttu-id="00a32-159">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="00a32-159">Path parameters</span></span>

| <span data-ttu-id="00a32-160">Nombre del parámetro</span><span class="sxs-lookup"><span data-stu-id="00a32-160">Parameter name</span></span> | <span data-ttu-id="00a32-161">Valor</span><span class="sxs-lookup"><span data-stu-id="00a32-161">Value</span></span>  | <span data-ttu-id="00a32-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="00a32-162">Description</span></span>                                       |
|:---------------|:-------|:--------------------------------------------------|
| <span data-ttu-id="00a32-163">_driveId_</span><span class="sxs-lookup"><span data-stu-id="00a32-163">_driveId_</span></span>      | <span data-ttu-id="00a32-164">string</span><span class="sxs-lookup"><span data-stu-id="00a32-164">string</span></span> | <span data-ttu-id="00a32-165">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00a32-165">Required.</span></span> <span data-ttu-id="00a32-166">El identificador de la unidad que se ha solicitado.</span><span class="sxs-lookup"><span data-stu-id="00a32-166">The identifier for the drive requested.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="00a32-167">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="00a32-167">Optional query parameters</span></span>

<span data-ttu-id="00a32-168">Este método admite el [parámetro de consulta $select][odata-query-parameters] para dar forma a la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00a32-168">These method support the [$select query parameter][odata-query-parameters] to shape the response.</span></span>

## <a name="http-response"></a><span data-ttu-id="00a32-169">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="00a32-169">HTTP response</span></span>

<span data-ttu-id="00a32-170">Cada uno de estos métodos devuelve un [recurso Drive][drive-resource] para la unidad coincidente en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00a32-170">Each of these methods returns a [Drive resource][drive-resource] for the matching drive in the response body.</span></span>

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

### <a name="error-response-codes"></a><span data-ttu-id="00a32-171">Códigos de respuesta de error</span><span class="sxs-lookup"><span data-stu-id="00a32-171">Error response codes</span></span>

<span data-ttu-id="00a32-172">Si la unidad no existe y no se puede aprovisionar automáticamente (al usar la autenticación delegada) se devolverá una respuesta `HTTP 404`.</span><span class="sxs-lookup"><span data-stu-id="00a32-172">If the drive does not exist and cannot be provisioned automatically (when using delegated authentication) an `HTTP 404` response will be returned.</span></span>

[drive-resource]: ../resources/drive.md
[odata-query-parameters]: /graph/query-parameters

<!-- {
  "type": "#page.annotation",
  "description": "Get metadata for a OneDrive, OneDrive for Business, or Office 365 group drive",
  "keywords": "drive,onedrive,default drive,group drive",
  "section": "documentation",
  "tocPath": "Drives/Get drive"
} -->
