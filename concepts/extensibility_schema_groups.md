# <a name="add-custom-data-to-groups-using-schema-extensions"></a>Agregar datos personalizados a los grupos mediante extensiones de esquema 

Vamos a guiarle a través de un ejemplo para demostrarle cómo usar las *extensiones de esquema*. 

Imagine que es un programador en una empresa de software de administración de aprendizaje llamada "Graph Learn" que crea cursos de formación y materiales para empresas.  Los grupos de Office 365, con sus ricas experiencias de colaboración, son una forma fantástica de presentar el contenido del curso y registrar ejercicios entre los participantes tanto de cursos en línea como guiados por instructores.  Puede que quiera hacer que estos grupos de Office 365 utilizados para cursos de formación se puedan identificar fácilmente como tales, lo que permitirá a otros desarrolladores descubrir los cursos que haya creado y crear experiencias enriquecedoras a partir de los mismos.

En este escenario, vamos a mostrarle cómo:

1. Ver las definiciones de extensiones de esquema disponibles que puede utilizar.
2. Registrar una definición de extensión de esquema que tiene como objetivo grupos de cursos de formación.
3. Crear un nuevo grupo con datos extendidos basados en la definición de extensión de esquema que acaba de registrar.
4. Agregar, actualizar o eliminar datos personalizados a un grupo existente basado en una definición de extensión de esquema.
5. Leer un grupo y los datos de extensión.

>**Nota:** En este tema, se muestra cómo crear y leer los valores de extensión de esquema en un recurso de **group** (pasos 3-5).  Estos mismos métodos también son compatibles con los tipos de recurso **administrativeUnit**, **device** (dispositivo), **event** (evento), **message** (mensaje), **organization** (organización), **post** (publicación) y **user** (usuario).  Así que puede efectuar operaciones similares a las siguientes solicitudes de ejemplo en cualquiera de esos recursos. Tenga en cuenta que ** administrativeUnit "solo está disponible en el punto de conexión beta.

## <a name="1-view-available-schema-extensions"></a>1. Ver extensiones de esquema disponibles
En primer lugar, como desarrollador, quizá quiera encontrar otras definiciones de extensión de esquema que pueda reutilizar su aplicación.  Esto se puede hacer consultando el recurso **schemaExtension**.  
En el siguiente ejemplo, realizará una consulta por **id** para una extensión de esquema específica.

Observe que la extensión devuelta en la respuesta tiene **Available** como el valor **estado**, lo que indica que cualquier aplicación que tenga permisos para los recursos en la propiedad **targetTypes** puede utilizar y actualizar la extensión con cambios que se incorporen. En general, esta operación devuelve las extensiones de esquema que cumplen el filtro especificado independientemente de su **estado**, por lo que debe comprobar el estado de extensión antes de utilizarla.


