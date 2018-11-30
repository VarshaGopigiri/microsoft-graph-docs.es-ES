---
title: Crear o reemplazar una actividad
description: Crear una nueva o reemplazar una actividad de usuario existente para su aplicación. Si desea crear una actividad de usuario y su relacionados **historyItems** en una sola solicitud, puede usar Insertar profundo.
ms.openlocfilehash: 1a749f0c4303551ab9915c89d84e6757c61bd0a2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087876"
---
# <a name="create-or-replace-an-activity"></a><span data-ttu-id="81463-104">Crear o reemplazar una actividad</span><span class="sxs-lookup"><span data-stu-id="81463-104">Create or replace an activity</span></span>

> <span data-ttu-id="81463-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="81463-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="81463-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="81463-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="81463-107">Crear una nueva o reemplazar una actividad de usuario existente para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="81463-107">Create a new or replace an existing user activity for your app.</span></span> <span data-ttu-id="81463-108">Si desea crear una actividad de usuario y su relacionados **historyItems** en una sola solicitud, puede usar [profundo insertar](projectrome-put-activity.md#example-2---deep-insert).</span><span class="sxs-lookup"><span data-stu-id="81463-108">If you'd like to create a user activity and its related **historyItems** in one request, you can use [deep insert](projectrome-put-activity.md#example-2---deep-insert).</span></span>

## <a name="permissions"></a><span data-ttu-id="81463-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="81463-109">Permissions</span></span>

<span data-ttu-id="81463-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="81463-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="81463-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="81463-112">Permission type</span></span>      | <span data-ttu-id="81463-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="81463-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="81463-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="81463-114">Delegated (work or school account)</span></span> | <span data-ttu-id="81463-115">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="81463-115">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="81463-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="81463-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="81463-117">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="81463-117">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="81463-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="81463-118">Application</span></span> | <span data-ttu-id="81463-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="81463-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="81463-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="81463-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /me/activities/{appActivityId}
```

><span data-ttu-id="81463-121">**Nota:** El appActivityId en la dirección URL debe estar seguras de dirección URL (todos los caracteres excepto deben convertirse en su representación hexadecimal caracteres no reservados de RFC 2396), pero el appActivityId original no tiene que estar seguro de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="81463-121">**Note:** The appActivityId in the URL needs to be URL-safe (all characters except for RFC 2396 unreserved characters must be converted to their hexadecimal representation), but the original appActivityId does not have to be URL-safe.</span></span>

## <a name="request-headers"></a><span data-ttu-id="81463-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="81463-122">Request headers</span></span>

|<span data-ttu-id="81463-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="81463-123">Name</span></span> | <span data-ttu-id="81463-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="81463-124">Type</span></span> | <span data-ttu-id="81463-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="81463-125">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="81463-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="81463-126">Authorization</span></span> | <span data-ttu-id="81463-127">string</span><span class="sxs-lookup"><span data-stu-id="81463-127">string</span></span> | <span data-ttu-id="81463-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="81463-p105">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="81463-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="81463-130">Request body</span></span>

<span data-ttu-id="81463-131">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de la [actividad](../resources/projectrome-activity.md) .</span><span class="sxs-lookup"><span data-stu-id="81463-131">In the request body, supply a JSON representation of an [activity](../resources/projectrome-activity.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="81463-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81463-132">Response</span></span>

<span data-ttu-id="81463-133">Si tiene éxito, este método devuelve el `201 Created` código de respuesta si se ha creado la actividad o `200 OK` si se ha reemplazado la actividad.</span><span class="sxs-lookup"><span data-stu-id="81463-133">If successful, this method returns the `201 Created` response code if the activity was created or `200 OK` if the activity was replaced.</span></span>

## <a name="example-1"></a><span data-ttu-id="81463-134">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="81463-134">Example 1</span></span>

#### <a name="request"></a><span data-ttu-id="81463-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="81463-135">Request</span></span>

<span data-ttu-id="81463-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="81463-136">The following is an example of the request.</span></span>

<!-- {
    "blockType": "ignored",
    "name": "upsert_activity"
} -->

```http
PUT https://graph.microsoft.com/beta/me/activities/%2Farticle%3F12345
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
            "addImageQuery": "false"
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

#### <a name="response"></a><span data-ttu-id="81463-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81463-137">Response</span></span>

<span data-ttu-id="81463-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="81463-138">The following is an example of the response.</span></span>

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.activity"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Location: https://graph.microsoft.com/beta/me/activities/14332800362997268276

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

## <a name="example-2---deep-insert"></a><span data-ttu-id="81463-139">Ejemplo 2: insertar profundo</span><span class="sxs-lookup"><span data-stu-id="81463-139">Example 2 - Deep insert</span></span>

#### <a name="request"></a><span data-ttu-id="81463-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="81463-140">Request</span></span>

<span data-ttu-id="81463-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="81463-141">The following is an example of the request.</span></span>

<!-- {
    "blockType": "ignored",
    "name": "upsert_activity"
} -->

```http
PUT https://graph.microsoft.com/beta/me/activities/%2Farticle%3F12345
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
            "addImageQuery": "false",
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

#### <a name="response"></a><span data-ttu-id="81463-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="81463-142">Response</span></span>

<span data-ttu-id="81463-143">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="81463-143">The following is an example of the response.</span></span>

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.activity"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Location: https://graph.microsoft.com/beta/me/activities/14332800362997268276

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
