# <a name="create-user"></a><span data-ttu-id="068df-101">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="068df-101">Create user</span></span>

> <span data-ttu-id="068df-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="068df-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="068df-103">Cree un objeto [user](../resources/intune_shared_user.md).</span><span class="sxs-lookup"><span data-stu-id="068df-103">Create a new [user](../resources/intune_shared_user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="068df-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="068df-104">Prerequisites</span></span>
<span data-ttu-id="068df-105">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="068df-105">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="068df-106">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="068df-106">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>  <span data-ttu-id="068df-107">Los permisos específicos necesarios depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="068df-107">The specific permission required depends on the context.</span></span>

|<span data-ttu-id="068df-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="068df-108">Permission type</span></span>|<span data-ttu-id="068df-109">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="068df-109">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="068df-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="068df-110">Delegated (work or school account)</span></span>| <span data-ttu-id="068df-111">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="068df-111">_varies by context_</span></span> |
| <span data-ttu-id="068df-112">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="068df-112">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="068df-113">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="068df-113">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="068df-114">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="068df-114">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="068df-115">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="068df-115">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="068df-116">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="068df-116">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="068df-117">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="068df-117">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="068df-118">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="068df-118">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="068df-119">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="068df-119">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="068df-120">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="068df-120">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="068df-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="068df-121">Not supported.</span></span>|
|<span data-ttu-id="068df-122">Aplicación</span><span class="sxs-lookup"><span data-stu-id="068df-122">Application</span></span>|<span data-ttu-id="068df-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="068df-123">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="068df-124">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="068df-124">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users
```

## <a name="request-headers"></a><span data-ttu-id="068df-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="068df-125">Request headers</span></span>
|<span data-ttu-id="068df-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="068df-126">Header</span></span>|<span data-ttu-id="068df-127">Valor</span><span class="sxs-lookup"><span data-stu-id="068df-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="068df-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="068df-128">Authorization</span></span>|<span data-ttu-id="068df-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="068df-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="068df-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="068df-130">Accept</span></span>|<span data-ttu-id="068df-131">application/json</span><span class="sxs-lookup"><span data-stu-id="068df-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="068df-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="068df-132">Request body</span></span>
<span data-ttu-id="068df-133">En el cuerpo de la solicitud, especifique una representación JSON del objeto user.</span><span class="sxs-lookup"><span data-stu-id="068df-133">In the request body, supply a JSON representation for the user object.</span></span>

<span data-ttu-id="068df-134">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto user.</span><span class="sxs-lookup"><span data-stu-id="068df-134">The following table shows the properties that are required when you create the user.</span></span>

|<span data-ttu-id="068df-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="068df-135">Property</span></span>|<span data-ttu-id="068df-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="068df-136">Type</span></span>|<span data-ttu-id="068df-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="068df-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="068df-138">id</span><span class="sxs-lookup"><span data-stu-id="068df-138">id</span></span>|<span data-ttu-id="068df-139">String</span><span class="sxs-lookup"><span data-stu-id="068df-139">String</span></span>|<span data-ttu-id="068df-140">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="068df-140">Unique identifier of the user.</span></span>|
|<span data-ttu-id="068df-141">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="068df-141">**Onboarding**</span></span>|
|<span data-ttu-id="068df-142">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="068df-142">deviceEnrollmentLimit</span></span>|<span data-ttu-id="068df-143">Int32</span><span class="sxs-lookup"><span data-stu-id="068df-143">Int32</span></span>|<span data-ttu-id="068df-144">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="068df-144">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="068df-145">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="068df-145">Allowed values are 5 or 1000.</span></span>|

<span data-ttu-id="068df-146">Compatibilidad con propiedades de cuerpo de solicitud varía según el contexto.</span><span class="sxs-lookup"><span data-stu-id="068df-146">Request body property support varies according to context.</span></span>

## <a name="response"></a><span data-ttu-id="068df-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="068df-147">Response</span></span>
<span data-ttu-id="068df-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [user](../resources/intune_shared_user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="068df-148">If successful, this method returns a `201 Created` response code and a [user](../resources/intune_shared_user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="068df-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="068df-149">Example</span></span>

### <a name="request"></a><span data-ttu-id="068df-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="068df-150">Request</span></span>
<span data-ttu-id="068df-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="068df-151">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/v1.0/users
Content-type: application/json
Content-length: 46

{
  "@odata.type": "#microsoft.graph.user"
}
```

### <a name="response"></a><span data-ttu-id="068df-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="068df-152">Response</span></span>
<span data-ttu-id="068df-153">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="068df-153">Here is an example of the response.</span></span> <span data-ttu-id="068df-154">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="068df-154">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="068df-155">Las propiedades que devuelve una llamada real varían según el contexto.</span><span class="sxs-lookup"><span data-stu-id="068df-155">Properties returned from an actual call vary according to context.</span></span>

``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



