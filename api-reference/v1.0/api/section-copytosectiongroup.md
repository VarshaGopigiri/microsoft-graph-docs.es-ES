---
title: 'sección: copyToSectionGroup'
description: Copia una sección a un grupo de secciones específico.
localization_priority: Normal
ms.openlocfilehash: 671cd28db66517b0b04d8b9d99cc1dccba17206e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846574"
---
# <a name="section-copytosectiongroup"></a><span data-ttu-id="e3b5b-103">sección: copyToSectionGroup</span><span class="sxs-lookup"><span data-stu-id="e3b5b-103">section: copyToSectionGroup</span></span>
<span data-ttu-id="e3b5b-104">Copia una sección a un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-104">Copies a section to a specific section group.</span></span>

<span data-ttu-id="e3b5b-105">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-105">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="permissions"></a><span data-ttu-id="e3b5b-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="e3b5b-106">Permissions</span></span>
<span data-ttu-id="e3b5b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3b5b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e3b5b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3b5b-109">Permission type</span></span>      | <span data-ttu-id="e3b5b-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3b5b-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e3b5b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3b5b-111">Delegated (work or school account)</span></span> | <span data-ttu-id="e3b5b-112">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3b5b-112">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="e3b5b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3b5b-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e3b5b-114">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e3b5b-114">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="e3b5b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3b5b-115">Application</span></span> | <span data-ttu-id="e3b5b-116">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3b5b-116">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e3b5b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3b5b-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/copyToSectionGroup
POST /users/{id | userPrincipalName}/onenote/sections/{id}/copyToSectionGroup
POST /groups/{id}/onenote/sections/{id}/copyToSectionGroup
```
## <a name="request-headers"></a><span data-ttu-id="e3b5b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3b5b-118">Request headers</span></span>
| <span data-ttu-id="e3b5b-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3b5b-119">Name</span></span>       | <span data-ttu-id="e3b5b-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3b5b-120">Type</span></span> | <span data-ttu-id="e3b5b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3b5b-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e3b5b-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="e3b5b-122">Authorization</span></span>  | <span data-ttu-id="e3b5b-123">string</span><span class="sxs-lookup"><span data-stu-id="e3b5b-123">string</span></span>  | <span data-ttu-id="e3b5b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e3b5b-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e3b5b-126">Content-Type</span></span> | <span data-ttu-id="e3b5b-127">string</span><span class="sxs-lookup"><span data-stu-id="e3b5b-127">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="e3b5b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3b5b-128">Request body</span></span>
<span data-ttu-id="e3b5b-129">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-129">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="e3b5b-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e3b5b-130">Parameter</span></span>    | <span data-ttu-id="e3b5b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3b5b-131">Type</span></span>   |<span data-ttu-id="e3b5b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3b5b-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e3b5b-133">groupId</span><span class="sxs-lookup"><span data-stu-id="e3b5b-133">groupId</span></span>|<span data-ttu-id="e3b5b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="e3b5b-134">String</span></span>|<span data-ttu-id="e3b5b-p103">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-p103">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="e3b5b-137">id</span><span class="sxs-lookup"><span data-stu-id="e3b5b-137">id</span></span>|<span data-ttu-id="e3b5b-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="e3b5b-138">String</span></span>|<span data-ttu-id="e3b5b-p104">Obligatorio. El id. del grupo de secciones de destino.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-p104">Required. The id of the destination section group.</span></span> |
|<span data-ttu-id="e3b5b-141">renameAs</span><span class="sxs-lookup"><span data-stu-id="e3b5b-141">renameAs</span></span>|<span data-ttu-id="e3b5b-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="e3b5b-142">String</span></span>|<span data-ttu-id="e3b5b-p105">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-p105">The name of the copy. Defaults to the name of the existing item.</span></span> |

<!--groupId missing-->
<!--|siteCollectionId|String||
|siteId|String||-->

## <a name="response"></a><span data-ttu-id="e3b5b-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3b5b-145">Response</span></span>

<span data-ttu-id="e3b5b-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation-get.md).</span><span class="sxs-lookup"><span data-stu-id="e3b5b-p106">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation-get.md).</span></span>

## <a name="example"></a><span data-ttu-id="e3b5b-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3b5b-148">Example</span></span>
<span data-ttu-id="e3b5b-149">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-149">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e3b5b-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3b5b-150">Request</span></span>
<span data-ttu-id="e3b5b-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-151">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "section_copytosectiongroup"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/copyToSectionGroup
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="e3b5b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3b5b-152">Response</span></span>
<span data-ttu-id="e3b5b-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3b5b-153">Here is an example of the response.</span></span>
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
  "description": "section: copyToSectionGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
