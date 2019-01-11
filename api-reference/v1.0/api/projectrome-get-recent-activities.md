---
title: Obtener las actividades recientes del usuario
description: " API. El servicio consultará para la historyItems más reciente y, a continuación, extraer las actividades relacionadas. Las actividades se ordenarán según la más reciente **lastModified** en el **historyItem**. Esto significa que no se incluyan actividades sin **historyItems** en la respuesta. El permiso UserActivity.ReadWrite.CreatedByApp también aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación. Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes. Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar."
localization_priority: Normal
ms.openlocfilehash: 9ae67169395b3667e8ba6ef34ce6a4b9c4567ac5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844257"
---
# <a name="get-recent-user-activities"></a><span data-ttu-id="894b0-109">Obtener las actividades recientes del usuario</span><span class="sxs-lookup"><span data-stu-id="894b0-109">Get recent user activities</span></span>

<span data-ttu-id="894b0-110">Obtenga las actividades recientes para un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="894b0-110">Get recent activities for a given user.</span></span> <span data-ttu-id="894b0-111">Esta función de OData tiene algunos comportamientos predeterminados que se incluye para hacer funcione como una API "usados más recientemente".</span><span class="sxs-lookup"><span data-stu-id="894b0-111">This OData function has some default behaviors included to make it operate like a "most recently used" API.</span></span> <span data-ttu-id="894b0-112">El servicio consultará para el más reciente [historyItems](../resources/projectrome-historyitem.md)y, a continuación, extraer las actividades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="894b0-112">The service will query for the most recent [historyItems](../resources/projectrome-historyitem.md), and then pull those related activities.</span></span> <span data-ttu-id="894b0-113">Las actividades se ordenarán según la más reciente **lastModified** en el **historyItem**.</span><span class="sxs-lookup"><span data-stu-id="894b0-113">Activities will be sorted according to the most recent **lastModified** on the **historyItem**.</span></span> <span data-ttu-id="894b0-114">Esto significa que no se incluyan actividades sin **historyItems** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="894b0-114">This means that activities without **historyItems** will not be included in the response.</span></span> <span data-ttu-id="894b0-115">El permiso UserActivity.ReadWrite.CreatedByApp también aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="894b0-115">The UserActivity.ReadWrite.CreatedByApp permission will also apply extra filtering to the response, so that only activities created by your application are returned.</span></span> <span data-ttu-id="894b0-116">Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes.</span><span class="sxs-lookup"><span data-stu-id="894b0-116">This server-side filtering might result in empty pages if the user is particularly active and other applications have created more recent activities.</span></span> <span data-ttu-id="894b0-117">Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.</span><span class="sxs-lookup"><span data-stu-id="894b0-117">To get your application's activities, use the **nextLink** property to paginate.</span></span>

## <a name="permissions"></a><span data-ttu-id="894b0-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="894b0-118">Permissions</span></span>

