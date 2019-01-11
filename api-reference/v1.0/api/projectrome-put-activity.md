---
title: Crear o reemplazar una actividad
description: Crear una nueva o reemplazar una actividad de usuario existente para su aplicación. Si desea crear una actividad de usuario y su relacionados **historyItems** en una sola solicitud, puede usar Insertar profundo.
localization_priority: Normal
ms.openlocfilehash: faaebd5e3e88cca7c442be46505aac434111f148
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812085"
---
# <a name="create-or-replace-an-activity"></a><span data-ttu-id="e5e91-104">Crear o reemplazar una actividad</span><span class="sxs-lookup"><span data-stu-id="e5e91-104">Create or replace an activity</span></span>

<span data-ttu-id="e5e91-105">Crear una nueva o reemplazar una actividad de usuario existente para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5e91-105">Create a new or replace an existing user activity for your app.</span></span> <span data-ttu-id="e5e91-106">Si desea crear una actividad de usuario y su relacionados **historyItems** en una sola solicitud, puede usar [profundo insertar](projectrome-put-activity.md#example-2---deep-insert).</span><span class="sxs-lookup"><span data-stu-id="e5e91-106">If you'd like to create a user activity and its related **historyItems** in one request, you can use [deep insert](projectrome-put-activity.md#example-2---deep-insert).</span></span>

## <a name="permissions"></a><span data-ttu-id="e5e91-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5e91-107">Permissions</span></span>

<span data-ttu-id="e5e91-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e5e91-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="e5e91-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5e91-110">Permission type</span></span>      | <span data-ttu-id="e5e91-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5e91-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5e91-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5e91-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e5e91-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="e5e91-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="e5e91-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5e91-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5e91-115">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="e5e91-115">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="e5e91-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5e91-116">Application</span></span> | <span data-ttu-id="e5e91-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5e91-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e5e91-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5e91-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /me/activities/{appActivityId}
```

><span data-ttu-id="e5e91-119">**Nota:** El appActivityId en la dirección URL debe estar seguras de dirección URL (todos los caracteres excepto deben convertirse en su representación hexadecimal caracteres no reservados de RFC 2396), pero el appActivityId original no tiene que estar seguro de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="e5e91-119">**Note:** The appActivityId in the URL needs to be URL-safe (all characters except for RFC 2396 unreserved characters must be converted to their hexadecimal representation), but the original appActivityId does not have to be URL-safe.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e5e91-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5e91-120">Request headers</span></span>

|<span data-ttu-id="e5e91-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5e91-121">Name</span></span> | <span data-ttu-id="e5e91-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5e91-122">Type</span></span> | <span data-ttu-id="e5e91-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5e91-123">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="e5e91-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="e5e91-124">Authorization</span></span> | <span data-ttu-id="e5e91-125">string</span><span class="sxs-lookup"><span data-stu-id="e5e91-125">string</span></span> | <span data-ttu-id="e5e91-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5e91-p104">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e5e91-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5e91-128">Request body</span></span>

<span data-ttu-id="e5e91-129">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de la [actividad](../resources/projectrome-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="e5e91-129">In the request body, supply a JSON representation of an [activity](../resources/projectrome-activity.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e5e91-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5e91-130">Response</span></span>

<span data-ttu-id="e5e91-131">Si tiene éxito, este método devuelve el `201 Created` código de respuesta si se ha creado la actividad o `200 OK` si se ha reemplazado la actividad.</span><span class="sxs-lookup"><span data-stu-id="e5e91-131">If successful, this method returns the `201 Created` response code if the activity was created or `200 OK` if the activity was replaced.</span></span>

## <a name="example-1"></a><span data-ttu-id="e5e91-132">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5e91-132">Example 1</span></span>

#### <a name="request"></a><span data-ttu-id="e5e91-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5e91-133">Request</span></span>

<span data-ttu-id="e5e91-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5e91-134">The following is an example of the request.</span></span>

<!-- {
    "blockType": "ignored",
    "name": "upsert_activity"
} -->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/%2Farticle%3F12345
Content-type: application/json
Content-length: 364

{
    "appActivityId": "/article?12345",
    "activitySourceHost": "https://www.contoso.com",
    "userTimezone": "Africa/Casablanca",
    "appDisplayName": "Contoso, Ltd.",
    "activationUrl": "https://www.contoso.com/article?id=12345",
    "contentUrl": "https://www.contoso.com/article?id=12345",
    "fallbackUrl": "https://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "https://schema.org",
        "@type": "Article",
        "author": "Jennifer Booth",
        "name": "How to Tie a Reef Knot"
    },
    "visualElements": {
        "attribution": {
            "iconUrl": "https://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false,
        },
        "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
        "backgroundColor": "#ff0000",
        "displayText": "Contoso How-To: How to Tie a Reef Knot",
        "content": {
            "$schema": "https://adaptivecards.io/schemas/adaptive-card.json",
            "type": "AdaptiveCard",
            "body":
            [{
                "type": "TextBlock",
                "text": "Contoso MainPage"
            }]
        }
    }
}
```

#### <a name="response"></a><span data-ttu-id="e5e91-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5e91-135">Response</span></span>

<span data-ttu-id="e5e91-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5e91-136">The following is an example of the response.</span></span>

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.userActivity"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Location: https://graph.microsoft.com/v1.0/me/activities/14332800362997268276

