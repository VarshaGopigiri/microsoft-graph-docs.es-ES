# <a name="list-managedappregistrations"></a><span data-ttu-id="b2de6-101">Enumerar managedAppRegistrations</span><span class="sxs-lookup"><span data-stu-id="b2de6-101">List managedAppRegistrations</span></span>

> <span data-ttu-id="b2de6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2de6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2de6-103">Enumere las propiedades y las relaciones de los objetos [managedAppRegistration](../resources/intune_mam_managedappregistration.md).</span><span class="sxs-lookup"><span data-stu-id="b2de6-103">List properties and relationships of the [managedAppRegistration](../resources/intune_mam_managedappregistration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b2de6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b2de6-104">Prerequisites</span></span>
<span data-ttu-id="b2de6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b2de6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b2de6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2de6-107">Permission type</span></span>|<span data-ttu-id="b2de6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2de6-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b2de6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2de6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b2de6-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b2de6-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="b2de6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2de6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b2de6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2de6-112">Not supported.</span></span>|
|<span data-ttu-id="b2de6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2de6-113">Application</span></span>|<span data-ttu-id="b2de6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2de6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b2de6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2de6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations
```

## <a name="request-headers"></a><span data-ttu-id="b2de6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2de6-116">Request headers</span></span>
|<span data-ttu-id="b2de6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2de6-117">Header</span></span>|<span data-ttu-id="b2de6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b2de6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b2de6-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="b2de6-119">Authorization</span></span>|<span data-ttu-id="b2de6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b2de6-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b2de6-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b2de6-121">Accept</span></span>|<span data-ttu-id="b2de6-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b2de6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b2de6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b2de6-123">Request body</span></span>
<span data-ttu-id="b2de6-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b2de6-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b2de6-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2de6-125">Response</span></span>
<span data-ttu-id="b2de6-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppRegistration](../resources/intune_mam_managedappregistration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2de6-126">If successful, this method returns a `200 OK` response code and a collection of [managedAppRegistration](../resources/intune_mam_managedappregistration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b2de6-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2de6-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="b2de6-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2de6-128">Request</span></span>
<span data-ttu-id="b2de6-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2de6-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations
```

### <a name="response"></a><span data-ttu-id="b2de6-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2de6-130">Response</span></span>
<span data-ttu-id="b2de6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b2de6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 806

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppRegistration",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "applicationVersion": "Application Version value",
      "managementSdkVersion": "Management Sdk Version value",
      "platformVersion": "Platform Version value",
      "deviceType": "Device Type value",
      "deviceTag": "Device Tag value",
      "deviceName": "Device Name value",
      "flaggedReasons": [
        "rootedDevice"
      ],
      "userId": "User Id value",
      "appIdentifier": {
        "@odata.type": "microsoft.graph.mobileAppIdentifier"
      },
      "id": "5496aa60-aa60-5496-60aa-965460aa9654",
      "version": "Version value"
    }
  ]
}
```



