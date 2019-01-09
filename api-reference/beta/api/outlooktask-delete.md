---
title: Eliminar outlookTask
description: Eliminar la tarea de Outlook especificada en el buzón del usuario.
ms.openlocfilehash: cab78b8fea63c5044cc6faa6a1e4f09dd960bfd6
ms.sourcegitcommit: 6b1ba9b3be038cd6247de54a255bad560034fe42
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27771782"
---
# <a name="delete-outlooktask"></a><span data-ttu-id="0c6d8-103">Eliminar outlookTask</span><span class="sxs-lookup"><span data-stu-id="0c6d8-103">Delete outlookTask</span></span>

> <span data-ttu-id="0c6d8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0c6d8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0c6d8-106">Eliminar la tarea de Outlook especificada en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-106">Delete the specified Outlook task in the user's mailbox.</span></span>

## <a name="permissions"></a><span data-ttu-id="0c6d8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0c6d8-107">Permissions</span></span>

<span data-ttu-id="0c6d8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0c6d8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0c6d8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0c6d8-110">Permission type</span></span>      | <span data-ttu-id="0c6d8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0c6d8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0c6d8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0c6d8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="0c6d8-113">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0c6d8-113">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="0c6d8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0c6d8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0c6d8-115">Tasks.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0c6d8-115">Tasks.ReadWrite</span></span>    |
|<span data-ttu-id="0c6d8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0c6d8-116">Application</span></span> | <span data-ttu-id="0c6d8-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0c6d8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0c6d8-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/outlook/tasks/{id}
DELETE /users/{id|userPrincipalName}/outlook/tasks/{id}
```

## <a name="request-headers"></a><span data-ttu-id="0c6d8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6d8-119">Request headers</span></span>

| <span data-ttu-id="0c6d8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c6d8-120">Name</span></span>       | <span data-ttu-id="0c6d8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c6d8-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0c6d8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0c6d8-122">Authorization</span></span>  | <span data-ttu-id="0c6d8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0c6d8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6d8-125">Request body</span></span>

<span data-ttu-id="0c6d8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0c6d8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c6d8-127">Response</span></span>

<span data-ttu-id="0c6d8-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0c6d8-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c6d8-130">Example</span></span>

### <a name="request"></a><span data-ttu-id="0c6d8-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6d8-131">Request</span></span>

<span data-ttu-id="0c6d8-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_outlooktask"
}-->

```http
DELETE https://graph.microsoft.com/beta/me/outlook/tasks('AAMkADIyAAAhrb_QAAA=')
```

### <a name="response"></a><span data-ttu-id="0c6d8-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c6d8-133">Response</span></span>

<span data-ttu-id="0c6d8-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c6d8-134">Here is an example of the response.</span></span>
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
  "description": "Delete outlookTask",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->