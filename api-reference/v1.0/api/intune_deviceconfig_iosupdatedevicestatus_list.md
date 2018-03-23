# <a name="list-iosupdatedevicestatuses"></a><span data-ttu-id="b9cbf-101">Enumerar iosUpdateDeviceStatuses</span><span class="sxs-lookup"><span data-stu-id="b9cbf-101">List iosUpdateDeviceStatuses</span></span>

> <span data-ttu-id="b9cbf-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9cbf-103">Enumere las propiedades y las relaciones de los objetos [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="b9cbf-103">List properties and relationships of the [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b9cbf-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b9cbf-104">Prerequisites</span></span>
<span data-ttu-id="b9cbf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b9cbf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b9cbf-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b9cbf-107">Permission type</span></span>|<span data-ttu-id="b9cbf-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b9cbf-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b9cbf-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b9cbf-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b9cbf-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b9cbf-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b9cbf-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b9cbf-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b9cbf-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-112">Not supported.</span></span>|
|<span data-ttu-id="b9cbf-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b9cbf-113">Application</span></span>|<span data-ttu-id="b9cbf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b9cbf-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9cbf-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/iosUpdateStatuses
```

## <a name="request-headers"></a><span data-ttu-id="b9cbf-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9cbf-116">Request headers</span></span>
|<span data-ttu-id="b9cbf-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9cbf-117">Header</span></span>|<span data-ttu-id="b9cbf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b9cbf-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b9cbf-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="b9cbf-119">Authorization</span></span>|<span data-ttu-id="b9cbf-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="b9cbf-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b9cbf-121">Accept</span></span>|<span data-ttu-id="b9cbf-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b9cbf-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b9cbf-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9cbf-123">Request body</span></span>
<span data-ttu-id="b9cbf-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b9cbf-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9cbf-125">Response</span></span>
<span data-ttu-id="b9cbf-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-126">If successful, this method returns a `200 OK` response code and collection of [workbookPivotTable](../resources/intune_deviceconfig_iosupdatedevicestatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b9cbf-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9cbf-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="b9cbf-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9cbf-128">Request</span></span>
<span data-ttu-id="b9cbf-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/iosUpdateStatuses
```

### <a name="response"></a><span data-ttu-id="b9cbf-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9cbf-130">Response</span></span>
<span data-ttu-id="b9cbf-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9cbf-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 686

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
      "id": "63a79499-9499-63a7-9994-a7639994a763",
      "installStatus": "available",
      "osVersion": "Os Version value",
      "deviceId": "Device Id value",
      "userId": "User Id value",
      "deviceDisplayName": "Device Display Name value",
      "userName": "User Name value",
      "deviceModel": "Device Model value",
      "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
      "status": "notApplicable",
      "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```



