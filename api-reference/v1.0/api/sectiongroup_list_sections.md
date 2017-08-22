# <a name="list-sections"></a><span data-ttu-id="4cfbc-101">Enumerar secciones</span><span class="sxs-lookup"><span data-stu-id="4cfbc-101">List sections</span></span>

<span data-ttu-id="4cfbc-102">Recupere una lista de objetos [section](../resources/section.md) desde el grupo de sección especificado.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-102">Retrieve a list of [section](../resources/section.md) objects from the specified section group.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4cfbc-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4cfbc-103">Prerequisites</span></span>
<span data-ttu-id="4cfbc-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="4cfbc-104">One of the following **scopes** is required to execute this API:</span></span>  

<span data-ttu-id="4cfbc-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4cfbc-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="4cfbc-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4cfbc-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}/sections
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sections
GET /groups/{id}/onenote/sectionGroups/{id}/sections
GET /sites/{id}/onenote/sectionGroups/{id}/sections
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4cfbc-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4cfbc-107">Optional query parameters</span></span>
<span data-ttu-id="4cfbc-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="4cfbc-109">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-109">The default sort order is `name asc`.</span></span>

<span data-ttu-id="4cfbc-p101">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-p101">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>


## <a name="request-headers"></a><span data-ttu-id="4cfbc-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4cfbc-112">Request headers</span></span>
| <span data-ttu-id="4cfbc-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="4cfbc-113">Name</span></span>       | <span data-ttu-id="4cfbc-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="4cfbc-114">Type</span></span> | <span data-ttu-id="4cfbc-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cfbc-115">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="4cfbc-116">Authorization</span><span class="sxs-lookup"><span data-stu-id="4cfbc-116">Authorization</span></span>  | <span data-ttu-id="4cfbc-117">string</span><span class="sxs-lookup"><span data-stu-id="4cfbc-117">string</span></span>  | <span data-ttu-id="4cfbc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4cfbc-120">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4cfbc-120">Accept</span></span> | <span data-ttu-id="4cfbc-121">string</span><span class="sxs-lookup"><span data-stu-id="4cfbc-121">string</span></span> | `application/json` |  

## <a name="request-body"></a><span data-ttu-id="4cfbc-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4cfbc-122">Request body</span></span>
<span data-ttu-id="4cfbc-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4cfbc-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cfbc-124">Response</span></span>

<span data-ttu-id="4cfbc-125">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [section](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-125">If successful, this method returns a `200 OK` response code and a collection of [section](../resources/section.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4cfbc-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4cfbc-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4cfbc-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4cfbc-127">Request</span></span>
<span data-ttu-id="4cfbc-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sections"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}/sections
```
##### <a name="response"></a><span data-ttu-id="4cfbc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cfbc-129">Response</span></span>
<span data-ttu-id="4cfbc-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteSection",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 345

{
  "value": [
    {
      "isDefault": true,
      "pagesUrl": "pagesUrl-value",
      "displayName": "name-value",      
      "createdBy": {
        "user": {
          "id": "id-value",
          "displayName": "displayName-value"
        }
      },
      "lastModifiedBy": {
        "user": {
          "id": "id-value",
          "displayName": "displayName-value"
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
  "description": "List sections",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->