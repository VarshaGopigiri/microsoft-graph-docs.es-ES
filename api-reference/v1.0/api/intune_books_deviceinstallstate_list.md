# <a name="list-deviceinstallstates"></a><span data-ttu-id="670e1-101">Enumerar deviceInstallStates</span><span class="sxs-lookup"><span data-stu-id="670e1-101">List deviceInstallStates</span></span>

> <span data-ttu-id="670e1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="670e1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="670e1-103">Enumere las propiedades y las relaciones de los objetos [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="670e1-103">List properties and relationships of the [deviceInstallState](../resources/intune_books_deviceinstallstate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="670e1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="670e1-104">Prerequisites</span></span>
<span data-ttu-id="670e1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="670e1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="670e1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="670e1-107">Permission type</span></span>|<span data-ttu-id="670e1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="670e1-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="670e1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="670e1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="670e1-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="670e1-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="670e1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="670e1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="670e1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="670e1-112">Not supported.</span></span>|
|<span data-ttu-id="670e1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="670e1-113">Application</span></span>|<span data-ttu-id="670e1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="670e1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="670e1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="670e1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
GET /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="670e1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="670e1-116">Request headers</span></span>
|<span data-ttu-id="670e1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="670e1-117">Header</span></span>|<span data-ttu-id="670e1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="670e1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="670e1-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="670e1-119">Authorization</span></span>|<span data-ttu-id="670e1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="670e1-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="670e1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="670e1-121">Accept</span></span>|<span data-ttu-id="670e1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="670e1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="670e1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="670e1-123">Request body</span></span>
<span data-ttu-id="670e1-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="670e1-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="670e1-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="670e1-125">Response</span></span>
<span data-ttu-id="670e1-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceInstallState](../resources/intune_books_deviceinstallstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="670e1-126">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/intune_books_deviceinstallstate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="670e1-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="670e1-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="670e1-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="670e1-128">Request</span></span>
<span data-ttu-id="670e1-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="670e1-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
```

### <a name="response"></a><span data-ttu-id="670e1-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="670e1-130">Response</span></span>
<span data-ttu-id="670e1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="670e1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 496

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceInstallState",
      "id": "b9feb68f-b68f-b9fe-8fb6-feb98fb6feb9",
      "deviceName": "Device Name value",
      "deviceId": "Device Id value",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "installState": "installed",
      "errorCode": "Error Code value",
      "osVersion": "Os Version value",
      "osDescription": "Os Description value",
      "userName": "User Name value"
    }
  ]
}
```



