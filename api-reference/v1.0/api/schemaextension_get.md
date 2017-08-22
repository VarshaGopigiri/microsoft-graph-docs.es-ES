# <a name="get-schemaextension"></a><span data-ttu-id="a25ab-101">Obtener schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="a25ab-101">Get schemaExtension</span></span>
<span data-ttu-id="a25ab-102">Obtenga las propiedades de la definición [schemaExtensions](../resources/schemaextension.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="a25ab-102">Get the properties of the specified [schemaExtension](../resources/schemaextension.md) definition.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a25ab-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a25ab-103">Prerequisites</span></span>
<span data-ttu-id="a25ab-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="a25ab-104">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="a25ab-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a25ab-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a25ab-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a25ab-106">Optional query parameters</span></span>
<span data-ttu-id="a25ab-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a25ab-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a25ab-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a25ab-108">Request headers</span></span>
| <span data-ttu-id="a25ab-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="a25ab-109">Name</span></span>      |<span data-ttu-id="a25ab-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a25ab-110">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a25ab-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="a25ab-111">Authorization</span></span>  | <span data-ttu-id="a25ab-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a25ab-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a25ab-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a25ab-114">Content-Type</span></span>   | <span data-ttu-id="a25ab-115">application/json</span><span class="sxs-lookup"><span data-stu-id="a25ab-115">application/json</span></span> | 

## <a name="request-body"></a><span data-ttu-id="a25ab-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a25ab-116">Request body</span></span>
<span data-ttu-id="a25ab-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a25ab-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a25ab-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a25ab-118">Response</span></span>

<span data-ttu-id="a25ab-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a25ab-119">If successful, this method returns a `200 OK` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a25ab-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a25ab-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a25ab-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a25ab-121">Request</span></span>
<span data-ttu-id="a25ab-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a25ab-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_schemaextension"
}-->
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions/graphlearn_test
```
##### <a name="response"></a><span data-ttu-id="a25ab-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a25ab-123">Response</span></span>
<span data-ttu-id="a25ab-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a25ab-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 201

{
    "id":"graphlearn_test",
    "description": "Yet another test schema",
    "targetTypes": [
        "User", "Group"
    ],
    "status": "InDevelopment",
    "owner": "24d3b144-21ae-4080-943f-7067b395b913",
    "properties": [
        {
            "name": "testName",
            "type": "String"
        }
    ]
}
```

## <a name="see-also"></a><span data-ttu-id="a25ab-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a25ab-127">See also</span></span>

- [<span data-ttu-id="a25ab-128">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="a25ab-128">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="a25ab-129">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="a25ab-129">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->