---
title: Eliminar categoría de Outlook
description: Eliminar el objeto outlookCategory especificado.
author: angelgolfer-ms
ms.openlocfilehash: 1654b0d67e61ea9f999495eb239eb1d837690159
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321241"
---
# <a name="delete-outlook-category"></a><span data-ttu-id="03ebe-103">Eliminar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="03ebe-103">Delete Outlook category</span></span>

> <span data-ttu-id="03ebe-104">**Importante**: las API de la versión de /beta en Microsoft Graph está en vista preliminar y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="03ebe-104">**Important**: APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="03ebe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="03ebe-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="03ebe-106">Eliminar el objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="03ebe-106">Delete the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="03ebe-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="03ebe-107">Permissions</span></span>
<span data-ttu-id="03ebe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03ebe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="03ebe-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03ebe-110">Permission type</span></span>      | <span data-ttu-id="03ebe-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03ebe-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="03ebe-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03ebe-112">Delegated (work or school account)</span></span> | <span data-ttu-id="03ebe-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03ebe-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="03ebe-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03ebe-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="03ebe-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03ebe-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="03ebe-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03ebe-116">Application</span></span> | <span data-ttu-id="03ebe-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="03ebe-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="03ebe-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03ebe-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/masterCategories/{id}
DELETE /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="03ebe-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="03ebe-119">Optional query parameters</span></span>
<span data-ttu-id="03ebe-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03ebe-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="03ebe-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03ebe-121">Request headers</span></span>
| <span data-ttu-id="03ebe-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="03ebe-122">Name</span></span>      |<span data-ttu-id="03ebe-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="03ebe-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="03ebe-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="03ebe-124">Authorization</span></span>  | <span data-ttu-id="03ebe-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03ebe-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="03ebe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03ebe-127">Request body</span></span>
<span data-ttu-id="03ebe-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03ebe-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03ebe-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03ebe-129">Response</span></span>

<span data-ttu-id="03ebe-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03ebe-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03ebe-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03ebe-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="03ebe-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03ebe-133">Request</span></span>
<span data-ttu-id="03ebe-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03ebe-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_outlookcategory"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/outlook/masterCategories('4b1c2495-54c9-4a5e-90a2-0ab0b31987d8')
```
##### <a name="response"></a><span data-ttu-id="03ebe-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03ebe-135">Response</span></span>
<span data-ttu-id="03ebe-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03ebe-136">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "name": "delete_outlookcategory",
  "isEmpty": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->