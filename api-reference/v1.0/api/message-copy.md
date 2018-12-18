---
title: 'message: copy'
description: Copia un mensaje a una carpeta.
author: angelgolfer-ms
ms.openlocfilehash: 56517ce5233ab4327b57620fe8b240edd2acc45b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309299"
---
# <a name="message-copy"></a><span data-ttu-id="9304d-103">message: copy</span><span class="sxs-lookup"><span data-stu-id="9304d-103">message: copy</span></span>

<span data-ttu-id="9304d-104">Copia un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="9304d-104">Copy a message to a folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="9304d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9304d-105">Permissions</span></span>

<span data-ttu-id="9304d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9304d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="9304d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9304d-108">Permission type</span></span> | <span data-ttu-id="9304d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9304d-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="9304d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9304d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="9304d-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9304d-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9304d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9304d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9304d-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9304d-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="9304d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9304d-114">Application</span></span> | <span data-ttu-id="9304d-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9304d-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9304d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9304d-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/copy
POST /users/{id | userPrincipalName}/messages/{id}/copy
POST /me/mailFolders/{id}/messages/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="9304d-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9304d-117">Request headers</span></span>

| <span data-ttu-id="9304d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9304d-118">Header</span></span> | <span data-ttu-id="9304d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9304d-119">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="9304d-120">Autorización</span><span class="sxs-lookup"><span data-stu-id="9304d-120">Authorization</span></span> | <span data-ttu-id="9304d-121">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="9304d-121"></span></span> <span data-ttu-id="9304d-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9304d-122">Required.</span></span> |
| <span data-ttu-id="9304d-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9304d-123">Content-Type</span></span> | <span data-ttu-id="9304d-124">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="9304d-124"></span></span> <span data-ttu-id="9304d-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9304d-125">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9304d-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9304d-126">Request body</span></span>

<span data-ttu-id="9304d-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9304d-127">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9304d-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9304d-128">Parameter</span></span> | <span data-ttu-id="9304d-129">Type</span><span class="sxs-lookup"><span data-stu-id="9304d-129">Type</span></span> | <span data-ttu-id="9304d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9304d-130">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="9304d-131">destinationId</span><span class="sxs-lookup"><span data-stu-id="9304d-131">destinationId</span></span>|<span data-ttu-id="9304d-132">String</span><span class="sxs-lookup"><span data-stu-id="9304d-132">String</span></span>|<span data-ttu-id="9304d-133">El identificador de la carpeta de destino, o un nombre de carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="9304d-133">The destination folder ID, or a well-known folder name.</span></span> <span data-ttu-id="9304d-134">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="9304d-134">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="9304d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9304d-135">Response</span></span>

<span data-ttu-id="9304d-136">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un recurso de [mensaje](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9304d-136">If successful, this method returns `201 Created` response code and a [message](../resources/message.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9304d-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9304d-137">Example</span></span>

<span data-ttu-id="9304d-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9304d-138">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="9304d-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9304d-139">Request</span></span>
<span data-ttu-id="9304d-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9304d-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_copy"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="9304d-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9304d-141">Response</span></span>

<span data-ttu-id="9304d-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9304d-142">Here is an example of the response.</span></span>

> <span data-ttu-id="9304d-143">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="9304d-143">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="9304d-144">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9304d-144">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: copy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
