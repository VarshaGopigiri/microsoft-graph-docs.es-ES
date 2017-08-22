# <a name="list-notebooks"></a><span data-ttu-id="986b5-101">Enumerar blocs de notas</span><span class="sxs-lookup"><span data-stu-id="986b5-101">List notebooks</span></span>

<span data-ttu-id="986b5-102">Recupera una lista de objetos [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="986b5-102">Retrieve a list of [notebook](../resources/notebook.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="986b5-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="986b5-103">Prerequisites</span></span>
<span data-ttu-id="986b5-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="986b5-104">One of the following **scopes** is required to execute this API:</span></span>  

<span data-ttu-id="986b5-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="986b5-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="986b5-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="986b5-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks
GET /users/{id | userPrincipalName}/onenote/notebooks
GET /groups/{id}/onenote/notebooks
GET /sites/{id}/onenote/notebooks
```
## <a name="optional-query-parameters"></a><span data-ttu-id="986b5-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="986b5-107">Optional query parameters</span></span>
<span data-ttu-id="986b5-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="986b5-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="986b5-109">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="986b5-109">The default sort order is `name asc`.</span></span> 

<span data-ttu-id="986b5-110">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="986b5-110">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="986b5-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="986b5-111">Request headers</span></span>
| <span data-ttu-id="986b5-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="986b5-112">Name</span></span>       | <span data-ttu-id="986b5-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="986b5-113">Type</span></span> | <span data-ttu-id="986b5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="986b5-114">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="986b5-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="986b5-115">Authorization</span></span>  | <span data-ttu-id="986b5-116">string</span><span class="sxs-lookup"><span data-stu-id="986b5-116">string</span></span>  | <span data-ttu-id="986b5-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="986b5-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="986b5-119">Aceptar</span><span class="sxs-lookup"><span data-stu-id="986b5-119">Accept</span></span> | <span data-ttu-id="986b5-120">string</span><span class="sxs-lookup"><span data-stu-id="986b5-120">string</span></span> | `application/json` |  

## <a name="request-body"></a><span data-ttu-id="986b5-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="986b5-121">Request body</span></span>
<span data-ttu-id="986b5-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="986b5-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="986b5-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="986b5-123">Response</span></span>

<span data-ttu-id="986b5-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="986b5-124">If successful, this method returns a `200 OK` response code and collection of [notebook](../resources/notebook.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="986b5-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="986b5-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="986b5-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="986b5-126">Request</span></span>
<span data-ttu-id="986b5-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="986b5-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebooks"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks
```
##### <a name="response"></a><span data-ttu-id="986b5-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="986b5-128">Response</span></span>
<span data-ttu-id="986b5-p102">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="986b5-p102">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 369

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List notebooks",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->