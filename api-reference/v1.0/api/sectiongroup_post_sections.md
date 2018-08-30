# <a name="create-section"></a><span data-ttu-id="84d6d-101">Create section</span><span class="sxs-lookup"><span data-stu-id="84d6d-101">Create section</span></span>

<span data-ttu-id="84d6d-102">Crea una [onenoteSection](../resources/section.md) nueva en el grupo de sección especificado.</span><span class="sxs-lookup"><span data-stu-id="84d6d-102">Create a new [section](../resources/section.md) in the specified section group.</span></span>
## <a name="permissions"></a><span data-ttu-id="84d6d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="84d6d-103">Permissions</span></span>
<span data-ttu-id="84d6d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="84d6d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="84d6d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="84d6d-106">Permission type</span></span>      | <span data-ttu-id="84d6d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="84d6d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="84d6d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="84d6d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="84d6d-109">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="84d6d-109">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="84d6d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="84d6d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="84d6d-111">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84d6d-111">Notes.Create, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="84d6d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="84d6d-112">Application</span></span> | <span data-ttu-id="84d6d-113">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="84d6d-113">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="84d6d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84d6d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sectionGroups/{id}/sections
POST /users/{id | userPrincipalName}/onenote/sectionGroups/{id}/sections
POST /groups/{id}/onenote/sectionGroups/{id}/sections
POST /sites/{id}/onenote/sectionGroups/{id}/sections
```
## <a name="request-headers"></a><span data-ttu-id="84d6d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="84d6d-115">Request headers</span></span>
| <span data-ttu-id="84d6d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="84d6d-116">Name</span></span>       | <span data-ttu-id="84d6d-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="84d6d-117">Type</span></span> | <span data-ttu-id="84d6d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="84d6d-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="84d6d-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="84d6d-119">Authorization</span></span>  | <span data-ttu-id="84d6d-120">cadena</span><span class="sxs-lookup"><span data-stu-id="84d6d-120">string</span></span>  | <span data-ttu-id="84d6d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="84d6d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="84d6d-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="84d6d-123">Content-Type</span></span> | <span data-ttu-id="84d6d-124">cadena</span><span class="sxs-lookup"><span data-stu-id="84d6d-124">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="84d6d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="84d6d-125">Request body</span></span>
<span data-ttu-id="84d6d-126">En el cuerpo de la solicitud, asigne un nombre a la sección.</span><span class="sxs-lookup"><span data-stu-id="84d6d-126">In the request body, supply a name for the section.</span></span>

<span data-ttu-id="84d6d-p103">En el mismo nivel de jerarquía, los nombres de sección deben ser únicos. El nombre no puede contener más de 50 caracteres ni los caracteres siguientes: ?\*\/:<>|&#''%~</span><span class="sxs-lookup"><span data-stu-id="84d6d-p103">Within the same hierarchy level, section names must be unique. The name cannot contain more than 50 characters or contain the following characters:  ?\*\/:<>|&#''%~</span></span>

## <a name="response"></a><span data-ttu-id="84d6d-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84d6d-129">Response</span></span>

<span data-ttu-id="84d6d-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [onenoteSection](../resources/section.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="84d6d-130">If successful, this method returns a `201 Created` response code and a [user](../resources/section.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="84d6d-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84d6d-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="84d6d-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="84d6d-132">Request</span></span>
<span data-ttu-id="84d6d-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="84d6d-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_section_from_sectiongroup"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sectionGroups/{id}/sections
Content-type: application/json
Content-length: 27

{
  "displayName": "Section name"
}
```

##### <a name="response"></a><span data-ttu-id="84d6d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84d6d-134">Response</span></span>
<span data-ttu-id="84d6d-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="84d6d-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create Section",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->