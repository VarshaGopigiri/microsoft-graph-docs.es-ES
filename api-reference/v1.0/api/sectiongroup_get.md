# <a name="get-sectiongroup"></a><span data-ttu-id="d0e50-101">Obtener sectionGroup</span><span class="sxs-lookup"><span data-stu-id="d0e50-101">Get sectionGroup</span></span>

<span data-ttu-id="d0e50-102">Recupere las propiedades y relaciones de un objeto [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="d0e50-102">Retrieve the properties and relationships of a [sectionGroup](../resources/sectiongroup.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d0e50-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0e50-103">Prerequisites</span></span>
<span data-ttu-id="d0e50-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d0e50-104">One of the following **scopes** is required to execute this API:</span></span>  

<span data-ttu-id="d0e50-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0e50-105">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="d0e50-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0e50-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}
GET /groups/{id}/onenote/sectionGroups/{id}
GET /sites/{id}/onenote/sectionGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="d0e50-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d0e50-107">Optional query parameters</span></span>
<span data-ttu-id="d0e50-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0e50-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="d0e50-p101">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `name` y `self`. Los valores válidos de `expand` de los grupos de secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="d0e50-p101">The default query expands `parentNotebook` and selects its `id`, `name`, and `self` properties. Valid `expand` values for section groups are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d0e50-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0e50-111">Request headers</span></span>
| <span data-ttu-id="d0e50-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0e50-112">Name</span></span>       | <span data-ttu-id="d0e50-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0e50-113">Type</span></span> | <span data-ttu-id="d0e50-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0e50-114">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="d0e50-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0e50-115">Authorization</span></span>  | <span data-ttu-id="d0e50-116">string</span><span class="sxs-lookup"><span data-stu-id="d0e50-116">string</span></span>  | <span data-ttu-id="d0e50-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0e50-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d0e50-119">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d0e50-119">Accept</span></span> | <span data-ttu-id="d0e50-120">string</span><span class="sxs-lookup"><span data-stu-id="d0e50-120">string</span></span> | `application/json` | 

## <a name="request-body"></a><span data-ttu-id="d0e50-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0e50-121">Request body</span></span>
<span data-ttu-id="d0e50-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d0e50-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d0e50-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0e50-123">Response</span></span>

<span data-ttu-id="d0e50-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0e50-124">If successful, this method returns a `200 OK` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="d0e50-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0e50-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d0e50-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0e50-126">Request</span></span>
<span data-ttu-id="d0e50-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0e50-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroup"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="d0e50-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0e50-128">Response</span></span>
<span data-ttu-id="d0e50-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0e50-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sectiongroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 305

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get sectionGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->