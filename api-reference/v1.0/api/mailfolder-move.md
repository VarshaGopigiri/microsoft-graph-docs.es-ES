---
title: 'mailFolder: move'
description: Mueve un objeto mailfolder y su contenido a otro objeto mailfolder.
ms.openlocfilehash: 45b9cccf5f27baa49b3fd85864d9b22e4d9efae0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030121"
---
# <a name="mailfolder-move"></a><span data-ttu-id="3ad67-103">mailFolder: move</span><span class="sxs-lookup"><span data-stu-id="3ad67-103">mailFolder: move</span></span>

<span data-ttu-id="3ad67-104">Mueve un objeto mailfolder y su contenido a otro objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="3ad67-104">Move a mailfolder and its contents to another mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="3ad67-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3ad67-105">Permissions</span></span>

<span data-ttu-id="3ad67-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3ad67-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3ad67-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3ad67-108">Permission type</span></span> | <span data-ttu-id="3ad67-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3ad67-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="3ad67-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3ad67-110">Delegated (work or school account)</span></span> | <span data-ttu-id="3ad67-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ad67-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="3ad67-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3ad67-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3ad67-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ad67-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="3ad67-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3ad67-114">Application</span></span> | <span data-ttu-id="3ad67-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ad67-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3ad67-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3ad67-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/move
POST /users/{id | userPrincipalName}/mailFolders/{id}/move
```

## <a name="request-headers"></a><span data-ttu-id="3ad67-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3ad67-117">Request headers</span></span>

| <span data-ttu-id="3ad67-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ad67-118">Header</span></span> | <span data-ttu-id="3ad67-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3ad67-119">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="3ad67-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="3ad67-120">Authorization</span></span> | <span data-ttu-id="3ad67-121">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="3ad67-121"></span></span> <span data-ttu-id="3ad67-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3ad67-122">Required.</span></span> |
| <span data-ttu-id="3ad67-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3ad67-123">Content-Type</span></span> | <span data-ttu-id="3ad67-124">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="3ad67-124"></span></span> <span data-ttu-id="3ad67-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3ad67-125">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3ad67-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3ad67-126">Request body</span></span>

<span data-ttu-id="3ad67-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3ad67-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3ad67-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3ad67-128">Parameter</span></span> | <span data-ttu-id="3ad67-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ad67-129">Type</span></span> | <span data-ttu-id="3ad67-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ad67-130">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="3ad67-131">destinationId</span><span class="sxs-lookup"><span data-stu-id="3ad67-131">destinationId</span></span>|<span data-ttu-id="3ad67-132">String</span><span class="sxs-lookup"><span data-stu-id="3ad67-132">String</span></span>|<span data-ttu-id="3ad67-133">El identificador de la carpeta, o un nombre de carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="3ad67-133">The folder ID, or a well-known folder name.</span></span> <span data-ttu-id="3ad67-134">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="3ad67-134">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="3ad67-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ad67-135">Response</span></span>

<span data-ttu-id="3ad67-136">Si tiene éxito, este método devuelve `200 OK` código de respuesta y un recurso de [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ad67-136">If successful, this method returns `200 OK` response code and a [mailFolder](../resources/mailfolder.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3ad67-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ad67-137">Example</span></span>

<span data-ttu-id="3ad67-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3ad67-138">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="3ad67-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ad67-139">Request</span></span>

<span data-ttu-id="3ad67-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ad67-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "mailfolder_move"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/move
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="3ad67-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ad67-141">Response</span></span>

<span data-ttu-id="3ad67-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ad67-142">Here is an example of the response.</span></span>

> <span data-ttu-id="3ad67-143">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="3ad67-143">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="3ad67-144">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3ad67-144">All the properties will be returned from an actual call.</span></span>
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
  "description": "mailFolder: move",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
