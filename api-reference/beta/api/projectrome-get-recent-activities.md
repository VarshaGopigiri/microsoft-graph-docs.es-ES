---
title: Obtener las actividades recientes del usuario
description: " API. El servicio consultará para la historyItems más reciente y, a continuación, extraer las actividades relacionadas. Las actividades se ordenarán según la más reciente **lastModified** en el **historyItem**. Esto significa que no se incluyan actividades sin **historyItems** en la respuesta. El permiso UserActivity.ReadWrite.CreatedByApp también aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación. Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes. Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar."
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: 0cb0a4ba5a46489990b172a3acb5a542ef697740
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973555"
---
# <a name="get-recent-user-activities"></a><span data-ttu-id="64169-109">Obtener las actividades recientes del usuario</span><span class="sxs-lookup"><span data-stu-id="64169-109">Get recent user activities</span></span>

> <span data-ttu-id="64169-110">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="64169-110">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="64169-111">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="64169-111">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="64169-112">Obtenga las actividades recientes para un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="64169-112">Get recent activities for a given user.</span></span> <span data-ttu-id="64169-113">Esta función de OData tiene algunos comportamientos predeterminados que se incluye para hacer funcione como una API "usados más recientemente".</span><span class="sxs-lookup"><span data-stu-id="64169-113">This OData function has some default behaviors included to make it operate like a "most recently used" API.</span></span> <span data-ttu-id="64169-114">El servicio consultará para el más reciente [historyItems](../resources/projectrome-historyitem.md)y, a continuación, extraer las actividades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="64169-114">The service will query for the most recent [historyItems](../resources/projectrome-historyitem.md), and then pull those related activities.</span></span> <span data-ttu-id="64169-115">Las actividades se ordenarán según la más reciente **lastModified** en el **historyItem**.</span><span class="sxs-lookup"><span data-stu-id="64169-115">Activities will be sorted according to the most recent **lastModified** on the **historyItem**.</span></span> <span data-ttu-id="64169-116">Esto significa que no se incluyan actividades sin **historyItems** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64169-116">This means that activities without **historyItems** will not be included in the response.</span></span> <span data-ttu-id="64169-117">El permiso UserActivity.ReadWrite.CreatedByApp también aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="64169-117">The UserActivity.ReadWrite.CreatedByApp permission will also apply extra filtering to the response, so that only activities created by your application are returned.</span></span> <span data-ttu-id="64169-118">Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes.</span><span class="sxs-lookup"><span data-stu-id="64169-118">This server-side filtering might result in empty pages if the user is particularly active and other applications have created more recent activities.</span></span> <span data-ttu-id="64169-119">Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.</span><span class="sxs-lookup"><span data-stu-id="64169-119">To get your application's activities, use the **nextLink** property to paginate.</span></span>

## <a name="permissions"></a><span data-ttu-id="64169-120">Permisos</span><span class="sxs-lookup"><span data-stu-id="64169-120">Permissions</span></span>

<span data-ttu-id="64169-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64169-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="64169-123">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64169-123">Permission type</span></span>      | <span data-ttu-id="64169-124">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64169-124">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="64169-125">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64169-125">Delegated (work or school account)</span></span> | <span data-ttu-id="64169-126">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="64169-126">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="64169-127">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64169-127">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="64169-128">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="64169-128">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="64169-129">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64169-129">Application</span></span> | <span data-ttu-id="64169-130">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64169-130">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="64169-131">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64169-131">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities/recent
```

## <a name="optional-query-parameters"></a><span data-ttu-id="64169-132">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="64169-132">Optional query parameters</span></span>

<span data-ttu-id="64169-133">Este método es compatible con algunos de [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64169-133">This method supports some [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> <span data-ttu-id="64169-134">Se admiten los siguientes parámetros de consulta:</span><span class="sxs-lookup"><span data-stu-id="64169-134">The following query parameters are supported:</span></span>

- <span data-ttu-id="64169-135">Expanda $ para la propiedad de navegación **historyItems** .</span><span class="sxs-lookup"><span data-stu-id="64169-135">$expand for the **historyItems** navigation property.</span></span>
- <span data-ttu-id="64169-136">$top para limitar el número máximo de elementos en las páginas.</span><span class="sxs-lookup"><span data-stu-id="64169-136">$top to limit the maximum number of items across pages.</span></span>
- <span data-ttu-id="64169-137">$filter en la propiedad **lastModifiedDateTime** para **actividades** o **historyItems**, si expandida.</span><span class="sxs-lookup"><span data-stu-id="64169-137">$filter on the **lastModifiedDateTime** property for either **activities** or **historyItems**, if expanded.</span></span>

<span data-ttu-id="64169-138">Los siguientes son algunos ejemplos de consultas compatibles con codificación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="64169-138">The following are some examples of supported queries with URL encoding.</span></span>

```
/me/activities/recent?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities/recent?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities/recent?$top=5
```

## <a name="request-headers"></a><span data-ttu-id="64169-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64169-139">Request headers</span></span>

|<span data-ttu-id="64169-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="64169-140">Name</span></span> | <span data-ttu-id="64169-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="64169-141">Type</span></span> | <span data-ttu-id="64169-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="64169-142">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="64169-143">Autorización</span><span class="sxs-lookup"><span data-stu-id="64169-143">Authorization</span></span> | <span data-ttu-id="64169-144">string</span><span class="sxs-lookup"><span data-stu-id="64169-144">string</span></span> | <span data-ttu-id="64169-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64169-p106">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="64169-147">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64169-147">Request body</span></span>

<span data-ttu-id="64169-148">No se especifica un cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64169-148">Do not specify a request body.</span></span>

## <a name="response"></a><span data-ttu-id="64169-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64169-149">Response</span></span>

<span data-ttu-id="64169-150">Si tiene éxito, este método devuelve el `200 OK` código de respuesta con las actividades recientes del usuario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="64169-150">If successful, this method returns the `200 OK` response code with the user's recent activities for your application.</span></span>

## <a name="example"></a><span data-ttu-id="64169-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64169-151">Example</span></span>

##### <a name="request"></a><span data-ttu-id="64169-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64169-152">Request</span></span>

<span data-ttu-id="64169-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64169-153">The following is an example of the request.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "get_recent_activities"
}-->

```http
GET https://graph.microsoft.com/beta/me/activities/recent
```

##### <a name="response"></a><span data-ttu-id="64169-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64169-154">Response</span></span>

<span data-ttu-id="64169-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64169-155">The following is an example of the response.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.activity)"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(userActivity)",
    "@odata.nextLink": "https://graph.microsoft.com/beta/me/activities/recent?$skiptoken=%24filter%3dlastModifiedDateTime+lt+2018-02-26T18%3a06%3a19.365Z",
    "value": [{
        "@odata.type": "#microsoft.graph.activity",
        "activitySourceHost": "https://www.contoso.com",
        "createdDateTime": "2018-02-26T18:34:29.592Z",
        "lastModifiedDateTime": "2018-02-26T18:34:29.607Z",
        "id": "5347642601316252694",
        "appActivityId": "/article?12345",
        "visualElements": {
            "attribution": {
              "iconUrl": "https://www.contoso.com/icon",
              "alternateText": "Contoso, Ltd.",
              "addImageQuery": "false",
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
  "tocPath": ""
}-->
