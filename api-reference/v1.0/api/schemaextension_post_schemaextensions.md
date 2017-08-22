# <a name="create-schemaextension"></a><span data-ttu-id="6b0b1-101">Crear schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="6b0b1-101">Create schemaExtension</span></span>

<span data-ttu-id="6b0b1-102">Crear una nueva definición de [schemaExtension](../resources/schemaextension.md) para extender a un [tipo de recurso compatible](../../../concepts/extensibility_overview.md#supported-resources).</span><span class="sxs-lookup"><span data-stu-id="6b0b1-102">Create a new [schemaExtension](../resources/schemaextension.md) definition to extend a [supporting resource type](../../../concepts/extensibility_overview.md#supported-resources).</span></span>

<span data-ttu-id="6b0b1-p101">Las extensiones de esquema permiten agregar datos personalizados fuertemente tipados a un recurso. La aplicación que crea una extensión de esquema es la propietaria de la aplicación. Dependiendo del [estado](../../../concepts/extensibility_overview.md#schema-extensions-lifecycle) de la extensión, solamente el propietario de la aplicación puede actualizar o eliminar la extensión.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-p101">Schema extensions let you add strongly-typed custom data to a resource. The app that creates a schema extension is the owner app. Depending on the [state](../../../concepts/extensibility_overview.md#schema-extensions-lifecycle) of the extension, the owner app, and only the owner app, may update or delete the extension.</span></span> 

<span data-ttu-id="6b0b1-106">Vea ejemplos de cómo [definir una extensión de esquema que describe un curso de aprendizaje](../../../concepts/extensibility_schema_groups.md#2-register-a-schema-extension-definition-that-describes-a-training-course), utilice la definición de la extensión de esquema para [crear un nuevo grupo con los datos del curso de aprendizaje](../../../concepts/extensibility_schema_groups.md#3-create-a-new-group-with-extended-data), y [agregue datos del curso de aprendizaje a un grupo existente](../../../concepts/extensibility_schema_groups.md#4-add-update-or-remove-custom-data-in-an-existing-group).</span><span class="sxs-lookup"><span data-stu-id="6b0b1-106">See examples of how to [define a schema extension that describes a training course](../../../concepts/extensibility_schema_groups.md#2-register-a-schema-extension-definition-that-describes-a-training-course), use the schema extension definition to [create a new group with training course data](../../../concepts/extensibility_schema_groups.md#3-create-a-new-group-with-extended-data), and [add training course data to an existing group](../../../concepts/extensibility_schema_groups.md#4-add-update-or-remove-custom-data-in-an-existing-group).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6b0b1-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6b0b1-107">Prerequisites</span></span>
<span data-ttu-id="6b0b1-108">Se requiere el siguiente **ámbito** para ejecutar esta API: *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="6b0b1-108">The following **scope** is required to execute this API: *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="6b0b1-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b0b1-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /schemaExtensions
```

## <a name="request-headers"></a><span data-ttu-id="6b0b1-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6b0b1-110">Request headers</span></span>
| <span data-ttu-id="6b0b1-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="6b0b1-111">Name</span></span>       | <span data-ttu-id="6b0b1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b0b1-112">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6b0b1-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="6b0b1-113">Authorization</span></span>  | <span data-ttu-id="6b0b1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6b0b1-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6b0b1-116">Content-Type</span></span>  | <span data-ttu-id="6b0b1-117">application/json</span><span class="sxs-lookup"><span data-stu-id="6b0b1-117">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6b0b1-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6b0b1-118">Request body</span></span>
<span data-ttu-id="6b0b1-119">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="6b0b1-119">In the request body, supply a JSON representation of [schemaExtension](../resources/schemaextension.md) object.</span></span>

<span data-ttu-id="6b0b1-120">En la tabla siguiente se muestran las propiedades necesarias para crear una extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-120">The following table shows the properties that are required when you create a schema extension.</span></span>

| <span data-ttu-id="6b0b1-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6b0b1-121">Parameter</span></span> | <span data-ttu-id="6b0b1-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="6b0b1-122">Type</span></span> | <span data-ttu-id="6b0b1-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b0b1-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6b0b1-124">description</span><span class="sxs-lookup"><span data-stu-id="6b0b1-124">description</span></span>|<span data-ttu-id="6b0b1-125">String</span><span class="sxs-lookup"><span data-stu-id="6b0b1-125">String</span></span>|<span data-ttu-id="6b0b1-126">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-126">Description for the schema extension.</span></span>|
|<span data-ttu-id="6b0b1-127">id</span><span class="sxs-lookup"><span data-stu-id="6b0b1-127">id</span></span>|<span data-ttu-id="6b0b1-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="6b0b1-128">String</span></span>|<span data-ttu-id="6b0b1-129">Identificador único para la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-129">The unique identifier for the schema extension definition.</span></span> <br><span data-ttu-id="6b0b1-130">Puede asignar un valor de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="6b0b1-130">You can assign a value in one of two ways:</span></span> <ul><li><span data-ttu-id="6b0b1-p103">Concatenar el nombre de uno de los dominios comprobados con un nombre para la extensión del esquema con el fin de formar una cadena única en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}. Por ejemplo, `contoso_mySchema`. </span><span class="sxs-lookup"><span data-stu-id="6b0b1-p103">Concatenate the name of one of your verified domains with a name for the schema extension to form a unique string in this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}. As an example, `contoso_mySchema`. </span></span></li><li><span data-ttu-id="6b0b1-p104">Proporcionar un nombre de esquema y permitir a Microsoft Graph utilizar ese nombre de esquema para completar la asignación del **id.** en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Un ejemplo sería `extkvbmkofy_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-p104">Provide a schema name, and let Microsoft Graph use that schema name to complete the **id** assignment in this format: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. An example would be `extkvbmkofy_mySchema`.</span></span></li></ul><span data-ttu-id="6b0b1-135">Una vez creada, esta propiedad no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-135">This property cannot be changed after creation.</span></span> |
|<span data-ttu-id="6b0b1-136">properties</span><span class="sxs-lookup"><span data-stu-id="6b0b1-136">properties</span></span>|<span data-ttu-id="6b0b1-137">Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="6b0b1-137">[extensionSchemaProperty](../resources/extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="6b0b1-138">La colección de tipos y nombres de propiedad que conforman la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-138">The collection of property names and types that make up the schema extension definition.</span></span>|
|<span data-ttu-id="6b0b1-139">targetTypes</span><span class="sxs-lookup"><span data-stu-id="6b0b1-139">targetTypes</span></span>|<span data-ttu-id="6b0b1-140">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="6b0b1-140">String collection</span></span>|<span data-ttu-id="6b0b1-141">Conjunto de tipos de recursos de Microsoft Graph (compatibles con extensiones de esquema) a los que se puede aplicar la definición de extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-141">Set of Microsoft Graph resource types (that support schema extensions) that this schema extension definition can be applied to.</span></span>|

## <a name="response"></a><span data-ttu-id="6b0b1-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b0b1-142">Response</span></span>

<span data-ttu-id="6b0b1-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-143">If successful, this method returns `201, Created` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6b0b1-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b0b1-144">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="6b0b1-145">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="6b0b1-145">Request 1</span></span>

<span data-ttu-id="6b0b1-p105">El primer ejemplo se muestra mediante un nombre de dominio comprobado, `graphlearn`, y un nombre de esquema, `courses`, para formar una cadena única para la propiedad **id** de la definición de la extensión de esquema. La cadena única se basa en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-p105">The first example shows using a verified domain name, `graphlearn`, and a schema name, `courses`, to form a unique string for the **id** property of the schema extension definition. The unique string is based on this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span></span>

<span data-ttu-id="6b0b1-148">En el cuerpo de la solicitud, proporcione la representación JSON del objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="6b0b1-148">In the request body, supply a JSON representation of the [schemaExtension](../resources/schemaextension.md) object.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_schemaextension_from_schemaextensions_1"
}-->
```http
POST https://graph.microsoft.com/v1.0/schemaExtensions
Content-type: application/json

{
    "id":"graphlearn_courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "properties": [
        {
            "name": "courseId",
            "type": "Integer"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```

##### <a name="response-1"></a><span data-ttu-id="6b0b1-149">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="6b0b1-149">Response 1</span></span>

<span data-ttu-id="6b0b1-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 420

{
    "id": "graphlearn_courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "status": "InDevelopment",
    "owner": "24d3b144-21ae-4080-943f-7067b395b913",
    "properties": [
        {
            "name": "courseId",
            "type": "String"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```

##### <a name="request-2"></a><span data-ttu-id="6b0b1-153">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="6b0b1-153">Request 2</span></span>

<span data-ttu-id="6b0b1-p107">El segundo ejemplo muestra la especificación de un nombre de esquema, `courses`, en la propiedad **id** de la solicitud, junto con la representación JSON del resto de las propiedades del objeto [schemaExtension](../resources/schemaextension.md). Microsoft Graph asignará y devolverá un valor de cadena único en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-p107">The second example shows specifying just a schema name, `courses`, in the **id** property in the request, together with the JSON representation of the rest of the properties in the [schemaExtension](../resources/schemaextension.md) object. Microsoft Graph will assign and return a unique string value in the response.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_schemaextension_from_schemaextensions_2"
}-->
```http
POST https://graph.microsoft.com/v1.0/schemaExtensions
Content-type: application/json

{
    "id":"courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "properties": [
        {
            "name": "courseId",
            "type": "Integer"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```

##### <a name="response-2"></a><span data-ttu-id="6b0b1-156">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="6b0b1-156">Response 2</span></span>

<span data-ttu-id="6b0b1-p108">La respuesta incluye una cadena única en la propiedad **id** que se basa en el nombre del esquema proporcionado en la solicitud, junto con el resto de la definición de esquema recién creada. El valor de **id** en la respuesta se basa en el formato, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b0b1-p108">The response includes a unique string in the **id** property that is based on the schema name provided in the request, together with the rest of the newly created schema definition. The value in **id** in the response is based on the format, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 420

{
    "id": "extk9eruy7c_courses",
    "description": "Graph Learn training courses extensions",
    "targetTypes": [
        "Group"
    ],
    "status": "InDevelopment",
    "owner": "24d3b144-21ae-4080-943f-7067b395b913",
    "properties": [
        {
            "name": "courseId",
            "type": "String"
        },
        {
            "name": "courseName",
            "type": "String"
        },
        {
            "name": "courseType",
            "type": "String"
        }
    ]
}
```


## <a name="see-also"></a><span data-ttu-id="6b0b1-161">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6b0b1-161">See also</span></span>

- [<span data-ttu-id="6b0b1-162">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="6b0b1-162">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="6b0b1-163">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="6b0b1-163">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->