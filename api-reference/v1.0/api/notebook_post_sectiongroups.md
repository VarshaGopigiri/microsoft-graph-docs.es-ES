# <a name="create-sectiongroup"></a><span data-ttu-id="bfc6b-101">Crear sectionGroup</span><span class="sxs-lookup"><span data-stu-id="bfc6b-101">Create sectionGroup</span></span>

<span data-ttu-id="bfc6b-102">Cree un [grupo de sección](../resources/sectiongroup.md) en el bloc de notas especificado.</span><span class="sxs-lookup"><span data-stu-id="bfc6b-102">Create a new [section group](../resources/sectiongroup.md) in the specified notebook.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bfc6b-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bfc6b-103">Prerequisites</span></span>
<span data-ttu-id="bfc6b-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="bfc6b-104">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="bfc6b-105">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bfc6b-105">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="bfc6b-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bfc6b-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/sectionGroups
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/sectionGroups
POST /groups/{id}/onenote/notebooks/{id}/sectionGroups
POST /sites/{id}/onenote/notebooks/{id}/sectionGroups
```
## <a name="request-headers"></a><span data-ttu-id="bfc6b-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bfc6b-107">Request headers</span></span>
| <span data-ttu-id="bfc6b-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="bfc6b-108">Name</span></span>       | <span data-ttu-id="bfc6b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfc6b-109">Type</span></span> | <span data-ttu-id="bfc6b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfc6b-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bfc6b-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="bfc6b-111">Authorization</span></span>  | <span data-ttu-id="bfc6b-112">string</span><span class="sxs-lookup"><span data-stu-id="bfc6b-112">string</span></span>  | <span data-ttu-id="bfc6b-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bfc6b-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bfc6b-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bfc6b-115">Content-Type</span></span> | <span data-ttu-id="bfc6b-116">string</span><span class="sxs-lookup"><span data-stu-id="bfc6b-116">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="bfc6b-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bfc6b-117">Request body</span></span>
<span data-ttu-id="bfc6b-118">En el cuerpo de la solicitud, asigne un nombre al grupo de sección.</span><span class="sxs-lookup"><span data-stu-id="bfc6b-118">In the request body, supply a name for the section group.</span></span>

<span data-ttu-id="bfc6b-p102">En el mismo nivel de jerarquía, los nombres de grupo de sección deben ser únicos. El nombre no puede contener más de 50 caracteres ni los caracteres siguientes: ?*\/:<>|&#''%~</span><span class="sxs-lookup"><span data-stu-id="bfc6b-p102">Within the same hierarchy level, section group names must be unique. The name cannot contain more than 50 characters or contain the following characters:  ?*\/:<>|&#''%~</span></span>

## <a name="response"></a><span data-ttu-id="bfc6b-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfc6b-121">Response</span></span>

<span data-ttu-id="bfc6b-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [sectionGroup](../resources/sectiongroup.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bfc6b-122">If successful, this method returns `201 Created` response code and a [sectionGroup](../resources/sectiongroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bfc6b-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bfc6b-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bfc6b-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bfc6b-124">Request</span></span>
<span data-ttu-id="bfc6b-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfc6b-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_sectiongroup_from_notebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/sectionGroups
Content-type: application/json
Content-length: 30

{
  "displayName": "Section group name"
}
```

##### <a name="response"></a><span data-ttu-id="bfc6b-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bfc6b-126">Response</span></span>
<span data-ttu-id="bfc6b-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bfc6b-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create SectionGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
