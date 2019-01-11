---
title: Eliminar un historyItem
description: Eliminar un elemento de historial existente para una actividad de usuario existente.
localization_priority: Normal
ms.openlocfilehash: 3476aba19a2de09f5b4c168ab2a4075b74fd2a93
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861925"
---
# <a name="delete-a-historyitem"></a><span data-ttu-id="43790-103">Eliminar un historyItem</span><span class="sxs-lookup"><span data-stu-id="43790-103">Delete a historyItem</span></span>

<span data-ttu-id="43790-104">Eliminar un elemento de historial existente para una actividad de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="43790-104">Delete an existing history item for an existing user activity.</span></span>

## <a name="permissions"></a><span data-ttu-id="43790-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="43790-105">Permissions</span></span>

<span data-ttu-id="43790-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43790-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="43790-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43790-108">Permission type</span></span>      | <span data-ttu-id="43790-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43790-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="43790-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43790-110">Delegated (work or school account)</span></span> | <span data-ttu-id="43790-111">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="43790-111">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="43790-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43790-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43790-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="43790-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="43790-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43790-114">Application</span></span> | <span data-ttu-id="43790-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43790-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="43790-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43790-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/activities/{id}/historyItems/{id}
```

## <a name="request-headers"></a><span data-ttu-id="43790-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43790-117">Request headers</span></span>

|<span data-ttu-id="43790-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="43790-118">Name</span></span> | <span data-ttu-id="43790-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="43790-119">Type</span></span> | <span data-ttu-id="43790-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="43790-120">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="43790-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="43790-121">Authorization</span></span> | <span data-ttu-id="43790-122">string</span><span class="sxs-lookup"><span data-stu-id="43790-122">string</span></span> | <span data-ttu-id="43790-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43790-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="43790-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43790-125">Request body</span></span>

<span data-ttu-id="43790-126">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43790-126">No request body.</span></span>

## <a name="response"></a><span data-ttu-id="43790-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43790-127">Response</span></span>

<span data-ttu-id="43790-128">Si tiene éxito, este método devuelve el `204 No Content` código de respuesta si se ha eliminado el elemento de historial.</span><span class="sxs-lookup"><span data-stu-id="43790-128">If successful, this method returns the `204 No Content` response code if the history item was deleted.</span></span>

## <a name="example"></a><span data-ttu-id="43790-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43790-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="43790-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43790-130">Request</span></span>

<span data-ttu-id="43790-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43790-131">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_historyItem"
}-->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/{activity-id}/historyItems/{item-id}
```

##### <a name="response"></a><span data-ttu-id="43790-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43790-132">Response</span></span>

<span data-ttu-id="43790-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43790-133">Here is an example of the response.</span></span>

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
