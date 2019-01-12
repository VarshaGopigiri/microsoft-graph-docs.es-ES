---
title: 'página: copyToSection'
description: Copia una página en una sección específica.
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: b09c47ab7dbaec7b7dd63d134cdefae1260d9e8d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934824"
---
# <a name="page-copytosection"></a><span data-ttu-id="c78a1-103">página: copyToSection</span><span class="sxs-lookup"><span data-stu-id="c78a1-103">page: copyToSection</span></span>
<span data-ttu-id="c78a1-104">Copia una página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="c78a1-104">Copies a page to a specific section.</span></span>

<span data-ttu-id="c78a1-105">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="c78a1-105">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="permissions"></a><span data-ttu-id="c78a1-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c78a1-106">Permissions</span></span>
<span data-ttu-id="c78a1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c78a1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c78a1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c78a1-109">Permission type</span></span>      | <span data-ttu-id="c78a1-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c78a1-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c78a1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c78a1-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c78a1-112">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c78a1-112">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="c78a1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c78a1-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c78a1-114">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c78a1-114">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="c78a1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c78a1-115">Application</span></span> | <span data-ttu-id="c78a1-116">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c78a1-116">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c78a1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c78a1-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/pages/{id}/copyToSection
POST /users/{id | userPrincipalName}/onenote/pages/{id}/copyToSection
POST /groups/{id}/onenote/pages/{id}/copyToSection
```
## <a name="request-headers"></a><span data-ttu-id="c78a1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c78a1-118">Request headers</span></span>
| <span data-ttu-id="c78a1-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="c78a1-119">Name</span></span>       | <span data-ttu-id="c78a1-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="c78a1-120">Type</span></span> | <span data-ttu-id="c78a1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c78a1-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c78a1-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="c78a1-122">Authorization</span></span>  | <span data-ttu-id="c78a1-123">string</span><span class="sxs-lookup"><span data-stu-id="c78a1-123">string</span></span>  | <span data-ttu-id="c78a1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c78a1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c78a1-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c78a1-126">Content-Type</span></span> | <span data-ttu-id="c78a1-127">string</span><span class="sxs-lookup"><span data-stu-id="c78a1-127">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="c78a1-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c78a1-128">Request body</span></span>
<span data-ttu-id="c78a1-129">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="c78a1-129">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="c78a1-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c78a1-130">Parameter</span></span>    | <span data-ttu-id="c78a1-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c78a1-131">Type</span></span>   |<span data-ttu-id="c78a1-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c78a1-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c78a1-133">groupId</span><span class="sxs-lookup"><span data-stu-id="c78a1-133">groupId</span></span>|<span data-ttu-id="c78a1-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="c78a1-134">String</span></span>|<span data-ttu-id="c78a1-p103">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="c78a1-p103">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="c78a1-137">id</span><span class="sxs-lookup"><span data-stu-id="c78a1-137">id</span></span>|<span data-ttu-id="c78a1-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="c78a1-138">String</span></span>|<span data-ttu-id="c78a1-p104">Obligatorio. El id. de la sección de destino.</span><span class="sxs-lookup"><span data-stu-id="c78a1-p104">Required. The id of the destination section.</span></span>|

## <a name="response"></a><span data-ttu-id="c78a1-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c78a1-141">Response</span></span>

<span data-ttu-id="c78a1-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation-get.md).</span><span class="sxs-lookup"><span data-stu-id="c78a1-p105">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation-get.md).</span></span>

## <a name="example"></a><span data-ttu-id="c78a1-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c78a1-144">Example</span></span>
<span data-ttu-id="c78a1-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c78a1-145">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c78a1-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c78a1-146">Request</span></span>
<span data-ttu-id="c78a1-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c78a1-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "page_copytosection"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/pages/{id}/copyToSection
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "groupId": "groupId-value"
}
```

##### <a name="response"></a><span data-ttu-id="c78a1-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c78a1-148">Response</span></span>
<span data-ttu-id="c78a1-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c78a1-149">Here is an example of the response.</span></span>
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
  "description": "page: copyToSection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
