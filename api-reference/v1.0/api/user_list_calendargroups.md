# <a name="list-calendargroups"></a><span data-ttu-id="236c4-101">List calendarGroups</span><span class="sxs-lookup"><span data-stu-id="236c4-101">List calendarGroups</span></span>

<span data-ttu-id="236c4-102">Obtiene los grupos de calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="236c4-102">Get the user's calendar groups.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="236c4-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="236c4-103">Prerequisites</span></span>
<span data-ttu-id="236c4-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read; Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="236c4-104">One of the following scopes is required to execute this API: Calendars.Read; Calendars.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="236c4-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="236c4-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/calendarGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="236c4-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="236c4-106">Optional query parameters</span></span>
<span data-ttu-id="236c4-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="236c4-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="236c4-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="236c4-108">Request headers</span></span>
| <span data-ttu-id="236c4-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="236c4-109">Header</span></span>       | <span data-ttu-id="236c4-110">Valor</span><span class="sxs-lookup"><span data-stu-id="236c4-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="236c4-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="236c4-111">Authorization</span></span>  | <span data-ttu-id="236c4-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="236c4-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="236c4-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="236c4-114">Content-Type</span></span>  | <span data-ttu-id="236c4-115">application/json</span><span class="sxs-lookup"><span data-stu-id="236c4-115">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="236c4-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="236c4-116">Request body</span></span>
<span data-ttu-id="236c4-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="236c4-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="236c4-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="236c4-118">Response</span></span>

<span data-ttu-id="236c4-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="236c4-119">If successful, this method returns a `200 OK` response code and collection of [CalendarGroup](../resources/calendargroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="236c4-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="236c4-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="236c4-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="236c4-121">Request</span></span>
<span data-ttu-id="236c4-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="236c4-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendargroups"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups
```
##### <a name="response"></a><span data-ttu-id="236c4-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="236c4-123">Response</span></span>
<span data-ttu-id="236c4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="236c4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 155

{
  "value": [
    {
      "name": "name-value",
      "classId": "classId-value",
      "changeKey": "changeKey-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List calendarGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
