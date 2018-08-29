# <a name="create-or-replace-an-activity"></a><span data-ttu-id="6073b-101">Crear o reemplazar una actividad</span><span class="sxs-lookup"><span data-stu-id="6073b-101">Create or replace an activity</span></span>

<span data-ttu-id="6073b-102">Crear o reemplazar una actividad de usuario existente para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="6073b-102">Create a new or replace an existing user activity for your app.</span></span> <span data-ttu-id="6073b-103">Si desea crear una actividad de usuario y los **historyItems** relacionados en una sola solicitud, puede usar [deep insert](projectrome_put_activity.md#example-2---deep-insert).</span><span class="sxs-lookup"><span data-stu-id="6073b-103">If you'd like to create a user activity and its related **historyItems** in one request, you can use [deep insert](projectrome_put_activity.md#example-2---deep-insert).</span></span>

## <a name="permissions"></a><span data-ttu-id="6073b-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="6073b-104">Permissions</span></span>

<span data-ttu-id="6073b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6073b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="6073b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6073b-107">Permission type</span></span>      | <span data-ttu-id="6073b-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6073b-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6073b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6073b-109">Delegated (work or school account)</span></span> | <span data-ttu-id="6073b-110">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="6073b-110">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="6073b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6073b-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6073b-112">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="6073b-112">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="6073b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6073b-113">Application</span></span> | <span data-ttu-id="6073b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6073b-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6073b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6073b-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /me/activities/{appActivityId}
```

><span data-ttu-id="6073b-116">**Nota:** El appActivityId de la dirección URL debe ser seguro en términos de URL (todos los caracteres excepto los no reservados para RFC 2396 deben convertirse a su representación hexadecimal), pero el appActivityId original no tiene que ser seguro en lo que respecta a la URL.</span><span class="sxs-lookup"><span data-stu-id="6073b-116">**Note:** The appActivityId in the URL needs to be URL-safe (all characters except for RFC 2396 unreserved characters must be converted to their hexadecimal representation), but the original appActivityId does not have to be URL-safe.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6073b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6073b-117">Request headers</span></span>

|<span data-ttu-id="6073b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="6073b-118">Name</span></span> | <span data-ttu-id="6073b-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="6073b-119">Type</span></span> | <span data-ttu-id="6073b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6073b-120">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="6073b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="6073b-121">Authorization</span></span> | <span data-ttu-id="6073b-122">cadena</span><span class="sxs-lookup"><span data-stu-id="6073b-122">string</span></span> | <span data-ttu-id="6073b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6073b-p103">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6073b-125">Request body</span><span class="sxs-lookup"><span data-stu-id="6073b-125">Request body</span></span>

<span data-ttu-id="6073b-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [activity](../resources/projectrome_activity.md).</span><span class="sxs-lookup"><span data-stu-id="6073b-126">In the request body, supply a JSON representation of an [educationClass](../resources/projectrome_activity.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="6073b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6073b-127">Response</span></span>

<span data-ttu-id="6073b-128">Si tiene éxito, este método devuelve el código de respuesta `201 Created` si se ha creado la actividad o `200 OK` si se ha reemplazado la actividad.</span><span class="sxs-lookup"><span data-stu-id="6073b-128">If successful, this method returns the `201 Created` response code if the activity was created or `200 OK` if the activity was replaced.</span></span>

## <a name="example-1"></a><span data-ttu-id="6073b-129">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="6073b-129">Example 1</span></span>

#### <a name="request"></a><span data-ttu-id="6073b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6073b-130">Request</span></span>

<span data-ttu-id="6073b-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6073b-131">The following is an example of the request.</span></span>

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
    "activationUrl": "http://www.contoso.com/article?id=12345",
    "contentUrl": "http://www.contoso.com/article?id=12345",
    "fallbackUrl": "http://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "http://schema.org",
        "@type": "Article",
        "author": "Jennifer Booth",
        "name": "How to Tie a Reef Knot"
    },
    "visualElements": {
        "attribution": {
            "iconUrl": "http://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false,
        },
        "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
        "backgroundColor": "#ff0000",
        "displayText": "Contoso How-To: How to Tie a Reef Knot",
        "content": {
            "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
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

#### <a name="response"></a><span data-ttu-id="6073b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6073b-132">Response</span></span>

<span data-ttu-id="6073b-133">A continuación se muestra un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6073b-133">The following is an example of the response.</span></span>

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
    "activitySourceHost": "http://contoso.com",
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
            "iconUrl": "http://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false
        },
        "backgroundColor": "#ff0000",
        "content": {
            "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
            "type": "AdaptiveCard",
            "body":
            [{
                "type": "TextBlock",
                "text": "Contoso MainPage"
            }]
        }
    },
    "activationUrl": "http://www.contoso.com/article?id=12345",
    "appDisplayName": "Contoso, Ltd.",
    "userTimezone": "Africa/Casablanca",
    "fallbackUrl": "http://www.contoso.com/article?id=12345",
    "contentUrl": "http://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "http://schema.org",
        "@type": "Article",
        "author": "Jennifer Booth",
        "name": "How to Tie a Reef Knot"
    },
}
```

## <a name="example-2---deep-insert"></a><span data-ttu-id="6073b-134">Ejemplo 2: Deep insert</span><span class="sxs-lookup"><span data-stu-id="6073b-134">Example 2 - Deep insert</span></span>

#### <a name="request"></a><span data-ttu-id="6073b-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6073b-135">Request</span></span>

<span data-ttu-id="6073b-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6073b-136">The following is an example of the request.</span></span>

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
    "activationUrl": "http://www.contoso.com/article?id=12345",
    "contentUrl": "http://www.contoso.com/article?id=12345",
    "fallbackUrl": "http://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "http://schema.org",
        "@type": "Article",
        "author": "Jennifer Booth",
        "name": "How to Tie a Reef Knot"
    },
    "visualElements": {
        "attribution": {
            "iconUrl": "http://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false,
        },
        "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
        "backgroundColor": "#ff0000",
        "displayText": "Contoso How-To: How to Tie a Reef Knot",
        "content": {
            "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
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

#### <a name="response"></a><span data-ttu-id="6073b-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6073b-137">Response</span></span>

<span data-ttu-id="6073b-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6073b-138">The following is an example of the response.</span></span>

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
    "activitySourceHost": "http://contoso.com",
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
            "iconUrl": "http://www.contoso.com/icon",
            "alternateText": "Contoso, Ltd.",
            "addImageQuery": false
        },
        "backgroundColor": "#ff0000",
        "content": {
            "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
            "type": "AdaptiveCard",
            "body":
            [{
                "type": "TextBlock",
                "text": "Contoso MainPage"
            }]
        }
    },
    "activationUrl": "http://www.contoso.com/article?id=12345",
    "appDisplayName": "Contoso, Ltd.",
    "userTimezone": "Africa/Casablanca",
    "fallbackUrl": "http://www.contoso.com/article?id=12345",
    "contentUrl": "http://www.contoso.com/article?id=12345",
    "contentInfo": {
        "@context": "http://schema.org",
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
