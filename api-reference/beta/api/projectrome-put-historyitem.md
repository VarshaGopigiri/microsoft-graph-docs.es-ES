---
title: Crear o reemplazar un historyItem
description: Crear un nuevo o reemplazar un elemento de historial existente para una actividad de usuario existente.
ms.openlocfilehash: 068e5cb4b98879c1dba5eeef56517b99c3fe47c8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090828"
---
# <a name="create-or-replace-a-historyitem"></a><span data-ttu-id="bcc52-103">Crear o reemplazar un historyItem</span><span class="sxs-lookup"><span data-stu-id="bcc52-103">Create or replace a historyItem</span></span>

> <span data-ttu-id="bcc52-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bcc52-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bcc52-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bcc52-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bcc52-106">Crear un nuevo o reemplazar un elemento de historial existente para una actividad de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="bcc52-106">Create a new or replace an existing history item for an existing user activity.</span></span>

## <a name="permissions"></a><span data-ttu-id="bcc52-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="bcc52-107">Permissions</span></span>

<span data-ttu-id="bcc52-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bcc52-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="bcc52-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bcc52-110">Permission type</span></span>      | <span data-ttu-id="bcc52-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bcc52-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bcc52-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bcc52-112">Delegated (work or school account)</span></span> | <span data-ttu-id="bcc52-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="bcc52-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="bcc52-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bcc52-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bcc52-115">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="bcc52-115">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="bcc52-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bcc52-116">Application</span></span> | <span data-ttu-id="bcc52-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bcc52-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="bcc52-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bcc52-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /me/activities/{id}/historyItems/{id}
```

<span data-ttu-id="bcc52-119">Identificador debe ser un GUID.</span><span class="sxs-lookup"><span data-stu-id="bcc52-119">Id needs to be a GUID.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bcc52-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bcc52-120">Request headers</span></span>

|<span data-ttu-id="bcc52-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="bcc52-121">Name</span></span> | <span data-ttu-id="bcc52-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="bcc52-122">Type</span></span> | <span data-ttu-id="bcc52-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcc52-123">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="bcc52-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bcc52-124">Authorization</span></span> | <span data-ttu-id="bcc52-125">string</span><span class="sxs-lookup"><span data-stu-id="bcc52-125">string</span></span> | <span data-ttu-id="bcc52-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bcc52-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="bcc52-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bcc52-128">Request body</span></span>

<span data-ttu-id="bcc52-129">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [historyItem](../resources/projectrome-historyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="bcc52-129">In the request body, supply a JSON representation of a [historyItem](../resources/projectrome-historyitem.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="bcc52-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcc52-130">Response</span></span>

<span data-ttu-id="bcc52-131">Si tiene éxito, este método devuelve el `201 Created` código de respuesta si se ha creado la historyItem o `200 OK` si se ha sustituido el historyItem.</span><span class="sxs-lookup"><span data-stu-id="bcc52-131">If successful, this method returns the `201 Created` response code if the historyItem was created or `200 OK` if the historyItem was replaced.</span></span>

## <a name="example"></a><span data-ttu-id="bcc52-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bcc52-132">Example</span></span>

#### <a name="request"></a><span data-ttu-id="bcc52-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bcc52-133">Request</span></span>

<span data-ttu-id="bcc52-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bcc52-134">Here is an example of the request.</span></span>

<!-- {
    "blockType": "ignored",
    "name": "upsert_historyItem"
} -->

```http
PUT https://graph.microsoft.com/beta/me/activities/13881113971988980728/historyItems/390e06e2-7e5b-4133-8014-fac7ac5991af
Content-type: application/json
Content-length: 364

{
    "startedDateTime": "2015-02-11T20:54:04.3457274+00:00",
    "userTimezone": "Africa/Casablanca",
    "lastActiveDateTime": "2015-02-11T20:54:04.3457274+00:00"
}
```

#### <a name="response"></a><span data-ttu-id="bcc52-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bcc52-135">Response</span></span>

<span data-ttu-id="bcc52-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcc52-136">Here is an example of the response.</span></span>

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.historyItem"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#users('user%40contoso.com')/activities('13881113971988980728')/historyItems/$entity",
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