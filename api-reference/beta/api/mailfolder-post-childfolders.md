---
title: Crear mailFolder
description: Utilice esta API para crear un nuevo mailFolder secundarios.
ms.openlocfilehash: 44d9e9ebfd721a68734376342500ad1e2a182cda
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087533"
---
# <a name="create-mailfolder"></a><span data-ttu-id="5349d-103">Crear mailFolder</span><span class="sxs-lookup"><span data-stu-id="5349d-103">Create mailFolder</span></span>

> <span data-ttu-id="5349d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5349d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5349d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5349d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5349d-106">Utilice esta API para crear un nuevo de secundarios [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5349d-106">Use this API to create a new child [mailFolder](../resources/mailfolder.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="5349d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5349d-107">Permissions</span></span>

<span data-ttu-id="5349d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5349d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5349d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5349d-110">Permission type</span></span> | <span data-ttu-id="5349d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5349d-111">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="5349d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5349d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="5349d-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5349d-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="5349d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5349d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5349d-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5349d-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="5349d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5349d-116">Application</span></span> | <span data-ttu-id="5349d-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5349d-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5349d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5349d-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="5349d-119">Especifique la carpeta principal en la dirección URL de consulta como un identificador de carpeta o nombre de una carpeta conocida.</span><span class="sxs-lookup"><span data-stu-id="5349d-119">Specify the parent folder in the query URL as a folder ID, or a well-known folder name.</span></span> <span data-ttu-id="5349d-120">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5349d-120">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>

## <a name="request-headers"></a><span data-ttu-id="5349d-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5349d-121">Request headers</span></span>

| <span data-ttu-id="5349d-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5349d-122">Header</span></span> | <span data-ttu-id="5349d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5349d-123">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="5349d-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="5349d-124">Authorization</span></span> | <span data-ttu-id="5349d-125">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="5349d-125"></span></span> <span data-ttu-id="5349d-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5349d-126">Required.</span></span> |
| <span data-ttu-id="5349d-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5349d-127">Content-Type</span></span> | <span data-ttu-id="5349d-128">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="5349d-128"></span></span> <span data-ttu-id="5349d-129">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5349d-129">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5349d-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5349d-130">Request body</span></span>

<span data-ttu-id="5349d-p106">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5349d-p106">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="5349d-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5349d-133">Parameter</span></span> | <span data-ttu-id="5349d-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="5349d-134">Type</span></span> | <span data-ttu-id="5349d-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="5349d-135">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="5349d-136">displayName</span><span class="sxs-lookup"><span data-stu-id="5349d-136">displayName</span></span>|<span data-ttu-id="5349d-137">String</span><span class="sxs-lookup"><span data-stu-id="5349d-137">String</span></span>|<span data-ttu-id="5349d-138">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="5349d-138">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="5349d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5349d-139">Response</span></span>

<span data-ttu-id="5349d-140">Si tiene éxito, este método devuelve `201 Created` código de respuesta y un objeto [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5349d-140">If successful, this method returns `201 Created` response code and a [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5349d-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5349d-141">Example</span></span>

#### <a name="request"></a><span data-ttu-id="5349d-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5349d-142">Request</span></span>

<span data-ttu-id="5349d-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5349d-143">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_mailfolder"
}-->

```http
POST https://graph.microsoft.com/beta/me/mailFolders/{id}/childFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```

#### <a name="response"></a><span data-ttu-id="5349d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5349d-144">Response</span></span>

<span data-ttu-id="5349d-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5349d-145">The following is an example of the response.</span></span>

> <span data-ttu-id="5349d-146">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="5349d-146">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="5349d-147">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5349d-147">All the properties will be returned from an actual call.</span></span>
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
  "description": "Create mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
