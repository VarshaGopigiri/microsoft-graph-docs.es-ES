---
title: Obtener categoría de Outlook
description: Obtener las propiedades y relaciones del objeto outlookCategory especificado.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 4359c3bd87a5eecc3d8b153538b15039ab8be7c6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934908"
---
# <a name="get-outlook-category"></a><span data-ttu-id="bd9a5-103">Obtener categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="bd9a5-103">Get Outlook category</span></span>


<span data-ttu-id="bd9a5-104">Obtener las propiedades y relaciones del objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="bd9a5-104">Get the properties and relationships of the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="bd9a5-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd9a5-105">Permissions</span></span>
<span data-ttu-id="bd9a5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bd9a5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bd9a5-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd9a5-108">Permission type</span></span>      | <span data-ttu-id="bd9a5-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd9a5-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bd9a5-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd9a5-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bd9a5-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="bd9a5-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="bd9a5-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd9a5-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bd9a5-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="bd9a5-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="bd9a5-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd9a5-114">Application</span></span> | <span data-ttu-id="bd9a5-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="bd9a5-115">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="bd9a5-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd9a5-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/masterCategories/{id}
GET /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bd9a5-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bd9a5-117">Optional query parameters</span></span>
<span data-ttu-id="bd9a5-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd9a5-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bd9a5-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd9a5-119">Request headers</span></span>
| <span data-ttu-id="bd9a5-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd9a5-120">Name</span></span>      |<span data-ttu-id="bd9a5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd9a5-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="bd9a5-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="bd9a5-122">Authorization</span></span>  | <span data-ttu-id="bd9a5-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd9a5-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bd9a5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd9a5-125">Request body</span></span>
<span data-ttu-id="bd9a5-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bd9a5-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bd9a5-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd9a5-127">Response</span></span>

<span data-ttu-id="bd9a5-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd9a5-128">If successful, this method returns a `200 OK` response code and [outlookCategory](../resources/outlookcategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bd9a5-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd9a5-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bd9a5-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd9a5-130">Request</span></span>
<span data-ttu-id="bd9a5-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd9a5-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["de912e4d-c790-4da9-949c-ccd933aaa0f7"],
  "name": "get_outlookcategory"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/masterCategories/de912e4d-c790-4da9-949c-ccd933aaa0f7
```
##### <a name="response"></a><span data-ttu-id="bd9a5-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd9a5-132">Response</span></span>
<span data-ttu-id="bd9a5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd9a5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
