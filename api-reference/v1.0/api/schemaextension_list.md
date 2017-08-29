# <a name="list-schemaextensions"></a><span data-ttu-id="f044b-101">Enumerar schemaExtensions</span><span class="sxs-lookup"><span data-stu-id="f044b-101">List schemaExtensions</span></span>

<span data-ttu-id="f044b-102">Obtenga una lista de objetos [schemaExtension](../resources/schemaextension.md) creada por cualquier aplicación de su propiedad en el inquilino actual (que puede estar **InDevelopment** (en desarrollo), **Available** (disponible) o **Deprecated** (en desuso) y el resto de extensiones de esquema propiedad de las otras aplicaciones que estén marcadas como **Available**.</span><span class="sxs-lookup"><span data-stu-id="f044b-102">Get a list of [schemaExtension](../resources/schemaextension.md) objects created by any apps you own in the current tenant (that can be **InDevelopment**, **Available**, or **Deprecated**), and all other schema extensions owned by other apps that are marked as **Available**.</span></span> 

## <a name="permissions"></a><span data-ttu-id="f044b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f044b-103">Permissions</span></span>
<span data-ttu-id="f044b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f044b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="f044b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f044b-106">Permission type</span></span>      | <span data-ttu-id="f044b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f044b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f044b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f044b-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f044b-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="f044b-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="f044b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f044b-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f044b-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f044b-111">Not supported.</span></span>    |
|<span data-ttu-id="f044b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f044b-112">Application</span></span> | <span data-ttu-id="f044b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f044b-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f044b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f044b-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /schemaExtensions
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f044b-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f044b-115">Optional query parameters</span></span>
<span data-ttu-id="f044b-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f044b-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f044b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f044b-117">Request headers</span></span>
| <span data-ttu-id="f044b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="f044b-118">Name</span></span>      |<span data-ttu-id="f044b-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f044b-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="f044b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f044b-120">Authorization</span></span>  | <span data-ttu-id="f044b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f044b-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f044b-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f044b-123">Content-Type</span></span>   | <span data-ttu-id="f044b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f044b-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="f044b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f044b-125">Request body</span></span>
<span data-ttu-id="f044b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f044b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f044b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f044b-127">Response</span></span>

<span data-ttu-id="f044b-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [schemaExtension](../resources/schemaextension.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f044b-128">If successful, this method returns a `200 OK` response code and collection of [schemaExtension](../resources/schemaextension.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f044b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f044b-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f044b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f044b-130">Request</span></span>
<span data-ttu-id="f044b-131">En el ejemplo siguiente se muestra cómo buscar una extensión accesible concreta entre todas las demás filtrando por su **id.** único.</span><span class="sxs-lookup"><span data-stu-id="f044b-131">The following example shows how to look among all the accessible extensions for a specific one by filtering on its unique **id**.</span></span> 
<!-- {
  "blockType": "request",
  "name": "get_schemaextensions"
}-->
```http
GET https://graph.microsoft.com/v1.0/schemaExtensions?$filter=id%20eq%20'graphlearn_test'
```
##### <a name="response"></a><span data-ttu-id="f044b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f044b-132">Response</span></span>
<span data-ttu-id="f044b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f044b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="f044b-136">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="f044b-136">See also</span></span>

- [<span data-ttu-id="f044b-137">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="f044b-137">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="f044b-138">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="f044b-138">Add custom data to groups using schema extensions</span></span>](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List schemaExtensions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->