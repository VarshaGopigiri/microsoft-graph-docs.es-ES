---
title: Eliminar categoría de Outlook
description: Eliminar el objeto outlookCategory especificado.
ms.openlocfilehash: a240df167918892face0da8932af0f2ff3d23152
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085001"
---
# <a name="delete-outlook-category"></a><span data-ttu-id="28a34-103">Eliminar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="28a34-103">Delete Outlook category</span></span>

> <span data-ttu-id="28a34-104">**Importante**: las API de la versión de /beta en Microsoft Graph está en vista preliminar y están sujetos a cambios.</span><span class="sxs-lookup"><span data-stu-id="28a34-104">**Important**: APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="28a34-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="28a34-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="28a34-106">Eliminar el objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="28a34-106">Delete the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="28a34-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="28a34-107">Permissions</span></span>
<span data-ttu-id="28a34-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="28a34-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="28a34-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="28a34-110">Permission type</span></span>      | <span data-ttu-id="28a34-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="28a34-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="28a34-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="28a34-112">Delegated (work or school account)</span></span> | <span data-ttu-id="28a34-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="28a34-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="28a34-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="28a34-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="28a34-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="28a34-115">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="28a34-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="28a34-116">Application</span></span> | <span data-ttu-id="28a34-117">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="28a34-117">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="28a34-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28a34-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/masterCategories/{id}
DELETE /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="28a34-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="28a34-119">Optional query parameters</span></span>
<span data-ttu-id="28a34-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28a34-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="28a34-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28a34-121">Request headers</span></span>
| <span data-ttu-id="28a34-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="28a34-122">Name</span></span>      |<span data-ttu-id="28a34-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="28a34-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="28a34-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="28a34-124">Authorization</span></span>  | <span data-ttu-id="28a34-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="28a34-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="28a34-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28a34-127">Request body</span></span>
<span data-ttu-id="28a34-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="28a34-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="28a34-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28a34-129">Response</span></span>

<span data-ttu-id="28a34-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28a34-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="28a34-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28a34-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="28a34-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28a34-133">Request</span></span>
<span data-ttu-id="28a34-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="28a34-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_outlookcategory"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/outlook/masterCategories('4b1c2495-54c9-4a5e-90a2-0ab0b31987d8')
```
##### <a name="response"></a><span data-ttu-id="28a34-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28a34-135">Response</span></span>
<span data-ttu-id="28a34-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28a34-136">Here is an example of the response.</span></span>
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