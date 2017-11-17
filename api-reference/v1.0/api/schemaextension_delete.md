# <a name="delete-schemaextension"></a><span data-ttu-id="f7cbc-101">Eliminar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="f7cbc-101">Delete schemaExtension</span></span>

<span data-ttu-id="f7cbc-102">Elimine la definición de una [extensión de esquema](../resources/schemaExtension.md).</span><span class="sxs-lookup"><span data-stu-id="f7cbc-102">Delete the definition of a [schema extension](../resources/schemaExtension.md).</span></span>

<span data-ttu-id="f7cbc-p101">Solo la aplicación que creó la extensión de esquema (la aplicación propietaria) puede eliminar la definición de la extensión de esquema, y solo cuando la extensión esté en el estado **InDevelopment**. Eliminar una definición de extensión de esquema no afecta al acceso a los datos personalizados que se han agregado a las instancias de recurso a partir de esa definición.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-p101">Only the app that created the schema extension (owner app) can delete the schema extension definition, and only when the extension is in the **InDevelopment** state. Deleting a schema extension definition does not affect accessing custom data that has been added to resource instances based on that definition.</span></span>


## <a name="permissions"></a><span data-ttu-id="f7cbc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f7cbc-105">Permissions</span></span>
<span data-ttu-id="f7cbc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f7cbc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="f7cbc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7cbc-108">Permission type</span></span>      | <span data-ttu-id="f7cbc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7cbc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f7cbc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7cbc-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f7cbc-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f7cbc-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f7cbc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7cbc-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f7cbc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-113">Not supported.</span></span>    |
|<span data-ttu-id="f7cbc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7cbc-114">Application</span></span> | <span data-ttu-id="f7cbc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f7cbc-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7cbc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /schemaExtensions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="f7cbc-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7cbc-117">Request headers</span></span>
| <span data-ttu-id="f7cbc-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f7cbc-118">Name</span></span>      |<span data-ttu-id="f7cbc-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7cbc-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f7cbc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f7cbc-120">Authorization</span></span>  | <span data-ttu-id="f7cbc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f7cbc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7cbc-123">Request body</span></span>
<span data-ttu-id="f7cbc-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f7cbc-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7cbc-125">Response</span></span>

<span data-ttu-id="f7cbc-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f7cbc-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7cbc-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f7cbc-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7cbc-129">Request</span></span>
<span data-ttu-id="f7cbc-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_schemaextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/schemaExtensions/{id}
```
##### <a name="response"></a><span data-ttu-id="f7cbc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7cbc-131">Response</span></span>
<span data-ttu-id="f7cbc-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7cbc-132">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="f7cbc-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7cbc-133">See also</span></span>

- [<span data-ttu-id="f7cbc-134">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="f7cbc-134">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="f7cbc-135">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="f7cbc-135">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->