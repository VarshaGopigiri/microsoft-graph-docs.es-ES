# <a name="get-section"></a><span data-ttu-id="05774-101">Obtener sección</span><span class="sxs-lookup"><span data-stu-id="05774-101">Get section</span></span>

<span data-ttu-id="05774-102">Recupere las propiedades y las relaciones de un objeto [section](../resources/section.md).</span><span class="sxs-lookup"><span data-stu-id="05774-102">Retrieve the properties and relationships of a [section](../resources/section.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="05774-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="05774-103">Permissions</span></span>
<span data-ttu-id="05774-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="05774-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="05774-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05774-106">Permission type</span></span>      | <span data-ttu-id="05774-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05774-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="05774-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05774-108">Delegated (work or school account)</span></span> | <span data-ttu-id="05774-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05774-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="05774-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05774-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05774-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="05774-111">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="05774-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05774-112">Application</span></span> | <span data-ttu-id="05774-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05774-113">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="05774-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05774-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sections/{id}
GET /users/{id | userPrincipalName}/onenote/sections/{id}
GET /groups/{id}/onenote/sections/{id}
GET /sites/{id}/onenote/sections/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="05774-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="05774-115">Optional query parameters</span></span>
<span data-ttu-id="05774-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05774-116">This method supports the `select` and `expand` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="05774-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="05774-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="05774-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05774-119">Request headers</span></span>
| <span data-ttu-id="05774-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="05774-120">Name</span></span>       | <span data-ttu-id="05774-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="05774-121">Type</span></span> | <span data-ttu-id="05774-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="05774-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="05774-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="05774-123">Authorization</span></span>  | <span data-ttu-id="05774-124">string</span><span class="sxs-lookup"><span data-stu-id="05774-124">string</span></span>  | <span data-ttu-id="05774-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05774-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="05774-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="05774-127">Accept</span></span> | <span data-ttu-id="05774-128">string</span><span class="sxs-lookup"><span data-stu-id="05774-128">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="05774-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05774-129">Request body</span></span>
<span data-ttu-id="05774-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="05774-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="05774-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05774-131">Response</span></span>

<span data-ttu-id="05774-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [section](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05774-132">If successful, this method returns a `200 OK` response code and a [section](../resources/section.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="05774-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05774-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="05774-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05774-134">Request</span></span>
<span data-ttu-id="05774-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="05774-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_section"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sections/{id}
```
##### <a name="response"></a><span data-ttu-id="05774-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05774-136">Response</span></span>
<span data-ttu-id="05774-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05774-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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