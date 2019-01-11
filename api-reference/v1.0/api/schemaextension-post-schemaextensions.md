---
title: Crear schemaExtensions
description: Crear una nueva definición de schemaExtension para extender a un tipo de recurso compatible.
localization_priority: Priority
ms.openlocfilehash: 100602336f32ce7d13318650a7e473b7635f768c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857431"
---
# <a name="create-schemaextension"></a><span data-ttu-id="05cc5-103">Crear schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="05cc5-103">Create schemaExtension</span></span>

<span data-ttu-id="05cc5-104">Crear una nueva definición de [schemaExtension](../resources/schemaextension.md) para extender a un [tipo de recurso compatible](/graph/extensibility-overview#supported-resources).</span><span class="sxs-lookup"><span data-stu-id="05cc5-104">Create a new [schemaExtension](../resources/schemaextension.md) definition to extend a [supporting resource type](/graph/extensibility-overview#supported-resources).</span></span>

<span data-ttu-id="05cc5-p101">Las extensiones de esquema permiten agregar datos personalizados fuertemente tipados a un recurso. La aplicación que crea una extensión de esquema es la propietaria de la aplicación. Dependiendo del [estado](/graph/extensibility-overview#schema-extensions-lifecycle) de la extensión, solamente el propietario de la aplicación puede actualizar o eliminar la extensión.</span><span class="sxs-lookup"><span data-stu-id="05cc5-p101">Schema extensions let you add strongly-typed custom data to a resource. The app that creates a schema extension is the owner app. Depending on the [state](/graph/extensibility-overview#schema-extensions-lifecycle) of the extension, the owner app, and only the owner app, may update or delete the extension.</span></span> 

<span data-ttu-id="05cc5-108">Vea ejemplos de cómo [definir una extensión de esquema que describe un curso de aprendizaje](/graph/extensibility-schema-groups#2-register-a-schema-extension-definition-that-describes-a-training-course), utilice la definición de la extensión de esquema para [crear un nuevo grupo con los datos del curso de aprendizaje](/graph/extensibility-schema-groups#3-create-a-new-group-with-extended-data), y [agregue datos del curso de aprendizaje a un grupo existente](/graph/extensibility-schema-groups#4-add-update-or-remove-custom-data-in-an-existing-group).</span><span class="sxs-lookup"><span data-stu-id="05cc5-108">See examples of how to [define a schema extension that describes a training course](/graph/extensibility-schema-groups#2-register-a-schema-extension-definition-that-describes-a-training-course), use the schema extension definition to [create a new group with training course data](/graph/extensibility-schema-groups#3-create-a-new-group-with-extended-data), and [add training course data to an existing group](/graph/extensibility-schema-groups#4-add-update-or-remove-custom-data-in-an-existing-group).</span></span>

## <a name="permissions"></a><span data-ttu-id="05cc5-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="05cc5-109">Permissions</span></span>
<span data-ttu-id="05cc5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="05cc5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="05cc5-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05cc5-112">Permission type</span></span>      | <span data-ttu-id="05cc5-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05cc5-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="05cc5-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05cc5-114">Delegated (work or school account)</span></span> | <span data-ttu-id="05cc5-115">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="05cc5-115">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="05cc5-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05cc5-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05cc5-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05cc5-117">Not supported.</span></span>    |
|<span data-ttu-id="05cc5-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05cc5-118">Application</span></span> | <span data-ttu-id="05cc5-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05cc5-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="05cc5-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05cc5-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /schemaExtensions
```

## <a name="request-headers"></a><span data-ttu-id="05cc5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="05cc5-121">Request headers</span></span>
| <span data-ttu-id="05cc5-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="05cc5-122">Name</span></span>       | <span data-ttu-id="05cc5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="05cc5-123">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="05cc5-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="05cc5-124">Authorization</span></span>  | <span data-ttu-id="05cc5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05cc5-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="05cc5-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="05cc5-127">Content-Type</span></span>  | <span data-ttu-id="05cc5-128">application/json</span><span class="sxs-lookup"><span data-stu-id="05cc5-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="05cc5-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="05cc5-129">Request body</span></span>
<span data-ttu-id="05cc5-130">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="05cc5-130">In the request body, supply a JSON representation of [schemaExtension](../resources/schemaextension.md) object.</span></span>

<span data-ttu-id="05cc5-131">En la tabla siguiente se muestran las propiedades necesarias para crear una extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="05cc5-131">The following table shows the properties that are required when you create a schema extension.</span></span>

| <span data-ttu-id="05cc5-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="05cc5-132">Parameter</span></span> | <span data-ttu-id="05cc5-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="05cc5-133">Type</span></span> | <span data-ttu-id="05cc5-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="05cc5-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="05cc5-135">description</span><span class="sxs-lookup"><span data-stu-id="05cc5-135">description</span></span>|<span data-ttu-id="05cc5-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="05cc5-136">String</span></span>|<span data-ttu-id="05cc5-137">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="05cc5-137">Description for the schema extension.</span></span>|
|<span data-ttu-id="05cc5-138">id</span><span class="sxs-lookup"><span data-stu-id="05cc5-138">id</span></span>|<span data-ttu-id="05cc5-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="05cc5-139">String</span></span>|<span data-ttu-id="05cc5-140">Identificador único para la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="05cc5-140">The unique identifier for the schema extension definition.</span></span> <br><span data-ttu-id="05cc5-141">Puede asignar un valor de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="05cc5-141">You can assign a value in one of two ways:</span></span> <ul><li><span data-ttu-id="05cc5-142">Concatenar el nombre de uno de los dominios comprobados con un nombre para la extensión del esquema con el fin de formar una cadena única en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span><span class="sxs-lookup"><span data-stu-id="05cc5-142">Concatenate the name of one of your verified domains with a name for the schema extension to form a unique string in this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span></span> <span data-ttu-id="05cc5-143">Por ejemplo: `contoso_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="05cc5-143">As an example, `contoso_mySchema`.</span></span> <span data-ttu-id="05cc5-144">NOTA: Solo se admiten los dominios comprobados bajo los siguientes dominios de primer nivel: `.com`, `.net`, `.gov`, `.edu` o `.org`.</span><span class="sxs-lookup"><span data-stu-id="05cc5-144">NOTE: Only verified domains under the following top-level domains are supported: `.com`,`.net`, `.gov`, `.edu` or `.org`.</span></span> </li><li><span data-ttu-id="05cc5-p105">Proporcionar un nombre de esquema y permitir a Microsoft Graph utilizar ese nombre de esquema para completar la asignación del **id.** en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Un ejemplo sería `extkvbmkofy_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="05cc5-p105">Provide a schema name, and let Microsoft Graph use that schema name to complete the **id** assignment in this format: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. An example would be `extkvbmkofy_mySchema`.</span></span></li></ul><span data-ttu-id="05cc5-147">Una vez creada, esta propiedad no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="05cc5-147">This property cannot be changed after creation.</span></span> |
|<span data-ttu-id="05cc5-148">owner</span><span class="sxs-lookup"><span data-stu-id="05cc5-148">owner</span></span>|<span data-ttu-id="05cc5-149">String</span><span class="sxs-lookup"><span data-stu-id="05cc5-149">String</span></span>|<span data-ttu-id="05cc5-150">(Opcional) El `appId` de la aplicación que es el propietario de la extensión del esquema.</span><span class="sxs-lookup"><span data-stu-id="05cc5-150">(Optional) The `appId` of the application that is the owner of the schema extension.</span></span> <span data-ttu-id="05cc5-151">Esta propiedad se puede proporcionar en la creación, para establecer el propietario.</span><span class="sxs-lookup"><span data-stu-id="05cc5-151">This property can be supplied on creation, to set the owner.</span></span>  <span data-ttu-id="05cc5-152">Si no se proporciona, entonces la aplicación de llamada `appId` se establecerá como la propietaria.</span><span class="sxs-lookup"><span data-stu-id="05cc5-152">If not supplied, then the calling application's `appId` will be set as the owner.</span></span> <span data-ttu-id="05cc5-153">Así, por ejemplo, si crea una nueva definición de extensión de esquema mediante el Probador de gráfico, **debe** proporcionar la propiedad owner.</span><span class="sxs-lookup"><span data-stu-id="05cc5-153">So, for example, if creating a new schema extension definition using Graph Explorer, you **must** supply the owner property.</span></span> <span data-ttu-id="05cc5-154">Una vez establecida, esta propiedad es de solo lectura y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="05cc5-154">Once set, this property is read-only and cannot be changed.</span></span>|
|<span data-ttu-id="05cc5-155">properties</span><span class="sxs-lookup"><span data-stu-id="05cc5-155">properties</span></span>|<span data-ttu-id="05cc5-156">Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="05cc5-156">[extensionSchemaProperty](../resources/extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="05cc5-157">La colección de tipos y nombres de propiedad que conforman la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="05cc5-157">The collection of property names and types that make up the schema extension definition.</span></span>|
|<span data-ttu-id="05cc5-158">targetTypes</span><span class="sxs-lookup"><span data-stu-id="05cc5-158">targetTypes</span></span>|<span data-ttu-id="05cc5-159">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="05cc5-159">String collection</span></span>|<span data-ttu-id="05cc5-160">Conjunto de tipos de recursos de Microsoft Graph (compatibles con extensiones de esquema) a los que se puede aplicar la definición de extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="05cc5-160">Set of Microsoft Graph resource types (that support schema extensions) that this schema extension definition can be applied to.</span></span>|

## <a name="response"></a><span data-ttu-id="05cc5-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05cc5-161">Response</span></span>

<span data-ttu-id="05cc5-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05cc5-162">If successful, this method returns `201 Created` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="05cc5-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05cc5-163">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="05cc5-164">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="05cc5-164">Request 1</span></span>

<span data-ttu-id="05cc5-p107">El primer ejemplo se muestra mediante un nombre de dominio comprobado, `graphlearn`, y un nombre de esquema, `courses`, para formar una cadena única para la propiedad **id** de la definición de la extensión de esquema. La cadena única se basa en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span><span class="sxs-lookup"><span data-stu-id="05cc5-p107">The first example shows using a verified domain name, `graphlearn`, and a schema name, `courses`, to form a unique string for the **id** property of the schema extension definition. The unique string is based on this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span></span>

<span data-ttu-id="05cc5-167">En el cuerpo de la solicitud, proporcione la representación JSON del objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="05cc5-167">In the request body, supply a JSON representation of the [schemaExtension](../resources/schemaextension.md) object.</span></span>
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

##### <a name="response-1"></a><span data-ttu-id="05cc5-168">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="05cc5-168">Response 1</span></span>

<span data-ttu-id="05cc5-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05cc5-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request-2"></a><span data-ttu-id="05cc5-172">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="05cc5-172">Request 2</span></span>

<span data-ttu-id="05cc5-p109">El segundo ejemplo muestra la especificación de un nombre de esquema, `courses`, en la propiedad **id** de la solicitud, junto con la representación JSON del resto de las propiedades del objeto [schemaExtension](../resources/schemaextension.md). Microsoft Graph asignará y devolverá un valor de cadena único en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05cc5-p109">The second example shows specifying just a schema name, `courses`, in the **id** property in the request, together with the JSON representation of the rest of the properties in the [schemaExtension](../resources/schemaextension.md) object. Microsoft Graph will assign and return a unique string value in the response.</span></span>

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

##### <a name="response-2"></a><span data-ttu-id="05cc5-175">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="05cc5-175">Response 2</span></span>

<span data-ttu-id="05cc5-p110">La respuesta incluye una cadena única en la propiedad **id** que se basa en el nombre del esquema proporcionado en la solicitud, junto con el resto de la definición de esquema recién creada. El valor de **id** en la respuesta se basa en el formato, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="05cc5-p110">The response includes a unique string in the **id** property that is based on the schema name provided in the request, together with the rest of the newly created schema definition. The value in **id** in the response is based on the format, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


## <a name="see-also"></a><span data-ttu-id="05cc5-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="05cc5-180">See also</span></span>

- [<span data-ttu-id="05cc5-181">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="05cc5-181">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="05cc5-182">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="05cc5-182">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
