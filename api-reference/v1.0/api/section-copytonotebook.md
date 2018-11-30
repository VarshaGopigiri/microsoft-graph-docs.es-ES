---
title: 'sección: copyToNotebook'
description: Copia una sección a un bloc de notas específico.
ms.openlocfilehash: 365e4745f01c3d011cbf8cf0186a16b5eb580c5b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031122"
---
# <a name="section-copytonotebook"></a><span data-ttu-id="9fe8d-103">sección: copyToNotebook</span><span class="sxs-lookup"><span data-stu-id="9fe8d-103">section: copyToNotebook</span></span>
<span data-ttu-id="9fe8d-104">Copia una sección a un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-104">Copies a section to a specific notebook.</span></span>

<span data-ttu-id="9fe8d-105">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-105">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>
## <a name="permissions"></a><span data-ttu-id="9fe8d-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="9fe8d-106">Permissions</span></span>
<span data-ttu-id="9fe8d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9fe8d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9fe8d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9fe8d-109">Permission type</span></span>      | <span data-ttu-id="9fe8d-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9fe8d-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9fe8d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9fe8d-111">Delegated (work or school account)</span></span> | <span data-ttu-id="9fe8d-112">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9fe8d-112">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="9fe8d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9fe8d-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9fe8d-114">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9fe8d-114">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="9fe8d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9fe8d-115">Application</span></span> | <span data-ttu-id="9fe8d-116">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9fe8d-116">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9fe8d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9fe8d-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/copyToNotebook
POST /users/{id | userPrincipalName}/onenote/sections/{id}/copyToNotebook
POST /groups/{id}/onenote/sections/{id}/copyToNotebook
```
## <a name="request-headers"></a><span data-ttu-id="9fe8d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9fe8d-118">Request headers</span></span>
| <span data-ttu-id="9fe8d-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="9fe8d-119">Name</span></span>       | <span data-ttu-id="9fe8d-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fe8d-120">Type</span></span> | <span data-ttu-id="9fe8d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fe8d-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9fe8d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="9fe8d-122">Authorization</span></span>  | <span data-ttu-id="9fe8d-123">string</span><span class="sxs-lookup"><span data-stu-id="9fe8d-123">string</span></span>  | <span data-ttu-id="9fe8d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9fe8d-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9fe8d-126">Content-Type</span></span> | <span data-ttu-id="9fe8d-127">string</span><span class="sxs-lookup"><span data-stu-id="9fe8d-127">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="9fe8d-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9fe8d-128">Request body</span></span>
<span data-ttu-id="9fe8d-129">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-129">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="9fe8d-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9fe8d-130">Parameter</span></span>    | <span data-ttu-id="9fe8d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fe8d-131">Type</span></span>   |<span data-ttu-id="9fe8d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fe8d-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9fe8d-133">groupId</span><span class="sxs-lookup"><span data-stu-id="9fe8d-133">groupId</span></span>|<span data-ttu-id="9fe8d-134">String</span><span class="sxs-lookup"><span data-stu-id="9fe8d-134">String</span></span>|<span data-ttu-id="9fe8d-p103">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-p103">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="9fe8d-137">id</span><span class="sxs-lookup"><span data-stu-id="9fe8d-137">id</span></span>|<span data-ttu-id="9fe8d-138">String</span><span class="sxs-lookup"><span data-stu-id="9fe8d-138">String</span></span>|<span data-ttu-id="9fe8d-p104">Obligatorio. El id. del bloc de notas de destino.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-p104">Required. The id of the destination notebook.</span></span> |
|<span data-ttu-id="9fe8d-141">renameAs</span><span class="sxs-lookup"><span data-stu-id="9fe8d-141">renameAs</span></span>|<span data-ttu-id="9fe8d-142">String</span><span class="sxs-lookup"><span data-stu-id="9fe8d-142">String</span></span>|<span data-ttu-id="9fe8d-p105">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-p105">The name of the copy. Defaults to the name of the existing item.</span></span> |

## <a name="response"></a><span data-ttu-id="9fe8d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fe8d-145">Response</span></span>

<span data-ttu-id="9fe8d-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation-get.md).</span><span class="sxs-lookup"><span data-stu-id="9fe8d-p106">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation-get.md).</span></span>

## <a name="example"></a><span data-ttu-id="9fe8d-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fe8d-148">Example</span></span>
<span data-ttu-id="9fe8d-149">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-149">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9fe8d-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9fe8d-150">Request</span></span>
<span data-ttu-id="9fe8d-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-151">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "section_copytonotebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/copyToNotebook
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="9fe8d-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fe8d-152">Response</span></span>
<span data-ttu-id="9fe8d-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fe8d-153">Here is an example of the response.</span></span>
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