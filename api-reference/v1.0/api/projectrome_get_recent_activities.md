# <a name="get-recent-user-activities"></a><span data-ttu-id="15dd0-101">Obtener actividades recientes del usuario</span><span class="sxs-lookup"><span data-stu-id="15dd0-101">Get user activities</span></span>

<span data-ttu-id="15dd0-102">Obtenga las actividades recientes para un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="15dd0-102">Get recent activities for a given user.</span></span> <span data-ttu-id="15dd0-103">Esta función de OData tiene algunos comportamientos predeterminados incluidos para hacer que funcione como una API "usada más recientemente".</span><span class="sxs-lookup"><span data-stu-id="15dd0-103">This OData function has some default behaviors included to make it operate like a "most recently used" API.</span></span> <span data-ttu-id="15dd0-104">El servicio consultará el [historyItems](../resources/projectrome_historyitem.md) más reciente y, a continuación, extraerá las actividades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="15dd0-104">The service will query for the most recent [historyItems](../resources/projectrome_historyitem.md), and then pull those related activities.</span></span> <span data-ttu-id="15dd0-105">Las actividades se ordenarán según la más reciente **lastModified** en el **historyItem**.</span><span class="sxs-lookup"><span data-stu-id="15dd0-105">Activities will be sorted according to the most recent **lastModified** on the **historyItem**.</span></span> <span data-ttu-id="15dd0-106">Esto significa que no se incluirán actividades sin **historyItems** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15dd0-106">This means that activities without **historyItems** will not be included in the response.</span></span> <span data-ttu-id="15dd0-107">El permiso UserActivity.ReadWrite.CreatedByApp también aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="15dd0-107">The UserActivity.ReadWrite.CreatedByApp permission will also apply extra filtering to the response, so that only activities created by your application are returned.</span></span> <span data-ttu-id="15dd0-108">Este filtrado del lado del servidor podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes.</span><span class="sxs-lookup"><span data-stu-id="15dd0-108">This server-side filtering might result in empty pages if the user is particularly active and other applications have created more recent activities.</span></span> <span data-ttu-id="15dd0-109">Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** para paginar.</span><span class="sxs-lookup"><span data-stu-id="15dd0-109">To get your application's activities, use the **nextLink** property to paginate.</span></span>

## <a name="permissions"></a><span data-ttu-id="15dd0-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="15dd0-110">Permissions</span></span>

<span data-ttu-id="15dd0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="15dd0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="15dd0-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15dd0-113">Permission type</span></span>      | <span data-ttu-id="15dd0-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15dd0-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="15dd0-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15dd0-115">Delegated (work or school account)</span></span> | <span data-ttu-id="15dd0-116">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="15dd0-116">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="15dd0-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15dd0-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="15dd0-118">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="15dd0-118">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="15dd0-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15dd0-119">Application</span></span> | <span data-ttu-id="15dd0-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15dd0-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="15dd0-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15dd0-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities/recent
```

## <a name="optional-query-parameters"></a><span data-ttu-id="15dd0-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="15dd0-122">Optional query parameters</span></span>

<span data-ttu-id="15dd0-123">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15dd0-123">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span> <span data-ttu-id="15dd0-124">Se admiten los siguientes parámetros de consulta:</span><span class="sxs-lookup"><span data-stu-id="15dd0-124">The following query parameters are supported:</span></span>

- <span data-ttu-id="15dd0-125">$expand para la propiedad de navegación **historyItems**.</span><span class="sxs-lookup"><span data-stu-id="15dd0-125">$expand for the **historyItems** navigation property.</span></span>
- <span data-ttu-id="15dd0-126">$top para limitar el número máximo de elementos en las páginas.</span><span class="sxs-lookup"><span data-stu-id="15dd0-126">$top to limit the maximum number of items across pages.</span></span>
- <span data-ttu-id="15dd0-127">$filter en la propiedad **lastModifiedDateTime** para **activities** o **historyItems**, si se expande.</span><span class="sxs-lookup"><span data-stu-id="15dd0-127">$filter on the **lastModifiedDateTime** property for either **activities** or **historyItems**, if expanded.</span></span>

<span data-ttu-id="15dd0-128">Los siguientes son algunos ejemplos de consultas compatibles con codificación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="15dd0-128">The following are some examples of supported queries with URL encoding.</span></span>

```
/me/activities/recent?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities/recent?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities/recent?$top=5
```

## <a name="request-headers"></a><span data-ttu-id="15dd0-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15dd0-129">Request headers</span></span>

|<span data-ttu-id="15dd0-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="15dd0-130">Name</span></span> | <span data-ttu-id="15dd0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="15dd0-131">Type</span></span> | <span data-ttu-id="15dd0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="15dd0-132">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="15dd0-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="15dd0-133">Authorization</span></span> | <span data-ttu-id="15dd0-134">cadena</span><span class="sxs-lookup"><span data-stu-id="15dd0-134">string</span></span> | <span data-ttu-id="15dd0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15dd0-p104">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="15dd0-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15dd0-137">Request body</span></span>

<span data-ttu-id="15dd0-138">No se especifica un cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15dd0-138">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="15dd0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15dd0-139">Response</span></span>

<span data-ttu-id="15dd0-140">Si tiene éxito, este método devuelve el código de respuesta `200 OK` con las actividades recientes del usuario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="15dd0-140">If successful, this method returns the `200 OK` response code with the user's recent activities for your application.</span></span>

## <a name="example"></a><span data-ttu-id="15dd0-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15dd0-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="15dd0-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15dd0-142">Request</span></span>

<span data-ttu-id="15dd0-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15dd0-143">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_recent_activities"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/activities/recent
```

##### <a name="response"></a><span data-ttu-id="15dd0-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15dd0-144">Response</span></span>

<span data-ttu-id="15dd0-145">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15dd0-145">The following is an example of the response.</span></span>

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
              "iconUrl": "http://www.contoso.com/icon",
              "alternateText": "Contoso, Ltd.",
              "addImageQuery": false,
              },
            "displayText": "Contoso How-To: How to Tie a Reef Knot",
            "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
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

    "Warning: get_recent_activities/container/visualElements:
      Schema validation failed on property 'visualElements' ['microsoft.graph.visualInfo']",

    "Warning: get_recent_activities/container/visualElements/content:
      Schema validation failed on property 'content' ['microsoft.graph.Json']",

    "Warning: get_recent_activities/container/visualElements/content/$schema:
      Undocumented property '$schema' [String] was not expected on resource microsoft.graph.Json.",

    "Warning: get_recent_activities/container/visualElements/content/body:
      Undocumented property 'body' [Collection(Object)] was not expected on resource microsoft.graph.Json.",

    "Warning: get_recent_activities/container/visualElements/content/type:
      Undocumented property 'type' [String] was not expected on resource microsoft.graph.Json."

  ],
  "tocPath": ""
}-->
