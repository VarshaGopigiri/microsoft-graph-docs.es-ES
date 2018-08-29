# <a name="wipe-action"></a><span data-ttu-id="19282-101">Acción wipe</span><span class="sxs-lookup"><span data-stu-id="19282-101">wipe action</span></span>

> <span data-ttu-id="19282-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="19282-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="19282-103">Eliminar los datos de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="19282-103">Wipe a device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="19282-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="19282-104">Prerequisites</span></span>
<span data-ttu-id="19282-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="19282-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="19282-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19282-107">Permission type</span></span>|<span data-ttu-id="19282-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19282-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="19282-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19282-109">Delegated (work or school account)</span></span>|<span data-ttu-id="19282-110">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="19282-110">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="19282-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19282-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="19282-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19282-112">Not supported.</span></span>|
|<span data-ttu-id="19282-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19282-113">Application</span></span>|<span data-ttu-id="19282-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="19282-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="19282-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19282-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/wipe
POST /deviceManagement/managedDevices/{managedDeviceId}/wipe
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/wipe
```

## <a name="request-headers"></a><span data-ttu-id="19282-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19282-116">Request headers</span></span>
|<span data-ttu-id="19282-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19282-117">Header</span></span>|<span data-ttu-id="19282-118">Valor</span><span class="sxs-lookup"><span data-stu-id="19282-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="19282-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="19282-119">Authorization</span></span>|<span data-ttu-id="19282-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="19282-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="19282-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="19282-121">Accept</span></span>|<span data-ttu-id="19282-122">application/json</span><span class="sxs-lookup"><span data-stu-id="19282-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="19282-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19282-123">Request body</span></span>
<span data-ttu-id="19282-124">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="19282-124">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="19282-125">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="19282-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="19282-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="19282-126">Property</span></span>|<span data-ttu-id="19282-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="19282-127">Type</span></span>|<span data-ttu-id="19282-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="19282-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="19282-129">keepEnrollmentData</span><span class="sxs-lookup"><span data-stu-id="19282-129">keepEnrollmentData</span></span>|<span data-ttu-id="19282-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="19282-130">Boolean</span></span>|<span data-ttu-id="19282-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="19282-131">Not yet documented</span></span>|
|<span data-ttu-id="19282-132">keepUserData</span><span class="sxs-lookup"><span data-stu-id="19282-132">keepUserData</span></span>|<span data-ttu-id="19282-133">Boolean</span><span class="sxs-lookup"><span data-stu-id="19282-133">Boolean</span></span>|<span data-ttu-id="19282-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="19282-134">Not yet documented</span></span>|
|<span data-ttu-id="19282-135">macOsUnlockCode</span><span class="sxs-lookup"><span data-stu-id="19282-135">macOsUnlockCode</span></span>|<span data-ttu-id="19282-136">String</span><span class="sxs-lookup"><span data-stu-id="19282-136">String</span></span>|<span data-ttu-id="19282-137">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="19282-137">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="19282-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19282-138">Response</span></span>
<span data-ttu-id="19282-139">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="19282-139">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="19282-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19282-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="19282-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="19282-141">Request</span></span>
<span data-ttu-id="19282-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="19282-142">Here is an example of the request.</span></span>

<!-- { "blockType": "request" } -->
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/wipe
Content-type: application/json

{
  "keepEnrollmentData": true,
  "keepUserData": true,
  "macOsUnlockCode": "Mac Os Unlock Code value"
}
```

### <a name="response"></a><span data-ttu-id="19282-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19282-143">Response</span></span>
<span data-ttu-id="19282-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="19282-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- { "blockType": "response" } -->
``` http
HTTP/1.1 204 No Content
```



