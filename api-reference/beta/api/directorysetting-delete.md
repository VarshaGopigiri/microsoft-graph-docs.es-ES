---
title: Eliminar una configuración de Active directory
description: Eliminar una configuración de Active directory.
ms.openlocfilehash: 442c4f0433dd1595708b478f527bf881a055713d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088130"
---
# <a name="delete-a-directory-setting"></a><span data-ttu-id="ddbcc-103">Eliminar una configuración de Active directory</span><span class="sxs-lookup"><span data-stu-id="ddbcc-103">Delete a directory setting</span></span>

> <span data-ttu-id="ddbcc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ddbcc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ddbcc-106">Eliminar una configuración de Active directory.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-106">Delete a directory setting.</span></span>

> <span data-ttu-id="ddbcc-107">**Nota**: la versión de /beta de esta API es sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-107">**Note**: The /beta version of this API is only applies to groups.</span></span> <span data-ttu-id="ddbcc-108">Se ha cambiado la versión /v1.0 de esta API para *Eliminar groupSettings*.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-108">The /v1.0 version of this API has been renamed to *Delete groupSettings*.</span></span>

## <a name="permissions"></a><span data-ttu-id="ddbcc-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ddbcc-109">Permissions</span></span>
<span data-ttu-id="ddbcc-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ddbcc-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ddbcc-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ddbcc-112">Permission type</span></span>      | <span data-ttu-id="ddbcc-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ddbcc-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ddbcc-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ddbcc-114">Delegated (work or school account)</span></span> | <span data-ttu-id="ddbcc-115">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ddbcc-115">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ddbcc-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ddbcc-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ddbcc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-117">Not supported.</span></span>    |
|<span data-ttu-id="ddbcc-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ddbcc-118">Application</span></span> | <span data-ttu-id="ddbcc-119">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ddbcc-119">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ddbcc-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ddbcc-120">HTTP request</span></span>
<span data-ttu-id="ddbcc-121"><!-- { "blockType": "ignored" } -->Eliminar un todo el inquilino específico o configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="ddbcc-121"><!-- { "blockType": "ignored" } --> Delete a specific tenant-wide or group setting</span></span>
```http
DELETE /settings/{id}
DELETE /groups/{id}/settings/{id}

```
## <a name="request-headers"></a><span data-ttu-id="ddbcc-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ddbcc-122">Request headers</span></span>
| <span data-ttu-id="ddbcc-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="ddbcc-123">Name</span></span>       | <span data-ttu-id="ddbcc-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddbcc-124">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ddbcc-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="ddbcc-125">Authorization</span></span>  | <span data-ttu-id="ddbcc-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ddbcc-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ddbcc-128">Request body</span></span>
<span data-ttu-id="ddbcc-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ddbcc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddbcc-130">Response</span></span>

<span data-ttu-id="ddbcc-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ddbcc-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ddbcc-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ddbcc-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ddbcc-134">Request</span></span>
<span data-ttu-id="ddbcc-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ddbcc-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_directorysetting"
}-->
```http
DELETE https://graph.microsoft.com/beta/settings/{id}
```
##### <a name="response"></a><span data-ttu-id="ddbcc-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ddbcc-136">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete directorySetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->