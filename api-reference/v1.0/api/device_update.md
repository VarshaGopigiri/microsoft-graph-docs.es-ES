# <a name="update-device"></a><span data-ttu-id="34cb3-101">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="34cb3-101">Update device</span></span>

<span data-ttu-id="34cb3-102">Actualiza las propiedades de un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="34cb3-102">Update the properties of a registered device.</span></span>

<span data-ttu-id="34cb3-103">Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).</span><span class="sxs-lookup"><span data-stu-id="34cb3-103">Only certain properties of a device can be updated through approved Mobile Device Managment (MDM) apps.</span></span>

## <a name="permissions"></a><span data-ttu-id="34cb3-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="34cb3-104">Permissions</span></span>
<span data-ttu-id="34cb3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="34cb3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="34cb3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34cb3-107">Permission type</span></span>      | <span data-ttu-id="34cb3-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34cb3-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34cb3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34cb3-109">Delegated (work or school account)</span></span> | <span data-ttu-id="34cb3-110">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="34cb3-110">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="34cb3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34cb3-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="34cb3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34cb3-112">Not supported.</span></span> |
|<span data-ttu-id="34cb3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34cb3-113">Application</span></span> | <span data-ttu-id="34cb3-114">No se admite</span><span class="sxs-lookup"><span data-stu-id="34cb3-114">Not supported</span></span> |

## <a name="http-request"></a><span data-ttu-id="34cb3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34cb3-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```
> <span data-ttu-id="34cb3-116">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="34cb3-116">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="34cb3-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34cb3-117">Request headers</span></span>
| <span data-ttu-id="34cb3-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="34cb3-118">Name</span></span>       | <span data-ttu-id="34cb3-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="34cb3-119">Type</span></span> | <span data-ttu-id="34cb3-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="34cb3-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="34cb3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="34cb3-121">Authorization</span></span>  | <span data-ttu-id="34cb3-122">string</span><span class="sxs-lookup"><span data-stu-id="34cb3-122">string</span></span>  | <span data-ttu-id="34cb3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34cb3-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="34cb3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34cb3-125">Request body</span></span>

<span data-ttu-id="34cb3-126">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="34cb3-126">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span> <span data-ttu-id="34cb3-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="34cb3-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="34cb3-128">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="34cb3-128">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="34cb3-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34cb3-129">Property</span></span>     | <span data-ttu-id="34cb3-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="34cb3-130">Type</span></span>   |<span data-ttu-id="34cb3-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="34cb3-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34cb3-132">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="34cb3-132">accountEnabled</span></span>|<span data-ttu-id="34cb3-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="34cb3-133">Boolean</span></span>| <span data-ttu-id="34cb3-134">**true** si la cuenta está habilitada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="34cb3-134">true if the account is enabled; otherwise, false.</span></span> |
|<span data-ttu-id="34cb3-135">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="34cb3-135">operatingSystem</span></span>|<span data-ttu-id="34cb3-136">String</span><span class="sxs-lookup"><span data-stu-id="34cb3-136">String</span></span>|<span data-ttu-id="34cb3-137">Tipo de sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34cb3-137">The type of operating system on the device. Required.</span></span>|
|<span data-ttu-id="34cb3-138">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="34cb3-138">operatingSystemVersion</span></span>|<span data-ttu-id="34cb3-139">String</span><span class="sxs-lookup"><span data-stu-id="34cb3-139">String</span></span>|<span data-ttu-id="34cb3-140">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34cb3-140">The version of the operating system on the device. Required.</span></span>|
|<span data-ttu-id="34cb3-141">displayName</span><span class="sxs-lookup"><span data-stu-id="34cb3-141">displayName</span></span>|<span data-ttu-id="34cb3-142">String</span><span class="sxs-lookup"><span data-stu-id="34cb3-142">String</span></span>|<span data-ttu-id="34cb3-143">Nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34cb3-143">The display name for the device. Required.</span></span>|
|<span data-ttu-id="34cb3-144">isCompliant</span><span class="sxs-lookup"><span data-stu-id="34cb3-144">isCompliant</span></span>|<span data-ttu-id="34cb3-145">Boolean</span><span class="sxs-lookup"><span data-stu-id="34cb3-145">Boolean</span></span>|<span data-ttu-id="34cb3-146">**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="34cb3-146">**true** if the device complies with Mobile Device Management (MDM) policies; otherwise, **false**.</span></span> <span data-ttu-id="34cb3-147">Solo lo puede actualizar una aplicación MDM aprobada.</span><span class="sxs-lookup"><span data-stu-id="34cb3-147">This can only be updated by an approved MDM app.</span></span> |
|<span data-ttu-id="34cb3-148">isManaged</span><span class="sxs-lookup"><span data-stu-id="34cb3-148">isManaged</span></span>|<span data-ttu-id="34cb3-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="34cb3-149">Boolean</span></span>|<span data-ttu-id="34cb3-150">**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="34cb3-150">**true** if the device is managed by a Mobile Device Management (MDM) app such as Intune; otherwise, **false**.</span></span> <span data-ttu-id="34cb3-151">Solo lo puede actualizar una aplicación MDM aprobada.</span><span class="sxs-lookup"><span data-stu-id="34cb3-151">This can only be updated by an approved MDM app.</span></span> |

## <a name="response"></a><span data-ttu-id="34cb3-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34cb3-152">Response</span></span>

<span data-ttu-id="34cb3-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="34cb3-153">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="34cb3-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34cb3-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="34cb3-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34cb3-155">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "update_device"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/devices/{id}
Content-type: application/json
Content-length: 31

{
  "accountEnabled": false
}
```
##### <a name="response"></a><span data-ttu-id="34cb3-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34cb3-156">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```
