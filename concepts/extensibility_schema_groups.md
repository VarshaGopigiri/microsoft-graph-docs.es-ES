# <a name="add-custom-data-to-groups-using-schema-extensions"></a><span data-ttu-id="cb614-101">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="cb614-101">Add custom data to groups using schema extensions</span></span> 

<span data-ttu-id="cb614-102">Vamos a guiarle a través de un ejemplo para demostrarle cómo usar las *extensiones de esquema*.</span><span class="sxs-lookup"><span data-stu-id="cb614-102">We're going to walk you through an example to demonstrate how to use *schema extensions*.</span></span> 

<span data-ttu-id="cb614-p101">Imagine que es un programador en una empresa de software de administración de aprendizaje llamada "Graph Learn" que crea cursos de formación y materiales para empresas.  Los grupos de Office 365, con sus ricas experiencias de colaboración, son una forma fantástica de presentar el contenido del curso y registrar ejercicios entre los participantes tanto de cursos en línea como guiados por instructores.  Puede que quiera hacer que estos grupos de Office 365 utilizados para cursos de formación se puedan identificar fácilmente como tales, lo que permitirá a otros desarrolladores descubrir los cursos que haya creado y crear experiencias enriquecedoras a partir de los mismos.</span><span class="sxs-lookup"><span data-stu-id="cb614-p101">Imagine you're a developer in a Learning Management Software company called “Graph Learn” that builds training courses and materials for businesses.  Office 365 groups, with their rich collaborative experiences, is a fantastic way to deliver course content and record exercises among participants for both online courses and instructor-led courses.  You may want to make those Office 365 groups used for training courses easily identifiable as training courses, which will allow other developers to discover your groups and build rich experiences on top of your learning courses.</span></span>

<span data-ttu-id="cb614-106">En este escenario, vamos a mostrarle cómo:</span><span class="sxs-lookup"><span data-stu-id="cb614-106">For this scenario, we're going to show you how to:</span></span>

1. <span data-ttu-id="cb614-107">Ver las definiciones de extensiones de esquema disponibles que puede utilizar.</span><span class="sxs-lookup"><span data-stu-id="cb614-107">View available schema extension definitions that you could use.</span></span>
2. <span data-ttu-id="cb614-108">Registrar una definición de extensión de esquema que tiene como objetivo grupos de cursos de formación.</span><span class="sxs-lookup"><span data-stu-id="cb614-108">Register a schema extension definition that targets groups for training courses.</span></span>
3. <span data-ttu-id="cb614-109">Crear un nuevo grupo con datos extendidos basados en la definición de extensión de esquema que acaba de registrar.</span><span class="sxs-lookup"><span data-stu-id="cb614-109">Create a new group with extended data based on the schema extension definition that you just registered.</span></span>
4. <span data-ttu-id="cb614-110">Agregar, actualizar o eliminar datos personalizados a un grupo existente basado en una definición de extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="cb614-110">Add, update, or remove custom data in an existing group based on a schema extension definition.</span></span>
5. <span data-ttu-id="cb614-111">Leer un grupo y los datos de extensión.</span><span class="sxs-lookup"><span data-stu-id="cb614-111">Read back a group and the extension data.</span></span>

><span data-ttu-id="cb614-p102">**Nota:** En este tema, se muestra cómo crear y leer los valores de extensión de esquema en un recurso de **group** (pasos 3-5).  Estos mismos métodos también son compatibles con los tipos de recurso **administrativeUnit**, **device** (dispositivo), **event** (evento), **message** (mensaje), **organization** (organización), **post** (publicación) y **user** (usuario).  Así que puede efectuar operaciones similares a las siguientes solicitudes de ejemplo en cualquiera de esos recursos. Tenga en cuenta que **administrativeUnit** solo está disponible en el punto de conexión beta.</span><span class="sxs-lookup"><span data-stu-id="cb614-p102">**Note:** This topic shows you how to create and read schema extension values on a **group** resource (steps 3-5).  The same methods are supported for the **administrativeUnit**, **device**, **event**, **message**, **organization**, **post**, and **user** resource types as well.  So you can carry out similar operations as the example requests below on any of those resources. Note that **administrativeUnit** is available only in the beta endpoint.</span></span>