{
    "activitySourceHost": "https://contoso.com",
    "createdDateTime": "2017-06-09T20:54:43.969Z",
    "lastModifiedDateTime": "2017-06-09T20:54:43.969Z",
    "id": "14332800362997268276",
    "appActivityId": "/article?12345",
    "status":"updated",
    "expirationDateTime": "2017-02-26T20:20:48.114Z",
    "id": "14332800362997268276",
    "visualElements": {
        "displayText": "Contoso How-To: How to Tie a Reef Knot",
        "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
        "attribution": {
            "iconUrl": "https://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false
        },
        "backgroundColor": "#ff0000",
        "content": {
            "$schema": "https://adaptivecards.io/schemas/adaptive-card.json",
            "type": "AdaptiveCard",
            "body":
            [{
                "type": "TextBlock",
                "text": "Contoso MainPage"
            }]
        }
    },
    "activationUrl": "https://www.contoso.com/article?id=12345",
    "appDisplayName": "Contoso, Ltd.",
    "userTimezone": "Africa/Casablanca",
    "fallbackUrl": "https://www.contoso.com/article?id=12345",
    "contentUrl": "https://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "https://schema.org",
        "@type": "Article",
        "author": "Jennifer Booth",
        "name": "How to Tie a Reef Knot"
    },
}
```

## <a name="example-2---deep-insert"></a><span data-ttu-id="e5e91-137">Ejemplo 2: insertar profundo</span><span class="sxs-lookup"><span data-stu-id="e5e91-137">Example 2 - Deep insert</span></span>

#### <a name="request"></a><span data-ttu-id="e5e91-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5e91-138">Request</span></span>

<span data-ttu-id="e5e91-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5e91-139">The following is an example of the request.</span></span>

<!-- {
    "blockType": "ignored",
    "name": "upsert_activity"
} -->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/%2Farticle%3F12345
Content-type: application/json
Content-length: 364

{
    "appActivityId": "/article?12345",
    "activitySourceHost": "https://www.contoso.com",
    "userTimezone": "Africa/Casablanca",
    "appDisplayName": "Contoso, Ltd.",
    "activationUrl": "https://www.contoso.com/article?id=12345",
    "contentUrl": "https://www.contoso.com/article?id=12345",
    "fallbackUrl": "https://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "https://schema.org",
        "@type": "Article",
        "author": "Jennifer Booth",
        "name": "How to Tie a Reef Knot"
    },
    "visualElements": {
        "attribution": {
            "iconUrl": "https://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false,
        },
        "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
        "backgroundColor": "#ff0000",
        "displayText": "Contoso How-To: How to Tie a Reef Knot",
        "content": {
            "$schema": "https://adaptivecards.io/schemas/adaptive-card.json",
            "type": "AdaptiveCard",
            "body":
            [{
                "type": "TextBlock",
                "text": "Contoso MainPage"
            }]
        }
    },
    "historyItems":[
        {
            "userTimezone": "Africa/Casablanca",
            "startedDateTime": "2018-02-26T20:54:04.345Z",
            "lastActiveDateTime": "2018-02-26T20:54:24.345Z",
        }
    ]
}
```

#### <a name="response"></a><span data-ttu-id="e5e91-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5e91-140">Response</span></span>

<span data-ttu-id="e5e91-141">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5e91-141">The following is an example of the response.</span></span>

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.userActivity"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Location: https://graph.microsoft.com/v1.0/me/activities/14332800362997268276

{
    "activitySourceHost": "https://contoso.com",
    "createdDateTime": "2017-06-09T20:54:43.969Z",
    "lastModifiedDateTime": "2017-06-09T20:54:43.969Z",
    "id": "14332800362997268276",
    "appActivityId": "/article?12345",
    "status":"updated",
    "expirationDateTime": "2017-02-26T20:20:48.114Z",
    "id": "14332800362997268276",
    "visualElements": {
        "displayText": "Contoso How-To: How to Tie a Reef Knot",
        "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
        "attribution": {
            "iconUrl": "https://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false
        },
        "backgroundColor": "#ff0000",
        "content": {
            "$schema": "https://adaptivecards.io/schemas/adaptive-card.json",
            "type": "AdaptiveCard",
            "body":
            [{
                "type": "TextBlock",
                "text": "Contoso MainPage"
            }]
        }
    },
    "activationUrl": "https://www.contoso.com/article?id=12345",
    "appDisplayName": "Contoso, Ltd.",
    "userTimezone": "Africa/Casablanca",
    "fallbackUrl": "https://www.contoso.com/article?id=12345",
    "contentUrl": "https://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "https://schema.org",
        "@type": "Article",
        "author": "Jennifer Booth",
        "name": "How to Tie a Reef Knot"
    },
    "historyItems":[
        {
            "status": "updated",
            "userTimezone": "Africa/Casablanca",
            "createdDateTime": "2018-04-12T21:42:42.495Z",
            "lastModifiedDateTime": "2018-04-12T21:42:42.495Z",
            "id": "61fc8f36-919f-4b73-89d4-1cb7b159d912",
            "startedDateTime": "2018-02-26T20:54:04.345Z",
            "lastActiveDateTime": "2018-02-26T20:54:24.345Z",
            "expirationDateTime": "2018-05-12T21:42:42.495Z",
            "activeDurationSeconds": 20
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Upsert activity",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
