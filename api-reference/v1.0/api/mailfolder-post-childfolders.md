---
title: Create MailFolder
description: Use esta API para crear un objeto mailfolder secundario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 44a61fda9120faaac0d8d69590c677896796765e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860035"
---
# <a name="create-mailfolder"></a><span data-ttu-id="659e9-103">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="659e9-103">Create MailFolder</span></span>

<span data-ttu-id="659e9-104">Use esta API para crear un objeto mailfolder secundario.</span><span class="sxs-lookup"><span data-stu-id="659e9-104">Use this API to create a new child mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="659e9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="659e9-105">Permissions</span></span>

<span data-ttu-id="659e9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="659e9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="659e9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="659e9-108">Permission type</span></span> | <span data-ttu-id="659e9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="659e9-109">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="659e9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="659e9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="659e9-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="659e9-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="659e9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="659e9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="659e9-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="659e9-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="659e9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="659e9-114">Application</span></span> | <span data-ttu-id="659e9-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="659e9-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="659e9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="659e9-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="659e9-117">Especifique la carpeta principal en la dirección URL de consulta como un identificador de carpeta o nombre de una carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="659e9-117">Specify the parent folder in the query URL as a folder ID, or a well-known folder name.</span></span> <span data-ttu-id="659e9-118">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="659e9-118">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>

## <a name="request-headers"></a><span data-ttu-id="659e9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="659e9-119">Request headers</span></span>

| <span data-ttu-id="659e9-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="659e9-120">Header</span></span> | <span data-ttu-id="659e9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="659e9-121">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="659e9-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="659e9-122">Authorization</span></span> | <span data-ttu-id="659e9-123">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="659e9-123"></span></span> <span data-ttu-id="659e9-124">Necesario.</span><span class="sxs-lookup"><span data-stu-id="659e9-124">Required.</span></span> |
| <span data-ttu-id="659e9-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="659e9-125">Content-Type</span></span> | <span data-ttu-id="659e9-126">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="659e9-126"></span></span> <span data-ttu-id="659e9-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="659e9-127">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="659e9-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="659e9-128">Request body</span></span>

<span data-ttu-id="659e9-129">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="659e9-129">In the request body, provide a JSON object with the following parameters.</span></span> <span data-ttu-id="659e9-130">**displayName** es la única propiedad grabable de un objeto [mailFolder](../resources/mailfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="659e9-130">**displayName** is the only writable property for a [mailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="659e9-131">Parámetro</span><span class="sxs-lookup"><span data-stu-id="659e9-131">Parameter</span></span> | <span data-ttu-id="659e9-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="659e9-132">Type</span></span> | <span data-ttu-id="659e9-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="659e9-133">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="659e9-134">displayName</span><span class="sxs-lookup"><span data-stu-id="659e9-134">displayName</span></span>|<span data-ttu-id="659e9-135">String</span><span class="sxs-lookup"><span data-stu-id="659e9-135">String</span></span>|<span data-ttu-id="659e9-136">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="659e9-136">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="659e9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="659e9-137">Response</span></span>

<span data-ttu-id="659e9-138">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un recurso de [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="659e9-138">If successful, this method returns `201 Created` response code and a [mailFolder](../resources/mailfolder.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="659e9-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="659e9-139">Example</span></span>

##### <a name="request"></a><span data-ttu-id="659e9-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="659e9-140">Request</span></span>

<span data-ttu-id="659e9-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="659e9-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="659e9-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="659e9-142">Response</span></span>
<span data-ttu-id="659e9-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="659e9-143">Here is an example of the response.</span></span>

> <span data-ttu-id="659e9-144">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="659e9-144">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="659e9-145">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="659e9-145">All the properties will be returned from an actual call.</span></span>
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
