---
title: 'mailFolder: copy'
description: Copia un objeto mailfolder y su contenido en otro objeto mailfolder.
author: angelgolfer-ms
ms.openlocfilehash: 74a9c072089f3bd76439ce0fa7bd15f28f8cae2a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335626"
---
# <a name="mailfolder-copy"></a><span data-ttu-id="03384-103">mailFolder: copy</span><span class="sxs-lookup"><span data-stu-id="03384-103">mailFolder: copy</span></span>

> <span data-ttu-id="03384-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="03384-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="03384-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="03384-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="03384-106">Copia un objeto mailfolder y su contenido en otro objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="03384-106">Copy a mailfolder and its contents to another mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="03384-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="03384-107">Permissions</span></span>

<span data-ttu-id="03384-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03384-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="03384-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03384-110">Permission type</span></span> | <span data-ttu-id="03384-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03384-111">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="03384-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03384-112">Delegated (work or school account)</span></span> | <span data-ttu-id="03384-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03384-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="03384-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03384-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="03384-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03384-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="03384-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03384-116">Application</span></span> | <span data-ttu-id="03384-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03384-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="03384-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03384-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="03384-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03384-119">Request headers</span></span>

| <span data-ttu-id="03384-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03384-120">Header</span></span> | <span data-ttu-id="03384-121">Valor</span><span class="sxs-lookup"><span data-stu-id="03384-121">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="03384-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="03384-122">Authorization</span></span> | <span data-ttu-id="03384-123">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="03384-123"></span></span> <span data-ttu-id="03384-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03384-124">Required.</span></span> |
| <span data-ttu-id="03384-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="03384-125">Content-Type</span></span> | <span data-ttu-id="03384-126">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="03384-126"></span></span> <span data-ttu-id="03384-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03384-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="03384-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03384-128">Request body</span></span>

<span data-ttu-id="03384-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="03384-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="03384-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="03384-130">Parameter</span></span> | <span data-ttu-id="03384-131">Type</span><span class="sxs-lookup"><span data-stu-id="03384-131">Type</span></span> | <span data-ttu-id="03384-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="03384-132">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="03384-133">destinationId</span><span class="sxs-lookup"><span data-stu-id="03384-133">destinationId</span></span>|<span data-ttu-id="03384-134">String</span><span class="sxs-lookup"><span data-stu-id="03384-134">String</span></span>|<span data-ttu-id="03384-135">El identificador de la carpeta, o un nombre de carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="03384-135">The folder ID, or a well-known folder name.</span></span> <span data-ttu-id="03384-136">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="03384-136">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="03384-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03384-137">Response</span></span>

<span data-ttu-id="03384-138">Si tiene éxito, este método devuelve `200 OK` código de respuesta y un recurso de [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03384-138">If successful, this method returns `200 OK` response code and a [mailFolder](../resources/mailfolder.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03384-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03384-139">Example</span></span>

<span data-ttu-id="03384-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="03384-140">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="03384-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03384-141">Request</span></span>

<span data-ttu-id="03384-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03384-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "mailfolder_copy"
}-->

```http
POST https://graph.microsoft.com/beta/me/mailFolders/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="03384-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03384-143">Response</span></span>

<span data-ttu-id="03384-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03384-144">Here is an example of the response.</span></span>

> <span data-ttu-id="03384-145">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="03384-145">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="03384-146">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03384-146">All the properties will be returned from an actual call.</span></span>

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
