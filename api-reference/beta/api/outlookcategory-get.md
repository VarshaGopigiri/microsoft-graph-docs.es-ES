---
title: Obtener categoría de Outlook
description: Obtener las propiedades y relaciones del objeto outlookCategory especificado.
ms.openlocfilehash: b8447dd3d9efe90390b5c2160a50dfa290c07883
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088162"
---
# <a name="get-outlook-category"></a><span data-ttu-id="eb749-103">Obtener categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="eb749-103">Get Outlook category</span></span>

> <span data-ttu-id="eb749-104">**Importante**: las API de la versión de /beta en Microsoft Graph está en vista preliminar y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb749-104">**Important**: APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb749-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb749-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eb749-106">Obtener las propiedades y relaciones del objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="eb749-106">Get the properties and relationships of the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="eb749-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="eb749-107">Permissions</span></span>
<span data-ttu-id="eb749-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb749-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb749-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb749-110">Permission type</span></span>      | <span data-ttu-id="eb749-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb749-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eb749-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb749-112">Delegated (work or school account)</span></span> | <span data-ttu-id="eb749-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="eb749-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="eb749-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb749-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eb749-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="eb749-115">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="eb749-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb749-116">Application</span></span> | <span data-ttu-id="eb749-117">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="eb749-117">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="eb749-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb749-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/masterCategories/{id}
GET /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="eb749-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="eb749-119">Optional query parameters</span></span>
<span data-ttu-id="eb749-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb749-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="eb749-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb749-121">Request headers</span></span>
| <span data-ttu-id="eb749-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb749-122">Name</span></span>      |<span data-ttu-id="eb749-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb749-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="eb749-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="eb749-124">Authorization</span></span>  | <span data-ttu-id="eb749-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb749-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eb749-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb749-127">Request body</span></span>
<span data-ttu-id="eb749-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eb749-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eb749-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb749-129">Response</span></span>

<span data-ttu-id="eb749-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb749-130">If successful, this method returns a `200 OK` response code and [outlookCategory](../resources/outlookcategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="eb749-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb749-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eb749-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb749-132">Request</span></span>
<span data-ttu-id="eb749-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb749-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_outlookcategory"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/masterCategories('de912e4d-c790-4da9-949c-ccd933aaa0f7')
```
##### <a name="response"></a><span data-ttu-id="eb749-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb749-134">Response</span></span>
<span data-ttu-id="eb749-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb749-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
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