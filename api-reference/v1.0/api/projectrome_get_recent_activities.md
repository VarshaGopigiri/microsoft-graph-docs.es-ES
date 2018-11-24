# <a name="get-recent-user-activities"></a><span data-ttu-id="ea8e2-101">Obtener las actividades recientes del usuario</span><span class="sxs-lookup"><span data-stu-id="ea8e2-101">Get recent user activities</span></span>

<span data-ttu-id="ea8e2-102">Obtenga las actividades recientes para un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-102">Get recent activities for a given user.</span></span> <span data-ttu-id="ea8e2-103">Esta función de OData tiene algunos comportamientos predeterminados que se incluye para hacer funcione como una API "usados más recientemente".</span><span class="sxs-lookup"><span data-stu-id="ea8e2-103">This OData function has some default behaviors included to make it operate like a "most recently used" API.</span></span> <span data-ttu-id="ea8e2-104">El servicio consultará para el más reciente [historyItems](../resources/projectrome_historyitem.md)y, a continuación, extraer las actividades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-104">The service will query for the most recent [historyItems](../resources/projectrome_historyitem.md), and then pull those related activities.</span></span> <span data-ttu-id="ea8e2-105">Las actividades se ordenarán según la más reciente **lastModified** en el **historyItem**.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-105">Activities will be sorted according to the most recent **lastModified** on the **historyItem**.</span></span> <span data-ttu-id="ea8e2-106">Esto significa que no se incluyan actividades sin **historyItems** en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-106">This means that activities without **historyItems** will not be included in the response.</span></span> <span data-ttu-id="ea8e2-107">El permiso UserActivity.ReadWrite.CreatedByApp también aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-107">The UserActivity.ReadWrite.CreatedByApp permission will also apply extra filtering to the response, so that only activities created by your application are returned.</span></span> <span data-ttu-id="ea8e2-108">Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-108">This server-side filtering might result in empty pages if the user is particularly active and other applications have created more recent activities.</span></span> <span data-ttu-id="ea8e2-109">Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-109">To get your application's activities, use the **nextLink** property to paginate.</span></span>

## <a name="permissions"></a><span data-ttu-id="ea8e2-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea8e2-110">Permissions</span></span>

<span data-ttu-id="ea8e2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ea8e2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ea8e2-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea8e2-113">Permission type</span></span>      | <span data-ttu-id="ea8e2-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea8e2-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea8e2-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea8e2-115">Delegated (work or school account)</span></span> | <span data-ttu-id="ea8e2-116">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="ea8e2-116">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="ea8e2-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea8e2-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea8e2-118">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="ea8e2-118">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="ea8e2-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea8e2-119">Application</span></span> | <span data-ttu-id="ea8e2-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-120">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ea8e2-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea8e2-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities/recent
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ea8e2-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ea8e2-122">Optional query parameters</span></span>

<span data-ttu-id="ea8e2-123">Este método es compatible con algunos de [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-123">This method supports some [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> <span data-ttu-id="ea8e2-124">Se admiten los siguientes parámetros de consulta:</span><span class="sxs-lookup"><span data-stu-id="ea8e2-124">The following query parameters are supported:</span></span>

- <span data-ttu-id="ea8e2-125">Expanda $ para la propiedad de navegación **historyItems** .</span><span class="sxs-lookup"><span data-stu-id="ea8e2-125">$expand for the **historyItems** navigation property.</span></span>
- <span data-ttu-id="ea8e2-126">$top para limitar el número máximo de elementos en las páginas.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-126">$top to limit the maximum number of items across pages.</span></span>
- <span data-ttu-id="ea8e2-127">$filter en la propiedad **lastModifiedDateTime** para **actividades** o **historyItems**, si expandida.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-127">$filter on the **lastModifiedDateTime** property for either **activities** or **historyItems**, if expanded.</span></span>

<span data-ttu-id="ea8e2-128">Los siguientes son algunos ejemplos de consultas compatibles con codificación de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-128">The following are some examples of supported queries with URL encoding.</span></span>

```
/me/activities/recent?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities/recent?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities/recent?$top=5
```

## <a name="request-headers"></a><span data-ttu-id="ea8e2-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea8e2-129">Request headers</span></span>

|<span data-ttu-id="ea8e2-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="ea8e2-130">Name</span></span> | <span data-ttu-id="ea8e2-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea8e2-131">Type</span></span> | <span data-ttu-id="ea8e2-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea8e2-132">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="ea8e2-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea8e2-133">Authorization</span></span> | <span data-ttu-id="ea8e2-134">string</span><span class="sxs-lookup"><span data-stu-id="ea8e2-134">string</span></span> | <span data-ttu-id="ea8e2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-p104">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea8e2-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea8e2-137">Request body</span></span>

<span data-ttu-id="ea8e2-138">No se especifica un cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-138">Do not specify a request body.</span></span>

## <a name="response"></a><span data-ttu-id="ea8e2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea8e2-139">Response</span></span>

<span data-ttu-id="ea8e2-140">Si tiene éxito, este método devuelve el `200 OK` código de respuesta con las actividades recientes del usuario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-140">If successful, this method returns the `200 OK` response code with the user's recent activities for your application.</span></span>

## <a name="example"></a><span data-ttu-id="ea8e2-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea8e2-141">Example</span></span>

##### <a name="request"></a><span data-ttu-id="ea8e2-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea8e2-142">Request</span></span>

<span data-ttu-id="ea8e2-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-143">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_recent_activities"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/activities/recent
```

##### <a name="response"></a><span data-ttu-id="ea8e2-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea8e2-144">Response</span></span>

<span data-ttu-id="ea8e2-145">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea8e2-145">The following is an example of the response.</span></span>

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
