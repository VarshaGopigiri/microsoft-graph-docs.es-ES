---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Descargue una versión anterior
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: b0d8125f86459caa0fd9fd863a1a4f280e0ad89e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980114"
---
# <a name="download-contents-of-a-driveitemversion-resource-preview"></a><span data-ttu-id="8df0a-102">Descargar contenido de un recurso DriveItemVersion (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="8df0a-102">Download contents of a DriveItemVersion resource (preview)</span></span>

> <span data-ttu-id="8df0a-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8df0a-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8df0a-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8df0a-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8df0a-105">Recuperar el contenido de una versión específica de un [driveItem](../resources/driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="8df0a-105">Retrieve the contents of a specific version of a [driveItem](../resources/driveitem.md).</span></span> 

><span data-ttu-id="8df0a-106">**Nota:** No se admite la obtención del contenido de la versión actual.</span><span class="sxs-lookup"><span data-stu-id="8df0a-106">**Note:** Getting the content of the current version is not supported.</span></span> <span data-ttu-id="8df0a-107">En su lugar, use el [extremo de contenido driveItem](driveitem-get-content.md).</span><span class="sxs-lookup"><span data-stu-id="8df0a-107">Instead, use the [driveItem content endpoint](driveitem-get-content.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="8df0a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="8df0a-108">Permissions</span></span>

<span data-ttu-id="8df0a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8df0a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8df0a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8df0a-111">Permission type</span></span>      | <span data-ttu-id="8df0a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8df0a-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8df0a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8df0a-113">Delegated (work or school account)</span></span> | <span data-ttu-id="8df0a-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8df0a-114">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="8df0a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8df0a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8df0a-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8df0a-116">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="8df0a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8df0a-117">Application</span></span> | <span data-ttu-id="8df0a-118">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8df0a-118">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |


## <a name="http-request"></a><span data-ttu-id="8df0a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8df0a-119">HTTP request</span></span>

<!-- { "blockType": "ignored"} -->

```http
GET /drives/{drive-id}/items/{item-id}/versions/{version-id}/content
GET /groups/{group-id}/drive/{item-id}/versions/{version-id}/content
GET /me/drive/items/{item-id}/versions/{version-id}/content
GET /sites/{site-id}/drive/items/{item-id}/versions/{version-id}/content
GET /users/{user-id}/drive/items/{item-id}/versions/{version-id}/content
```

## <a name="response"></a><span data-ttu-id="8df0a-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8df0a-120">Response</span></span>

<span data-ttu-id="8df0a-121">Devuelve una respuesta `302 Found` que redirige a una dirección URL de descarga autenticada previamente para los bytes del archivo.</span><span class="sxs-lookup"><span data-stu-id="8df0a-121">Returns a `302 Found` response redirecting to a pre-authenticated download URL for the bytes of the file.</span></span>

<span data-ttu-id="8df0a-p104">Para descargar el contenido del archivo, la aplicación tendrá que seguir el encabezado `Location` de la respuesta. Muchas bibliotecas de cliente HTTP seguirán de forma automática el redireccionamiento 302 e iniciarán la descarga del archivo de forma inmediata.</span><span class="sxs-lookup"><span data-stu-id="8df0a-p104">To download the contents of the file your application will need to follow the `Location` header in the response. Many HTTP client libraries will automatically follow the 302 redirection and start downloading the file immedately.</span></span>

<span data-ttu-id="8df0a-124">Las URL de descarga autenticadas previamente solo son válidas durante un breve período de tiempo (unos minutos) y no requieren un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="8df0a-124">Pre-authenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header to download.</span></span>

## <a name="example"></a><span data-ttu-id="8df0a-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8df0a-125">Example</span></span>

<span data-ttu-id="8df0a-126">Este ejemplo recupera una versión de un archivo en la unidad del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="8df0a-126">This example retrieves a version of a file in the current user's drive.</span></span>

### <a name="request"></a><span data-ttu-id="8df0a-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8df0a-127">Request</span></span>

<!-- { "blockType": "request", "name": "get-version-contents", "scopes": "files.read", "tags": "service.graph" } -->

```http
GET /me/drive/items/{item-id}/versions/{version-id}/content
```

### <a name="response"></a><span data-ttu-id="8df0a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8df0a-128">Response</span></span>

<span data-ttu-id="8df0a-129">Esto devuelve una redirección donde se puede descargar el contenido de la versión.</span><span class="sxs-lookup"><span data-stu-id="8df0a-129">This returns a redirect to where the contents of the version can be downloaded.</span></span>

<!-- { "blockType": "response", "isEmpty": true  } -->

```http
HTTP/1.1 302 Redirect
Location: https://onedrive.com/34FF49D6...
```


## <a name="remarks"></a><span data-ttu-id="8df0a-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8df0a-130">Remarks</span></span>

<span data-ttu-id="8df0a-131">OneDrive no conserva todos los metadatos de las versiones anteriores de un archivo.</span><span class="sxs-lookup"><span data-stu-id="8df0a-131">OneDrive does not preserve the complete metadata for previous versions of a file.</span></span>

<span data-ttu-id="8df0a-132">Cuando la aplicación recupera la lista de versiones disponibles para un archivo, se devuelve un recurso de [driveItemVersion](../resources/driveitemversion.md) que proporciona la información disponible sobre la versión específica.</span><span class="sxs-lookup"><span data-stu-id="8df0a-132">When your app retrieves the list of available versions for a file, a [driveItemVersion](../resources/driveitemversion.md) resource is returned that provides the available information about the specific version.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "List, review, and download previous versions of a driveItem",
  "keywords": "version, version history, versions",
  "section": "documentation",
  "tocPath": "Items/Version history"
} -->
