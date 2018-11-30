---
title: Eliminar categoría de Outlook
description: Eliminar el objeto outlookCategory especificado.
ms.openlocfilehash: 4e28eff91c582fcb234c69cb9930c64c84d71724
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031993"
---
# <a name="delete-outlook-category"></a><span data-ttu-id="1fd07-103">Eliminar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="1fd07-103">Delete Outlook category</span></span>


<span data-ttu-id="1fd07-104">Eliminar el objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="1fd07-104">Delete the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="1fd07-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="1fd07-105">Permissions</span></span>
<span data-ttu-id="1fd07-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1fd07-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1fd07-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1fd07-108">Permission type</span></span>      | <span data-ttu-id="1fd07-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1fd07-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1fd07-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1fd07-110">Delegated (work or school account)</span></span> | <span data-ttu-id="1fd07-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1fd07-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="1fd07-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1fd07-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1fd07-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1fd07-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="1fd07-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1fd07-114">Application</span></span> | <span data-ttu-id="1fd07-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1fd07-115">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="1fd07-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1fd07-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/masterCategories/{id}
DELETE /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1fd07-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1fd07-117">Optional query parameters</span></span>
<span data-ttu-id="1fd07-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fd07-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1fd07-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1fd07-119">Request headers</span></span>
| <span data-ttu-id="1fd07-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="1fd07-120">Name</span></span>      |<span data-ttu-id="1fd07-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fd07-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1fd07-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1fd07-122">Authorization</span></span>  | <span data-ttu-id="1fd07-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1fd07-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1fd07-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1fd07-125">Request body</span></span>
<span data-ttu-id="1fd07-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1fd07-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1fd07-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fd07-127">Response</span></span>

<span data-ttu-id="1fd07-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fd07-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1fd07-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fd07-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1fd07-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1fd07-131">Request</span></span>
<span data-ttu-id="1fd07-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1fd07-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["4b1c2495-54c9-4a5e-90a2-0ab0b31987d8"],
  "name": "delete_outlookcategory"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/outlook/masterCategories/4b1c2495-54c9-4a5e-90a2-0ab0b31987d8
```
##### <a name="response"></a><span data-ttu-id="1fd07-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fd07-133">Response</span></span>
<span data-ttu-id="1fd07-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fd07-134">Here is an example of the response.</span></span>
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