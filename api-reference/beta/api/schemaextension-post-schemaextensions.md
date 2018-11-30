---
title: Crear schemaExtensions
description: Crear una nueva definición de schemaExtension para extender a un tipo de recurso compatible.
ms.openlocfilehash: 3ad3e3cb52b6abacf16643a7419b6297217d074c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085686"
---
# <a name="create-schemaextension"></a><span data-ttu-id="4bd5a-103">Crear schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="4bd5a-103">Create schemaExtension</span></span>

> <span data-ttu-id="4bd5a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4bd5a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4bd5a-106">Crear una nueva definición de [schemaExtension](../resources/schemaextension.md) para extender a un [tipo de recurso compatible](/graph/extensibility-overview#supported-resources).</span><span class="sxs-lookup"><span data-stu-id="4bd5a-106">Create a new [schemaExtension](../resources/schemaextension.md) definition to extend a [supporting resource type](/graph/extensibility-overview#supported-resources).</span></span>

<span data-ttu-id="4bd5a-p102">Las extensiones de esquema permiten agregar datos personalizados fuertemente tipados a un recurso. La aplicación que crea una extensión de esquema es la propietaria de la aplicación. Dependiendo del [estado](/graph/extensibility-overview#schema-extensions-lifecycle) de la extensión, solamente el propietario de la aplicación puede actualizar o eliminar la extensión.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p102">Schema extensions let you add strongly-typed custom data to a resource. The app that creates a schema extension is the owner app. Depending on the [state](/graph/extensibility-overview#schema-extensions-lifecycle) of the extension, the owner app, and only the owner app, may update or delete the extension.</span></span> 

<span data-ttu-id="4bd5a-110">Vea ejemplos de cómo [definir una extensión de esquema que describe un curso de aprendizaje](/graph/extensibility-schema-groups#2-register-a-schema-extension-definition-that-describes-a-training-course), utilice la definición de la extensión de esquema para [crear un nuevo grupo con los datos del curso de aprendizaje](/graph/extensibility-schema-groups#3-create-a-new-group-with-extended-data), y [agregue datos del curso de aprendizaje a un grupo existente](/graph/extensibility-schema-groups#4-add-update-or-remove-custom-data-in-an-existing-group).</span><span class="sxs-lookup"><span data-stu-id="4bd5a-110">See examples of how to [define a schema extension that describes a training course](/graph/extensibility-schema-groups#2-register-a-schema-extension-definition-that-describes-a-training-course), use the schema extension definition to [create a new group with training course data](/graph/extensibility-schema-groups#3-create-a-new-group-with-extended-data), and [add training course data to an existing group](/graph/extensibility-schema-groups#4-add-update-or-remove-custom-data-in-an-existing-group).</span></span>

## <a name="permissions"></a><span data-ttu-id="4bd5a-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="4bd5a-111">Permissions</span></span>
<span data-ttu-id="4bd5a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="4bd5a-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4bd5a-114">Permission type</span></span>      | <span data-ttu-id="4bd5a-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4bd5a-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4bd5a-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4bd5a-116">Delegated (work or school account)</span></span> | <span data-ttu-id="4bd5a-117">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4bd5a-117">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="4bd5a-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4bd5a-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4bd5a-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-119">Not supported.</span></span>    |
|<span data-ttu-id="4bd5a-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4bd5a-120">Application</span></span> | <span data-ttu-id="4bd5a-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="4bd5a-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4bd5a-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /schemaExtensions
```

## <a name="request-headers"></a><span data-ttu-id="4bd5a-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4bd5a-123">Request headers</span></span>
| <span data-ttu-id="4bd5a-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="4bd5a-124">Name</span></span>       | <span data-ttu-id="4bd5a-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bd5a-125">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="4bd5a-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="4bd5a-126">Authorization</span></span>  | <span data-ttu-id="4bd5a-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="4bd5a-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="4bd5a-129">Content-Type</span></span>  | <span data-ttu-id="4bd5a-130">application/json</span><span class="sxs-lookup"><span data-stu-id="4bd5a-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4bd5a-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4bd5a-131">Request body</span></span>
<span data-ttu-id="4bd5a-132">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="4bd5a-132">In the request body, supply a JSON representation of [schemaExtension](../resources/schemaextension.md) object.</span></span>

<span data-ttu-id="4bd5a-133">En la siguiente tabla se muestra las propiedades que están disponibles cuando se crea una extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-133">The following table shows the properties that are available when you create a schema extension.</span></span>

| <span data-ttu-id="4bd5a-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4bd5a-134">Parameter</span></span> | <span data-ttu-id="4bd5a-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bd5a-135">Type</span></span> | <span data-ttu-id="4bd5a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bd5a-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4bd5a-137">description</span><span class="sxs-lookup"><span data-stu-id="4bd5a-137">description</span></span>|<span data-ttu-id="4bd5a-138">String</span><span class="sxs-lookup"><span data-stu-id="4bd5a-138">String</span></span>|<span data-ttu-id="4bd5a-139">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-139">Description for the schema extension.</span></span>|
|<span data-ttu-id="4bd5a-140">id</span><span class="sxs-lookup"><span data-stu-id="4bd5a-140">id</span></span>|<span data-ttu-id="4bd5a-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bd5a-141">String</span></span>|<span data-ttu-id="4bd5a-142">Identificador único para la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-142">The unique identifier for the schema extension definition.</span></span> <br><span data-ttu-id="4bd5a-143">Puede asignar un valor de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="4bd5a-143">You can assign a value in one of two ways:</span></span> <ul><li><span data-ttu-id="4bd5a-144">Concatenar el nombre de uno de los dominios comprobados con un nombre para la extensión del esquema con el fin de formar una cadena única en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-144">Concatenate the name of one of your verified domains with a name for the schema extension to form a unique string in this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span></span> <span data-ttu-id="4bd5a-145">Por ejemplo: `contoso_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-145">As an example, `contoso_mySchema`.</span></span> <span data-ttu-id="4bd5a-146">NOTA: Solo se admiten los dominios comprobados bajo los siguientes dominios de primer nivel: `.com`, `.net`, `.gov`, `.edu` o `.org`.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-146">NOTE: Only verified domains under the following top-level domains are supported: `.com`,`.net`, `.gov`, `.edu` or `.org`.</span></span> </li><li><span data-ttu-id="4bd5a-p106">Proporcionar un nombre de esquema y permitir a Microsoft Graph utilizar ese nombre de esquema para completar la asignación del **id.** en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Un ejemplo sería `extkvbmkofy_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p106">Provide a schema name, and let Microsoft Graph use that schema name to complete the **id** assignment in this format: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. An example would be `extkvbmkofy_mySchema`.</span></span></li></ul><span data-ttu-id="4bd5a-149">Una vez creada, esta propiedad no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-149">This property cannot be changed after creation.</span></span> |
|<span data-ttu-id="4bd5a-150">owner</span><span class="sxs-lookup"><span data-stu-id="4bd5a-150">owner</span></span>|<span data-ttu-id="4bd5a-151">String</span><span class="sxs-lookup"><span data-stu-id="4bd5a-151">String</span></span>|<span data-ttu-id="4bd5a-152">(Opcional) El `appId` de la aplicación que es el propietario de la extensión del esquema.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-152">(Optional) The `appId` of the application that is the owner of the schema extension.</span></span> <span data-ttu-id="4bd5a-153">Esta propiedad se puede proporcionar en la creación, para establecer el propietario.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-153">This property can be supplied on creation, to set the owner.</span></span>  <span data-ttu-id="4bd5a-154">Si no se proporciona, entonces la aplicación de llamada `appId` se establecerá como la propietaria.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-154">If not supplied, then the calling application's `appId` will be set as the owner.</span></span> <span data-ttu-id="4bd5a-155">Así, por ejemplo, si crea una nueva definición de extensión de esquema mediante el Probador de gráfico, **debe** proporcionar la propiedad owner.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-155">So, for example, if creating a new schema extension definition using Graph Explorer, you **must** supply the owner property.</span></span> <span data-ttu-id="4bd5a-156">Una vez establecida, esta propiedad es de solo lectura y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-156">Once set, this property is read-only and cannot be changed.</span></span>|
|<span data-ttu-id="4bd5a-157">properties</span><span class="sxs-lookup"><span data-stu-id="4bd5a-157">properties</span></span>|<span data-ttu-id="4bd5a-158">Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="4bd5a-158">[extensionSchemaProperty](../resources/extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="4bd5a-159">La colección de tipos y nombres de propiedad que conforman la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-159">The collection of property names and types that make up the schema extension definition.</span></span>|
|<span data-ttu-id="4bd5a-160">targetTypes</span><span class="sxs-lookup"><span data-stu-id="4bd5a-160">targetTypes</span></span>|<span data-ttu-id="4bd5a-161">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="4bd5a-161">String collection</span></span>|<span data-ttu-id="4bd5a-162">Conjunto de tipos de recursos de Microsoft Graph (compatibles con extensiones de esquema) a los que se puede aplicar la definición de extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-162">Set of Microsoft Graph resource types (that support schema extensions) that this schema extension definition can be applied to.</span></span>|

## <a name="response"></a><span data-ttu-id="4bd5a-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bd5a-163">Response</span></span>

<span data-ttu-id="4bd5a-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-164">If successful, this method returns `201 Created` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4bd5a-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bd5a-165">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="4bd5a-166">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="4bd5a-166">Request 1</span></span>

<span data-ttu-id="4bd5a-p108">El primer ejemplo se muestra mediante un nombre de dominio comprobado, `graphlearn`, y un nombre de esquema, `courses`, para formar una cadena única para la propiedad **id** de la definición de la extensión de esquema. La cadena única se basa en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p108">The first example shows using a verified domain name, `graphlearn`, and a schema name, `courses`, to form a unique string for the **id** property of the schema extension definition. The unique string is based on this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span></span>

<span data-ttu-id="4bd5a-169">En el cuerpo de la solicitud, proporcione la representación JSON del objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="4bd5a-169">In the request body, supply a JSON representation of the [schemaExtension](../resources/schemaextension.md) object.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_schemaextension_from_schemaextensions_1"
}-->
```http
POST https://graph.microsoft.com/beta/schemaExtensions
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

##### <a name="response-1"></a><span data-ttu-id="4bd5a-170">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="4bd5a-170">Response 1</span></span>

<span data-ttu-id="4bd5a-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request-2"></a><span data-ttu-id="4bd5a-174">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="4bd5a-174">Request 2</span></span>

<span data-ttu-id="4bd5a-p110">El segundo ejemplo muestra la especificación de un nombre de esquema, `courses`, en la propiedad **id** de la solicitud, junto con la representación JSON del resto de las propiedades del objeto [schemaExtension](../resources/schemaextension.md). Microsoft Graph asignará y devolverá un valor de cadena único en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p110">The second example shows specifying just a schema name, `courses`, in the **id** property in the request, together with the JSON representation of the rest of the properties in the [schemaExtension](../resources/schemaextension.md) object. Microsoft Graph will assign and return a unique string value in the response.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_schemaextension_from_schemaextensions_2"
}-->
```http
POST https://graph.microsoft.com/beta/schemaExtensions
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

##### <a name="response-2"></a><span data-ttu-id="4bd5a-177">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="4bd5a-177">Response 2</span></span>

<span data-ttu-id="4bd5a-p111">La respuesta incluye una cadena única en la propiedad **id** que se basa en el nombre del esquema proporcionado en la solicitud, junto con el resto de la definición de esquema recién creada. El valor de **id** en la respuesta se basa en el formato, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bd5a-p111">The response includes a unique string in the **id** property that is based on the schema name provided in the request, together with the rest of the newly created schema definition. The value in **id** in the response is based on the format, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


## <a name="see-also"></a><span data-ttu-id="4bd5a-182">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4bd5a-182">See also</span></span>

- [<span data-ttu-id="4bd5a-183">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="4bd5a-183">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="4bd5a-184">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="4bd5a-184">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
