---
title: Obtener categoría de Outlook
description: Obtener las propiedades y relaciones del objeto outlookCategory especificado.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 6a7a64c572754dc8256693781c5c540a13c1c53f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864130"
---
# <a name="get-outlook-category"></a><span data-ttu-id="05323-103">Obtener categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="05323-103">Get Outlook category</span></span>


<span data-ttu-id="05323-104">Obtener las propiedades y relaciones del objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="05323-104">Get the properties and relationships of the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="05323-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="05323-105">Permissions</span></span>
<span data-ttu-id="05323-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05323-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="05323-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05323-108">Permission type</span></span>      | <span data-ttu-id="05323-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05323-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="05323-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05323-110">Delegated (work or school account)</span></span> | <span data-ttu-id="05323-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="05323-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="05323-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05323-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05323-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="05323-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="05323-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05323-114">Application</span></span> | <span data-ttu-id="05323-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="05323-115">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="05323-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05323-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/masterCategories/{id}
GET /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="05323-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="05323-117">Optional query parameters</span></span>
<span data-ttu-id="05323-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05323-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="05323-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05323-119">Request headers</span></span>
| <span data-ttu-id="05323-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="05323-120">Name</span></span>      |<span data-ttu-id="05323-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="05323-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="05323-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="05323-122">Authorization</span></span>  | <span data-ttu-id="05323-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05323-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="05323-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05323-125">Request body</span></span>
<span data-ttu-id="05323-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="05323-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="05323-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05323-127">Response</span></span>

<span data-ttu-id="05323-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05323-128">If successful, this method returns a `200 OK` response code and [outlookCategory](../resources/outlookcategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="05323-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05323-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="05323-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05323-130">Request</span></span>
<span data-ttu-id="05323-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05323-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["de912e4d-c790-4da9-949c-ccd933aaa0f7"],
  "name": "get_outlookcategory"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/masterCategories/de912e4d-c790-4da9-949c-ccd933aaa0f7
```
##### <a name="response"></a><span data-ttu-id="05323-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05323-132">Response</span></span>
<span data-ttu-id="05323-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05323-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 249

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
  "id":"de912e4d-c790-4da9-949c-ccd933aaa0f7",
  "displayName":"Yellow category",
  "color":"preset3"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
