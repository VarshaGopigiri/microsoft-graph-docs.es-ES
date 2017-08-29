# <a name="get-notebook"></a><span data-ttu-id="7d8b6-101">Obtener bloc de notas</span><span class="sxs-lookup"><span data-stu-id="7d8b6-101">Get notebook</span></span>

<span data-ttu-id="7d8b6-102">Recupera las propiedades y las relaciones de un objeto [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="7d8b6-102">Retrieve the properties and relationships of a [notebook](../resources/notebook.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="7d8b6-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7d8b6-103">Permissions</span></span>
<span data-ttu-id="7d8b6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7d8b6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7d8b6-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7d8b6-106">Permission type</span></span>      | <span data-ttu-id="7d8b6-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7d8b6-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="7d8b6-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7d8b6-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7d8b6-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d8b6-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="7d8b6-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7d8b6-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7d8b6-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7d8b6-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="7d8b6-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7d8b6-112">Application</span></span> | <span data-ttu-id="7d8b6-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7d8b6-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="7d8b6-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7d8b6-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/{id}
GET /users/{id | userPrincipalName}/onenote/notebooks/{id}
GET /groups/{id}/onenote/notebooks/{id}
GET /sites/{id}/onenote/notebooks/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="7d8b6-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7d8b6-115">Optional query parameters</span></span>
<span data-ttu-id="7d8b6-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d8b6-116">This method supports the `select` and `expand` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="7d8b6-117">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="7d8b6-117">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7d8b6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7d8b6-118">Request headers</span></span>
| <span data-ttu-id="7d8b6-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="7d8b6-119">Name</span></span>       | <span data-ttu-id="7d8b6-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d8b6-120">Type</span></span> | <span data-ttu-id="7d8b6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d8b6-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="7d8b6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="7d8b6-122">Authorization</span></span>  | <span data-ttu-id="7d8b6-123">string</span><span class="sxs-lookup"><span data-stu-id="7d8b6-123">string</span></span>  | <span data-ttu-id="7d8b6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7d8b6-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7d8b6-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7d8b6-126">Accept</span></span> | <span data-ttu-id="7d8b6-127">string</span><span class="sxs-lookup"><span data-stu-id="7d8b6-127">string</span></span> | `application/json` | 

## <a name="request-body"></a><span data-ttu-id="7d8b6-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7d8b6-128">Request body</span></span>
<span data-ttu-id="7d8b6-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7d8b6-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7d8b6-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d8b6-130">Response</span></span>

<span data-ttu-id="7d8b6-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7d8b6-131">If successful, this method returns a `200 OK` response code and a [notebook](../resources/notebook.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7d8b6-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7d8b6-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7d8b6-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7d8b6-133">Request</span></span>
<span data-ttu-id="7d8b6-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7d8b6-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebook"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}
```
##### <a name="response"></a><span data-ttu-id="7d8b6-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7d8b6-135">Response</span></span>
<span data-ttu-id="7d8b6-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7d8b6-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
