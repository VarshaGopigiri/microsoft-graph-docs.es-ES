# <a name="get-section"></a><span data-ttu-id="9a95a-101">Obtener section</span><span class="sxs-lookup"><span data-stu-id="9a95a-101">Get section</span></span>

<span data-ttu-id="9a95a-102">Recuperar las propiedades y relaciones de un objeto [onenoteSection](../resources/section.md).</span><span class="sxs-lookup"><span data-stu-id="9a95a-102">Retrieve the properties and relationships of [plannertaskdetails](../resources/section.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="9a95a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a95a-103">Permissions</span></span>
<span data-ttu-id="9a95a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9a95a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9a95a-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a95a-106">Permission type</span></span>      | <span data-ttu-id="9a95a-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a95a-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9a95a-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a95a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9a95a-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9a95a-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="9a95a-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a95a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a95a-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9a95a-111">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="9a95a-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a95a-112">Application</span></span> | <span data-ttu-id="9a95a-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9a95a-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9a95a-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a95a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections/{id}
GET /users/{id | userPrincipalName}/onenote/sections/{id}
GET /groups/{id}/onenote/sections/{id}
GET /sites/{id}/onenote/sections/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="9a95a-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9a95a-115">Optional query parameters</span></span>
<span data-ttu-id="9a95a-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a95a-116">This method supports the `select` and `expand` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="9a95a-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="9a95a-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9a95a-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a95a-119">Request headers</span></span>
| <span data-ttu-id="9a95a-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9a95a-120">Name</span></span>       | <span data-ttu-id="9a95a-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a95a-121">Type</span></span> | <span data-ttu-id="9a95a-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a95a-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="9a95a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a95a-123">Authorization</span></span>  | <span data-ttu-id="9a95a-124">cadena</span><span class="sxs-lookup"><span data-stu-id="9a95a-124">string</span></span>  | <span data-ttu-id="9a95a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a95a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9a95a-127">Accept</span><span class="sxs-lookup"><span data-stu-id="9a95a-127">Accept</span></span> | <span data-ttu-id="9a95a-128">cadena</span><span class="sxs-lookup"><span data-stu-id="9a95a-128">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="9a95a-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a95a-129">Request body</span></span>
<span data-ttu-id="9a95a-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9a95a-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9a95a-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a95a-131">Response</span></span>

<span data-ttu-id="9a95a-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [onenoteSection](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a95a-132">If successful, this method returns a `200 OK` response code and a [user](../resources/section.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="9a95a-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a95a-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9a95a-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a95a-134">Request</span></span>
<span data-ttu-id="9a95a-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a95a-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_section"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sections/{id}
```
##### <a name="response"></a><span data-ttu-id="9a95a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a95a-136">Response</span></span>
<span data-ttu-id="9a95a-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9a95a-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteSection"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 272

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get section",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->