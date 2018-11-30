---
title: Obtener sección
description: Recuperar las propiedades y relaciones de un objeto onenoteSection.
ms.openlocfilehash: ed4559e77d9acf96c850082e53bf6154aa10951a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030412"
---
# <a name="get-section"></a><span data-ttu-id="d16d9-103">Obtener sección</span><span class="sxs-lookup"><span data-stu-id="d16d9-103">Get section</span></span>

<span data-ttu-id="d16d9-104">Recuperar las propiedades y relaciones de un objeto [onenoteSection](../resources/section.md) .</span><span class="sxs-lookup"><span data-stu-id="d16d9-104">Retrieve the properties and relationships of a [onenoteSection](../resources/section.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="d16d9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="d16d9-105">Permissions</span></span>
<span data-ttu-id="d16d9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d16d9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d16d9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d16d9-108">Permission type</span></span>      | <span data-ttu-id="d16d9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d16d9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d16d9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d16d9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="d16d9-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d16d9-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="d16d9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d16d9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d16d9-113">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d16d9-113">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="d16d9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d16d9-114">Application</span></span> | <span data-ttu-id="d16d9-115">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d16d9-115">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d16d9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d16d9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections/{id}
GET /users/{id | userPrincipalName}/onenote/sections/{id}
GET /groups/{id}/onenote/sections/{id}
GET /sites/{id}/onenote/sections/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d16d9-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d16d9-117">Optional query parameters</span></span>
<span data-ttu-id="d16d9-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d16d9-118">This method supports the `select` and `expand` [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="d16d9-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="d16d9-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d16d9-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d16d9-121">Request headers</span></span>
| <span data-ttu-id="d16d9-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="d16d9-122">Name</span></span>       | <span data-ttu-id="d16d9-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d16d9-123">Type</span></span> | <span data-ttu-id="d16d9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d16d9-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d16d9-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="d16d9-125">Authorization</span></span>  | <span data-ttu-id="d16d9-126">string</span><span class="sxs-lookup"><span data-stu-id="d16d9-126">string</span></span>  | <span data-ttu-id="d16d9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d16d9-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d16d9-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d16d9-129">Accept</span></span> | <span data-ttu-id="d16d9-130">string</span><span class="sxs-lookup"><span data-stu-id="d16d9-130">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="d16d9-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d16d9-131">Request body</span></span>
<span data-ttu-id="d16d9-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d16d9-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d16d9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d16d9-133">Response</span></span>

<span data-ttu-id="d16d9-134">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [onenoteSection](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d16d9-134">If successful, this method returns a `200 OK` response code and a [onenoteSection](../resources/section.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d16d9-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d16d9-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d16d9-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d16d9-136">Request</span></span>
<span data-ttu-id="d16d9-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d16d9-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_section"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sections/{id}
```
##### <a name="response"></a><span data-ttu-id="d16d9-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d16d9-138">Response</span></span>
<span data-ttu-id="d16d9-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d16d9-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteSection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 272

{
  "isDefault": true,
  "pagesUrl": "pagesUrl-value",
  "displayName": "name-value",
  "createdBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  },
  "lastModifiedBy": {
    "user": {
      "id": "id-value",
      "displayName": "displayName-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get section",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->