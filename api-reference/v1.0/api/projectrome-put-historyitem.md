---
title: Crear o reemplazar un historyItem
description: Crear un nuevo o reemplazar un elemento de historial existente para una actividad de usuario existente.
ms.openlocfilehash: a33c5cb295ce0cd954c37154bc85eac0322937e0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032196"
---
# <a name="create-or-replace-a-historyitem"></a><span data-ttu-id="f3c6a-103">Crear o reemplazar un historyItem</span><span class="sxs-lookup"><span data-stu-id="f3c6a-103">Create or replace a historyItem</span></span>

<span data-ttu-id="f3c6a-104">Crear un nuevo o reemplazar un elemento de historial existente para una actividad de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="f3c6a-104">Create a new or replace an existing history item for an existing user activity.</span></span>

## <a name="permissions"></a><span data-ttu-id="f3c6a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f3c6a-105">Permissions</span></span>

<span data-ttu-id="f3c6a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3c6a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="f3c6a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3c6a-108">Permission type</span></span>      | <span data-ttu-id="f3c6a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3c6a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f3c6a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3c6a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f3c6a-111">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="f3c6a-111">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="f3c6a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3c6a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3c6a-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="f3c6a-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="f3c6a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3c6a-114">Application</span></span> | <span data-ttu-id="f3c6a-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3c6a-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f3c6a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3c6a-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /me/activities/{id}/historyItems/{id}
```

<span data-ttu-id="f3c6a-117">Identificador debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="f3c6a-117">Id needs to be a GUID.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f3c6a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3c6a-118">Request headers</span></span>

|<span data-ttu-id="f3c6a-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3c6a-119">Name</span></span> | <span data-ttu-id="f3c6a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3c6a-120">Type</span></span> | <span data-ttu-id="f3c6a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3c6a-121">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="f3c6a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="f3c6a-122">Authorization</span></span> | <span data-ttu-id="f3c6a-123">string</span><span class="sxs-lookup"><span data-stu-id="f3c6a-123">string</span></span> | <span data-ttu-id="f3c6a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3c6a-p102">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f3c6a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f3c6a-126">Request body</span></span>

<span data-ttu-id="f3c6a-127">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [historyItem](../resources/projectrome-historyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c6a-127">In the request body, supply a JSON representation of a [historyItem](../resources/projectrome-historyitem.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="f3c6a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3c6a-128">Response</span></span>

<span data-ttu-id="f3c6a-129">Si tiene éxito, este método devuelve el `201 Created` código de respuesta si se ha creado la historyItem o `200 OK` si se ha sustituido el historyItem.</span><span class="sxs-lookup"><span data-stu-id="f3c6a-129">If successful, this method returns the `201 Created` response code if the historyItem was created or `200 OK` if the historyItem was replaced.</span></span>

## <a name="example"></a><span data-ttu-id="f3c6a-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3c6a-130">Example</span></span>

#### <a name="request"></a><span data-ttu-id="f3c6a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3c6a-131">Request</span></span>

<span data-ttu-id="f3c6a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3c6a-132">Here is an example of the request.</span></span>

<!-- {
    "blockType": "ignored",
    "name": "upsert_historyItem"
} -->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/{activity-id}/historyItems/{item-id}
Content-type: application/json
Content-length: 364

{
    "startedDateTime": "2015-02-11T20:54:04.3457274+00:00",
    "userTimezone": "Africa/Casablanca",
    "lastActiveDateTime": "2015-02-11T20:54:04.3457274+00:00"
}
```

#### <a name="response"></a><span data-ttu-id="f3c6a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3c6a-133">Response</span></span>

<span data-ttu-id="f3c6a-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3c6a-134">Here is an example of the response.</span></span>

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.activityHistoryItem"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('user%40contoso.com')/activities('13881113971988980728')/historyItems/$entity",
    "status": "updated",
    "userTimezone": "Africa/Casablanca",
    "createdDateTime": "2018-02-26T20:28:22.14Z",
    "lastModifiedDateTime": "2018-02-26T20:28:22.155Z",
    "id": "9d0b74e4-4b41-43ea-b34d-f9c1bf9f809c",
    "startedDateTime": "2018-02-26T20:54:04.345Z",
    "lastActiveDateTime": "2018-02-26T20:54:24.345Z",
    "expirationDateTime": "2018-03-28T20:28:22.14Z",
    "activeDurationSeconds": 20
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Upsert historyitem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->