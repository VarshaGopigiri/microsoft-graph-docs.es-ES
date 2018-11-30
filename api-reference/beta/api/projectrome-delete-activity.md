---
title: Eliminar una actividad
description: Eliminar una actividad de usuario existente para su aplicación.
ms.openlocfilehash: 9cdd52a2d3f417828e63107465dc28a4791a02e1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087849"
---
# <a name="delete-an-activity"></a><span data-ttu-id="79596-103">Eliminar una actividad</span><span class="sxs-lookup"><span data-stu-id="79596-103">Delete an activity</span></span>

> <span data-ttu-id="79596-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="79596-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="79596-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="79596-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="79596-106">Eliminar una actividad de usuario existente para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="79596-106">Delete an existing user activity for your app.</span></span>

## <a name="permissions"></a><span data-ttu-id="79596-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="79596-107">Permissions</span></span>

<span data-ttu-id="79596-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="79596-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="79596-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79596-110">Permission type</span></span>      | <span data-ttu-id="79596-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79596-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79596-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79596-112">Delegated (work or school account)</span></span> | <span data-ttu-id="79596-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="79596-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="79596-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79596-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79596-115">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="79596-115">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="79596-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79596-116">Application</span></span> | <span data-ttu-id="79596-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="79596-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="79596-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79596-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/activities/{id}
```

## <a name="request-headers"></a><span data-ttu-id="79596-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79596-119">Request headers</span></span>

|<span data-ttu-id="79596-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="79596-120">Name</span></span> | <span data-ttu-id="79596-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="79596-121">Type</span></span> | <span data-ttu-id="79596-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="79596-122">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="79596-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="79596-123">Authorization</span></span> | <span data-ttu-id="79596-124">string</span><span class="sxs-lookup"><span data-stu-id="79596-124">string</span></span> | <span data-ttu-id="79596-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79596-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="79596-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79596-127">Request body</span></span>

<span data-ttu-id="79596-128">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79596-128">No request body.</span></span>

## <a name="response"></a><span data-ttu-id="79596-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79596-129">Response</span></span>

<span data-ttu-id="79596-130">Si tiene éxito, este método devuelve el `204 No Content` código de respuesta si se ha eliminado la actividad.</span><span class="sxs-lookup"><span data-stu-id="79596-130">If successful, this method returns the `204 No Content` response code if the activity was deleted.</span></span>

## <a name="example"></a><span data-ttu-id="79596-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79596-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="79596-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79596-132">Request</span></span>

<span data-ttu-id="79596-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79596-133">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_activity"
}-->

```http
DELETE https://graph.microsoft.com/beta/me/activities/13881113971988980728/
```

##### <a name="response"></a><span data-ttu-id="79596-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79596-134">Response</span></span>

<span data-ttu-id="79596-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79596-135">Here is an example of the response.</span></span>

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
  "description": "Delete activity",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->