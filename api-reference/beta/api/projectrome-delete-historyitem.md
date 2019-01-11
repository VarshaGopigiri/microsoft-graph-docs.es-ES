---
title: Eliminar un historyItem
description: Eliminar un elemento de historial existente para una actividad de usuario existente.
localization_priority: Normal
ms.openlocfilehash: d9468034f3a98e949eeb9f2da28c4a74c42cd991
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834982"
---
# <a name="delete-a-historyitem"></a><span data-ttu-id="7d09e-103">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="7d09e-103">Delete a historyItem</span></span>

> <span data-ttu-id="7d09e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7d09e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7d09e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7d09e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7d09e-106">Eliminar un elemento de historial existente para una actividad de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="7d09e-106">Delete an existing history item for an existing user activity.</span></span>

## <a name="permissions"></a><span data-ttu-id="7d09e-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7d09e-107">Permissions</span></span>

<span data-ttu-id="7d09e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7d09e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="7d09e-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d09e-110">Permission type</span></span>      | <span data-ttu-id="7d09e-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d09e-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7d09e-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d09e-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7d09e-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="7d09e-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="7d09e-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d09e-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7d09e-115">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="7d09e-115">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="7d09e-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d09e-116">Application</span></span> | <span data-ttu-id="7d09e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7d09e-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7d09e-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d09e-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/activities/{id}/historyItems/{id}
```

## <a name="request-headers"></a><span data-ttu-id="7d09e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d09e-119">Request headers</span></span>

|<span data-ttu-id="7d09e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d09e-120">Name</span></span> | <span data-ttu-id="7d09e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d09e-121">Type</span></span> | <span data-ttu-id="7d09e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d09e-122">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="7d09e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7d09e-123">Authorization</span></span> | <span data-ttu-id="7d09e-124">string</span><span class="sxs-lookup"><span data-stu-id="7d09e-124">string</span></span> | <span data-ttu-id="7d09e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d09e-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7d09e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d09e-127">Request body</span></span>

<span data-ttu-id="7d09e-128">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d09e-128">No request body.</span></span>

## <a name="response"></a><span data-ttu-id="7d09e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d09e-129">Response</span></span>

<span data-ttu-id="7d09e-130">Si tiene éxito, este método devuelve el `204 No Content` código de respuesta si se ha eliminado el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="7d09e-130">If successful, this method returns the `204 No Content` response code if the history item was deleted.</span></span>

## <a name="example"></a><span data-ttu-id="7d09e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d09e-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="7d09e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d09e-132">Request</span></span>

<span data-ttu-id="7d09e-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d09e-133">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_historyItem"
}-->

```http
PUT https://graph.microsoft.com/beta/me/activities/13881113971988980728/historyItems/390e06e2-7e5b-4133-8014-fac7ac5991af
```

##### <a name="response"></a><span data-ttu-id="7d09e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d09e-134">Response</span></span>

<span data-ttu-id="7d09e-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d09e-135">Here is an example of the response.</span></span>

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
