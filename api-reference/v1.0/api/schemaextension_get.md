# <a name="get-schemaextension"></a><span data-ttu-id="a9578-101">Obtener schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="a9578-101">Get schemaExtension</span></span>
<span data-ttu-id="a9578-102">Obtiene las propiedades de la definición [schemaExtensions](../resources/schemaextension.md) especificada.</span><span class="sxs-lookup"><span data-stu-id="a9578-102">Get the properties of the specified [schemaExtension](../resources/schemaextension.md) definition.</span></span>

## <a name="permissions"></a><span data-ttu-id="a9578-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a9578-103">Permissions</span></span>
<span data-ttu-id="a9578-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a9578-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="a9578-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a9578-106">Permission type</span></span>      | <span data-ttu-id="a9578-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a9578-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a9578-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a9578-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a9578-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a9578-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a9578-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a9578-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a9578-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9578-111">Not supported.</span></span>    |
|<span data-ttu-id="a9578-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a9578-112">Application</span></span> | <span data-ttu-id="a9578-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a9578-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a9578-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a9578-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a9578-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a9578-115">Optional query parameters</span></span>
<span data-ttu-id="a9578-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9578-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a9578-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a9578-117">Request headers</span></span>
| <span data-ttu-id="a9578-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="a9578-118">Name</span></span>      |<span data-ttu-id="a9578-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9578-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="a9578-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a9578-120">Authorization</span></span>  | <span data-ttu-id="a9578-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a9578-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="a9578-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="a9578-123">Content-Type</span></span>   | <span data-ttu-id="a9578-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a9578-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="a9578-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a9578-125">Request body</span></span>
<span data-ttu-id="a9578-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a9578-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a9578-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9578-127">Response</span></span>

<span data-ttu-id="a9578-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [schemaExtensions](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a9578-128">If successful, this method returns a `200 OK` response code and [schemaExtension](../resources/schemaextension.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a9578-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a9578-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a9578-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a9578-130">Request</span></span>
<span data-ttu-id="a9578-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a9578-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_schemaextension"
}-->
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions/graphlearn_test
```
##### <a name="response"></a><span data-ttu-id="a9578-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a9578-132">Response</span></span>
<span data-ttu-id="a9578-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a9578-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
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

## <a name="see-also"></a><span data-ttu-id="a9578-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9578-136">See also</span></span>

- [<span data-ttu-id="a9578-137">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="a9578-137">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="a9578-138">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="a9578-138">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get schemaExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->