<span data-ttu-id="894b0-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="894b0-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="894b0-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="894b0-121">Permission type</span></span>      | <span data-ttu-id="894b0-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="894b0-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="894b0-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="894b0-123">Delegated (work or school account)</span></span> | <span data-ttu-id="894b0-124">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="894b0-124">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="894b0-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="894b0-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="894b0-126">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="894b0-126">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="894b0-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="894b0-127">Application</span></span> | <span data-ttu-id="894b0-128">No admitida.</span><span class="sxs-lookup"><span data-stu-id="894b0-128">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="894b0-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="894b0-129">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities/recent
```

## <a name="optional-query-parameters"></a><span data-ttu-id="894b0-130">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="894b0-130">Optional query parameters</span></span>

<span data-ttu-id="894b0-131">Este método es compatible con algunos de [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="894b0-131">This method supports some [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> <span data-ttu-id="894b0-132">Se admiten los siguientes parámetros de consulta:</span><span class="sxs-lookup"><span data-stu-id="894b0-132">The following query parameters are supported:</span></span>

- <span data-ttu-id="894b0-133">Expanda $ para la propiedad de navegación **historyItems** .</span><span class="sxs-lookup"><span data-stu-id="894b0-133">$expand for the **historyItems** navigation property.</span></span>
- <span data-ttu-id="894b0-134">$top para limitar el número máximo de elementos en las páginas.</span><span class="sxs-lookup"><span data-stu-id="894b0-134">$top to limit the maximum number of items across pages.</span></span>
- <span data-ttu-id="894b0-135">$filter en la propiedad **lastModifiedDateTime** para **actividades** o **historyItems**, si expandida.</span><span class="sxs-lookup"><span data-stu-id="894b0-135">$filter on the **lastModifiedDateTime** property for either **activities** or **historyItems**, if expanded.</span></span>

<span data-ttu-id="894b0-136">Los siguientes son algunos ejemplos de consultas compatibles con codificación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="894b0-136">The following are some examples of supported queries with URL encoding.</span></span>

```
/me/activities/recent?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities/recent?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities/recent?$top=5
```

## <a name="request-headers"></a><span data-ttu-id="894b0-137">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="894b0-137">Request headers</span></span>

|<span data-ttu-id="894b0-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="894b0-138">Name</span></span> | <span data-ttu-id="894b0-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="894b0-139">Type</span></span> | <span data-ttu-id="894b0-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="894b0-140">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="894b0-141">Autorización</span><span class="sxs-lookup"><span data-stu-id="894b0-141">Authorization</span></span> | <span data-ttu-id="894b0-142">string</span><span class="sxs-lookup"><span data-stu-id="894b0-142">string</span></span> | <span data-ttu-id="894b0-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="894b0-p105">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="894b0-145">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="894b0-145">Request body</span></span>

<span data-ttu-id="894b0-146">No se especifica un cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="894b0-146">Do not specify a request body.</span></span>

## <a name="response"></a><span data-ttu-id="894b0-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="894b0-147">Response</span></span>

<span data-ttu-id="894b0-148">Si tiene éxito, este método devuelve el `200 OK` código de respuesta con las actividades recientes del usuario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="894b0-148">If successful, this method returns the `200 OK` response code with the user's recent activities for your application.</span></span>

## <a name="example"></a><span data-ttu-id="894b0-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="894b0-149">Example</span></span>

##### <a name="request"></a><span data-ttu-id="894b0-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="894b0-150">Request</span></span>

<span data-ttu-id="894b0-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="894b0-151">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_recent_activities"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/activities/recent
```

##### <a name="response"></a><span data-ttu-id="894b0-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="894b0-152">Response</span></span>

<span data-ttu-id="894b0-153">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="894b0-153">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.userActivity)"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(userActivity)",
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/activities/recent?$skiptoken=%24filter%3dlastModifiedDateTime+lt+2018-02-26T18%3a06%3a19.365Z",
    "value": [{
        "@odata.type": "#microsoft.graph.userActivity",
        "activitySourceHost": "https://www.contoso.com",
        "createdDateTime": "2018-02-26T18:34:29.592Z",
        "lastModifiedDateTime": "2018-02-26T18:34:29.607Z",
        "id": "5347642601316252694",
        "appActivityId": "/article?12345",
        "visualElements": {
            "attribution": {
              "iconUrl": "https://www.contoso.com/icon",
              "alternateText": "Contoso, Ltd.",
              "addImageQuery": false,
              },
            "displayText": "Contoso How-To: How to Tie a Reef Knot",
            "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
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
            "author": "John Doe",
            "name": "How to Tie a Reef Knot"
        },
        "expirationDateTime": "2018-03-28T18:34:29.607Z",
        "status": "updated"
    }]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get recent activities",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Error: get_recent_activities/container/contentInfo:
      Property 'contentInfo' is of type Custom but has no custom members.",

    "Warning: get_recent_activities/container/visualElements/content/$schema:
      Undocumented property '$schema' [String] was not expected on resource microsoft.graph.Json.",

    "Warning: get_recent_activities/container/visualElements/content/body:
      Undocumented property 'body' [Collection(Object)] was not expected on resource microsoft.graph.Json.",

    "Warning: get_recent_activities/container/visualElements/content/type:
      Undocumented property 'type' [String] was not expected on resource microsoft.graph.Json."

  ],
  "tocPath": ""
}-->
