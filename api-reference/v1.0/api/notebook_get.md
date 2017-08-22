# <a name="get-notebook"></a><span data-ttu-id="bbc67-101">Obtener bloc de notas</span><span class="sxs-lookup"><span data-stu-id="bbc67-101">Get notebook</span></span>

<span data-ttu-id="bbc67-102">Recupere las propiedades y las relaciones de un objeto [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="bbc67-102">Retrieve the properties and relationships of a [notebook](../resources/notebook.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bbc67-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bbc67-103">Prerequisites</span></span>
<span data-ttu-id="bbc67-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="bbc67-104">One of the following **scopes** is required to execute this API:</span></span>
  
<span data-ttu-id="bbc67-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bbc67-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="bbc67-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bbc67-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/{id}
GET /users/{id | userPrincipalName}/onenote/notebooks/{id}
GET /groups/{id}/onenote/notebooks/{id}
GET /sites/{id}/onenote/notebooks/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bbc67-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bbc67-107">Optional query parameters</span></span>
<span data-ttu-id="bbc67-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbc67-108">This method supports the `select` and `expand` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="bbc67-109">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="bbc67-109">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bbc67-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bbc67-110">Request headers</span></span>
| <span data-ttu-id="bbc67-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="bbc67-111">Name</span></span>       | <span data-ttu-id="bbc67-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbc67-112">Type</span></span> | <span data-ttu-id="bbc67-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbc67-113">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bbc67-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="bbc67-114">Authorization</span></span>  | <span data-ttu-id="bbc67-115">string</span><span class="sxs-lookup"><span data-stu-id="bbc67-115">string</span></span>  | <span data-ttu-id="bbc67-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bbc67-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bbc67-118">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bbc67-118">Accept</span></span> | <span data-ttu-id="bbc67-119">string</span><span class="sxs-lookup"><span data-stu-id="bbc67-119">string</span></span> | `application/json` | 

## <a name="request-body"></a><span data-ttu-id="bbc67-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bbc67-120">Request body</span></span>
<span data-ttu-id="bbc67-121">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bbc67-121">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bbc67-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbc67-122">Response</span></span>

<span data-ttu-id="bbc67-123">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bbc67-123">If successful, this method returns a `200 OK` response code and a [notebook](../resources/notebook.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bbc67-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bbc67-124">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bbc67-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bbc67-125">Request</span></span>
<span data-ttu-id="bbc67-126">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bbc67-126">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebook"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}
```
##### <a name="response"></a><span data-ttu-id="bbc67-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bbc67-127">Response</span></span>
<span data-ttu-id="bbc67-p102">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bbc67-p102">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 284

{
  "isDefault": true,
  "userRole": {
  },
  "isShared": true,
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "links": {
    "oneNoteClientUrl": {
      "href": "href-value"
    },
    "oneNoteWebUrl": {
      "href": "href-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get notebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
