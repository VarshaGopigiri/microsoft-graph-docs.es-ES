# <a name="list-notebooks"></a><span data-ttu-id="e2c48-101">Enumerar blocs de notas</span><span class="sxs-lookup"><span data-stu-id="e2c48-101">List notebooks</span></span>

<span data-ttu-id="e2c48-102">Recupera una lista de objetos [notebook](../resources/notebook.md).</span><span class="sxs-lookup"><span data-stu-id="e2c48-102">Retrieve a list of [notebook](../resources/notebook.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="e2c48-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e2c48-103">Permissions</span></span>
<span data-ttu-id="e2c48-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e2c48-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e2c48-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e2c48-106">Permission type</span></span>      | <span data-ttu-id="e2c48-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e2c48-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e2c48-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e2c48-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e2c48-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e2c48-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="e2c48-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e2c48-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e2c48-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e2c48-111">Notes.Create, Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="e2c48-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e2c48-112">Application</span></span> | <span data-ttu-id="e2c48-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e2c48-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e2c48-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e2c48-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks
GET /users/{id | userPrincipalName}/onenote/notebooks
GET /groups/{id}/onenote/notebooks
GET /sites/{id}/onenote/notebooks
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e2c48-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e2c48-115">Optional query parameters</span></span>
<span data-ttu-id="e2c48-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2c48-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="e2c48-117">El criterio de ordenación predeterminado es `name asc`.</span><span class="sxs-lookup"><span data-stu-id="e2c48-117">The default sort order is `name asc`.</span></span> 

<span data-ttu-id="e2c48-118">`sections` y `sectionGroups` son valores de `expand` para los blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="e2c48-118">Valid `expand` values for notebooks are `sections` and `sectionGroups`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e2c48-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2c48-119">Request headers</span></span>
| <span data-ttu-id="e2c48-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="e2c48-120">Name</span></span>       | <span data-ttu-id="e2c48-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2c48-121">Type</span></span> | <span data-ttu-id="e2c48-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2c48-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e2c48-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e2c48-123">Authorization</span></span>  | <span data-ttu-id="e2c48-124">string</span><span class="sxs-lookup"><span data-stu-id="e2c48-124">string</span></span>  | <span data-ttu-id="e2c48-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e2c48-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e2c48-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e2c48-127">Accept</span></span> | <span data-ttu-id="e2c48-128">string</span><span class="sxs-lookup"><span data-stu-id="e2c48-128">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="e2c48-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e2c48-129">Request body</span></span>
<span data-ttu-id="e2c48-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e2c48-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e2c48-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2c48-131">Response</span></span>

<span data-ttu-id="e2c48-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2c48-132">If successful, this method returns a `200 OK` response code and collection of [notebook](../resources/notebook.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e2c48-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2c48-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e2c48-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e2c48-134">Request</span></span>
<span data-ttu-id="e2c48-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2c48-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_notebooks"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks
```
##### <a name="response"></a><span data-ttu-id="e2c48-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2c48-136">Response</span></span>
<span data-ttu-id="e2c48-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e2c48-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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