---
title: 'sección: copyToNotebook'
description: Copia una sección a un bloc de notas específico.
ms.openlocfilehash: 393618ddae4fa20b47bdb77aa650185f3b2ed518
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082940"
---
# <a name="section-copytonotebook"></a><span data-ttu-id="5ed41-103">sección: copyToNotebook</span><span class="sxs-lookup"><span data-stu-id="5ed41-103">section: copyToNotebook</span></span>

> <span data-ttu-id="5ed41-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5ed41-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5ed41-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5ed41-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5ed41-106">Copia una sección a un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="5ed41-106">Copies a section to a specific notebook.</span></span>

<span data-ttu-id="5ed41-107">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="5ed41-107">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>
## <a name="permissions"></a><span data-ttu-id="5ed41-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="5ed41-108">Permissions</span></span>
<span data-ttu-id="5ed41-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5ed41-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5ed41-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5ed41-111">Permission type</span></span>      | <span data-ttu-id="5ed41-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5ed41-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5ed41-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5ed41-113">Delegated (work or school account)</span></span> | <span data-ttu-id="5ed41-114">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5ed41-114">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="5ed41-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5ed41-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5ed41-116">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5ed41-116">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="5ed41-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5ed41-117">Application</span></span> | <span data-ttu-id="5ed41-118">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5ed41-118">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5ed41-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5ed41-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/copyToNotebook
POST /users/{id | userPrincipalName}/onenote/sections/{id}/copyToNotebook
POST /groups/{id}/onenote/sections/{id}/copyToNotebook
POST /sites/{id}/onenote/sections/{id}/copyToNotebook
```
## <a name="request-headers"></a><span data-ttu-id="5ed41-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5ed41-120">Request headers</span></span>
| <span data-ttu-id="5ed41-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ed41-121">Name</span></span>       | <span data-ttu-id="5ed41-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ed41-122">Type</span></span> | <span data-ttu-id="5ed41-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ed41-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5ed41-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="5ed41-124">Authorization</span></span>  | <span data-ttu-id="5ed41-125">string</span><span class="sxs-lookup"><span data-stu-id="5ed41-125">string</span></span>  | <span data-ttu-id="5ed41-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5ed41-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5ed41-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5ed41-128">Content-Type</span></span> | <span data-ttu-id="5ed41-129">string</span><span class="sxs-lookup"><span data-stu-id="5ed41-129">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="5ed41-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5ed41-130">Request body</span></span>
<span data-ttu-id="5ed41-131">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="5ed41-131">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="5ed41-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5ed41-132">Parameter</span></span>    | <span data-ttu-id="5ed41-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ed41-133">Type</span></span>   |<span data-ttu-id="5ed41-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ed41-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5ed41-135">siteCollectionId</span><span class="sxs-lookup"><span data-stu-id="5ed41-135">siteCollectionId</span></span>|<span data-ttu-id="5ed41-136">String</span><span class="sxs-lookup"><span data-stu-id="5ed41-136">String</span></span>|<span data-ttu-id="5ed41-137">El identificador del sitio de SharePoint para copiar a.</span><span class="sxs-lookup"><span data-stu-id="5ed41-137">The id of the SharePoint site to copy to.</span></span> <span data-ttu-id="5ed41-138">Usar únicamente cuando se copia a un sitio de grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="5ed41-138">Use only when copying to an Office 365 team site.</span></span>|
|<span data-ttu-id="5ed41-139">siteId</span><span class="sxs-lookup"><span data-stu-id="5ed41-139">siteId</span></span>|<span data-ttu-id="5ed41-140">String</span><span class="sxs-lookup"><span data-stu-id="5ed41-140">String</span></span>|<span data-ttu-id="5ed41-141">El identificador del sitio web de SharePoint para copiar a.</span><span class="sxs-lookup"><span data-stu-id="5ed41-141">The id of the SharePoint web to copy to.</span></span> <span data-ttu-id="5ed41-142">Usar únicamente cuando se copia a un sitio de grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="5ed41-142">Use only when copying to an Office 365 team site.</span></span>|
|<span data-ttu-id="5ed41-143">groupId</span><span class="sxs-lookup"><span data-stu-id="5ed41-143">groupId</span></span>|<span data-ttu-id="5ed41-144">String</span><span class="sxs-lookup"><span data-stu-id="5ed41-144">String</span></span>|<span data-ttu-id="5ed41-p106">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="5ed41-p106">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="5ed41-147">id</span><span class="sxs-lookup"><span data-stu-id="5ed41-147">id</span></span>|<span data-ttu-id="5ed41-148">String</span><span class="sxs-lookup"><span data-stu-id="5ed41-148">String</span></span>|<span data-ttu-id="5ed41-p107">Obligatorio. El id. del bloc de notas de destino.</span><span class="sxs-lookup"><span data-stu-id="5ed41-p107">Required. The id of the destination notebook.</span></span> |
|<span data-ttu-id="5ed41-151">renameAs</span><span class="sxs-lookup"><span data-stu-id="5ed41-151">renameAs</span></span>|<span data-ttu-id="5ed41-152">String</span><span class="sxs-lookup"><span data-stu-id="5ed41-152">String</span></span>|<span data-ttu-id="5ed41-p108">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="5ed41-p108">The name of the copy. Defaults to the name of the existing item.</span></span> |

## <a name="response"></a><span data-ttu-id="5ed41-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ed41-155">Response</span></span>

<span data-ttu-id="5ed41-p109">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation-get.md).</span><span class="sxs-lookup"><span data-stu-id="5ed41-p109">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation-get.md).</span></span>

## <a name="example"></a><span data-ttu-id="5ed41-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5ed41-158">Example</span></span>
<span data-ttu-id="5ed41-159">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5ed41-159">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5ed41-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5ed41-160">Request</span></span>
<span data-ttu-id="5ed41-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5ed41-161">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "section_copytonotebook"
}-->
```http
POST https://graph.microsoft.com/beta/me/onenote/sections/{id}/copyToNotebook
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="5ed41-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ed41-162">Response</span></span>
<span data-ttu-id="5ed41-163">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5ed41-163">Here is an example of the response.</span></span>
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
  "description": "section: copyToNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->