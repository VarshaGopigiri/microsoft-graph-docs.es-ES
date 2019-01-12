---
title: 'bloc de notas: copyNotebook'
description: Copia un bloc de notas a la carpeta Blocs de notas de la biblioteca de documentos de destino. Se crea la carpeta si no existe.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: 4e74badfdd2386a976ad6ec5b1d639c164361ce4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984776"
---
# <a name="notebook-copynotebook"></a><span data-ttu-id="903a3-104">bloc de notas: copyNotebook</span><span class="sxs-lookup"><span data-stu-id="903a3-104">notebook: copyNotebook</span></span>

> <span data-ttu-id="903a3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="903a3-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="903a3-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="903a3-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="903a3-p103">Copia un bloc de notas a la carpeta Blocs de notas de la biblioteca de documentos de destino. Se crea la carpeta si no existe.</span><span class="sxs-lookup"><span data-stu-id="903a3-p103">Copies a notebook to the Notebooks folder in the destination Documents library. The folder is created if it doesn't exist.</span></span>

<span data-ttu-id="903a3-109">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="903a3-109">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="permissions"></a><span data-ttu-id="903a3-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="903a3-110">Permissions</span></span>
<span data-ttu-id="903a3-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="903a3-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="903a3-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="903a3-113">Permission type</span></span>      | <span data-ttu-id="903a3-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="903a3-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="903a3-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="903a3-115">Delegated (work or school account)</span></span> | <span data-ttu-id="903a3-116">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="903a3-116">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="903a3-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="903a3-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="903a3-118">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="903a3-118">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="903a3-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="903a3-119">Application</span></span> | <span data-ttu-id="903a3-120">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="903a3-120">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="903a3-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="903a3-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/copyNotebook
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/copyNotebook
POST /groups/{id}/onenote/notebooks/{id}/copyNotebook
POST /sites/{id}/onenote/notebooks/{id}/copyNotebook
```
## <a name="request-headers"></a><span data-ttu-id="903a3-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="903a3-122">Request headers</span></span>
| <span data-ttu-id="903a3-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="903a3-123">Name</span></span>       | <span data-ttu-id="903a3-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="903a3-124">Type</span></span> | <span data-ttu-id="903a3-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="903a3-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="903a3-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="903a3-126">Authorization</span></span>  | <span data-ttu-id="903a3-127">string</span><span class="sxs-lookup"><span data-stu-id="903a3-127">string</span></span>  | <span data-ttu-id="903a3-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="903a3-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="903a3-130">Content-Type</span><span class="sxs-lookup"><span data-stu-id="903a3-130">Content-Type</span></span> | <span data-ttu-id="903a3-131">string</span><span class="sxs-lookup"><span data-stu-id="903a3-131">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="903a3-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="903a3-132">Request body</span></span>
<span data-ttu-id="903a3-p106">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación. Puede enviarse un cuerpo vacío si no se necesita ninguno.</span><span class="sxs-lookup"><span data-stu-id="903a3-p106">In the request body, provide a JSON object that contains the parameters that your operation needs. It's okay to send an empty body if none are needed.</span></span>

| <span data-ttu-id="903a3-135">Parámetro</span><span class="sxs-lookup"><span data-stu-id="903a3-135">Parameter</span></span>    | <span data-ttu-id="903a3-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="903a3-136">Type</span></span>   |<span data-ttu-id="903a3-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="903a3-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="903a3-138">siteCollectionId</span><span class="sxs-lookup"><span data-stu-id="903a3-138">siteCollectionId</span></span>|<span data-ttu-id="903a3-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="903a3-139">String</span></span>|<span data-ttu-id="903a3-140">El identificador del sitio de SharePoint para copiar a.</span><span class="sxs-lookup"><span data-stu-id="903a3-140">The id of the SharePoint site to copy to.</span></span> <span data-ttu-id="903a3-141">Usar únicamente cuando se copia a un sitio de grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="903a3-141">Use only when copying to an Office 365 team site.</span></span>|
|<span data-ttu-id="903a3-142">siteId</span><span class="sxs-lookup"><span data-stu-id="903a3-142">siteId</span></span>|<span data-ttu-id="903a3-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="903a3-143">String</span></span>|<span data-ttu-id="903a3-144">El identificador del sitio web de SharePoint para copiar a.</span><span class="sxs-lookup"><span data-stu-id="903a3-144">The id of the SharePoint web to copy to.</span></span> <span data-ttu-id="903a3-145">Usar únicamente cuando se copia a un sitio de grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="903a3-145">Use only when copying to an Office 365 team site.</span></span>|
|<span data-ttu-id="903a3-146">groupId</span><span class="sxs-lookup"><span data-stu-id="903a3-146">groupId</span></span>|<span data-ttu-id="903a3-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="903a3-147">String</span></span>|<span data-ttu-id="903a3-p109">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="903a3-p109">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="903a3-150">renameAs</span><span class="sxs-lookup"><span data-stu-id="903a3-150">renameAs</span></span>|<span data-ttu-id="903a3-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="903a3-151">String</span></span>|<span data-ttu-id="903a3-p110">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="903a3-p110">The name of the copy. Defaults to the name of the existing item.</span></span> |

## <a name="response"></a><span data-ttu-id="903a3-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="903a3-154">Response</span></span>

<span data-ttu-id="903a3-p111">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation-get.md).</span><span class="sxs-lookup"><span data-stu-id="903a3-p111">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation-get.md).</span></span>

## <a name="example"></a><span data-ttu-id="903a3-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="903a3-157">Example</span></span>
<span data-ttu-id="903a3-158">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="903a3-158">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="903a3-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="903a3-159">Request</span></span>
<span data-ttu-id="903a3-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="903a3-160">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "notebook_copynotebook"
}-->
```http
POST https://graph.microsoft.com/beta/me/onenote/notebooks/{id}/copyNotebook
Content-type: application/json
Content-length: 108

{
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="903a3-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="903a3-161">Response</span></span>
<span data-ttu-id="903a3-162">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="903a3-162">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteOperation"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebook: copyNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