## <a name="1-view-available-schema-extensions"></a><span data-ttu-id="cb614-116">1. Ver extensiones de esquema disponibles</span><span class="sxs-lookup"><span data-stu-id="cb614-116">1. View available schema extensions</span></span>
<span data-ttu-id="cb614-p103">En primer lugar, como desarrollador, quizá quiera encontrar otras definiciones de extensión de esquema que pueda reutilizar su aplicación.  Esto se puede hacer consultando el recurso **schemaExtension**.</span><span class="sxs-lookup"><span data-stu-id="cb614-p103">First, as a developer, you might want to find any other schema extension definitions that our app could reuse.  This can be done by querying the **schemaExtension** resource.</span></span>  
<span data-ttu-id="cb614-119">En el siguiente ejemplo, realizará una consulta por **id** para una extensión de esquema específica.</span><span class="sxs-lookup"><span data-stu-id="cb614-119">In the example below, you're going to query for a specific schema extension by **id**.</span></span>

<span data-ttu-id="cb614-p104">Observe que la extensión devuelta en la respuesta tiene **Available** como el valor **estado**, lo que indica que cualquier aplicación que tenga permisos para los recursos en la propiedad **targetTypes** puede utilizar y actualizar la extensión con cambios que se incorporen. En general, esta operación devuelve las extensiones de esquema que cumplen el filtro especificado independientemente de su **estado**, por lo que debe comprobar el estado de extensión antes de utilizarla.</span><span class="sxs-lookup"><span data-stu-id="cb614-p104">Notice that the extension returned in the response has **Available** as the **status** value, which indicates that any app which has permission to the resources in the **targetTypes** property can use and update the extension with additive changes. In general, this operation returns any schema extensions that satisfy the specified filter regardless of **status**, so do check the extension status before using it.</span></span>


##### <a name="request"></a><span data-ttu-id="cb614-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb614-122">Request</span></span>
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions?$filter=id eq 'graphlearn_test'
```
##### <a name="response"></a><span data-ttu-id="cb614-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb614-123">Response</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-length: 420
{
    "value": [
        {
            "id":"graphlearn_test",
            "description": "Yet another test schema",
            "targetTypes": [
                "User", "Group"
            ],
            "status": "Available",
            "owner": "24d3b144-21ae-4080-943f-7067b395b913",
            "properties": [
                {
                    "name": "testName",
                    "type": "String"
                }
            ]
        }
    ]
}
```
## <a name="2-register-a-schema-extension-definition-that-describes-a-training-course"></a><span data-ttu-id="cb614-124">2. Registrar una definición de extensión de esquema que describe un curso de aprendizaje</span><span class="sxs-lookup"><span data-stu-id="cb614-124">2. Register a schema extension definition that describes a training course</span></span>
<span data-ttu-id="cb614-125">Si no puede encontrar una extensión de esquema que *sea* adecuada para sus necesidades, puede crear y registrar una definición de extensión nueva para el curso de aprendizaje en el recurso **group**.</span><span class="sxs-lookup"><span data-stu-id="cb614-125">If you can't find a schema extension that *is* appropriate for your needs, you can create and register a new extension definition for training courses on the **group** resource.</span></span>  

<span data-ttu-id="cb614-p105">Al crear una definición de extensión de esquema, debe proporcionar una cadena para la propiedad **id**. Hay dos formas de hacerlo: En el ejemplo siguiente, se muestra la forma preferida, que utiliza un nombre de dominio de cortesía (`graphlearn.com`) que se ha comprobado con su arrendatario. Concatene el nombre de dominio comprobado (`graphlearn`) con un nombre para la extensión de esquema (`courses`) y asigne el **id** con la cadena resultante, `graphlearn_courses`.</span><span class="sxs-lookup"><span data-stu-id="cb614-p105">When creating a schema extension definition, you should provide a string for the **id** property. There are two ways to do this. The following example shows the preferred way, which uses a vanity domain name (`graphlearn.com`) that has been verified with your tenant. Concatenate the verified domain name (`graphlearn`) with a name for the schema extension (`courses`), and assign **id** with the resultant string, `graphlearn_courses`.</span></span>  

