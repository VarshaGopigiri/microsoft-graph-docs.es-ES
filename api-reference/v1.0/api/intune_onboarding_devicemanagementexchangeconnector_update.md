# <a name="update-devicemanagementexchangeconnector"></a><span data-ttu-id="61e78-101">Actualizar deviceManagementExchangeConnector</span><span class="sxs-lookup"><span data-stu-id="61e78-101">Update deviceManagementExchangeConnector</span></span>

> <span data-ttu-id="61e78-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="61e78-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="61e78-103">Actualice las propiedades de un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="61e78-103">Update the properties of a [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="61e78-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="61e78-104">Prerequisites</span></span>
<span data-ttu-id="61e78-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="61e78-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="61e78-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61e78-107">Permission type</span></span>|<span data-ttu-id="61e78-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61e78-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="61e78-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61e78-109">Delegated (work or school account)</span></span>|<span data-ttu-id="61e78-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61e78-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="61e78-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61e78-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="61e78-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61e78-112">Not supported.</span></span>|
|<span data-ttu-id="61e78-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61e78-113">Application</span></span>|<span data-ttu-id="61e78-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61e78-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="61e78-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61e78-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="61e78-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61e78-116">Request headers</span></span>
|<span data-ttu-id="61e78-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61e78-117">Header</span></span>|<span data-ttu-id="61e78-118">Valor</span><span class="sxs-lookup"><span data-stu-id="61e78-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="61e78-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="61e78-119">Authorization</span></span>|<span data-ttu-id="61e78-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="61e78-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="61e78-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="61e78-121">Accept</span></span>|<span data-ttu-id="61e78-122">application/json</span><span class="sxs-lookup"><span data-stu-id="61e78-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="61e78-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="61e78-123">Request body</span></span>
<span data-ttu-id="61e78-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="61e78-124">In the request body, supply a JSON representation for the [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object.</span></span>

<span data-ttu-id="61e78-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="61e78-125">The following table shows the properties that are required when you create the [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span></span>

|<span data-ttu-id="61e78-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61e78-126">Property</span></span>|<span data-ttu-id="61e78-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="61e78-127">Type</span></span>|<span data-ttu-id="61e78-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="61e78-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="61e78-129">id</span><span class="sxs-lookup"><span data-stu-id="61e78-129">id</span></span>|<span data-ttu-id="61e78-130">String</span><span class="sxs-lookup"><span data-stu-id="61e78-130">String</span></span>|<span data-ttu-id="61e78-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="61e78-131">Not yet documented</span></span>|
|<span data-ttu-id="61e78-132">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="61e78-132">lastSyncDateTime</span></span>|<span data-ttu-id="61e78-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61e78-133">DateTimeOffset</span></span>|<span data-ttu-id="61e78-134">Última hora de sincronización para Exchange Connector</span><span class="sxs-lookup"><span data-stu-id="61e78-134">Last sync time for the Exchange Connector</span></span>|
|<span data-ttu-id="61e78-135">status</span><span class="sxs-lookup"><span data-stu-id="61e78-135">status</span></span>|[<span data-ttu-id="61e78-136">deviceManagementExchangeConnectorStatus</span><span class="sxs-lookup"><span data-stu-id="61e78-136">deviceManagementExchangeConnectorStatus</span></span>](../resources/intune_onboarding_devicemanagementexchangeconnectorstatus.md)|<span data-ttu-id="61e78-137">Estado del conector de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61e78-137">Exchange Connector Status.</span></span> <span data-ttu-id="61e78-138">Los valores posibles son: `none`, `connectionPending`, `connected` y `disconnected`.</span><span class="sxs-lookup"><span data-stu-id="61e78-138">Possible values are: `none`, `connectionPending`, `connected`, `disconnected`.</span></span>|
|<span data-ttu-id="61e78-139">primarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="61e78-139">primarySmtpAddress</span></span>|<span data-ttu-id="61e78-140">String</span><span class="sxs-lookup"><span data-stu-id="61e78-140">String</span></span>|<span data-ttu-id="61e78-141">Dirección de correo electrónico que se usó para configurar el Exchange Connector de Service To Service.</span><span class="sxs-lookup"><span data-stu-id="61e78-141">Email address used to configure the Service To Service Exchange Connector.</span></span>|
|<span data-ttu-id="61e78-142">serverName</span><span class="sxs-lookup"><span data-stu-id="61e78-142">serverName</span></span>|<span data-ttu-id="61e78-143">String</span><span class="sxs-lookup"><span data-stu-id="61e78-143">String</span></span>|<span data-ttu-id="61e78-144">El nombre del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="61e78-144">The name of the Exchange server.</span></span>|
|<span data-ttu-id="61e78-145">connectorServerName</span><span class="sxs-lookup"><span data-stu-id="61e78-145">connectorServerName</span></span>|<span data-ttu-id="61e78-146">String</span><span class="sxs-lookup"><span data-stu-id="61e78-146">String</span></span>|<span data-ttu-id="61e78-147">El nombre del servidor que hospeda el Exchange Connector.</span><span class="sxs-lookup"><span data-stu-id="61e78-147">The name of the server hosting the Exchange Connector.</span></span>|
|<span data-ttu-id="61e78-148">exchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="61e78-148">exchangeConnectorType</span></span>|[<span data-ttu-id="61e78-149">deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="61e78-149">deviceManagementExchangeConnectorType</span></span>](../resources/intune_onboarding_devicemanagementexchangeconnectortype.md)|<span data-ttu-id="61e78-150">El tipo de Exchange Connector configurado.</span><span class="sxs-lookup"><span data-stu-id="61e78-150">The type of Exchange Connector Configured.</span></span> <span data-ttu-id="61e78-151">Los valores posibles son: `onPremises`, `hosted`, `serviceToService` y `dedicated`.</span><span class="sxs-lookup"><span data-stu-id="61e78-151">Possible values are: `onPremises`, `hosted`, `serviceToService`, `dedicated`.</span></span>|
|<span data-ttu-id="61e78-152">version</span><span class="sxs-lookup"><span data-stu-id="61e78-152">version</span></span>|<span data-ttu-id="61e78-153">String</span><span class="sxs-lookup"><span data-stu-id="61e78-153">String</span></span>|<span data-ttu-id="61e78-154">La versión del ExchangeConnectorAgent</span><span class="sxs-lookup"><span data-stu-id="61e78-154">The version of the ExchangeConnectorAgent</span></span>|
|<span data-ttu-id="61e78-155">exchangeAlias</span><span class="sxs-lookup"><span data-stu-id="61e78-155">exchangeAlias</span></span>|<span data-ttu-id="61e78-156">String</span><span class="sxs-lookup"><span data-stu-id="61e78-156">String</span></span>|<span data-ttu-id="61e78-157">Un alias asignado al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="61e78-157">An alias assigned to the Exchange server</span></span>|
|<span data-ttu-id="61e78-158">exchangeOrganization</span><span class="sxs-lookup"><span data-stu-id="61e78-158">exchangeOrganization</span></span>|<span data-ttu-id="61e78-159">String</span><span class="sxs-lookup"><span data-stu-id="61e78-159">String</span></span>|<span data-ttu-id="61e78-160">Organización de Exchange al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="61e78-160">Exchange Organization to the Exchange server</span></span>|



## <a name="response"></a><span data-ttu-id="61e78-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61e78-161">Response</span></span>
<span data-ttu-id="61e78-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61e78-162">If successful, this method returns a `200 OK` response code and an updated [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61e78-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61e78-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="61e78-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="61e78-164">Request</span></span>
<span data-ttu-id="61e78-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61e78-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
Content-type: application/json
Content-length: 490

{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "status": "connectionPending",
  "primarySmtpAddress": "Primary Smtp Address value",
  "serverName": "Server Name value",
  "connectorServerName": "Connector Server Name value",
  "exchangeConnectorType": "hosted",
  "version": "Version value",
  "exchangeAlias": "Exchange Alias value",
  "exchangeOrganization": "Exchange Organization value"
}
```

### <a name="response"></a><span data-ttu-id="61e78-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61e78-166">Response</span></span>
<span data-ttu-id="61e78-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="61e78-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 539

{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
  "id": "e11c1de8-1de8-e11c-e81d-1ce1e81d1ce1",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "status": "connectionPending",
  "primarySmtpAddress": "Primary Smtp Address value",
  "serverName": "Server Name value",
  "connectorServerName": "Connector Server Name value",
  "exchangeConnectorType": "hosted",
  "version": "Version value",
  "exchangeAlias": "Exchange Alias value",
  "exchangeOrganization": "Exchange Organization value"
}
```



