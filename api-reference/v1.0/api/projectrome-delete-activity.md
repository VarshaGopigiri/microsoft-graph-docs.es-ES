---
title: Eliminar una actividad
description: Eliminar una actividad de usuario existente para su aplicación.
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: cbe12a373f06c2893a5ca202247865f4ce4a8f52
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966856"
---
# <a name="delete-an-activity"></a><span data-ttu-id="c462f-103">Eliminar una actividad</span><span class="sxs-lookup"><span data-stu-id="c462f-103">Delete an activity</span></span>

<span data-ttu-id="c462f-104">Eliminar una actividad de usuario existente para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="c462f-104">Delete an existing user activity for your app.</span></span>

## <a name="permissions"></a><span data-ttu-id="c462f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c462f-105">Permissions</span></span>

<span data-ttu-id="c462f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c462f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="c462f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c462f-108">Permission type</span></span>      | <span data-ttu-id="c462f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c462f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c462f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c462f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c462f-111">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="c462f-111">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="c462f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c462f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c462f-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="c462f-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="c462f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c462f-114">Application</span></span> | <span data-ttu-id="c462f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c462f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="c462f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c462f-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/activities/{id}
```

## <a name="request-headers"></a><span data-ttu-id="c462f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c462f-117">Request headers</span></span>

|<span data-ttu-id="c462f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c462f-118">Name</span></span> | <span data-ttu-id="c462f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c462f-119">Type</span></span> | <span data-ttu-id="c462f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c462f-120">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="c462f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="c462f-121">Authorization</span></span> | <span data-ttu-id="c462f-122">string</span><span class="sxs-lookup"><span data-stu-id="c462f-122">string</span></span> | <span data-ttu-id="c462f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c462f-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c462f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c462f-125">Request body</span></span>

<span data-ttu-id="c462f-126">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c462f-126">No request body.</span></span>

## <a name="response"></a><span data-ttu-id="c462f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c462f-127">Response</span></span>

<span data-ttu-id="c462f-128">Si tiene éxito, este método devuelve el `204 No Content` código de respuesta si se ha eliminado la actividad.</span><span class="sxs-lookup"><span data-stu-id="c462f-128">If successful, this method returns the `204 No Content` response code if the activity was deleted.</span></span>

## <a name="example"></a><span data-ttu-id="c462f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c462f-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c462f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c462f-130">Request</span></span>

<span data-ttu-id="c462f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c462f-131">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_activity"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/me/activities/{activity-id}/
```

##### <a name="response"></a><span data-ttu-id="c462f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c462f-132">Response</span></span>

<span data-ttu-id="c462f-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c462f-133">Here is an example of the response.</span></span>

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
