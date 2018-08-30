# <a name="list-sections"></a><span data-ttu-id="414e9-101">Listar secciones</span><span class="sxs-lookup"><span data-stu-id="414e9-101">List sections</span></span>

<span data-ttu-id="414e9-102">Recupera una lista de objetos [onenoteSection](../resources/section.md) desde el grupo de sección especificado.</span><span class="sxs-lookup"><span data-stu-id="414e9-102">Retrieve a list of [section](../resources/section.md) objects from the specified section group.</span></span>
## <a name="permissions"></a><span data-ttu-id="414e9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="414e9-103">Permissions</span></span>
<span data-ttu-id="414e9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="414e9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="414e9-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="414e9-106">Permission type</span></span>      | <span data-ttu-id="414e9-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="414e9-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="414e9-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="414e9-108">Delegated (work or school account)</span></span> | <span data-ttu-id="414e9-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="414e9-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="414e9-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="414e9-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="414e9-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="414e9-111">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="414e9-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="414e9-112">Application</span></span> | <span data-ttu-id="414e9-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="414e9-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="414e9-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="414e9-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/sectionGroups/{id}/sections
GET /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sections
GET /groups/{id}/onenote/sectionGroups/{id}/sections
GET /sites/{id}/onenote/sectionGroups/{id}/sections
```
## <a name="optional-query-parameters"></a><span data-ttu-id="414e9-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="414e9-115">Optional query parameters</span></span>
<span data-ttu-id="414e9-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="414e9-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="414e9-117">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="414e9-117">The default sort order is `name asc`.</span></span>

<span data-ttu-id="414e9-p102">La consulta predeterminada expande `parentNotebook` y selecciona sus propiedades `id`, `displayName` y `self`. Los valores válidos de `expand` para las secciones son `parentNotebook` y `parentSectionGroup`.</span><span class="sxs-lookup"><span data-stu-id="414e9-p102">The default query expands `parentNotebook` and selects its `id`, `displayName`, and `self` properties. Valid `expand` values for sections are `parentNotebook` and `parentSectionGroup`.</span></span>


## <a name="request-headers"></a><span data-ttu-id="414e9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="414e9-120">Request headers</span></span>
| <span data-ttu-id="414e9-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="414e9-121">Name</span></span>       | <span data-ttu-id="414e9-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="414e9-122">Type</span></span> | <span data-ttu-id="414e9-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="414e9-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="414e9-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="414e9-124">Authorization</span></span>  | <span data-ttu-id="414e9-125">cadena</span><span class="sxs-lookup"><span data-stu-id="414e9-125">string</span></span>  | <span data-ttu-id="414e9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="414e9-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="414e9-128">Aceptar</span><span class="sxs-lookup"><span data-stu-id="414e9-128">Accept</span></span> | <span data-ttu-id="414e9-129">cadena</span><span class="sxs-lookup"><span data-stu-id="414e9-129">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="414e9-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="414e9-130">Request body</span></span>
<span data-ttu-id="414e9-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="414e9-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="414e9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="414e9-132">Response</span></span>

<span data-ttu-id="414e9-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [onenoteSection](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="414e9-133">If successful, this method returns a `200 OK` response code and a collection of [user](../resources/section.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="414e9-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="414e9-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="414e9-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="414e9-135">Request</span></span>
<span data-ttu-id="414e9-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="414e9-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_sections"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}/sections
```
##### <a name="response"></a><span data-ttu-id="414e9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="414e9-137">Response</span></span>
<span data-ttu-id="414e9-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="414e9-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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