# <a name="get-device"></a><span data-ttu-id="0a107-101">Obtener device</span><span class="sxs-lookup"><span data-stu-id="0a107-101">Get device</span></span>

<span data-ttu-id="0a107-102">Obtiene las propiedades y relaciones de un objeto device.</span><span class="sxs-lookup"><span data-stu-id="0a107-102">Get the properties and relationships of a device object.</span></span>
## <a name="permissions"></a><span data-ttu-id="0a107-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="0a107-103">Permissions</span></span>
<span data-ttu-id="0a107-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0a107-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="0a107-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0a107-106">Permission type</span></span>      | <span data-ttu-id="0a107-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0a107-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="0a107-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0a107-108">Delegated (work or school account)</span></span> | <span data-ttu-id="0a107-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="0a107-109">One of the following scopes is required to execute this API: Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="0a107-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0a107-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0a107-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0a107-111">Not supported.</span></span>    | 
|<span data-ttu-id="0a107-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0a107-112">Application</span></span> | <span data-ttu-id="0a107-113">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0a107-113">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="0a107-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0a107-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}
```
> <span data-ttu-id="0a107-115">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="0a107-115">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="0a107-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0a107-116">Optional query parameters</span></span>
<span data-ttu-id="0a107-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a107-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0a107-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0a107-118">Request headers</span></span>
| <span data-ttu-id="0a107-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="0a107-119">Name</span></span>       | <span data-ttu-id="0a107-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a107-120">Type</span></span> | <span data-ttu-id="0a107-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a107-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="0a107-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a107-122">Authorization</span></span>  | <span data-ttu-id="0a107-123">string</span><span class="sxs-lookup"><span data-stu-id="0a107-123">string</span></span>  | <span data-ttu-id="0a107-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a107-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0a107-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0a107-126">Request body</span></span>
<span data-ttu-id="0a107-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0a107-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0a107-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a107-128">Response</span></span>

<span data-ttu-id="0a107-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0a107-129">If successful, this method returns a `200 OK` response code and [device](../resources/device.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0a107-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a107-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0a107-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0a107-131">Request</span></span>
<span data-ttu-id="0a107-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0a107-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_device"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="0a107-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0a107-133">Response</span></span>
<span data-ttu-id="0a107-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0a107-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type": 2,
      "key":"Y3YxN2E1MWFlYw==",
      "identityProvider": null
    }
  ],
  "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
  "displayName":"Test device",
  "id": "id-value",
  "operatingSystem":"linux",
  "operatingSystemVersion":"1"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
