# <a name="list-acceptedsenders"></a><span data-ttu-id="0e354-101">List acceptedSenders</span><span class="sxs-lookup"><span data-stu-id="0e354-101">List acceptedSenders</span></span>
<span data-ttu-id="0e354-102">Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.</span><span class="sxs-lookup"><span data-stu-id="0e354-102">Get a list of users or groups that are in the acceptedSenders list for this group.</span></span>

<span data-ttu-id="0e354-p101">Los usuarios de la lista de remitentes aceptados pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud GET). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes aceptados y de remitentes rechazados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="0e354-p101">Users in the accepted senders list can post to conversations of the group (identified in the GET request URL). Make sure you do not specify the same user or group in the accepted senders and rejected senders lists, otherwise you will get an error.</span></span>

## <a name="permissions"></a><span data-ttu-id="0e354-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0e354-105">Permissions</span></span>
<span data-ttu-id="0e354-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0e354-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0e354-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e354-108">Permission type</span></span>      | <span data-ttu-id="0e354-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e354-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0e354-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e354-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0e354-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e354-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="0e354-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e354-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0e354-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e354-113">Not supported.</span></span>    |
|<span data-ttu-id="0e354-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e354-114">Application</span></span> | <span data-ttu-id="0e354-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e354-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0e354-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e354-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/acceptedSenders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="0e354-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0e354-117">Optional query parameters</span></span>
<span data-ttu-id="0e354-118">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e354-118">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0e354-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e354-119">Request headers</span></span>
| <span data-ttu-id="0e354-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e354-120">Header</span></span>       | <span data-ttu-id="0e354-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0e354-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0e354-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e354-122">Authorization</span></span>  | <span data-ttu-id="0e354-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0e354-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0e354-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e354-125">Request body</span></span>
<span data-ttu-id="0e354-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0e354-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0e354-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e354-127">Response</span></span>
<span data-ttu-id="0e354-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e354-128">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e354-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e354-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="0e354-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e354-130">Request</span></span>
<span data-ttu-id="0e354-131">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e354-131">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_acceptedsenders"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders
```

#### <a name="response"></a><span data-ttu-id="0e354-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e354-132">Response</span></span>
<span data-ttu-id="0e354-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e354-133">Here is an example of the response.</span></span>
><span data-ttu-id="0e354-134">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="0e354-134">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="0e354-135">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e354-135">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List acceptedSenders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->