# <a name="list-devices"></a><span data-ttu-id="368d0-101">List devices</span><span class="sxs-lookup"><span data-stu-id="368d0-101">List devices</span></span>

<span data-ttu-id="368d0-102">Recupera una lista de objetos de dispositivo registrados en la organización.</span><span class="sxs-lookup"><span data-stu-id="368d0-102">Retrieve a list of device objects registered in the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="368d0-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="368d0-103">Permissions</span></span>
<span data-ttu-id="368d0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="368d0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="368d0-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="368d0-106">Permission type</span></span>      | <span data-ttu-id="368d0-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="368d0-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="368d0-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="368d0-108">Delegated (work or school account)</span></span> | <span data-ttu-id="368d0-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="368d0-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="368d0-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="368d0-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="368d0-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="368d0-111">Not supported.</span></span>    |
|<span data-ttu-id="368d0-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="368d0-112">Application</span></span> | <span data-ttu-id="368d0-113">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="368d0-113">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="368d0-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="368d0-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices
```
## <a name="optional-query-parameters"></a><span data-ttu-id="368d0-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="368d0-115">Optional query parameters</span></span>
<span data-ttu-id="368d0-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="368d0-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="368d0-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="368d0-117">Request headers</span></span>
| <span data-ttu-id="368d0-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="368d0-118">Name</span></span>       | <span data-ttu-id="368d0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="368d0-119">Type</span></span> | <span data-ttu-id="368d0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="368d0-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="368d0-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="368d0-121">Authorization</span></span>  | <span data-ttu-id="368d0-122">string</span><span class="sxs-lookup"><span data-stu-id="368d0-122">string</span></span>  | <span data-ttu-id="368d0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="368d0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="368d0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="368d0-125">Request body</span></span>
<span data-ttu-id="368d0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="368d0-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="368d0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="368d0-127">Response</span></span>

<span data-ttu-id="368d0-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="368d0-128">If successful, this method returns a `200 OK` response code and collection of [device](../resources/device.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="368d0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="368d0-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="368d0-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="368d0-130">Request</span></span>
<span data-ttu-id="368d0-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="368d0-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_devices"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices
```

##### <a name="response"></a><span data-ttu-id="368d0-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="368d0-132">Response</span></span>
<span data-ttu-id="368d0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="368d0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "accountEnabled":false,
      "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
      "displayName":"Test device",
      "id": "id-value",
      "operatingSystem":"linux",
      "operatingSystemVersion":"1"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List devices",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
