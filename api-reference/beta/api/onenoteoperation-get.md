---
title: Obtener onenoteOperation
description: 'Obtenga el estado de una operación de larga duración de OneNote. Esto se aplica a las operaciones que devuelvan el encabezado **Operation-Location** en la respuesta, como `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup` y `and CopyToSection`.   '
localization_priority: Normal
ms.openlocfilehash: b62f83266560f217d9569c6ee7ca39dd53198bb7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824769"
---
# <a name="get-onenoteoperation"></a><span data-ttu-id="c7add-104">Obtener onenoteOperation</span><span class="sxs-lookup"><span data-stu-id="c7add-104">Get onenoteOperation</span></span>

> <span data-ttu-id="c7add-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c7add-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c7add-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c7add-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c7add-p103">Obtenga el estado de una operación de larga duración de OneNote. Esto se aplica a las operaciones que devuelvan el encabezado **Operation-Location** en la respuesta, como `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup` y `and CopyToSection`.</span><span class="sxs-lookup"><span data-stu-id="c7add-p103">Get the status of a long-running OneNote operation. This applies to operations that return the **Operation-Location** header in the response, such as `CopyNotebook`, `CopyToNotebook`, `CopyToSectionGroup`, `and CopyToSection`.</span></span>   

<span data-ttu-id="c7add-109">Puede sondear el extremo de Operation-Location hasta que la propiedad de `status` devuelva `completed` o `failed`.</span><span class="sxs-lookup"><span data-stu-id="c7add-109">You can poll the Operation-Location endpoint until the `status` property returns `completed` or `failed`.</span></span> 

<span data-ttu-id="c7add-110">Si el estado es `completed`, la propiedad de `resourceLocation` contiene el URI del extremo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7add-110">If the status is `completed`, the `resourceLocation` property contains the resource endpoint URI.</span></span> 

<span data-ttu-id="c7add-111">Si el estado es `failed`, el error y las propiedades de `@api.diagnostics` facilitan información del error.</span><span class="sxs-lookup"><span data-stu-id="c7add-111">If the status is `failed`, the error and `@api.diagnostics` properties provide error information.</span></span>

## <a name="permissions"></a><span data-ttu-id="c7add-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="c7add-112">Permissions</span></span>
<span data-ttu-id="c7add-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7add-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7add-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7add-115">Permission type</span></span>      | <span data-ttu-id="c7add-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7add-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c7add-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7add-117">Delegated (work or school account)</span></span> | <span data-ttu-id="c7add-118">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7add-118">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="c7add-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7add-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c7add-120">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c7add-120">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="c7add-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7add-121">Application</span></span> | <span data-ttu-id="c7add-122">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7add-122">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c7add-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7add-123">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/operations/{id}
GET /users/{id | userPrincipalName}/onenote/operations/{id}
GET /groups/{id}/onenote/operations/{id}
GET /sites/{id}/onenote/operations/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c7add-124">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c7add-124">Optional query parameters</span></span>
<span data-ttu-id="c7add-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7add-125">None.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c7add-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7add-126">Request headers</span></span>
| <span data-ttu-id="c7add-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="c7add-127">Name</span></span>       | <span data-ttu-id="c7add-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7add-128">Type</span></span> | <span data-ttu-id="c7add-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7add-129">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c7add-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="c7add-130">Authorization</span></span>  | <span data-ttu-id="c7add-131">string</span><span class="sxs-lookup"><span data-stu-id="c7add-131">string</span></span>  | <span data-ttu-id="c7add-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7add-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c7add-134">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c7add-134">Accept</span></span> | <span data-ttu-id="c7add-135">string</span><span class="sxs-lookup"><span data-stu-id="c7add-135">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="c7add-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7add-136">Request body</span></span>
<span data-ttu-id="c7add-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c7add-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7add-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7add-138">Response</span></span>

<span data-ttu-id="c7add-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [onenoteOperation](../resources/onenoteoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7add-139">If successful, this method returns a `200 OK` response code and [onenoteOperation](../resources/onenoteoperation.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c7add-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7add-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c7add-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7add-141">Request</span></span>
<span data-ttu-id="c7add-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7add-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_onenoteoperation"
}-->
```http
GET https://graph.microsoft.com/beta/me/onenote/operations/{id}
```
##### <a name="response"></a><span data-ttu-id="c7add-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7add-143">Response</span></span>
<span data-ttu-id="c7add-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7add-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
