---
title: Eliminar un historyItem
description: Eliminar un elemento de historial existente para una actividad de usuario existente.
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: 30e7ee53e6546d6c70e3d576e0e2eb57965cf46f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979862"
---
# <a name="delete-a-historyitem"></a><span data-ttu-id="29079-103">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="29079-103">Delete a historyItem</span></span>

> <span data-ttu-id="29079-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="29079-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="29079-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="29079-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="29079-106">Eliminar un elemento de historial existente para una actividad de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="29079-106">Delete an existing history item for an existing user activity.</span></span>

## <a name="permissions"></a><span data-ttu-id="29079-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="29079-107">Permissions</span></span>

<span data-ttu-id="29079-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="29079-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="29079-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="29079-110">Permission type</span></span>      | <span data-ttu-id="29079-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="29079-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="29079-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="29079-112">Delegated (work or school account)</span></span> | <span data-ttu-id="29079-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="29079-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="29079-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="29079-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="29079-115">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="29079-115">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="29079-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="29079-116">Application</span></span> | <span data-ttu-id="29079-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29079-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="29079-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="29079-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/activities/{id}/historyItems/{id}
```

## <a name="request-headers"></a><span data-ttu-id="29079-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="29079-119">Request headers</span></span>

|<span data-ttu-id="29079-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="29079-120">Name</span></span> | <span data-ttu-id="29079-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="29079-121">Type</span></span> | <span data-ttu-id="29079-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="29079-122">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="29079-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="29079-123">Authorization</span></span> | <span data-ttu-id="29079-124">string</span><span class="sxs-lookup"><span data-stu-id="29079-124">string</span></span> | <span data-ttu-id="29079-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="29079-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="29079-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="29079-127">Request body</span></span>

<span data-ttu-id="29079-128">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29079-128">No request body.</span></span>

## <a name="response"></a><span data-ttu-id="29079-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29079-129">Response</span></span>

<span data-ttu-id="29079-130">Si tiene éxito, este método devuelve el `204 No Content` código de respuesta si se ha eliminado el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="29079-130">If successful, this method returns the `204 No Content` response code if the history item was deleted.</span></span>

## <a name="example"></a><span data-ttu-id="29079-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29079-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="29079-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="29079-132">Request</span></span>

<span data-ttu-id="29079-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29079-133">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_historyItem"
}-->

```http
PUT https://graph.microsoft.com/beta/me/activities/13881113971988980728/historyItems/390e06e2-7e5b-4133-8014-fac7ac5991af
```

##### <a name="response"></a><span data-ttu-id="29079-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29079-134">Response</span></span>

<span data-ttu-id="29079-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29079-135">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete historyitem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
