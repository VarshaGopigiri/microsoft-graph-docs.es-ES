# <a name="list-devicecomplianceuserstatuses"></a><span data-ttu-id="54f4a-101">Incluir en una lista deviceComplianceUserStatuses</span><span class="sxs-lookup"><span data-stu-id="54f4a-101">List deviceComplianceUserStatuses</span></span>

> <span data-ttu-id="54f4a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54f4a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54f4a-103">Enumere las propiedades y las relaciones de los objetos [deviceComplianceUserStatus](../resources/intune_deviceconfig_devicecomplianceuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="54f4a-103">List properties and relationships of the [deviceComplianceUserStatus](../resources/intune_deviceconfig_devicecomplianceuserstatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54f4a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54f4a-104">Prerequisites</span></span>
<span data-ttu-id="54f4a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="54f4a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="54f4a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54f4a-107">Permission type</span></span>|<span data-ttu-id="54f4a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54f4a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54f4a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54f4a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="54f4a-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="54f4a-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="54f4a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54f4a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54f4a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54f4a-112">Not supported.</span></span>|
|<span data-ttu-id="54f4a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54f4a-113">Application</span></span>|<span data-ttu-id="54f4a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54f4a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54f4a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54f4a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="54f4a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54f4a-116">Request headers</span></span>
|<span data-ttu-id="54f4a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54f4a-117">Header</span></span>|<span data-ttu-id="54f4a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="54f4a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54f4a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="54f4a-119">Authorization</span></span>|<span data-ttu-id="54f4a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54f4a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54f4a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="54f4a-121">Accept</span></span>|<span data-ttu-id="54f4a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="54f4a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54f4a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54f4a-123">Request body</span></span>
<span data-ttu-id="54f4a-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="54f4a-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="54f4a-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54f4a-125">Response</span></span>
<span data-ttu-id="54f4a-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceComplianceUserStatus](../resources/intune_deviceconfig_devicecomplianceuserstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54f4a-126">If successful, this method returns a `200 OK` response code and a collection of [deviceComplianceUserStatus](../resources/intune_deviceconfig_devicecomplianceuserstatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54f4a-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54f4a-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="54f4a-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54f4a-128">Request</span></span>
<span data-ttu-id="54f4a-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54f4a-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses
```

### <a name="response"></a><span data-ttu-id="54f4a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54f4a-130">Response</span></span>
<span data-ttu-id="54f4a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54f4a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 397

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceComplianceUserStatus",
      "id": "a0b566cd-66cd-a0b5-cd66-b5a0cd66b5a0",
      "userDisplayName": "User Display Name value",
      "devicesCount": 12,
      "status": "notApplicable",
      "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```