<span data-ttu-id="cb614-p106">A continuación, especifique una descripción (para habilitar la capacidad de descubrimiento), tipos objetivo (que definan a qué recursos se aplica esta extensión) y las propiedades personalizadas que forman el esquema.  En este ejemplo, se especifican las propiedades personalizadas `courseId`, `courseName` y `courseType` y sus tipos.</span><span class="sxs-lookup"><span data-stu-id="cb614-p106">Then, specify a description (to enable discoverability), target types (defining which resources this extension applies to), and the custom properties that make up the schema.  In this example, specify the `courseId`, `courseName` and `courseType` custom properties and their types.</span></span>

<span data-ttu-id="cb614-132">Consulte un [ejemplo de otra forma de asignar **id.** en la solicitud](../api-reference/v1.0/api/schemaextension_post_schemaextensions.md#request-2), que requiere que se especifique solo un nombre de esquema.</span><span class="sxs-lookup"><span data-stu-id="cb614-132">See an [example of the other way to assign **id** in the request](../api-reference/v1.0/api/schemaextension_post_schemaextensions.md#request-2), that requires you to provide only a schema name.</span></span>

<span data-ttu-id="cb614-p107">Observe que cuando crea inicialmente una extensión de esquema, el estado es **InDevelopment**. Mientras se está desarrollando la extensión, puede mantenerla en este estado, durante el cual solo la aplicación que la creó puede actualizarla con los cambios que se incorporen o eliminarla. Cuando esté preparado para compartir la extensión para su uso por otras aplicaciones, establezca el **estado** en **Available**.</span><span class="sxs-lookup"><span data-stu-id="cb614-p107">Notice that when you initially create a schema extension, its status is **InDevelopment**. While you're developing the extension, you can keep it in this status, during which only your app that created it can update it with additive changes or delete it. When you are ready to share the extension for use by other apps, set **status** to **Available**.</span></span>

##### <a name="request"></a><span data-ttu-id="cb614-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb614-136">Request</span></span>
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
##### <a name="response"></a><span data-ttu-id="cb614-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb614-137">Response</span></span>
```http
HTTP/1.1 201 Created
Content-Type: application/json
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

## <a name="3-create-a-new-group-with-extended-data"></a><span data-ttu-id="cb614-138">3. Crear un nuevo grupo con datos extendidos</span><span class="sxs-lookup"><span data-stu-id="cb614-138">3. Create a new group with extended data</span></span> 
<span data-ttu-id="cb614-p108">Crear un _nuevo_ grupo y ampliarlo con datos adicionales con la definición de extensión de esquema `graphlearn_courses` que acaba de registrar.  Se trata de un ```POST``` estándar para el recurso **grupo**, con la extensión de tipo complejo `graphlearn_courses` adicional definida en el cuerpo de la solicitud.  La respuesta no reflejará ninguna extensión de datos. Necesitamos ```$select``` explícitamente la extensión por el nombre con una operación ```GET```.</span><span class="sxs-lookup"><span data-stu-id="cb614-p108">Create a _new_ group and extend it with extra data using the `graphlearn_courses` schema extension definition that we just registered.  This is a standard ```POST``` to the **group** resource, with the additional `graphlearn_courses` complex type extension defined in the request body.  The response will not mirror back any data extensions. We need to explicitly ```$select``` the extension by name using a ```GET``` operation.</span></span>

##### <a name="request"></a><span data-ttu-id="cb614-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb614-143">Request</span></span>
```http
POST https://graph.microsoft.com/v1.0/groups
Content-type: application/json
{
    "displayName": "New Managers March 2017",
    "description": "New Managers training course for March 2017",
    "groupTypes": ["Unified"],
    "mailEnabled": true,
    "mailNickname": "newMan201703",
    "securityEnabled": false,
    "graphlearn_courses": {
        "courseId":"123",
        "courseName":"New Managers",
        "courseType":"Online"
    }
}
```
##### <a name="response"></a><span data-ttu-id="cb614-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb614-144">Response</span></span>
```http
HTTP/1.1 201 Created
Content-Type: application/json
Content-length: 420
{
    "id": "dfc8016f-db97-4c47-a582-49cb8f849355",
    "createdDateTime": "2017-02-09T00:17:05Z",
    "description": "New Managers training course for March 2017",
    "displayName": "New Managers March 2017",
    "groupTypes": [
        "Unified"
    ],
    "mail": "newMan201703@graphlearn.com",
    "mailEnabled": true,
    "mailNickname": "newMan201703",
    "securityEnabled": false,
    "theme": null,
    "visibility": "Public"
}
```

## <a name="4-add-update-or-remove-custom-data-in-an-existing-group"></a><span data-ttu-id="cb614-145">4. Agregar, actualizar o eliminar datos personalizados en un grupo existente</span><span class="sxs-lookup"><span data-stu-id="cb614-145">4. Add, update, or remove custom data in an existing group</span></span>
<span data-ttu-id="cb614-146">Puede extender y agregar datos a una instancia de grupo _existente_ con la extensión de tipo complejo `graphlearn_courses` adicional definida en el cuerpo de una solicitud ```PATCH```.</span><span class="sxs-lookup"><span data-stu-id="cb614-146">You can extend and add custom data to an _existing_ group instance with the additional `graphlearn_courses` complex type extension defined in the body of a ```PATCH``` request.</span></span>  

##### <a name="request"></a><span data-ttu-id="cb614-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb614-147">Request</span></span>
```http
PATCH https://graph.microsoft.com/v1.0/groups/dfc8016f-db97-4c47-a582-49cb8f849355
Content-type: application/json
Content-length: 230
{
    "graphlearn_courses":{
        "courseId":"123",
        "courseName":"New Managers",
        "courseType":"Online"
    }   
}
```
##### <a name="response"></a><span data-ttu-id="cb614-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb614-148">Response</span></span>
```http
HTTP/1.1 204 No Content
```

<span data-ttu-id="cb614-149">Si desea actualizar los valores de los datos de extensión, ponga todo el tipo complejo de extensión en el cuerpo de una solicitud ```PATCH``` (de forma similar a cuando se añaden datos personalizados a un recurso existente).</span><span class="sxs-lookup"><span data-stu-id="cb614-149">If you want to update the values of the extension data, put the entire extension complex type in the body of a ```PATCH``` request (similar to adding custom data to an existing resource).</span></span>

<span data-ttu-id="cb614-150">También puede eliminar datos personalizados agregados a una instancia de recurso estableciendo la propiedad correspondiente de la extensión en NULL.</span><span class="sxs-lookup"><span data-stu-id="cb614-150">You can also remove custom data added to a resource instance by setting the corresponding extension property to null.</span></span> 

<span data-ttu-id="cb614-151">Para eliminar una extensión de esquema de una instancia del recurso, establezca el tipo complejo de extensión en esa instancia en NULL.</span><span class="sxs-lookup"><span data-stu-id="cb614-151">To remove a schema extension from a resource instance, set the extension complex type in that instance to null.</span></span>


## <a name="5-get-a-group-and-its-extension-data"></a><span data-ttu-id="cb614-152">5. Obtener un grupo y sus datos de extensión</span><span class="sxs-lookup"><span data-stu-id="cb614-152">5. Get a group and its extension data</span></span>
<span data-ttu-id="cb614-153">Una forma práctica para buscar un grupo (o grupos) es usar `$filter` para coincidir con los valores de propiedad de extensión específica, como un identificador o nombre de extensión.</span><span class="sxs-lookup"><span data-stu-id="cb614-153">A handy way to look for a group (or groups) is to use `$filter` to match for specific extension property values, such as an extension name or ID.</span></span> 

<span data-ttu-id="cb614-154">A continuación, para obtener los datos personalizados en un grupo, utilice `$select` para incluir la extensión por nombre (en este caso por `graphlearn_courses`).</span><span class="sxs-lookup"><span data-stu-id="cb614-154">Then, to get the custom data in a group, use `$select` to include the extension by name (in this case by `graphlearn_courses`).</span></span>

<span data-ttu-id="cb614-p109">El ejemplo siguiente busca el grupo que tiene la extensión `graphlearn_courses` con un `courseId` de coincidencia de valor de propiedad `123`, y obtiene las propiedades del grupo **displayName**, **id** y **descripción** y los datos personalizados en la extensión `graphlearn_courses`. (En la consulta actual, asegúrese de aplicar la codificación de la URL según sea necesario).</span><span class="sxs-lookup"><span data-stu-id="cb614-p109">The following example looks for the group that has the `graphlearn_courses` extension with a `courseId` property value matching `123`, and gets the group properties **displayName**, **id**, and **description**, and the custom data in the `graphlearn_courses` extension. (In the actual query, make sure you apply URL encoding as necessary.)</span></span>

#### <a name="request"></a><span data-ttu-id="cb614-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb614-157">Request</span></span>

```http
GET https://graph.microsoft.com/v1.0/groups?$filter=graphlearn_courses/courseId eq ‘123’&$select=displayName,id,description,graphlearn_courses
```


##### <a name="response"></a><span data-ttu-id="cb614-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb614-158">Response</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-length: 326
{
  "value": [
    {
      "displayName": "New Managers March 2017",
      "id": "14429ae5-3e74-41a2-9fa8-028fbb984637",
      "description": "New Managers training course for March 2017",
      "graphlearn_courses": {
        "@odata.type": "#microsoft.graph.ComplexExtensionValue",
        "courseId":"123",
        "courseName":"New Managers",
        "courseType":"Online"
      }
    }
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="cb614-159">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cb614-159">See also</span></span>

- [<span data-ttu-id="cb614-160">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="cb614-160">Add custom data to resources using extensions</span></span>](extensibility_overview.md)
- [<span data-ttu-id="cb614-161">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="cb614-161">Add custom data to users using open extensions (preview)</span></span>](extensibility_open_users.md)
- [<span data-ttu-id="cb614-162">Dominios de Office 365</span><span class="sxs-lookup"><span data-stu-id="cb614-162">Office 365 domains</span></span>](https://technet.microsoft.com/en-us/library/office-365-domains.aspx)
- [<span data-ttu-id="cb614-163">Agregar y comprobar un dominio para el nuevo Office 365</span><span class="sxs-lookup"><span data-stu-id="cb614-163">Adding and Verifying a Domain for the NEW Office 365</span></span>](http://office365support.ca/adding-and-verifying-a-domain-for-the-new-office-365/)
- [<span data-ttu-id="cb614-164">Tipo de recurso schemaExtension</span><span class="sxs-lookup"><span data-stu-id="cb614-164">schemaExtension resource type</span></span>](../api-reference/v1.0/resources/schemaextension.md)
- [<span data-ttu-id="cb614-165">Listar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="cb614-165">List schemaExtensions</span></span>](../api-reference/v1.0/api/schemaextension_list.md)
- [<span data-ttu-id="cb614-166">Crear schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="cb614-166">Create schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_post_schemaextensions.md)
- [<span data-ttu-id="cb614-167">Obtener schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="cb614-167">Get schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_get.md)
- [<span data-ttu-id="cb614-168">Actualizar schemaExtension</span><span class="sxs-lookup"><span data-stu-id="cb614-168">Update schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_update.md)
- [<span data-ttu-id="cb614-169">Eliminar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="cb614-169">Delete schemaExtension</span></span>](../api-reference/v1.0/api/schemaextension_delete.md)
