---
title: Obtener onenoteOperation
description: 'Obtenga el estado de una operación de larga duración de OneNote. Esto se aplica a las operaciones que devuelvan el encabezado **Operation-Location** en la respuesta, como `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup` y `and CopyToSection`.   '
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: c869702b856f03bccbbc5101e8e72facd3287738
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932388"
---
# <a name="get-onenoteoperation"></a><span data-ttu-id="3a34b-104">Obtener onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="3a34b-104">Get onenoteOperation</span></span>

<span data-ttu-id="3a34b-p102">Obtenga el estado de una operación de larga duración de OneNote. Esto se aplica a las operaciones que devuelvan el encabezado **Operation-Location** en la respuesta, como `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup` y `and CopyToSection`.</span><span class="sxs-lookup"><span data-stu-id="3a34b-p102">Get the status of a long-running OneNote operation. This applies to operations that return the **Operation-Location** header in the response, such as `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup`, `and CopyToSection`.</span></span>   

<span data-ttu-id="3a34b-107">Puede sondear el extremo de Operation-Location hasta que la propiedad de `status` devuelva `completed` o `failed`.</span><span class="sxs-lookup"><span data-stu-id="3a34b-107">You can poll the Operation-Location endpoint until the `status` property returns `completed` or `failed`.</span></span> 

<span data-ttu-id="3a34b-108">Si el estado es `completed`, la propiedad de `resourceLocation` contiene el URI del extremo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a34b-108">If the status is `completed`, the `resourceLocation` property contains the resource endpoint URI.</span></span> 

<span data-ttu-id="3a34b-109">Si el estado es `failed`, el error y las propiedades de `@api.diagnostics` facilitan información del error.</span><span class="sxs-lookup"><span data-stu-id="3a34b-109">If the status is `failed`, the error and `@api.diagnostics` properties provide error information.</span></span>

## <a name="permissions"></a><span data-ttu-id="3a34b-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="3a34b-110">Permissions</span></span>
<span data-ttu-id="3a34b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3a34b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3a34b-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a34b-113">Permission type</span></span>      | <span data-ttu-id="3a34b-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a34b-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3a34b-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a34b-115">Delegated (work or school account)</span></span> | <span data-ttu-id="3a34b-116">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3a34b-116">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="3a34b-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a34b-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3a34b-118">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3a34b-118">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="3a34b-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a34b-119">Application</span></span> | <span data-ttu-id="3a34b-120">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3a34b-120">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3a34b-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a34b-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/operations/{id}
GET /users/{id | userPrincipalName}/onenote/operations/{id}
GET /groups/{id}/onenote/operations/{id}
GET /sites/{id}/onenote/operations/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3a34b-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3a34b-122">Optional query parameters</span></span>
<span data-ttu-id="3a34b-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3a34b-123">None.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3a34b-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a34b-124">Request headers</span></span>
| <span data-ttu-id="3a34b-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="3a34b-125">Name</span></span>       | <span data-ttu-id="3a34b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a34b-126">Type</span></span> | <span data-ttu-id="3a34b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a34b-127">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3a34b-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="3a34b-128">Authorization</span></span>  | <span data-ttu-id="3a34b-129">string</span><span class="sxs-lookup"><span data-stu-id="3a34b-129">string</span></span>  | <span data-ttu-id="3a34b-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a34b-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3a34b-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3a34b-132">Accept</span></span> | <span data-ttu-id="3a34b-133">string</span><span class="sxs-lookup"><span data-stu-id="3a34b-133">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="3a34b-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a34b-134">Request body</span></span>
<span data-ttu-id="3a34b-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3a34b-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3a34b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a34b-136">Response</span></span>

<span data-ttu-id="3a34b-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [onenoteOperation](../resources/onenoteoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a34b-137">If successful, this method returns a `200 OK` response code and [onenoteOperation](../resources/onenoteoperation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3a34b-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a34b-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3a34b-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a34b-139">Request</span></span>
<span data-ttu-id="3a34b-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a34b-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_onenoteoperation"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/operations/{id}
```
##### <a name="response"></a><span data-ttu-id="3a34b-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a34b-141">Response</span></span>
<span data-ttu-id="3a34b-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a34b-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteOperation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "id": "id-value",
  "status": "status-value",
  "createdDateTime": "2016-10-19T10:37:00Z",
  "lastActionDateTime": "2016-10-19T10:37:00Z",
  "resourceLocation": "resourceLocation-value",
  "resourceId": "resourceId-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get onenoteOperation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
