# <a name="logoutsharedappledeviceactiveuser-action"></a><span data-ttu-id="89641-101">Acción logoutSharedAppleDeviceActiveUser</span><span class="sxs-lookup"><span data-stu-id="89641-101">logoutSharedAppleDeviceActiveUser action</span></span>

> <span data-ttu-id="89641-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="89641-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="89641-103">Cerrar la sesión del usuario activo del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="89641-103">Logout shared Apple device active user</span></span>
## <a name="prerequisites"></a><span data-ttu-id="89641-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="89641-104">Prerequisites</span></span>
<span data-ttu-id="89641-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="89641-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="89641-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89641-107">Permission type</span></span>|<span data-ttu-id="89641-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89641-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="89641-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89641-109">Delegated (work or school account)</span></span>|<span data-ttu-id="89641-110">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="89641-110">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="89641-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89641-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="89641-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89641-112">Not supported.</span></span>|
|<span data-ttu-id="89641-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89641-113">Application</span></span>|<span data-ttu-id="89641-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89641-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="89641-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89641-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
POST /deviceManagement/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
```

## <a name="request-headers"></a><span data-ttu-id="89641-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89641-116">Request headers</span></span>
|<span data-ttu-id="89641-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89641-117">Header</span></span>|<span data-ttu-id="89641-118">Valor</span><span class="sxs-lookup"><span data-stu-id="89641-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="89641-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="89641-119">Authorization</span></span>|<span data-ttu-id="89641-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="89641-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="89641-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="89641-121">Accept</span></span>|<span data-ttu-id="89641-122">application/json</span><span class="sxs-lookup"><span data-stu-id="89641-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="89641-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89641-123">Request body</span></span>
<span data-ttu-id="89641-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="89641-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="89641-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89641-125">Response</span></span>
<span data-ttu-id="89641-126">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="89641-126">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="89641-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89641-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="89641-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89641-128">Request</span></span>
<span data-ttu-id="89641-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89641-129">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
```

### <a name="response"></a><span data-ttu-id="89641-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89641-130">Response</span></span>
<span data-ttu-id="89641-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="89641-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



