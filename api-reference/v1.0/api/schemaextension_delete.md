# <a name="delete-schemaextension"></a><span data-ttu-id="1fa81-101">Eliminar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="1fa81-101">Delete schemaExtension</span></span>

<span data-ttu-id="1fa81-102">Elimine la definición de una [extensión de esquema](../resources/schemaExtension.md).</span><span class="sxs-lookup"><span data-stu-id="1fa81-102">Delete the definition of a [schema extension](../resources/schemaExtension.md).</span></span>

<span data-ttu-id="1fa81-p101">Solo la aplicación que creó la extensión de esquema (la aplicación propietaria) puede eliminar la definición de la extensión de esquema, y solo cuando la extensión esté en el estado **InDevelopment**. Eliminar una definición de extensión de esquema no afecta al acceso a los datos personalizados que se han agregado a las instancias de recurso a partir de esa definición.</span><span class="sxs-lookup"><span data-stu-id="1fa81-p101">Only the app that created the schema extension (owner app) can delete the schema extension definition, and only when the extension is in the **InDevelopment** state. Deleting a schema extension definition does not affect accessing custom data that has been added to resource instances based on that definition.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="1fa81-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1fa81-105">Prerequisites</span></span>
<span data-ttu-id="1fa81-106">Se requiere el siguiente **ámbito** para ejecutar esta API: *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="1fa81-106">The following **scope** is required to execute this API: *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="1fa81-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1fa81-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /schemaExtensions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="1fa81-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1fa81-108">Request headers</span></span>
| <span data-ttu-id="1fa81-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="1fa81-109">Name</span></span>      |<span data-ttu-id="1fa81-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fa81-110">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="1fa81-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="1fa81-111">Authorization</span></span>  | <span data-ttu-id="1fa81-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1fa81-p102">Bearer {token}. Required.</span></span> |
 

## <a name="request-body"></a><span data-ttu-id="1fa81-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1fa81-114">Request body</span></span>
<span data-ttu-id="1fa81-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1fa81-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1fa81-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fa81-116">Response</span></span>

<span data-ttu-id="1fa81-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fa81-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1fa81-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fa81-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1fa81-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1fa81-120">Request</span></span>
<span data-ttu-id="1fa81-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1fa81-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_schemaextension"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/schemaExtensions/{id}
```
##### <a name="response"></a><span data-ttu-id="1fa81-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fa81-122">Response</span></span>
<span data-ttu-id="1fa81-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fa81-123">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a><span data-ttu-id="1fa81-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1fa81-124">See also</span></span>

- [<span data-ttu-id="1fa81-125">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="1fa81-125">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="1fa81-126">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="1fa81-126">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->