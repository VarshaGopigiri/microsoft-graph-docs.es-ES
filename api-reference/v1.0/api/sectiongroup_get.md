# <a name="get-sectiongroup"></a><span data-ttu-id="fc57f-101">Obtener sectionGroup</span><span class="sxs-lookup"><span data-stu-id="fc57f-101">Get sectionGroup</span></span>

<span data-ttu-id="fc57f-102">Recupera las propiedades y relaciones de un objeto [sectionGroup](../resources/sectiongroup.md).</span><span class="sxs-lookup"><span data-stu-id="fc57f-102">Retrieve the properties and relationships of a [sectionGroup](../resources/sectiongroup.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="fc57f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="fc57f-103">Permissions</span></span>
<span data-ttu-id="fc57f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fc57f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fc57f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc57f-106">Permission type</span></span>      | <span data-ttu-id="fc57f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc57f-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="fc57f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc57f-108">Delegated (work or school account)</span></span> | <span data-ttu-id="fc57f-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc57f-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="fc57f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc57f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fc57f-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fc57f-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="fc57f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc57f-112">Application</span></span> | <span data-ttu-id="fc57f-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc57f-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="fc57f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc57f-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}
GET /groups/{id}/onenote/sectionGroups/{id}
GET /sites/{id}/onenote/sectionGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="fc57f-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fc57f-115">Optional query parameters</span></span>
<span data-ttu-id="fc57f-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc57f-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="fc57f-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `name` y `self`. Los valores válidos de `expand` de los grupos de secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="fc57f-p102">The default query expands `parentNotebook` and selects its `id`, `name`, and `self` properties. Valid `expand` values for section groups are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="fc57f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc57f-119">Request headers</span></span>
| <span data-ttu-id="fc57f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fc57f-120">Name</span></span>       | <span data-ttu-id="fc57f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc57f-121">Type</span></span> | <span data-ttu-id="fc57f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc57f-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="fc57f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc57f-123">Authorization</span></span>  | <span data-ttu-id="fc57f-124">string</span><span class="sxs-lookup"><span data-stu-id="fc57f-124">string</span></span>  | <span data-ttu-id="fc57f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fc57f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fc57f-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fc57f-127">Accept</span></span> | <span data-ttu-id="fc57f-128">string</span><span class="sxs-lookup"><span data-stu-id="fc57f-128">string</span></span> | `application/json` | 

## <a name="request-body"></a><span data-ttu-id="fc57f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc57f-129">Request body</span></span>
<span data-ttu-id="fc57f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fc57f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fc57f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc57f-131">Response</span></span>

<span data-ttu-id="fc57f-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [sectionGroup](../resources/sectiongroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc57f-132">If successful, this method returns a `200 OK` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fc57f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc57f-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fc57f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc57f-134">Request</span></span>
<span data-ttu-id="fc57f-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc57f-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sectiongroup"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="fc57f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc57f-136">Response</span></span>
<span data-ttu-id="fc57f-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc57f-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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