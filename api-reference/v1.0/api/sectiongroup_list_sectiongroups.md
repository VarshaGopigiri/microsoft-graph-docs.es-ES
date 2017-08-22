# <a name="list-sectiongroups"></a><span data-ttu-id="7c760-101">Enumerar sectionGroups</span><span class="sxs-lookup"><span data-stu-id="7c760-101">List sectionGroups</span></span>

<span data-ttu-id="7c760-102">Recupere una lista de [grupos de sección](../resources/sectiongroup.md) desde el grupo de sección especificado.</span><span class="sxs-lookup"><span data-stu-id="7c760-102">Retrieve a list of [section groups](../resources/sectiongroup.md) from the specified section group.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7c760-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7c760-103">Prerequisites</span></span>
<span data-ttu-id="7c760-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="7c760-104">One of the following **scopes** is required to execute this API:</span></span>  

<span data-ttu-id="7c760-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7c760-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="7c760-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7c760-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}/sectionGroups
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sectionGroups
GET /groups/{id}/onenote/sectionGroups/{id}/sectionGroups
GET /sites/{id}/onenote/sectionGroups/{id}/sectionGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7c760-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7c760-107">Optional query parameters</span></span>
<span data-ttu-id="7c760-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c760-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="7c760-109">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="7c760-109">The default sort order is `name asc`.</span></span>

<span data-ttu-id="7c760-p101">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` de los grupos de secciones son `sections`, `sectionGroups`, `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="7c760-p101">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for section groups are `sections`, `sectionGroups`, `parentNotebook`, and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7c760-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7c760-112">Request headers</span></span>
| <span data-ttu-id="7c760-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c760-113">Name</span></span>       | <span data-ttu-id="7c760-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c760-114">Type</span></span> | <span data-ttu-id="7c760-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c760-115">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7c760-116">Authorization</span><span class="sxs-lookup"><span data-stu-id="7c760-116">Authorization</span></span>  | <span data-ttu-id="7c760-117">string</span><span class="sxs-lookup"><span data-stu-id="7c760-117">string</span></span>  | <span data-ttu-id="7c760-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c760-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7c760-120">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7c760-120">Accept</span></span> | <span data-ttu-id="7c760-121">string</span><span class="sxs-lookup"><span data-stu-id="7c760-121">string</span></span> | `application/json` |  

## <a name="request-body"></a><span data-ttu-id="7c760-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7c760-122">Request body</span></span>
<span data-ttu-id="7c760-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7c760-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7c760-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c760-124">Response</span></span>

<span data-ttu-id="7c760-125">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c760-125">If successful, this method returns a `200 OK` response code and a collection of [sectionGroup](../resources/sectiongroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7c760-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c760-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7c760-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7c760-127">Request</span></span>
<span data-ttu-id="7c760-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c760-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroups"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}/sectionGroups
```
##### <a name="response"></a><span data-ttu-id="7c760-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c760-129">Response</span></span>
<span data-ttu-id="7c760-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c760-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectiongroup",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 378

{
  "value": [
    {
      "sectionsUrl": "sectionsUrl-value",
      "sectionGroupsUrl": "sectionGroupsUrl-value",
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
  "description": "List sectionGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->