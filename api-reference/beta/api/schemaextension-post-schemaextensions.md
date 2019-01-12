---
title: Crear schemaExtensions
description: Crear una nueva definición de schemaExtension para extender a un tipo de recurso compatible.
localization_priority: Normal
author: dkershaw10
ms.openlocfilehash: c12a47880147d973583fe4104fcb3535674f512a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975781"
---
# <a name="create-schemaextension"></a><span data-ttu-id="dc63c-103">Crear schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="dc63c-103">Create schemaExtension</span></span>

> <span data-ttu-id="dc63c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dc63c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dc63c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dc63c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dc63c-106">Crear una nueva definición de [schemaExtension](../resources/schemaextension.md) para extender a un [tipo de recurso compatible](/graph/extensibility-overview#supported-resources).</span><span class="sxs-lookup"><span data-stu-id="dc63c-106">Create a new [schemaExtension](../resources/schemaextension.md) definition to extend a [supporting resource type](/graph/extensibility-overview#supported-resources).</span></span>

<span data-ttu-id="dc63c-p102">Las extensiones de esquema permiten agregar datos personalizados fuertemente tipados a un recurso. La aplicación que crea una extensión de esquema es la propietaria de la aplicación. Dependiendo del [estado](/graph/extensibility-overview#schema-extensions-lifecycle) de la extensión, solamente el propietario de la aplicación puede actualizar o eliminar la extensión.</span><span class="sxs-lookup"><span data-stu-id="dc63c-p102">Schema extensions let you add strongly-typed custom data to a resource. The app that creates a schema extension is the owner app. Depending on the [state](/graph/extensibility-overview#schema-extensions-lifecycle) of the extension, the owner app, and only the owner app, may update or delete the extension.</span></span> 

<span data-ttu-id="dc63c-110">Vea ejemplos de cómo [definir una extensión de esquema que describe un curso de aprendizaje](/graph/extensibility-schema-groups#2-register-a-schema-extension-definition-that-describes-a-training-course), utilice la definición de la extensión de esquema para [crear un nuevo grupo con los datos del curso de aprendizaje](/graph/extensibility-schema-groups#3-create-a-new-group-with-extended-data), y [agregue datos del curso de aprendizaje a un grupo existente](/graph/extensibility-schema-groups#4-add-update-or-remove-custom-data-in-an-existing-group).</span><span class="sxs-lookup"><span data-stu-id="dc63c-110">See examples of how to [define a schema extension that describes a training course](/graph/extensibility-schema-groups#2-register-a-schema-extension-definition-that-describes-a-training-course), use the schema extension definition to [create a new group with training course data](/graph/extensibility-schema-groups#3-create-a-new-group-with-extended-data), and [add training course data to an existing group](/graph/extensibility-schema-groups#4-add-update-or-remove-custom-data-in-an-existing-group).</span></span>

## <a name="permissions"></a><span data-ttu-id="dc63c-111">Permisos</span><span class="sxs-lookup"><span data-stu-id="dc63c-111">Permissions</span></span>
<span data-ttu-id="dc63c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc63c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="dc63c-114">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc63c-114">Permission type</span></span>      | <span data-ttu-id="dc63c-115">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc63c-115">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc63c-116">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc63c-116">Delegated (work or school account)</span></span> | <span data-ttu-id="dc63c-117">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="dc63c-117">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="dc63c-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc63c-118">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc63c-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc63c-119">Not supported.</span></span>    |
|<span data-ttu-id="dc63c-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc63c-120">Application</span></span> | <span data-ttu-id="dc63c-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc63c-121">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc63c-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc63c-122">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /schemaExtensions
```

## <a name="request-headers"></a><span data-ttu-id="dc63c-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc63c-123">Request headers</span></span>
| <span data-ttu-id="dc63c-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc63c-124">Name</span></span>       | <span data-ttu-id="dc63c-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc63c-125">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="dc63c-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc63c-126">Authorization</span></span>  | <span data-ttu-id="dc63c-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc63c-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="dc63c-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="dc63c-129">Content-Type</span></span>  | <span data-ttu-id="dc63c-130">application/json</span><span class="sxs-lookup"><span data-stu-id="dc63c-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="dc63c-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc63c-131">Request body</span></span>
<span data-ttu-id="dc63c-132">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="dc63c-132">In the request body, supply a JSON representation of [schemaExtension](../resources/schemaextension.md) object.</span></span>

<span data-ttu-id="dc63c-133">En la siguiente tabla se muestra las propiedades que están disponibles cuando se crea una extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="dc63c-133">The following table shows the properties that are available when you create a schema extension.</span></span>

| <span data-ttu-id="dc63c-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dc63c-134">Parameter</span></span> | <span data-ttu-id="dc63c-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc63c-135">Type</span></span> | <span data-ttu-id="dc63c-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc63c-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dc63c-137">description</span><span class="sxs-lookup"><span data-stu-id="dc63c-137">description</span></span>|<span data-ttu-id="dc63c-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="dc63c-138">String</span></span>|<span data-ttu-id="dc63c-139">Descripción de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="dc63c-139">Description for the schema extension.</span></span>|
|<span data-ttu-id="dc63c-140">id</span><span class="sxs-lookup"><span data-stu-id="dc63c-140">id</span></span>|<span data-ttu-id="dc63c-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="dc63c-141">String</span></span>|<span data-ttu-id="dc63c-142">Identificador único para la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="dc63c-142">The unique identifier for the schema extension definition.</span></span> <br><span data-ttu-id="dc63c-143">Puede asignar un valor de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="dc63c-143">You can assign a value in one of two ways:</span></span> <ul><li><span data-ttu-id="dc63c-144">Concatenar el nombre de uno de los dominios comprobados con un nombre para la extensión del esquema con el fin de formar una cadena única en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span><span class="sxs-lookup"><span data-stu-id="dc63c-144">Concatenate the name of one of your verified domains with a name for the schema extension to form a unique string in this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span></span> <span data-ttu-id="dc63c-145">Por ejemplo: `contoso_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="dc63c-145">As an example, `contoso_mySchema`.</span></span> <span data-ttu-id="dc63c-146">NOTA: Solo se admiten los dominios comprobados bajo los siguientes dominios de primer nivel: `.com`, `.net`, `.gov`, `.edu` o `.org`.</span><span class="sxs-lookup"><span data-stu-id="dc63c-146">NOTE: Only verified domains under the following top-level domains are supported: `.com`,`.net`, `.gov`, `.edu` or `.org`.</span></span> </li><li><span data-ttu-id="dc63c-p106">Proporcionar un nombre de esquema y permitir a Microsoft Graph utilizar ese nombre de esquema para completar la asignación del **id.** en este formato: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Un ejemplo sería `extkvbmkofy_mySchema`.</span><span class="sxs-lookup"><span data-stu-id="dc63c-p106">Provide a schema name, and let Microsoft Graph use that schema name to complete the **id** assignment in this format: ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. An example would be `extkvbmkofy_mySchema`.</span></span></li></ul><span data-ttu-id="dc63c-149">Una vez creada, esta propiedad no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="dc63c-149">This property cannot be changed after creation.</span></span> |
|<span data-ttu-id="dc63c-150">owner</span><span class="sxs-lookup"><span data-stu-id="dc63c-150">owner</span></span>|<span data-ttu-id="dc63c-151">String</span><span class="sxs-lookup"><span data-stu-id="dc63c-151">String</span></span>|<span data-ttu-id="dc63c-152">(Opcional) El `appId` de la aplicación que es el propietario de la extensión del esquema.</span><span class="sxs-lookup"><span data-stu-id="dc63c-152">(Optional) The `appId` of the application that is the owner of the schema extension.</span></span> <span data-ttu-id="dc63c-153">Esta propiedad se puede proporcionar en la creación, para establecer el propietario.</span><span class="sxs-lookup"><span data-stu-id="dc63c-153">This property can be supplied on creation, to set the owner.</span></span>  <span data-ttu-id="dc63c-154">Si no se proporciona, entonces la aplicación de llamada `appId` se establecerá como la propietaria.</span><span class="sxs-lookup"><span data-stu-id="dc63c-154">If not supplied, then the calling application's `appId` will be set as the owner.</span></span> <span data-ttu-id="dc63c-155">Así, por ejemplo, si crea una nueva definición de extensión de esquema mediante el Probador de gráfico, **debe** proporcionar la propiedad owner.</span><span class="sxs-lookup"><span data-stu-id="dc63c-155">So, for example, if creating a new schema extension definition using Graph Explorer, you **must** supply the owner property.</span></span> <span data-ttu-id="dc63c-156">Una vez establecida, esta propiedad es de solo lectura y no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="dc63c-156">Once set, this property is read-only and cannot be changed.</span></span>|
|<span data-ttu-id="dc63c-157">properties</span><span class="sxs-lookup"><span data-stu-id="dc63c-157">properties</span></span>|<span data-ttu-id="dc63c-158">Colección [extensionSchemaProperty](../resources/extensionschemaproperty.md)</span><span class="sxs-lookup"><span data-stu-id="dc63c-158">[extensionSchemaProperty](../resources/extensionschemaproperty.md) collection</span></span>|<span data-ttu-id="dc63c-159">La colección de tipos y nombres de propiedad que conforman la definición de la extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="dc63c-159">The collection of property names and types that make up the schema extension definition.</span></span>|
|<span data-ttu-id="dc63c-160">targetTypes</span><span class="sxs-lookup"><span data-stu-id="dc63c-160">targetTypes</span></span>|<span data-ttu-id="dc63c-161">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="dc63c-161">String collection</span></span>|<span data-ttu-id="dc63c-162">Conjunto de tipos de recursos de Microsoft Graph (compatibles con extensiones de esquema) a los que se puede aplicar la definición de extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="dc63c-162">Set of Microsoft Graph resource types (that support schema extensions) that this schema extension definition can be applied to.</span></span>|

## <a name="response"></a><span data-ttu-id="dc63c-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc63c-163">Response</span></span>

<span data-ttu-id="dc63c-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc63c-164">If successful, this method returns `201 Created` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dc63c-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc63c-165">Example</span></span>

##### <a name="request-1"></a><span data-ttu-id="dc63c-166">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="dc63c-166">Request 1</span></span>

<span data-ttu-id="dc63c-p108">El primer ejemplo se muestra mediante un nombre de dominio comprobado, `graphlearn`, y un nombre de esquema, `courses`, para formar una cadena única para la propiedad **id** de la definición de la extensión de esquema. La cadena única se basa en este formato, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span><span class="sxs-lookup"><span data-stu-id="dc63c-p108">The first example shows using a verified domain name, `graphlearn`, and a schema name, `courses`, to form a unique string for the **id** property of the schema extension definition. The unique string is based on this format, \{_&#65279;domainName_\}\_\{_&#65279;schemaName_\}.</span></span>

<span data-ttu-id="dc63c-169">En el cuerpo de la solicitud, proporcione la representación JSON del objeto [schemaExtension](../resources/schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="dc63c-169">In the request body, supply a JSON representation of the [schemaExtension](../resources/schemaextension.md) object.</span></span>
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

##### <a name="response-1"></a><span data-ttu-id="dc63c-170">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="dc63c-170">Response 1</span></span>

<span data-ttu-id="dc63c-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc63c-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

##### <a name="request-2"></a><span data-ttu-id="dc63c-174">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="dc63c-174">Request 2</span></span>

<span data-ttu-id="dc63c-p110">El segundo ejemplo muestra la especificación de un nombre de esquema, `courses`, en la propiedad **id** de la solicitud, junto con la representación JSON del resto de las propiedades del objeto [schemaExtension](../resources/schemaextension.md). Microsoft Graph asignará y devolverá un valor de cadena único en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc63c-p110">The second example shows specifying just a schema name, `courses`, in the **id** property in the request, together with the JSON representation of the rest of the properties in the [schemaExtension](../resources/schemaextension.md) object. Microsoft Graph will assign and return a unique string value in the response.</span></span>

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

##### <a name="response-2"></a><span data-ttu-id="dc63c-177">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="dc63c-177">Response 2</span></span>

<span data-ttu-id="dc63c-p111">La respuesta incluye una cadena única en la propiedad **id** que se basa en el nombre del esquema proporcionado en la solicitud, junto con el resto de la definición de esquema recién creada. El valor de **id** en la respuesta se basa en el formato, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán en una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dc63c-p111">The response includes a unique string in the **id** property that is based on the schema name provided in the request, together with the rest of the newly created schema definition. The value in **id** in the response is based on the format, ext\{_&#65279;8-random-alphanumeric-chars_\}\_\{_&#65279;schema-name_\}. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


## <a name="see-also"></a><span data-ttu-id="dc63c-182">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc63c-182">See also</span></span>

- [<span data-ttu-id="dc63c-183">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="dc63c-183">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="dc63c-184">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="dc63c-184">Add custom data to groups using schema extensions</span></span>](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
