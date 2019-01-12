---
title: 'mailFolder: copy'
description: Copia un objeto mailfolder y su contenido en otro objeto mailfolder.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 37160f5b6f62ce29d605e84a93a7748f426bd240
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940739"
---
# <a name="mailfolder-copy"></a><span data-ttu-id="c84f2-103">mailFolder: copy</span><span class="sxs-lookup"><span data-stu-id="c84f2-103">mailFolder: copy</span></span>

<span data-ttu-id="c84f2-104">Copia un objeto mailfolder y su contenido en otro objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="c84f2-104">Copy a mailfolder and its contents to another mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="c84f2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c84f2-105">Permissions</span></span>

<span data-ttu-id="c84f2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c84f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c84f2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c84f2-108">Permission type</span></span> | <span data-ttu-id="c84f2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c84f2-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="c84f2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c84f2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c84f2-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c84f2-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c84f2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c84f2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c84f2-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c84f2-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="c84f2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c84f2-114">Application</span></span> | <span data-ttu-id="c84f2-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c84f2-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c84f2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c84f2-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="c84f2-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c84f2-117">Request headers</span></span>
| <span data-ttu-id="c84f2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c84f2-118">Header</span></span> | <span data-ttu-id="c84f2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c84f2-119">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="c84f2-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c84f2-120">Authorization</span></span> | <span data-ttu-id="c84f2-121">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="c84f2-121"></span></span> <span data-ttu-id="c84f2-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c84f2-122">Required.</span></span> |
| <span data-ttu-id="c84f2-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c84f2-123">Content-Type</span></span> | <span data-ttu-id="c84f2-124">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="c84f2-124"></span></span> <span data-ttu-id="c84f2-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c84f2-125">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c84f2-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c84f2-126">Request body</span></span>

<span data-ttu-id="c84f2-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c84f2-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c84f2-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c84f2-128">Parameter</span></span> | <span data-ttu-id="c84f2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c84f2-129">Type</span></span> | <span data-ttu-id="c84f2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c84f2-130">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="c84f2-131">destinationId</span><span class="sxs-lookup"><span data-stu-id="c84f2-131">destinationId</span></span>|<span data-ttu-id="c84f2-132">String</span><span class="sxs-lookup"><span data-stu-id="c84f2-132">String</span></span>|<span data-ttu-id="c84f2-133">El identificador de la carpeta, o un nombre de carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="c84f2-133">The folder ID, or a well-known folder name.</span></span> <span data-ttu-id="c84f2-134">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="c84f2-134">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="c84f2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c84f2-135">Response</span></span>

<span data-ttu-id="c84f2-136">Si tiene éxito, este método devuelve `200 OK` código de respuesta y un recurso de [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c84f2-136">If successful, this method returns `200 OK` response code and a [mailFolder](../resources/mailfolder.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c84f2-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c84f2-137">Example</span></span>

<span data-ttu-id="c84f2-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c84f2-138">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="c84f2-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c84f2-139">Request</span></span>
<span data-ttu-id="c84f2-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c84f2-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "mailfolder_copy"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="c84f2-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c84f2-141">Response</span></span>

<span data-ttu-id="c84f2-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c84f2-142">Here is an example of the response.</span></span>

> <span data-ttu-id="c84f2-143">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c84f2-143">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c84f2-144">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c84f2-144">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailFolder: copy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