##### <a name="request"></a>Solicitud
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions?$filter=id eq 'graphlearn_test'
```
##### <a name="response"></a>Respuesta
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
## <a name="2-register-a-schema-extension-definition-that-describes-a-training-course"></a>2. Registrar una definición de extensión de esquema que describe un curso de aprendizaje
Si no puede encontrar una extensión de esquema que *sea* adecuada para sus necesidades, puede crear y registrar una definición de extensión nueva para el curso de aprendizaje en el recurso **group**.  

Al crear una definición de extensión de esquema, debe proporcionar una cadena para la propiedad **id**. Hay dos formas de hacerlo: En el ejemplo siguiente, se muestra la forma preferida, que utiliza un nombre de dominio de cortesía (`graphlearn.com`) que se ha comprobado con su arrendatario. Concatene el nombre de dominio comprobado (`graphlearn`) con un nombre para la extensión de esquema (`courses`) y asigne el **id** con la cadena resultante, `graphlearn_courses`.  

A continuación, especifique una descripción (para habilitar la capacidad de descubrimiento), tipos objetivo (que definan a qué recursos se aplica esta extensión) y las propiedades personalizadas que forman el esquema.  En este ejemplo, se especifican las propiedades personalizadas `courseId`, `courseName` y `courseType` y sus tipos.

Consulte un [ejemplo de otra forma de asignar **id.** en la solicitud](../api-reference/v1.0/api/schemaextension_post_schemaextensions.md#request-2), que requiere que se especifique solo un nombre de esquema.

Observe que cuando crea inicialmente una extensión de esquema, el estado es **InDevelopment**. Mientras se está desarrollando la extensión, puede mantenerla en este estado, durante el cual solo la aplicación que la creó puede actualizarla con los cambios que se incorporen o eliminarla. Cuando esté preparado para compartir la extensión para su uso por otras aplicaciones, establezca el **estado** en **Available**.

##### <a name="request"></a>Solicitud
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
##### <a name="response"></a>Respuesta
```http
HTTP/1.1 201 Created
Content-Type: application/json
Content-length: 420
{
    "id": "graphlearn_course",
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

## <a name="3-create-a-new-group-with-extended-data"></a>3. Crear un nuevo grupo con datos extendidos 
Crear un _nuevo_ grupo y ampliarlo con datos adicionales con la definición de extensión de esquema `graphlearn_courses` que acaba de registrar.  Se trata de un ```POST``` estándar para el recurso **grupo**, con la extensión de tipo complejo `graphlearn_courses` adicional definida en el cuerpo de la solicitud.  La respuesta no reflejará ninguna extensión de datos. Necesitamos ```$select``` explícitamente la extensión por el nombre con una operación ```GET```.

##### <a name="request"></a>Solicitud
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
##### <a name="response"></a>Respuesta
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

## <a name="4-add-update-or-remove-custom-data-in-an-existing-group"></a>4. Agregar, actualizar o eliminar datos personalizados en un grupo existente
Puede extender y agregar datos a una instancia de grupo _existente_ con la extensión de tipo complejo `graphlearn_courses` adicional definida en el cuerpo de una solicitud ```PATCH```.  

##### <a name="request"></a>Solicitud
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
##### <a name="response"></a>Respuesta
```http
HTTP/1.1 204 No Content
```

Si desea actualizar los valores de los datos de extensión, ponga todo el tipo complejo de extensión en el cuerpo de una solicitud ```PATCH``` (de forma similar a cuando se añaden datos personalizados a un recurso existente).

También puede eliminar datos personalizados agregados a una instancia de recurso estableciendo la propiedad correspondiente de la extensión en NULL. 

Para eliminar una extensión de esquema de una instancia del recurso, establezca el tipo complejo de extensión en esa instancia en NULL.


## <a name="5-get-a-group-and-its-extension-data"></a>5. Obtener un grupo y sus datos de extensión
Una forma práctica para buscar un grupo (o grupos) es usar `$filter` para coincidir con los valores de propiedad de extensión específica, como un identificador o nombre de extensión. 

A continuación, para obtener los datos personalizados en un grupo, utilice `$select` para incluir la extensión por nombre (en este caso por `graphlearn_courses`).

El ejemplo siguiente busca el grupo que tiene la extensión `graphlearn_courses` con un `courseId` de coincidencia de valor de propiedad `123`, y obtiene las propiedades del grupo **displayName**, **id** y **descripción** y los datos personalizados en la extensión `graphlearn_courses`. (En la consulta actual, asegúrese de aplicar la codificación de la URL según sea necesario).

#### <a name="request"></a>Solicitud

```http
GET https://graph.microsoft.com/v1.0/groups?$filter=graphlearn_courses/courseId eq ‘123’&$select=displayName,id,description,graphlearn_courses
```


##### <a name="response"></a>Respuesta
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

## <a name="see-also"></a>Recursos adicionales

- [Agregar datos personalizados a los recursos mediante extensiones](extensibility_overview.md)
- [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](extensibility_open_users.md)
- [Dominios de Office 365](https://technet.microsoft.com/en-us/library/office-365-domains.aspx)
- [Agregar y comprobar un dominio para el nuevo Office 365](http://office365support.ca/adding-and-verifying-a-domain-for-the-new-office-365/)
- [Tipo de recurso schemaExtension](../api-reference/v1.0/resources/schemaextension.md)
- [Listar schemaExtensions](../api-reference/v1.0/api/schemaextension_list.md)
- [Crear schemaExtensions](../api-reference/v1.0/api/schemaextension_post_schemaextensions.md)
- [Obtener schemaExtensions](../api-reference/v1.0/api/schemaextension_get.md)
- [Actualizar schemaExtension](../api-reference/v1.0/api/schemaextension_update.md)
- [Eliminar schemaExtensions](../api-reference/v1.0/api/schemaextension_delete.md)