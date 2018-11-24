# <a name="get-device"></a><span data-ttu-id="cc626-101">Obtener device</span><span class="sxs-lookup"><span data-stu-id="cc626-101">Get device</span></span>

<span data-ttu-id="cc626-102">Obtiene las propiedades y relaciones de un objeto device.</span><span class="sxs-lookup"><span data-stu-id="cc626-102">Get the properties and relationships of a device object.</span></span>
## <a name="permissions"></a><span data-ttu-id="cc626-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="cc626-103">Permissions</span></span>
<span data-ttu-id="cc626-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cc626-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="cc626-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc626-106">Permission type</span></span>      | <span data-ttu-id="cc626-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc626-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc626-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc626-108">Delegated (work or school account)</span></span> | <span data-ttu-id="cc626-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="cc626-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="cc626-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc626-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc626-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc626-111">Not supported.</span></span>    |
|<span data-ttu-id="cc626-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc626-112">Application</span></span> | <span data-ttu-id="cc626-113">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc626-113">Device.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc626-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc626-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /devices/{id}
```
> <span data-ttu-id="cc626-115">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="cc626-115">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="cc626-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cc626-116">Optional query parameters</span></span>
<span data-ttu-id="cc626-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc626-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cc626-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc626-118">Request headers</span></span>
| <span data-ttu-id="cc626-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc626-119">Name</span></span>       | <span data-ttu-id="cc626-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc626-120">Type</span></span> | <span data-ttu-id="cc626-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc626-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="cc626-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc626-122">Authorization</span></span>  | <span data-ttu-id="cc626-123">string</span><span class="sxs-lookup"><span data-stu-id="cc626-123">string</span></span>  | <span data-ttu-id="cc626-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc626-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cc626-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc626-126">Request body</span></span>
<span data-ttu-id="cc626-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cc626-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cc626-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc626-128">Response</span></span>

<span data-ttu-id="cc626-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc626-129">If successful, this method returns a `200 OK` response code and [device](../resources/device.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="cc626-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc626-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cc626-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc626-131">Request</span></span>
<span data-ttu-id="cc626-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc626-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_device"
}-->
```http
GET https://graph.microsoft.com/v1.0/devices/{id}
```
##### <a name="response"></a><span data-ttu-id="cc626-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc626-133">Response</span></span>
<span data-ttu-id="cc626-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc626-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
