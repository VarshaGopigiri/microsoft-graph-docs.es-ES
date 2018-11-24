# <a name="get-user-activities"></a><span data-ttu-id="e5dfd-101">Obtener las actividades del usuario</span><span class="sxs-lookup"><span data-stu-id="e5dfd-101">Get user activities</span></span>

<span data-ttu-id="e5dfd-102">Obtener las actividades de un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-102">Get activities for a given user.</span></span> <span data-ttu-id="e5dfd-103">A diferencia de la **reciente** OData (función), se devolverán las actividades sin historiales.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-103">Unlike the **recent** OData function, activities without histories will be returned.</span></span> <span data-ttu-id="e5dfd-104">El permiso UserActivity.ReadWrite.CreatedByApp se aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-104">The permission UserActivity.ReadWrite.CreatedByApp will apply extra filtering to the response, so that only activities created by your application are returned.</span></span> <span data-ttu-id="e5dfd-105">Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-105">This server-side filtering might result in empty pages if the user is particularly active and other applications have created more recent activities.</span></span> <span data-ttu-id="e5dfd-106">Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-106">To get your application's activities, use the **nextLink** property to paginate.</span></span>

## <a name="permissions"></a><span data-ttu-id="e5dfd-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5dfd-107">Permissions</span></span>

<span data-ttu-id="e5dfd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e5dfd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e5dfd-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5dfd-110">Permission type</span></span>      | <span data-ttu-id="e5dfd-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5dfd-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5dfd-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5dfd-112">Delegated (work or school account)</span></span> | <span data-ttu-id="e5dfd-113">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="e5dfd-113">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="e5dfd-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5dfd-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5dfd-115">UserActivity.ReadWrite.CreatedByApp</span><span class="sxs-lookup"><span data-stu-id="e5dfd-115">UserActivity.ReadWrite.CreatedByApp</span></span>    |
|<span data-ttu-id="e5dfd-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5dfd-116">Application</span></span> | <span data-ttu-id="e5dfd-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e5dfd-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5dfd-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e5dfd-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e5dfd-119">Optional query parameters</span></span>

<span data-ttu-id="e5dfd-120">Este método es compatible con algunos de [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-120">This method supports some [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span> <span data-ttu-id="e5dfd-121">Se admiten los siguientes parámetros de consulta:</span><span class="sxs-lookup"><span data-stu-id="e5dfd-121">The following query parameters are supported:</span></span>

- <span data-ttu-id="e5dfd-122">Expanda $ para la propiedad de navegación **historyItems** .</span><span class="sxs-lookup"><span data-stu-id="e5dfd-122">$expand for the **historyItems** navigation property.</span></span>
- <span data-ttu-id="e5dfd-123">$top para limitar el número máximo de elementos en las páginas.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-123">$top to limit the maximum number of items across pages.</span></span>
- <span data-ttu-id="e5dfd-124">$filter en la propiedad **lastModifiedDateTime** para actividades o **historyItems**, si expandida.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-124">$filter on the **lastModifiedDateTime** property for either activities or **historyItems**, if expanded.</span></span>

<span data-ttu-id="e5dfd-125">Los siguientes son algunos ejemplos de consultas compatibles con codificación URL:</span><span class="sxs-lookup"><span data-stu-id="e5dfd-125">The following are some examples of supported queries with URL encoding:</span></span>

```
/me/activities?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities?$top=5
```

## <a name="request-headers"></a><span data-ttu-id="e5dfd-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5dfd-126">Request headers</span></span>

|<span data-ttu-id="e5dfd-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5dfd-127">Name</span></span> | <span data-ttu-id="e5dfd-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5dfd-128">Type</span></span> | <span data-ttu-id="e5dfd-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5dfd-129">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="e5dfd-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5dfd-130">Authorization</span></span> | <span data-ttu-id="e5dfd-131">string</span><span class="sxs-lookup"><span data-stu-id="e5dfd-131">string</span></span> | <span data-ttu-id="e5dfd-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-p104">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e5dfd-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5dfd-134">Request body</span></span>

<span data-ttu-id="e5dfd-135">Ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-135">No request body.</span></span>

## <a name="response"></a><span data-ttu-id="e5dfd-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5dfd-136">Response</span></span>

<span data-ttu-id="e5dfd-137">Si tiene éxito, este método devuelve el `200 OK` código de respuesta con las actividades del usuario para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-137">If successful, this method returns the `200 OK` response code with the user's activities for your application.</span></span>

## <a name="example"></a><span data-ttu-id="e5dfd-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5dfd-138">Example</span></span>

##### <a name="request"></a><span data-ttu-id="e5dfd-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5dfd-139">Request</span></span>

<span data-ttu-id="e5dfd-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-140">The following is an example of the request.</span></span>

<!-- {
  "blockType": "ignored",
  "name": "get_activities"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/activities
```

##### <a name="response"></a><span data-ttu-id="e5dfd-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5dfd-141">Response</span></span>

<span data-ttu-id="e5dfd-142">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5dfd-142">The following is an example of the response.</span></span>

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.activity)"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Collection(userActivity)",
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/activities?$skiptoken=%24filter%3dlastModifiedDateTime+lt+2018-02-26T18%3a06%3a19.365Z",
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
  "description": "Get activities",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
