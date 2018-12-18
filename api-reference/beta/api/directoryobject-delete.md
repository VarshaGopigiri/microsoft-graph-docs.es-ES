---
title: Delete directoryObject
description: Eliminar directoryObject.
author: lleonard-msft
ms.openlocfilehash: f53ffc488529c2af4b566ada52f213d1fc132c60
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361414"
---
# <a name="delete-directoryobject"></a><span data-ttu-id="806d1-103">Delete directoryObject</span><span class="sxs-lookup"><span data-stu-id="806d1-103">Delete directoryObject</span></span>

> <span data-ttu-id="806d1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="806d1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="806d1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="806d1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="806d1-106">Eliminar directoryObject.</span><span class="sxs-lookup"><span data-stu-id="806d1-106">Delete directoryObject.</span></span>
## <a name="permissions"></a><span data-ttu-id="806d1-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="806d1-107">Permissions</span></span>
<span data-ttu-id="806d1-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="806d1-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="806d1-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="806d1-110">Permission type</span></span>      | <span data-ttu-id="806d1-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="806d1-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="806d1-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="806d1-112">Delegated (work or school account)</span></span> | <span data-ttu-id="806d1-113">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="806d1-113">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="806d1-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="806d1-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="806d1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="806d1-115">Not supported.</span></span>    |
|<span data-ttu-id="806d1-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="806d1-116">Application</span></span> | <span data-ttu-id="806d1-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="806d1-117">Not supported.</span></span> |

<span data-ttu-id="806d1-118">**Nota:** Los usuarios, grupos y contactos son tipos de objeto de Active directory.</span><span class="sxs-lookup"><span data-stu-id="806d1-118">**NOTE:** Users, groups, and contacts are types of directory object.</span></span> <span data-ttu-id="806d1-119">Como resultado, si necesita eliminar los usuarios, el permiso siguiente puede y debe usarse: User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="806d1-119">As a result,if you need to delete users, the following permission can and should be used: User.ReadWrite.All</span></span>
## <a name="http-request"></a><span data-ttu-id="806d1-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="806d1-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /directoryObjects/{id}

```
## <a name="request-headers"></a><span data-ttu-id="806d1-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="806d1-121">Request headers</span></span>
| <span data-ttu-id="806d1-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="806d1-122">Name</span></span>       | <span data-ttu-id="806d1-123">Type</span><span class="sxs-lookup"><span data-stu-id="806d1-123">Type</span></span> | <span data-ttu-id="806d1-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="806d1-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="806d1-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="806d1-125">Authorization</span></span>  | <span data-ttu-id="806d1-126">string</span><span class="sxs-lookup"><span data-stu-id="806d1-126">string</span></span>  | <span data-ttu-id="806d1-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="806d1-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="806d1-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="806d1-129">Request body</span></span>
<span data-ttu-id="806d1-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="806d1-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="806d1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="806d1-131">Response</span></span>

<span data-ttu-id="806d1-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="806d1-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="806d1-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="806d1-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="806d1-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="806d1-135">Request</span></span>
<span data-ttu-id="806d1-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="806d1-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_directoryobject"
}-->
```http
DELETE https://graph.microsoft.com/beta/directoryObject/{id}
```
##### <a name="response"></a><span data-ttu-id="806d1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="806d1-137">Response</span></span>
<span data-ttu-id="806d1-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="806d1-138">Here is an example of the response.</span></span> 
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
  "description": "Delete directoryObject",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->