---
title: Eliminación de aplicación
description: Elimina una aplicación.
ms.openlocfilehash: fc1f315de3e12574d51c58c56c1f37f39bdcd980
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085958"
---
# <a name="delete-application"></a><span data-ttu-id="d975a-103">Eliminación de aplicación</span><span class="sxs-lookup"><span data-stu-id="d975a-103">Delete application</span></span>

> <span data-ttu-id="d975a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d975a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d975a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d975a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d975a-106">Elimina una aplicación.</span><span class="sxs-lookup"><span data-stu-id="d975a-106">Deletes an application.</span></span>

## <a name="permissions"></a><span data-ttu-id="d975a-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="d975a-107">Permissions</span></span>
<span data-ttu-id="d975a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d975a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d975a-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d975a-110">Permission type</span></span>      | <span data-ttu-id="d975a-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d975a-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d975a-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d975a-112">Delegated (work or school account)</span></span> | <span data-ttu-id="d975a-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d975a-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d975a-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d975a-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d975a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d975a-115">Not supported.</span></span>    |
|<span data-ttu-id="d975a-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d975a-116">Application</span></span> | <span data-ttu-id="d975a-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d975a-117">Application.ReadWrite.OwnedBy, Application.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d975a-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d975a-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /applications/{id}
```

## <a name="request-headers"></a><span data-ttu-id="d975a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d975a-119">Request headers</span></span>
| <span data-ttu-id="d975a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="d975a-120">Name</span></span>       | <span data-ttu-id="d975a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="d975a-121">Type</span></span> | <span data-ttu-id="d975a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="d975a-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d975a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d975a-123">Authorization</span></span>  | <span data-ttu-id="d975a-124">string</span><span class="sxs-lookup"><span data-stu-id="d975a-124">string</span></span>  | <span data-ttu-id="d975a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d975a-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d975a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d975a-127">Request body</span></span>
<span data-ttu-id="d975a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d975a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d975a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d975a-129">Response</span></span>

<span data-ttu-id="d975a-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d975a-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d975a-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d975a-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d975a-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d975a-133">Request</span></span>
<span data-ttu-id="d975a-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d975a-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_application"
}-->
```http
DELETE https://graph.microsoft.com/beta/applications/{id}
```
##### <a name="response"></a><span data-ttu-id="d975a-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d975a-135">Response</span></span>
<span data-ttu-id="d975a-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d975a-136">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete application",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->