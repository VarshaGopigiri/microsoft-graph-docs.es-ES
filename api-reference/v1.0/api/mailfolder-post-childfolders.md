---
title: Create MailFolder
description: Use esta API para crear un objeto mailfolder secundario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: bf078e34f216dde5a3daf3bcf0cecd27517e7da7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941446"
---
# <a name="create-mailfolder"></a><span data-ttu-id="7b000-103">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="7b000-103">Create MailFolder</span></span>

<span data-ttu-id="7b000-104">Use esta API para crear un objeto mailfolder secundario.</span><span class="sxs-lookup"><span data-stu-id="7b000-104">Use this API to create a new child mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="7b000-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b000-105">Permissions</span></span>

<span data-ttu-id="7b000-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b000-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7b000-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b000-108">Permission type</span></span> | <span data-ttu-id="7b000-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b000-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="7b000-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b000-110">Delegated (work or school account)</span></span> | <span data-ttu-id="7b000-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b000-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="7b000-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b000-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b000-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b000-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="7b000-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b000-114">Application</span></span> | <span data-ttu-id="7b000-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b000-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="7b000-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b000-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="7b000-117">Especifique la carpeta principal en la dirección URL de consulta como un identificador de carpeta o nombre de una carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="7b000-117">Specify the parent folder in the query URL as a folder ID, or a well-known folder name.</span></span> <span data-ttu-id="7b000-118">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="7b000-118">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>

## <a name="request-headers"></a><span data-ttu-id="7b000-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b000-119">Request headers</span></span>

| <span data-ttu-id="7b000-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b000-120">Header</span></span> | <span data-ttu-id="7b000-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7b000-121">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="7b000-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="7b000-122">Authorization</span></span> | <span data-ttu-id="7b000-123">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="7b000-123"></span></span> <span data-ttu-id="7b000-124">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b000-124">Required.</span></span> |
| <span data-ttu-id="7b000-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7b000-125">Content-Type</span></span> | <span data-ttu-id="7b000-126">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="7b000-126"></span></span> <span data-ttu-id="7b000-127">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b000-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7b000-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b000-128">Request body</span></span>

<span data-ttu-id="7b000-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b000-129">In the request body, provide a JSON object with the following parameters.</span></span> <span data-ttu-id="7b000-130">**displayName** es la única propiedad grabable de un objeto [mailFolder](../resources/mailfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="7b000-130">**displayName** is the only writable property for a [mailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="7b000-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7b000-131">Parameter</span></span> | <span data-ttu-id="7b000-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b000-132">Type</span></span> | <span data-ttu-id="7b000-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b000-133">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="7b000-134">displayName</span><span class="sxs-lookup"><span data-stu-id="7b000-134">displayName</span></span>|<span data-ttu-id="7b000-135">String</span><span class="sxs-lookup"><span data-stu-id="7b000-135">String</span></span>|<span data-ttu-id="7b000-136">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="7b000-136">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="7b000-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b000-137">Response</span></span>

<span data-ttu-id="7b000-138">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un recurso de [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b000-138">If successful, this method returns `201 Created` response code and a [mailFolder](../resources/mailfolder.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7b000-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b000-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="7b000-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b000-140">Request</span></span>

<span data-ttu-id="7b000-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b000-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_mailfolder"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/childFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```

##### <a name="response"></a><span data-ttu-id="7b000-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b000-142">Response</span></span>
<span data-ttu-id="7b000-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b000-143">Here is an example of the response.</span></span>

> <span data-ttu-id="7b000-144">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="7b000-144">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="7b000-145">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b000-145">All the properties will be returned from an actual call.</span></span>
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
  "description": "Create MailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
