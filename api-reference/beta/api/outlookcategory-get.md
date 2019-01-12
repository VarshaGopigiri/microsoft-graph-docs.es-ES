---
title: Obtener categoría de Outlook
description: Obtener las propiedades y relaciones del objeto outlookCategory especificado.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: c296aea62fec7090cb76607911f6be178f1ebdbb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949720"
---
# <a name="get-outlook-category"></a><span data-ttu-id="41bbe-103">Obtener categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="41bbe-103">Get Outlook category</span></span>

> <span data-ttu-id="41bbe-104">**Importante**: las API de la versión de /beta en Microsoft Graph está en vista preliminar y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="41bbe-104">**Important**: APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41bbe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="41bbe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="41bbe-106">Obtener las propiedades y relaciones del objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="41bbe-106">Get the properties and relationships of the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="41bbe-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="41bbe-107">Permissions</span></span>
<span data-ttu-id="41bbe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41bbe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="41bbe-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41bbe-110">Permission type</span></span>      | <span data-ttu-id="41bbe-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41bbe-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="41bbe-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41bbe-112">Delegated (work or school account)</span></span> | <span data-ttu-id="41bbe-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="41bbe-113">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="41bbe-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41bbe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="41bbe-115">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="41bbe-115">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="41bbe-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41bbe-116">Application</span></span> | <span data-ttu-id="41bbe-117">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="41bbe-117">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="41bbe-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41bbe-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/masterCategories/{id}
GET /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="41bbe-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="41bbe-119">Optional query parameters</span></span>
<span data-ttu-id="41bbe-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41bbe-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="41bbe-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41bbe-121">Request headers</span></span>
| <span data-ttu-id="41bbe-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="41bbe-122">Name</span></span>      |<span data-ttu-id="41bbe-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="41bbe-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="41bbe-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="41bbe-124">Authorization</span></span>  | <span data-ttu-id="41bbe-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="41bbe-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="41bbe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41bbe-127">Request body</span></span>
<span data-ttu-id="41bbe-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="41bbe-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="41bbe-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41bbe-129">Response</span></span>

<span data-ttu-id="41bbe-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookcategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41bbe-130">If successful, this method returns a `200 OK` response code and [outlookCategory](../resources/outlookcategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="41bbe-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41bbe-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="41bbe-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41bbe-132">Request</span></span>
<span data-ttu-id="41bbe-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41bbe-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_outlookcategory"
}-->
```http
GET https://graph.microsoft.com/beta/me/outlook/masterCategories('de912e4d-c790-4da9-949c-ccd933aaa0f7')
```
##### <a name="response"></a><span data-ttu-id="41bbe-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41bbe-134">Response</span></span>
<span data-ttu-id="41bbe-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41bbe-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
