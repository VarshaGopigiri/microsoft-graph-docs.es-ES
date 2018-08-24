# <a name="update-device"></a><span data-ttu-id="84231-101">Actualizar device</span><span class="sxs-lookup"><span data-stu-id="84231-101">Update device</span></span>

<span data-ttu-id="84231-102">Actualiza las propiedades de un dispositivo registrado.</span><span class="sxs-lookup"><span data-stu-id="84231-102">Update the properties of a registered device.</span></span>

<span data-ttu-id="84231-103">Solo algunas propiedades de un dispositivo pueden actualizarse a través de aplicaciones aprobadas de administración de dispositivos móviles (MDM).</span><span class="sxs-lookup"><span data-stu-id="84231-103">Only certain properties of a device can be updated through approved Mobile Device Managment (MDM) apps.</span></span>

## <a name="permissions"></a><span data-ttu-id="84231-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="84231-104">Permissions</span></span>
<span data-ttu-id="84231-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="84231-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="84231-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="84231-107">Permission type</span></span>      | <span data-ttu-id="84231-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="84231-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="84231-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="84231-109">Delegated (work or school account)</span></span> | <span data-ttu-id="84231-110">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="84231-110">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="84231-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="84231-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="84231-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="84231-112">Not supported.</span></span> |
|<span data-ttu-id="84231-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="84231-113">Application</span></span> | <span data-ttu-id="84231-114">No se admite</span><span class="sxs-lookup"><span data-stu-id="84231-114">Not supported</span></span> |

## <a name="http-request"></a><span data-ttu-id="84231-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="84231-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /devices/{id}
```
> <span data-ttu-id="84231-116">Nota: El "id" de la solicitud es la propiedad "id" del dispositivo, no la propiedad "deviceId".</span><span class="sxs-lookup"><span data-stu-id="84231-116">Note: The "id" in the request is the "id" property of the device, not the "deviceId" property.</span></span>

## <a name="request-headers"></a><span data-ttu-id="84231-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="84231-117">Request headers</span></span>
| <span data-ttu-id="84231-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="84231-118">Name</span></span>       | <span data-ttu-id="84231-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="84231-119">Type</span></span> | <span data-ttu-id="84231-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="84231-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="84231-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="84231-121">Authorization</span></span>  | <span data-ttu-id="84231-122">cadena</span><span class="sxs-lookup"><span data-stu-id="84231-122">string</span></span>  | <span data-ttu-id="84231-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="84231-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="84231-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="84231-125">Request body</span></span>

<span data-ttu-id="84231-126">En el cuerpo de la solicitud, proporcione los valores de las propiedades [device](../resources/device.md) que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="84231-126">In the request body, supply the values for the [device](../resources/device.md) properties that should be updated.</span></span> <span data-ttu-id="84231-127">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="84231-127">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="84231-128">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="84231-128">For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="84231-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84231-129">Property</span></span>     | <span data-ttu-id="84231-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="84231-130">Type</span></span>   |<span data-ttu-id="84231-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="84231-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="84231-132">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="84231-132">accountEnabled</span></span>|<span data-ttu-id="84231-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="84231-133">Boolean</span></span>| <span data-ttu-id="84231-134">**true** si la cuenta está habilitada; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="84231-134">**true** if the account is enabled; otherwise, **false**.</span></span> |
|<span data-ttu-id="84231-135">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="84231-135">operatingSystem</span></span>|<span data-ttu-id="84231-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="84231-136">String</span></span>|<span data-ttu-id="84231-137">Tipo de sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84231-137">The type of operating system on the device.</span></span>|
|<span data-ttu-id="84231-138">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="84231-138">operatingSystemVersion</span></span>|<span data-ttu-id="84231-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="84231-139">String</span></span>|<span data-ttu-id="84231-140">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84231-140">The version of the operating system on the device</span></span>|
|<span data-ttu-id="84231-141">displayName</span><span class="sxs-lookup"><span data-stu-id="84231-141">displayName</span></span>|<span data-ttu-id="84231-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="84231-142">String</span></span>|<span data-ttu-id="84231-143">Nombre para mostrar del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="84231-143">The display name for the device.</span></span>|
|<span data-ttu-id="84231-144">isCompliant</span><span class="sxs-lookup"><span data-stu-id="84231-144">isCompliant</span></span>|<span data-ttu-id="84231-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="84231-145">Boolean</span></span>|<span data-ttu-id="84231-146">**true** si el dispositivo cumple con las directivas de administración de dispositivos móviles (MDM); en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="84231-146">**true** if the device complies with Mobile Device Management (MDM) policies; otherwise, **false**.</span></span> <span data-ttu-id="84231-147">Esto solo lo puede actualizar Intune para cualquier tipo de sistema operativo del dispositivo o por una [aplicación MDM aprobada](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="84231-147">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |
|<span data-ttu-id="84231-148">isManaged</span><span class="sxs-lookup"><span data-stu-id="84231-148">isManaged</span></span>|<span data-ttu-id="84231-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="84231-149">Boolean</span></span>|<span data-ttu-id="84231-150">**true** si una aplicación de administración de dispositivos móviles (MDM) administra el dispositivo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="84231-150">**true** if the device is managed by a Mobile Device Management (MDM) app; otherwise, **false**.</span></span> <span data-ttu-id="84231-151">Esto solo lo puede actualizar Intune para cualquier tipo de sistema operativo del dispositivo o por una [aplicación MDM aprobada](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) para dispositivos de sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="84231-151">This can only be updated by Intune for any device OS type or by an [approved MDM app](https://docs.microsoft.com/windows/client-management/mdm/azure-active-directory-integration-with-mdm) for Windows OS devices.</span></span> |

## <a name="response"></a><span data-ttu-id="84231-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84231-152">Response</span></span>

<span data-ttu-id="84231-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="84231-153">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="84231-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84231-154">Example</span></span>
##### <a name="request"></a><span data-ttu-id="84231-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="84231-155">Request</span></span>

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
##### <a name="response"></a><span data-ttu-id="84231-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="84231-156">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.device"
} -->
```http
HTTP/1.1 204 No Content
```
