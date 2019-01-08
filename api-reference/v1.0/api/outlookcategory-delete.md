---
title: Eliminar categoría de Outlook
description: Eliminar el objeto outlookCategory especificado.
author: angelgolfer-ms
ms.openlocfilehash: b82125c33c7b11274bfee80d9d1949ea776745c4
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748496"
---
# <a name="delete-outlook-category"></a><span data-ttu-id="c789b-103">Eliminar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="c789b-103">Delete Outlook category</span></span>


<span data-ttu-id="c789b-104">Eliminar el objeto [outlookCategory](../resources/outlookcategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="c789b-104">Delete the specified [outlookCategory](../resources/outlookcategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="c789b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c789b-105">Permissions</span></span>
<span data-ttu-id="c789b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c789b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c789b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c789b-108">Permission type</span></span>      | <span data-ttu-id="c789b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c789b-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c789b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c789b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c789b-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c789b-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="c789b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c789b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c789b-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c789b-113">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="c789b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c789b-114">Application</span></span> | <span data-ttu-id="c789b-115">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c789b-115">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c789b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c789b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/masterCategories/{id}
DELETE /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```

## <a name="request-headers"></a><span data-ttu-id="c789b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c789b-117">Request headers</span></span>
| <span data-ttu-id="c789b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c789b-118">Name</span></span>      |<span data-ttu-id="c789b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c789b-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c789b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c789b-120">Authorization</span></span>  | <span data-ttu-id="c789b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c789b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c789b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c789b-123">Request body</span></span>
<span data-ttu-id="c789b-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c789b-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c789b-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c789b-125">Response</span></span>

<span data-ttu-id="c789b-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c789b-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c789b-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c789b-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c789b-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c789b-129">Request</span></span>
<span data-ttu-id="c789b-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c789b-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["4b1c2495-54c9-4a5e-90a2-0ab0b31987d8"],
  "name": "delete_outlookcategory"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/outlook/masterCategories/4b1c2495-54c9-4a5e-90a2-0ab0b31987d8
```
##### <a name="response"></a><span data-ttu-id="c789b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c789b-131">Response</span></span>
<span data-ttu-id="c789b-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c789b-132">Here is an example of the response.</span></span>
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