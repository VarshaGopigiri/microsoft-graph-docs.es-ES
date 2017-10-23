# <a name="create-device"></a><span data-ttu-id="bc1da-101">Create device</span><span class="sxs-lookup"><span data-stu-id="bc1da-101">Create device</span></span>

<span data-ttu-id="bc1da-102">Crea y registra un nuevo dispositivo en la organización.</span><span class="sxs-lookup"><span data-stu-id="bc1da-102">Create and register a new device in the organization.</span></span>

## <a name="permissions"></a><span data-ttu-id="bc1da-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="bc1da-103">Permissions</span></span>
<span data-ttu-id="bc1da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bc1da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="bc1da-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc1da-106">Permission type</span></span>      | <span data-ttu-id="bc1da-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc1da-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bc1da-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc1da-108">Delegated (work or school account)</span></span> | <span data-ttu-id="bc1da-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="bc1da-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="bc1da-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc1da-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bc1da-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc1da-111">Not supported.</span></span>    |
|<span data-ttu-id="bc1da-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc1da-112">Application</span></span> | <span data-ttu-id="bc1da-113">Device.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bc1da-113">Device.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bc1da-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc1da-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /devices

```
## <a name="request-headers"></a><span data-ttu-id="bc1da-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc1da-115">Request headers</span></span>
| <span data-ttu-id="bc1da-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc1da-116">Name</span></span>       | <span data-ttu-id="bc1da-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc1da-117">Type</span></span> | <span data-ttu-id="bc1da-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc1da-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bc1da-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc1da-119">Authorization</span></span>  | <span data-ttu-id="bc1da-120">string</span><span class="sxs-lookup"><span data-stu-id="bc1da-120">string</span></span>  | <span data-ttu-id="bc1da-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc1da-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bc1da-123">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="bc1da-123">Content-type</span></span> | <span data-ttu-id="bc1da-124">string</span><span class="sxs-lookup"><span data-stu-id="bc1da-124">string</span></span> | <span data-ttu-id="bc1da-125">application/json</span><span class="sxs-lookup"><span data-stu-id="bc1da-125">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="bc1da-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc1da-126">Request body</span></span>
<span data-ttu-id="bc1da-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="bc1da-127">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="bc1da-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc1da-128">Response</span></span>

<span data-ttu-id="bc1da-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [device](../resources/device.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc1da-129">If successful, this method returns `201 Created` response code and [device](../resources/device.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc1da-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc1da-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="bc1da-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc1da-131">Request</span></span>
<span data-ttu-id="bc1da-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc1da-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_device_from_devices"
}-->
```http
POST https://graph.microsoft.com/v1.0/devices
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type":2,
      "key":"Y3YxN2E1MWFlYw=="
    }
  ],
  "deviceId":"4c299165-6e8f-4b45-a5ba-c5d250a707ff",
  "displayName":"Test device",
  "operatingSystem":"linux",
  "operatingSystemVersion":"1"
}
```
<span data-ttu-id="bc1da-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [device](../resources/device.md).</span><span class="sxs-lookup"><span data-stu-id="bc1da-133">In the request body, supply a JSON representation of [device](../resources/device.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="bc1da-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc1da-134">Response</span></span>
<span data-ttu-id="bc1da-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc1da-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "accountEnabled":false,
  "alternativeSecurityIds":
  [
    {
      "type":2,
      "key":"Y3YxN2E1MWFlYw=="
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
  "description": "Create device",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
