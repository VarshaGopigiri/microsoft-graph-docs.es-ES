# <a name="list-devicecompliancescheduledactionforrules"></a><span data-ttu-id="55b74-101">Incluir en una lista deviceComplianceScheduledActionForRules</span><span class="sxs-lookup"><span data-stu-id="55b74-101">List deviceComplianceScheduledActionForRules</span></span>

> <span data-ttu-id="55b74-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="55b74-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="55b74-103">Enumere las propiedades y las relaciones de los objetos [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="55b74-103">List properties and relationships of the [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="55b74-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="55b74-104">Prerequisites</span></span>
<span data-ttu-id="55b74-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="55b74-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="55b74-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55b74-107">Permission type</span></span>|<span data-ttu-id="55b74-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55b74-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="55b74-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55b74-109">Delegated (work or school account)</span></span>|<span data-ttu-id="55b74-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="55b74-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="55b74-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55b74-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="55b74-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55b74-112">Not supported.</span></span>|
|<span data-ttu-id="55b74-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55b74-113">Application</span></span>|<span data-ttu-id="55b74-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55b74-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="55b74-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55b74-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
```

## <a name="request-headers"></a><span data-ttu-id="55b74-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55b74-116">Request headers</span></span>
|<span data-ttu-id="55b74-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55b74-117">Header</span></span>|<span data-ttu-id="55b74-118">Valor</span><span class="sxs-lookup"><span data-stu-id="55b74-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="55b74-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="55b74-119">Authorization</span></span>|<span data-ttu-id="55b74-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="55b74-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="55b74-121">Accept</span><span class="sxs-lookup"><span data-stu-id="55b74-121">Accept</span></span>|<span data-ttu-id="55b74-122">application/json</span><span class="sxs-lookup"><span data-stu-id="55b74-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="55b74-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55b74-123">Request body</span></span>
<span data-ttu-id="55b74-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="55b74-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="55b74-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55b74-125">Response</span></span>
<span data-ttu-id="55b74-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55b74-126">If successful, this method returns a `200 OK` response code and a collection of [deviceComplianceScheduledActionForRule](../resources/intune_deviceconfig_devicecompliancescheduledactionforrule.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55b74-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55b74-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="55b74-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55b74-128">Request</span></span>
<span data-ttu-id="55b74-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55b74-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
```

### <a name="response"></a><span data-ttu-id="55b74-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55b74-130">Response</span></span>
<span data-ttu-id="55b74-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="55b74-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 208

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
      "id": "f0075d5e-5d5e-f007-5e5d-07f05e5d07f0",
      "ruleName": "Rule Name value"
    }
  ]
}
```








