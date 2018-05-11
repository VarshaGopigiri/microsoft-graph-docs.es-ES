# <a name="list-organization"></a><span data-ttu-id="bd83e-101">List organization</span><span class="sxs-lookup"><span data-stu-id="bd83e-101">List organization</span></span>

> <span data-ttu-id="bd83e-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bd83e-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bd83e-103">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bd83e-103">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bd83e-104">Recupera una lista de objetos organization.</span><span class="sxs-lookup"><span data-stu-id="bd83e-104">Retrieve a list of organization objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="bd83e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd83e-105">Permissions</span></span>
<span data-ttu-id="bd83e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bd83e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bd83e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd83e-108">Permission type</span></span>      | <span data-ttu-id="bd83e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd83e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bd83e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd83e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="bd83e-111">User.Read, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bd83e-111">User.Read, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>   |
|<span data-ttu-id="bd83e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd83e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bd83e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd83e-113">Not supported.</span></span>    |
|<span data-ttu-id="bd83e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd83e-114">Application</span></span> | <span data-ttu-id="bd83e-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bd83e-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

> <span data-ttu-id="bd83e-116">Nota: Las aplicaciones que tienen el permiso User.Read solamente pueden leer las propiedades *id*, *displayName* y *verifiedDomains* de la organización.</span><span class="sxs-lookup"><span data-stu-id="bd83e-116">Note: Applications granted the User.Read permission are able to read only the *id*, *displayName*, and *verifiedDomains* properties of the organization.</span></span>  <span data-ttu-id="bd83e-117">El resto de propiedades devolverá valores `null`.</span><span class="sxs-lookup"><span data-stu-id="bd83e-117">All other properties will return with `null` values.</span></span> <span data-ttu-id="bd83e-118">Para leer todas las propiedades, use Directory.Read.All.</span><span class="sxs-lookup"><span data-stu-id="bd83e-118">To read all properties, use Directory.Read.All.</span></span>

## <a name="http-request"></a><span data-ttu-id="bd83e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd83e-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /organization
```
## <a name="optional-query-parameters"></a><span data-ttu-id="bd83e-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bd83e-120">Optional query parameters</span></span>
<span data-ttu-id="bd83e-121">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd83e-121">This method supports the [OData Query Parameters](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bd83e-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd83e-122">Request headers</span></span>
| <span data-ttu-id="bd83e-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd83e-123">Name</span></span>       | <span data-ttu-id="bd83e-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd83e-124">Type</span></span> | <span data-ttu-id="bd83e-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd83e-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="bd83e-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="bd83e-126">Authorization</span></span>  | <span data-ttu-id="bd83e-127">string</span><span class="sxs-lookup"><span data-stu-id="bd83e-127">string</span></span>  | <span data-ttu-id="bd83e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd83e-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bd83e-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bd83e-130">Request body</span></span>
<span data-ttu-id="bd83e-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bd83e-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bd83e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd83e-132">Response</span></span>

<span data-ttu-id="bd83e-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [organization](../resources/organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd83e-133">If successful, this method returns a `200 OK` response code and collection of [organization](../resources/organization.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="bd83e-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd83e-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bd83e-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd83e-135">Request</span></span>
<span data-ttu-id="bd83e-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd83e-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_organization"
}-->
```http
GET https://graph.microsoft.com/beta/organization
```
##### <a name="response"></a><span data-ttu-id="bd83e-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd83e-137">Response</span></span>
<span data-ttu-id="bd83e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd83e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.organization",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 500

{
  "value": [
    {
      "assignedPlans": [
        {
          "assignedDateTime": "2016-10-19T10:37:00Z",
          "capabilityStatus": "capabilityStatus-value",
          "service": "service-value",
          "servicePlanId": "servicePlanId-value"
        }
      ],
      "businessPhones": [
        "businessPhones-value"
      ],
      "city": "city-value",
      "country": "country-value",
      "countryLetterCode": "countryLetterCode-value",
      "displayName": "displayName-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List organization",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->