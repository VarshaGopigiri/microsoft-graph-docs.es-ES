# <a name="get-educationclass"></a><span data-ttu-id="c32f9-101">Obtener educationClass</span><span class="sxs-lookup"><span data-stu-id="c32f9-101">Get educationClass</span></span>

<span data-ttu-id="c32f9-102">Recupere una clase del sistema.</span><span class="sxs-lookup"><span data-stu-id="c32f9-102">Retrieve a class from the system.</span></span> <span data-ttu-id="c32f9-103">Una clase es un grupo universal con una propiedad especial que indica al sistema que el grupo es una clase.</span><span class="sxs-lookup"><span data-stu-id="c32f9-103">A class is a universal group with a special property that indicates to the system that the group is a class.</span></span> <span data-ttu-id="c32f9-104">Los miembros del grupo representan a los alumnos; los administradores representan a los profesores de la clase.</span><span class="sxs-lookup"><span data-stu-id="c32f9-104">Group members represent the students;  group admins represent the teachers in the class.</span></span> <span data-ttu-id="c32f9-105">Si usa el token delegado, el usuario solo verá las clases en las que son miembros.</span><span class="sxs-lookup"><span data-stu-id="c32f9-105">If you're using the delegated token, the user will only see classes in which they are members.</span></span>

## <a name="permissions"></a><span data-ttu-id="c32f9-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c32f9-106">Permissions</span></span>
<span data-ttu-id="c32f9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c32f9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c32f9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c32f9-109">Permission type</span></span>      | <span data-ttu-id="c32f9-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c32f9-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c32f9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c32f9-111">Delegated (work or school account)</span></span> |  <span data-ttu-id="c32f9-112">EduRoster.ReadBasic</span><span class="sxs-lookup"><span data-stu-id="c32f9-112">EduRoster.ReadBasic</span></span>  |
|<span data-ttu-id="c32f9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c32f9-113">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="c32f9-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="c32f9-114">Not supported</span></span>  |
|<span data-ttu-id="c32f9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c32f9-115">Application</span></span> | <span data-ttu-id="c32f9-116">EduRoster.Read.All, EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c32f9-116">EduRoster.Read.All, EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="c32f9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c32f9-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c32f9-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c32f9-118">Optional query parameters</span></span>
<span data-ttu-id="c32f9-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c32f9-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c32f9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c32f9-120">Request headers</span></span>
| <span data-ttu-id="c32f9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c32f9-121">Header</span></span>       | <span data-ttu-id="c32f9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c32f9-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c32f9-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c32f9-123">Authorization</span></span>  | <span data-ttu-id="c32f9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c32f9-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c32f9-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c32f9-126">Request body</span></span>
<span data-ttu-id="c32f9-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c32f9-127">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="c32f9-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c32f9-128">Response</span></span>
<span data-ttu-id="c32f9-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [educationClass](../resources/educationclass.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c32f9-129">If successful, this method returns a `200 OK` response code and an [educationClass](../resources/educationclass.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c32f9-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c32f9-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c32f9-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c32f9-131">Request</span></span>
<span data-ttu-id="c32f9-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c32f9-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_educationclass"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/{class-id}
```
##### <a name="response"></a><span data-ttu-id="c32f9-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c32f9-133">Response</span></span>
<span data-ttu-id="c32f9-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c32f9-134">The following is an example of the response.</span></span> 

><span data-ttu-id="c32f9-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c32f9-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 224

{
  "id": "11023",
  "description": "English Level 2",
  "classCode": "11023",
  "createdBy": {
    "user": {
      "displayName": "Susana Rocha",
      "id": "14012",
    }
  },
  "displayName": "English - Language 2",
  "externalId": "301",
  "externalName": "English Level 1",
  "externalSource": "School of Fine Art",
  "mailNickname": "fineartschool.net "
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->