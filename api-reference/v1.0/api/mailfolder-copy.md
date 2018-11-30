---
title: 'mailFolder: copy'
description: Copia un objeto mailfolder y su contenido en otro objeto mailfolder.
ms.openlocfilehash: 8cee2ad91fe40a9e9ef40c3a4662b76e71be1ccd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029122"
---
# <a name="mailfolder-copy"></a><span data-ttu-id="672a8-103">mailFolder: copy</span><span class="sxs-lookup"><span data-stu-id="672a8-103">mailFolder: copy</span></span>

<span data-ttu-id="672a8-104">Copia un objeto mailfolder y su contenido en otro objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="672a8-104">Copy a mailfolder and its contents to another mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="672a8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="672a8-105">Permissions</span></span>

<span data-ttu-id="672a8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="672a8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="672a8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="672a8-108">Permission type</span></span> | <span data-ttu-id="672a8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="672a8-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="672a8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="672a8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="672a8-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="672a8-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="672a8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="672a8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="672a8-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="672a8-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="672a8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="672a8-114">Application</span></span> | <span data-ttu-id="672a8-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="672a8-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="672a8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="672a8-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="672a8-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="672a8-117">Request headers</span></span>
| <span data-ttu-id="672a8-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="672a8-118">Header</span></span> | <span data-ttu-id="672a8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="672a8-119">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="672a8-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="672a8-120">Authorization</span></span> | <span data-ttu-id="672a8-121">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="672a8-121"></span></span> <span data-ttu-id="672a8-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="672a8-122">Required.</span></span> |
| <span data-ttu-id="672a8-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="672a8-123">Content-Type</span></span> | <span data-ttu-id="672a8-124">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="672a8-124"></span></span> <span data-ttu-id="672a8-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="672a8-125">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="672a8-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="672a8-126">Request body</span></span>

<span data-ttu-id="672a8-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="672a8-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="672a8-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="672a8-128">Parameter</span></span> | <span data-ttu-id="672a8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="672a8-129">Type</span></span> | <span data-ttu-id="672a8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="672a8-130">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="672a8-131">destinationId</span><span class="sxs-lookup"><span data-stu-id="672a8-131">destinationId</span></span>|<span data-ttu-id="672a8-132">String</span><span class="sxs-lookup"><span data-stu-id="672a8-132">String</span></span>|<span data-ttu-id="672a8-133">El identificador de la carpeta, o un nombre de carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="672a8-133">The folder ID, or a well-known folder name.</span></span> <span data-ttu-id="672a8-134">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="672a8-134">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="672a8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="672a8-135">Response</span></span>

<span data-ttu-id="672a8-136">Si tiene éxito, este método devuelve `200 OK` código de respuesta y un recurso de [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="672a8-136">If successful, this method returns `200 OK` response code and a [mailFolder](../resources/mailfolder.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="672a8-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="672a8-137">Example</span></span>

<span data-ttu-id="672a8-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="672a8-138">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="672a8-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="672a8-139">Request</span></span>
<span data-ttu-id="672a8-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="672a8-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="672a8-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="672a8-141">Response</span></span>

<span data-ttu-id="672a8-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="672a8-142">Here is an example of the response.</span></span>

> <span data-ttu-id="672a8-143">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="672a8-143">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="672a8-144">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="672a8-144">All the properties will be returned from an actual call.</span></span>
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