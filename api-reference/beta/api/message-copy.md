---
title: 'message: copy'
description: Copia un mensaje a una carpeta.
author: angelgolfer-ms
ms.openlocfilehash: e9d0661c01103fbfcf8991e0b28126b2f92e6ea4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27353252"
---
# <a name="message-copy"></a><span data-ttu-id="38c02-103">message: copy</span><span class="sxs-lookup"><span data-stu-id="38c02-103">message: copy</span></span>

> <span data-ttu-id="38c02-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38c02-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38c02-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38c02-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="38c02-106">Copia un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="38c02-106">Copy a message to a folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="38c02-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="38c02-107">Permissions</span></span>

<span data-ttu-id="38c02-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38c02-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="38c02-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38c02-110">Permission type</span></span> | <span data-ttu-id="38c02-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38c02-111">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="38c02-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38c02-112">Delegated (work or school account)</span></span> | <span data-ttu-id="38c02-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38c02-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="38c02-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38c02-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38c02-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38c02-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="38c02-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38c02-116">Application</span></span> | <span data-ttu-id="38c02-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="38c02-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="38c02-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38c02-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/copy
POST /users/{id | userPrincipalName}/messages/{id}/copy
POST /me/mailFolders/{id}/messages/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="38c02-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38c02-119">Request headers</span></span>

| <span data-ttu-id="38c02-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38c02-120">Header</span></span> | <span data-ttu-id="38c02-121">Valor</span><span class="sxs-lookup"><span data-stu-id="38c02-121">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="38c02-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="38c02-122">Authorization</span></span> | <span data-ttu-id="38c02-123">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="38c02-123"></span></span> <span data-ttu-id="38c02-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38c02-124">Required.</span></span> |
| <span data-ttu-id="38c02-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="38c02-125">Content-Type</span></span> | <span data-ttu-id="38c02-126">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="38c02-126"></span></span> <span data-ttu-id="38c02-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38c02-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="38c02-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38c02-128">Request body</span></span>

<span data-ttu-id="38c02-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="38c02-129">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="38c02-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="38c02-130">Parameter</span></span> | <span data-ttu-id="38c02-131">Type</span><span class="sxs-lookup"><span data-stu-id="38c02-131">Type</span></span> | <span data-ttu-id="38c02-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="38c02-132">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="38c02-133">destinationId</span><span class="sxs-lookup"><span data-stu-id="38c02-133">destinationId</span></span>|<span data-ttu-id="38c02-134">String</span><span class="sxs-lookup"><span data-stu-id="38c02-134">String</span></span>|<span data-ttu-id="38c02-135">El identificador de la carpeta de destino, o un nombre de carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="38c02-135">The destination folder ID, or a well-known folder name.</span></span> <span data-ttu-id="38c02-136">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="38c02-136">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="38c02-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38c02-137">Response</span></span>

<span data-ttu-id="38c02-138">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un recurso de [mensaje](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38c02-138">If successful, this method returns `201 Created` response code and a [message](../resources/message.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38c02-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38c02-139">Example</span></span>

<span data-ttu-id="38c02-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="38c02-140">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="38c02-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38c02-141">Request</span></span>

<span data-ttu-id="38c02-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38c02-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_copy"
}-->

```http
POST https://graph.microsoft.com/beta/me/messages/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="38c02-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38c02-143">Response</span></span>

<span data-ttu-id="38c02-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38c02-144">Here is an example of the response.</span></span>

> <span data-ttu-id="38c02-145">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="38c02-145">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="38c02-146">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38c02-146">All the properties will be returned from an actual call.</span></span>
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
  "receivedDateTime": "2016-10-19T10:37:00Z",
  "sentDateTime": "2016-10-19T10:37:00Z",
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
