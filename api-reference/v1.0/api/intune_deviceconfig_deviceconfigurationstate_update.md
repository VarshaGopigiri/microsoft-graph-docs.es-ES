# <a name="update-deviceconfigurationstate"></a><span data-ttu-id="a27e4-101">Actualizar deviceConfigurationState</span><span class="sxs-lookup"><span data-stu-id="a27e4-101">Update deviceConfigurationState</span></span>

> <span data-ttu-id="a27e4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a27e4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a27e4-103">Actualice las propiedades de un objeto [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).</span><span class="sxs-lookup"><span data-stu-id="a27e4-103">Update the properties of a [calendar](../resources/intune_deviceconfig_deviceconfigurationstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a27e4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a27e4-104">Prerequisites</span></span>
<span data-ttu-id="a27e4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a27e4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a27e4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a27e4-107">Permission type</span></span>|<span data-ttu-id="a27e4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a27e4-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a27e4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a27e4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a27e4-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a27e4-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a27e4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a27e4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a27e4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a27e4-112">Not supported.</span></span>|
|<span data-ttu-id="a27e4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a27e4-113">Application</span></span>|<span data-ttu-id="a27e4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a27e4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a27e4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a27e4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /managedDevices/{managedDevicesId}/deviceConfigurationStates/{deviceConfigurationStateId}
```

## <a name="request-headers"></a><span data-ttu-id="a27e4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a27e4-116">Request headers</span></span>
|<span data-ttu-id="a27e4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a27e4-117">Header</span></span>|<span data-ttu-id="a27e4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a27e4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a27e4-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="a27e4-119">Authorization</span></span>|<span data-ttu-id="a27e4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a27e4-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="a27e4-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a27e4-121">Accept</span></span>|<span data-ttu-id="a27e4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a27e4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a27e4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a27e4-123">Request body</span></span>
<span data-ttu-id="a27e4-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).</span><span class="sxs-lookup"><span data-stu-id="a27e4-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_deviceconfigurationstate.md) object.</span></span>

<span data-ttu-id="a27e4-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md).</span><span class="sxs-lookup"><span data-stu-id="a27e4-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="a27e4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a27e4-126">Property</span></span>|<span data-ttu-id="a27e4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a27e4-127">Type</span></span>|<span data-ttu-id="a27e4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a27e4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a27e4-129">id</span><span class="sxs-lookup"><span data-stu-id="a27e4-129">id</span></span>|<span data-ttu-id="a27e4-130">String</span><span class="sxs-lookup"><span data-stu-id="a27e4-130">String</span></span>|<span data-ttu-id="a27e4-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a27e4-131">Key of the setting.</span></span>|
|<span data-ttu-id="a27e4-132">settingStates</span><span class="sxs-lookup"><span data-stu-id="a27e4-132">settingStates</span></span>|<span data-ttu-id="a27e4-133">Colección [deviceConfigurationSettingState](../resources/intune_deviceconfig_deviceconfigurationsettingstate.md)</span><span class="sxs-lookup"><span data-stu-id="a27e4-133">[deviceConfigurationSettingState](../resources/intune_deviceconfig_deviceconfigurationsettingstate.md) collection</span></span>|<span data-ttu-id="a27e4-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a27e4-134">Not yet documented</span></span>|
|<span data-ttu-id="a27e4-135">displayName</span><span class="sxs-lookup"><span data-stu-id="a27e4-135">displayName</span></span>|<span data-ttu-id="a27e4-136">String</span><span class="sxs-lookup"><span data-stu-id="a27e4-136">String</span></span>|<span data-ttu-id="a27e4-137">El nombre de la directiva de este policyBase</span><span class="sxs-lookup"><span data-stu-id="a27e4-137">The name of the policy for this policyBase</span></span>|
|<span data-ttu-id="a27e4-138">version</span><span class="sxs-lookup"><span data-stu-id="a27e4-138">version</span></span>|<span data-ttu-id="a27e4-139">Int32</span><span class="sxs-lookup"><span data-stu-id="a27e4-139">Int32</span></span>|<span data-ttu-id="a27e4-140">La versión de la directiva</span><span class="sxs-lookup"><span data-stu-id="a27e4-140">The version of the message.</span></span>|
|<span data-ttu-id="a27e4-141">platformType</span><span class="sxs-lookup"><span data-stu-id="a27e4-141">PlatformType</span></span>|<span data-ttu-id="a27e4-142">String</span><span class="sxs-lookup"><span data-stu-id="a27e4-142">String</span></span>|<span data-ttu-id="a27e4-143">Tipo de plataforma al que se aplica la directiva. Los valores posibles son: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `all`.</span><span class="sxs-lookup"><span data-stu-id="a27e4-143">Platform type that the policy applies to Possible values are: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `all`.</span></span>|
|<span data-ttu-id="a27e4-144">state</span><span class="sxs-lookup"><span data-stu-id="a27e4-144">state</span></span>|<span data-ttu-id="a27e4-145">String</span><span class="sxs-lookup"><span data-stu-id="a27e4-145">String</span></span>|<span data-ttu-id="a27e4-146">Estado de cumplimiento de la directiva. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error` y `conflict`.</span><span class="sxs-lookup"><span data-stu-id="a27e4-146">The compliance state of the policy Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="a27e4-147">settingCount</span><span class="sxs-lookup"><span data-stu-id="a27e4-147">settingCount</span></span>|<span data-ttu-id="a27e4-148">Int32</span><span class="sxs-lookup"><span data-stu-id="a27e4-148">Int32</span></span>|<span data-ttu-id="a27e4-149">Recuento del número de ajustes que contiene una directiva</span><span class="sxs-lookup"><span data-stu-id="a27e4-149">Count of how many setting a policy holds</span></span>|



## <a name="response"></a><span data-ttu-id="a27e4-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a27e4-150">Response</span></span>
<span data-ttu-id="a27e4-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationState](../resources/intune_deviceconfig_deviceconfigurationstate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a27e4-151">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_deviceconfigurationstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a27e4-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a27e4-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="a27e4-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a27e4-153">Request</span></span>
<span data-ttu-id="a27e4-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a27e4-154">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/managedDevices/{managedDevicesId}/deviceConfigurationStates/{deviceConfigurationStateId}
Content-type: application/json
Content-length: 904

{
  "settingStates": [
    {
      "@odata.type": "microsoft.graph.deviceConfigurationSettingState",
      "setting": "Setting value",
      "settingName": "Setting Name value",
      "instanceDisplayName": "Instance Display Name value",
      "state": "notApplicable",
      "errorCode": 9,
      "errorDescription": "Error Description value",
      "userId": "User Id value",
      "userName": "User Name value",
      "userEmail": "User Email value",
      "userPrincipalName": "User Principal Name value",
      "sources": [
        {
          "@odata.type": "microsoft.graph.settingSource",
          "id": "Id value",
          "displayName": "Display Name value"
        }
      ],
      "currentValue": "Current Value value"
    }
  ],
  "displayName": "Display Name value",
  "version": 7,
  "platformType": "iOS",
  "state": "notApplicable",
  "settingCount": 12
}
```

### <a name="response"></a><span data-ttu-id="a27e4-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a27e4-155">Response</span></span>
<span data-ttu-id="a27e4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a27e4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1016

{
  "@odata.type": "#microsoft.graph.deviceConfigurationState",
  "id": "11692784-2784-1169-8427-691184276911",
  "settingStates": [
    {
      "@odata.type": "microsoft.graph.deviceConfigurationSettingState",
      "setting": "Setting value",
      "settingName": "Setting Name value",
      "instanceDisplayName": "Instance Display Name value",
      "state": "notApplicable",
      "errorCode": 9,
      "errorDescription": "Error Description value",
      "userId": "User Id value",
      "userName": "User Name value",
      "userEmail": "User Email value",
      "userPrincipalName": "User Principal Name value",
      "sources": [
        {
          "@odata.type": "microsoft.graph.settingSource",
          "id": "Id value",
          "displayName": "Display Name value"
        }
      ],
      "currentValue": "Current Value value"
    }
  ],
  "displayName": "Display Name value",
  "version": 7,
  "platformType": "iOS",
  "state": "notApplicable",
  "settingCount": 12
}
```



