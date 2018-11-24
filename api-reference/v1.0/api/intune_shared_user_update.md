# <a name="update-user"></a><span data-ttu-id="e0b5d-101">Actualizar usuario</span><span class="sxs-lookup"><span data-stu-id="e0b5d-101">Update user</span></span>

> <span data-ttu-id="e0b5d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e0b5d-103">Actualice las propiedades de un objeto [user](../resources/intune_shared_user.md).</span><span class="sxs-lookup"><span data-stu-id="e0b5d-103">Update the properties of a [user](../resources/intune_shared_user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e0b5d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e0b5d-104">Prerequisites</span></span>
<span data-ttu-id="e0b5d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e0b5d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e0b5d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e0b5d-107">Permission type</span></span>|<span data-ttu-id="e0b5d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e0b5d-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e0b5d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e0b5d-109">Delegated (work or school account)</span></span>| <span data-ttu-id="e0b5d-110">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="e0b5d-110">_varies by context_</span></span>|
| <span data-ttu-id="e0b5d-111">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="e0b5d-111">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="e0b5d-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0b5d-112">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="e0b5d-113">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="e0b5d-113">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="e0b5d-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0b5d-114">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="e0b5d-115">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="e0b5d-115">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="e0b5d-116">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0b5d-116">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="e0b5d-117">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="e0b5d-117">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="e0b5d-118">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0b5d-118">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="e0b5d-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e0b5d-119">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e0b5d-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-120">Not supported.</span></span>|
|<span data-ttu-id="e0b5d-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e0b5d-121">Application</span></span>|<span data-ttu-id="e0b5d-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-122">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e0b5d-123">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e0b5d-123">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="e0b5d-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0b5d-124">Request headers</span></span>
|<span data-ttu-id="e0b5d-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0b5d-125">Header</span></span>|<span data-ttu-id="e0b5d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e0b5d-126">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e0b5d-127">Authorization</span><span class="sxs-lookup"><span data-stu-id="e0b5d-127">Authorization</span></span>|<span data-ttu-id="e0b5d-128">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-128">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e0b5d-129">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e0b5d-129">Accept</span></span>|<span data-ttu-id="e0b5d-130">application/json</span><span class="sxs-lookup"><span data-stu-id="e0b5d-130">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e0b5d-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e0b5d-131">Request body</span></span>
<span data-ttu-id="e0b5d-132">En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune_shared_user.md).</span><span class="sxs-lookup"><span data-stu-id="e0b5d-132">In the request body, supply a JSON representation for the [user](../resources/intune_shared_user.md) object.</span></span>

<span data-ttu-id="e0b5d-133">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune_shared_user.md).</span><span class="sxs-lookup"><span data-stu-id="e0b5d-133">The following table shows the properties that are required when you create the [user](../resources/intune_shared_user.md).</span></span>

|<span data-ttu-id="e0b5d-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0b5d-134">Property</span></span>|<span data-ttu-id="e0b5d-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0b5d-135">Type</span></span>|<span data-ttu-id="e0b5d-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0b5d-136">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e0b5d-137">id</span><span class="sxs-lookup"><span data-stu-id="e0b5d-137">id</span></span>|<span data-ttu-id="e0b5d-138">String</span><span class="sxs-lookup"><span data-stu-id="e0b5d-138">String</span></span>|<span data-ttu-id="e0b5d-139">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-139">Unique identifier of the user.</span></span>|
|<span data-ttu-id="e0b5d-140">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="e0b5d-140">**Onboarding**</span></span>|
|<span data-ttu-id="e0b5d-141">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="e0b5d-141">deviceEnrollmentLimit</span></span>|<span data-ttu-id="e0b5d-142">Int32</span><span class="sxs-lookup"><span data-stu-id="e0b5d-142">Int32</span></span>|<span data-ttu-id="e0b5d-143">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-143">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="e0b5d-144">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-144">Allowed values are 5 or 1000.</span></span>|

## <a name="response"></a><span data-ttu-id="e0b5d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0b5d-145">Response</span></span>
<span data-ttu-id="e0b5d-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune_shared_user.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-146">If successful, this method returns a `200 OK` response code and an updated [user](../resources/intune_shared_user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e0b5d-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0b5d-147">Example</span></span>

### <a name="request"></a><span data-ttu-id="e0b5d-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e0b5d-148">Request</span></span>
<span data-ttu-id="e0b5d-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-149">Here is an example of the request.</span></span>

``` http
PATCH https://graph.microsoft.com/v1.0/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="e0b5d-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0b5d-150">Response</span></span>
<span data-ttu-id="e0b5d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e0b5d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



