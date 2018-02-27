# <a name="create-educationclass"></a><span data-ttu-id="08e7a-101">Crear educationClass</span><span class="sxs-lookup"><span data-stu-id="08e7a-101">Create educationClass</span></span>

<span data-ttu-id="08e7a-102">Cree una clase.</span><span class="sxs-lookup"><span data-stu-id="08e7a-102">Create a new class library project.</span></span> <span data-ttu-id="08e7a-103">Esto también creará un grupo universal.</span><span class="sxs-lookup"><span data-stu-id="08e7a-103">This will also create a universal group.</span></span> <span data-ttu-id="08e7a-104">Al usar esta API para crear una clase, se agregará propiedades especiales al grupo, que agregará características como, por ejemplo, tareas y un tratamiento especial en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="08e7a-104">When you use this API to create a class, it will add special properties to the group, which will add features such as assignments and special handling within Microsoft Teams.</span></span>

## <a name="permissions"></a><span data-ttu-id="08e7a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="08e7a-105">Permissions</span></span>
<span data-ttu-id="08e7a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="08e7a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="08e7a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08e7a-108">Permission type</span></span>      | <span data-ttu-id="08e7a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08e7a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="08e7a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08e7a-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="08e7a-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08e7a-111">Not supported.</span></span>  |
|<span data-ttu-id="08e7a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08e7a-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="08e7a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08e7a-113">Not supported.</span></span>  |
|<span data-ttu-id="08e7a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08e7a-114">Application</span></span> | <span data-ttu-id="08e7a-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="08e7a-115">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="08e7a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08e7a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /education/classes
```
## <a name="request-headers"></a><span data-ttu-id="08e7a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08e7a-117">Request headers</span></span>
| <span data-ttu-id="08e7a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08e7a-118">Header</span></span>       | <span data-ttu-id="08e7a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="08e7a-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="08e7a-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="08e7a-120">Authorization</span></span>  | <span data-ttu-id="08e7a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08e7a-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="08e7a-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="08e7a-123">Content-Type</span></span>  | <span data-ttu-id="08e7a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="08e7a-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="08e7a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08e7a-125">Request body</span></span>
<span data-ttu-id="08e7a-126">En el cuerpo de la solicitud, especifique una representación JSON de un objeto [educationClass](../resources/educationclass.md).</span><span class="sxs-lookup"><span data-stu-id="08e7a-126">In the request body, supply a JSON representation of an [invitation](../resources/educationclass.md) object.</span></span>


## <a name="response"></a><span data-ttu-id="08e7a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08e7a-127">Response</span></span>
<span data-ttu-id="08e7a-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08e7a-128">If successful, this method returns a `201 Created` response code and an [event](../resources/educationclass.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08e7a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08e7a-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="08e7a-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08e7a-130">Request</span></span>
<span data-ttu-id="08e7a-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08e7a-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationroot"
}-->
```http
POST https://graph.microsoft.com/v1.0/education/classes
Content-type: application/json
Content-length: 224

{
  "description": "Health Level 1",
  "classCode": "Health 501",
  "displayName": "Health 1",
  "externalId": "11019",
  "externalName": "Health Level 1",
  "externalSource": "sis",
  "mailNickname": "fineartschool.net"
}
```

##### <a name="response"></a><span data-ttu-id="08e7a-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08e7a-132">Response</span></span>
<span data-ttu-id="08e7a-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08e7a-133">The following is an example of the response.</span></span> 

><span data-ttu-id="08e7a-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="08e7a-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 224

{
    "id": "11019",
    "description": "Health Level 1",
    "classCode": "Health 501",
    "createdBy": {
      "user": {
        "displayName": "Susana Rocha",
        "id": "14012",
      }
    },
    "displayName": "Health 1",
    "externalId": "11019",
    "externalName": "Health Level 1",
    "externalSource": "sis",
    "mailNickname": "fineartschool.net"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->