# <a name="list-sectiongroups"></a><span data-ttu-id="7b6c1-101">Enumerar sectionGroups</span><span class="sxs-lookup"><span data-stu-id="7b6c1-101">List sectionGroups</span></span>

<span data-ttu-id="7b6c1-102">Recupera una lista de objetos [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="7b6c1-102">Retrieve a list of [sectionGroup](../resources/sectiongroup.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="7b6c1-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b6c1-103">Permissions</span></span>
<span data-ttu-id="7b6c1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7b6c1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7b6c1-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b6c1-106">Permission type</span></span>      | <span data-ttu-id="7b6c1-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b6c1-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="7b6c1-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b6c1-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7b6c1-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b6c1-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="7b6c1-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b6c1-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b6c1-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7b6c1-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="7b6c1-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b6c1-112">Application</span></span> | <span data-ttu-id="7b6c1-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b6c1-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="7b6c1-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b6c1-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups
GET /users/{id | userPrincipalName}/onenote/sectionGroups
GET /groups/{id}/onenote/sectionGroups
GET /sites/{id}/onenote/sectionGroups
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7b6c1-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7b6c1-115">Optional query parameters</span></span>
<span data-ttu-id="7b6c1-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="7b6c1-117">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-117">The default sort order is `name asc`.</span></span>

<span data-ttu-id="7b6c1-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` de los grupos de secciones son `sections`, `sectionGroups`, `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for section groups are `sections`, `sectionGroups`, `parentNotebook`, and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7b6c1-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b6c1-120">Request headers</span></span>
| <span data-ttu-id="7b6c1-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b6c1-121">Name</span></span>       | <span data-ttu-id="7b6c1-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b6c1-122">Type</span></span> | <span data-ttu-id="7b6c1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b6c1-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7b6c1-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="7b6c1-124">Authorization</span></span>  | <span data-ttu-id="7b6c1-125">string</span><span class="sxs-lookup"><span data-stu-id="7b6c1-125">string</span></span>  | <span data-ttu-id="7b6c1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7b6c1-128">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7b6c1-128">Accept</span></span> | <span data-ttu-id="7b6c1-129">string</span><span class="sxs-lookup"><span data-stu-id="7b6c1-129">string</span></span> | `application/json` |  

## <a name="request-body"></a><span data-ttu-id="7b6c1-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b6c1-130">Request body</span></span>
<span data-ttu-id="7b6c1-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7b6c1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b6c1-132">Response</span></span>

<span data-ttu-id="7b6c1-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-133">If successful, this method returns a `200 OK` response code and collection of [sectionGroup](../resources/sectiongroup.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7b6c1-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b6c1-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7b6c1-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b6c1-135">Request</span></span>
<span data-ttu-id="7b6c1-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroups"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups
```
##### <a name="response"></a><span data-ttu-id="7b6c1-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b6c1-137">Response</span></span>
<span data-ttu-id="7b6c1-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b6c1-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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