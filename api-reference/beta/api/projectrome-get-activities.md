---
title: Obtener las actividades del usuario
description: Obtener las actividades de un usuario determinado. A diferencia de la **reciente** OData (función), se devolverán las actividades sin historiales. El permiso UserActivity.ReadWrite.CreatedByApp se aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación. Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes. Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.
ms.openlocfilehash: e8a2fb02ac1de5fa45f8413c7313176902ca1c6e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090835"
---
# <a name="get-user-activities"></a><span data-ttu-id="18d15-107">Obtener las actividades del usuario</span><span class="sxs-lookup"><span data-stu-id="18d15-107">Get user activities</span></span>

> <span data-ttu-id="18d15-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18d15-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18d15-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18d15-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="18d15-110">Obtener las actividades de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="18d15-110">Get activities for a given user.</span></span> <span data-ttu-id="18d15-111">A diferencia de la **reciente** OData (función), se devolverán las actividades sin historiales.</span><span class="sxs-lookup"><span data-stu-id="18d15-111">Unlike the **recent** OData function, activities without histories will be returned.</span></span> <span data-ttu-id="18d15-112">El permiso UserActivity.ReadWrite.CreatedByApp se aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="18d15-112">The permission UserActivity.ReadWrite.CreatedByApp will apply extra filtering to the response, so that only activities created by your application are returned.</span></span> <span data-ttu-id="18d15-113">Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes.</span><span class="sxs-lookup"><span data-stu-id="18d15-113">This server-side filtering might result in empty pages if the user is particularly active and other applications have created more recent activities.</span></span> <span data-ttu-id="18d15-114">Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.</span><span class="sxs-lookup"><span data-stu-id="18d15-114">To get your application's activities, use the **nextLink** property to paginate.</span></span>

## <a name="permissions"></a><span data-ttu-id="18d15-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="18d15-115">Permissions</span></span>

<span data-ttu-id="18d15-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18d15-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="18d15-118">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18d15-118">Permission type</span></span>      | <span data-ttu-id="18d15-119">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18d15-119">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="18d15-120">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18d15-120">Delegated (work or school account)</span></span> | <span data-ttu-id="18d15-121">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="18d15-121">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="18d15-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18d15-122">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="18d15-123">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="18d15-123">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="18d15-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18d15-124">Application</span></span> | <span data-ttu-id="18d15-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18d15-125">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="18d15-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18d15-126">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities
```

## <a name="optional-query-parameters"></a><span data-ttu-id="18d15-127">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="18d15-127">Optional query parameters</span></span>

<span data-ttu-id="18d15-128">Este método es compatible con algunos de [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18d15-128">This method supports some [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> <span data-ttu-id="18d15-129">Se admiten los siguientes parámetros de consulta:</span><span class="sxs-lookup"><span data-stu-id="18d15-129">The following query parameters are supported:</span></span>

- <span data-ttu-id="18d15-130">Expanda $ para la propiedad de navegación **historyItems** .</span><span class="sxs-lookup"><span data-stu-id="18d15-130">$expand for the **historyItems** navigation property.</span></span>
- <span data-ttu-id="18d15-131">$top para limitar el número máximo de elementos en las páginas.</span><span class="sxs-lookup"><span data-stu-id="18d15-131">$top to limit the maximum number of items across pages.</span></span>
- <span data-ttu-id="18d15-132">$filter en la propiedad **lastModifiedDateTime** para **actividades** o **historyItems**, si expandida.</span><span class="sxs-lookup"><span data-stu-id="18d15-132">$filter on the **lastModifiedDateTime** property for either **activities** or **historyItems**, if expanded.</span></span>

<span data-ttu-id="18d15-133">Los siguientes son algunos ejemplos de consultas compatibles con codificación URL:</span><span class="sxs-lookup"><span data-stu-id="18d15-133">The following are some examples of supported queries with URL encoding:</span></span>

```
/me/activities?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities?$top=5
```

## <a name="request-headers"></a><span data-ttu-id="18d15-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18d15-134">Request headers</span></span>

|<span data-ttu-id="18d15-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="18d15-135">Name</span></span> | <span data-ttu-id="18d15-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="18d15-136">Type</span></span> | <span data-ttu-id="18d15-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="18d15-137">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="18d15-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="18d15-138">Authorization</span></span> | <span data-ttu-id="18d15-139">string</span><span class="sxs-lookup"><span data-stu-id="18d15-139">string</span></span> | <span data-ttu-id="18d15-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18d15-p106">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="18d15-142">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="18d15-142">Request body</span></span>

<span data-ttu-id="18d15-143">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18d15-143">No request body.</span></span>

## <a name="response"></a><span data-ttu-id="18d15-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18d15-144">Response</span></span>

<span data-ttu-id="18d15-145">Si tiene éxito, este método devuelve el `200 OK` código de respuesta con las actividades del usuario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="18d15-145">If successful, this method returns the `200 OK` response code with the user's activities for your application.</span></span>

## <a name="example"></a><span data-ttu-id="18d15-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18d15-146">Example</span></span>

##### <a name="request"></a><span data-ttu-id="18d15-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18d15-147">Request</span></span>

<span data-ttu-id="18d15-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18d15-148">The following is an example of the request.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "get_activities"
}-->

```http
GET https://graph.microsoft.com/beta/me/activities
```

##### <a name="response"></a><span data-ttu-id="18d15-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18d15-149">Response</span></span>

<span data-ttu-id="18d15-150">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18d15-150">The following is an example of the response.</span></span>

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
    "@odata.nextLink": "https://graph.microsoft.com/beta/me/activities?$skiptoken=%24filter%3dlastModifiedDateTime+lt+2018-02-26T18%3a06%3a19.365Z",
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
  "description": "Get activities",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
