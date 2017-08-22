# <a name="list-schemaextensions"></a><span data-ttu-id="ae7b1-101">Enumerar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="ae7b1-101">List schemaExtensions</span></span>

<span data-ttu-id="ae7b1-102">Obtenga una lista de objetos [schemaExtension](../resources/schemaextension.md) creada por cualquier aplicación de su propiedad en el inquilino actual (que puede estar **InDevelopment** (en desarrollo), **Available** (disponible) o **Deprecated** (en desuso) y el resto de extensiones de esquema propiedad de las otras aplicaciones que estén marcadas como **Available**.</span><span class="sxs-lookup"><span data-stu-id="ae7b1-102">Get a list of [schemaExtension](../resources/schemaextension.md) objects created by any apps you own in the current tenant (that can be **InDevelopment**, **Available**, or **Deprecated**), and all other schema extensions owned by other apps that are marked as **Available**.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ae7b1-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae7b1-103">Prerequisites</span></span>
<span data-ttu-id="ae7b1-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="ae7b1-104">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="ae7b1-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae7b1-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ae7b1-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ae7b1-106">Optional query parameters</span></span>
<span data-ttu-id="ae7b1-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae7b1-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ae7b1-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae7b1-108">Request headers</span></span>
| <span data-ttu-id="ae7b1-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae7b1-109">Name</span></span>      |<span data-ttu-id="ae7b1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae7b1-110">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="ae7b1-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae7b1-111">Authorization</span></span>  | <span data-ttu-id="ae7b1-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae7b1-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ae7b1-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ae7b1-114">Content-Type</span></span>   | <span data-ttu-id="ae7b1-115">application/json</span><span class="sxs-lookup"><span data-stu-id="ae7b1-115">application/json</span></span> | 

## <a name="request-body"></a><span data-ttu-id="ae7b1-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae7b1-116">Request body</span></span>
<span data-ttu-id="ae7b1-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ae7b1-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ae7b1-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae7b1-118">Response</span></span>

<span data-ttu-id="ae7b1-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [schemaExtension](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae7b1-119">If successful, this method returns a `200 OK` response code and collection of [schemaExtension](../resources/schemaextension.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ae7b1-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae7b1-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ae7b1-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae7b1-121">Request</span></span>
<span data-ttu-id="ae7b1-122">En el ejemplo siguiente se muestra cómo buscar una extensión accesible concreta entre todas las demás filtrando por su **id.** único.</span><span class="sxs-lookup"><span data-stu-id="ae7b1-122">The following example shows how to look among all the accessible extensions for a specific one by filtering on its unique **id**.</span></span> 
<!-- {
  "blockType": "request",
  "name": "get_schemaextensions"
}-->
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions?$filter=id%20eq%20'graphlearn_test'
```
##### <a name="response"></a><span data-ttu-id="ae7b1-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae7b1-123">Response</span></span>
<span data-ttu-id="ae7b1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ae7b1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 274

{
  "value": [
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
  ]
}
```

## <a name="see-also"></a><span data-ttu-id="ae7b1-127">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ae7b1-127">See also</span></span>

- [<span data-ttu-id="ae7b1-128">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="ae7b1-128">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="ae7b1-129">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="ae7b1-129">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List schemaExtensions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->