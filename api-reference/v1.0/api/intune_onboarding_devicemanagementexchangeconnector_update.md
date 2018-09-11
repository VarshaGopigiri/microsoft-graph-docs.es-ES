# <a name="update-devicemanagementexchangeconnector"></a><span data-ttu-id="7ed85-101">Actualizar deviceManagementExchangeConnector</span><span class="sxs-lookup"><span data-stu-id="7ed85-101">Update deviceManagementExchangeConnector</span></span>

> <span data-ttu-id="7ed85-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7ed85-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7ed85-103">Actualice las propiedades de un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7ed85-103">Update the properties of a [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7ed85-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7ed85-104">Prerequisites</span></span>
<span data-ttu-id="7ed85-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7ed85-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7ed85-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7ed85-107">Permission type</span></span>|<span data-ttu-id="7ed85-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7ed85-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7ed85-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7ed85-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7ed85-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7ed85-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="7ed85-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7ed85-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7ed85-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ed85-112">Not supported.</span></span>|
|<span data-ttu-id="7ed85-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7ed85-113">Application</span></span>|<span data-ttu-id="7ed85-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ed85-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7ed85-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7ed85-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
```

## <a name="request-headers"></a><span data-ttu-id="7ed85-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ed85-116">Request headers</span></span>
|<span data-ttu-id="7ed85-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ed85-117">Header</span></span>|<span data-ttu-id="7ed85-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7ed85-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7ed85-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="7ed85-119">Authorization</span></span>|<span data-ttu-id="7ed85-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7ed85-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7ed85-121">Accept</span><span class="sxs-lookup"><span data-stu-id="7ed85-121">Accept</span></span>|<span data-ttu-id="7ed85-122">application/json</span><span class="sxs-lookup"><span data-stu-id="7ed85-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7ed85-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7ed85-123">Request body</span></span>
<span data-ttu-id="7ed85-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7ed85-124">In the request body, supply a JSON representation for the [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object.</span></span>

<span data-ttu-id="7ed85-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="7ed85-125">The following table shows the properties that are required when you create the [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span></span>

|<span data-ttu-id="7ed85-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ed85-126">Property</span></span>|<span data-ttu-id="7ed85-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ed85-127">Type</span></span>|<span data-ttu-id="7ed85-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ed85-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7ed85-129">id</span><span class="sxs-lookup"><span data-stu-id="7ed85-129">id</span></span>|<span data-ttu-id="7ed85-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ed85-130">String</span></span>|<span data-ttu-id="7ed85-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7ed85-131">Not yet documented</span></span>|
|<span data-ttu-id="7ed85-132">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="7ed85-132">lastSyncDateTime</span></span>|<span data-ttu-id="7ed85-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ed85-133">DateTimeOffset</span></span>|<span data-ttu-id="7ed85-134">Última hora de sincronización para Exchange Connector</span><span class="sxs-lookup"><span data-stu-id="7ed85-134">Last sync time for the Exchange Connector</span></span>|
|<span data-ttu-id="7ed85-135">status</span><span class="sxs-lookup"><span data-stu-id="7ed85-135">status</span></span>|[<span data-ttu-id="7ed85-136">deviceManagementExchangeConnectorStatus</span><span class="sxs-lookup"><span data-stu-id="7ed85-136">deviceManagementExchangeConnectorStatus</span></span>](../resources/intune_onboarding_devicemanagementexchangeconnectorstatus.md)|<span data-ttu-id="7ed85-137">Estado de Exchange Connector.</span><span class="sxs-lookup"><span data-stu-id="7ed85-137">Exchange Connector Status Possible values are: , , , .</span></span> <span data-ttu-id="7ed85-138">Los valores posibles son: `none`, `connectionPending`, `connected` y `disconnected`.</span><span class="sxs-lookup"><span data-stu-id="7ed85-138">Possible values are: `none`, `connectionPending`, `connected`, `disconnected`.</span></span>|
|<span data-ttu-id="7ed85-139">primarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="7ed85-139">primarySmtpAddress</span></span>|<span data-ttu-id="7ed85-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ed85-140">String</span></span>|<span data-ttu-id="7ed85-141">Dirección de correo electrónico que se usó para configurar el Exchange Connector de Service To Service.</span><span class="sxs-lookup"><span data-stu-id="7ed85-141">Email address used to configure the Service To Service Exchange Connector.</span></span>|
|<span data-ttu-id="7ed85-142">serverName</span><span class="sxs-lookup"><span data-stu-id="7ed85-142">serverName</span></span>|<span data-ttu-id="7ed85-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ed85-143">String</span></span>|<span data-ttu-id="7ed85-144">El nombre del servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ed85-144">The name of the server hosting the Exchange Connector.</span></span>|
|<span data-ttu-id="7ed85-145">connectorServerName</span><span class="sxs-lookup"><span data-stu-id="7ed85-145">connectorServerName</span></span>|<span data-ttu-id="7ed85-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ed85-146">String</span></span>|<span data-ttu-id="7ed85-147">El nombre del servidor que hospeda el Exchange Connector.</span><span class="sxs-lookup"><span data-stu-id="7ed85-147">The name of the server hosting the Exchange Connector.</span></span>|
|<span data-ttu-id="7ed85-148">exchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="7ed85-148">exchangeConnectorType</span></span>|[<span data-ttu-id="7ed85-149">deviceManagementExchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="7ed85-149">deviceManagementExchangeConnectorType</span></span>](../resources/intune_onboarding_devicemanagementexchangeconnectortype.md)|<span data-ttu-id="7ed85-150">El tipo de Exchange Connector configurado.</span><span class="sxs-lookup"><span data-stu-id="7ed85-150">The type of Exchange Connector Configured.</span></span> <span data-ttu-id="7ed85-151">Los valores posibles son: `onPremises`, `hosted`, `serviceToService` y `dedicated`.</span><span class="sxs-lookup"><span data-stu-id="7ed85-151">Possible values are: `onPremises`, `hosted`, `serviceToService`, `dedicated`.</span></span>|
|<span data-ttu-id="7ed85-152">version</span><span class="sxs-lookup"><span data-stu-id="7ed85-152">version</span></span>|<span data-ttu-id="7ed85-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ed85-153">String</span></span>|<span data-ttu-id="7ed85-154">La versión del ExchangeConnectorAgent</span><span class="sxs-lookup"><span data-stu-id="7ed85-154">The version of the ExchangeConnectorAgent</span></span>|
|<span data-ttu-id="7ed85-155">exchangeAlias</span><span class="sxs-lookup"><span data-stu-id="7ed85-155">exchangeAlias</span></span>|<span data-ttu-id="7ed85-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ed85-156">String</span></span>|<span data-ttu-id="7ed85-157">Un alias asignado al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="7ed85-157">An alias assigned to the Exchange server</span></span>|
|<span data-ttu-id="7ed85-158">exchangeOrganization</span><span class="sxs-lookup"><span data-stu-id="7ed85-158">exchangeOrganization</span></span>|<span data-ttu-id="7ed85-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="7ed85-159">String</span></span>|<span data-ttu-id="7ed85-160">Organización de Exchange al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="7ed85-160">Exchange Organization to the Exchange server</span></span>|



## <a name="response"></a><span data-ttu-id="7ed85-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ed85-161">Response</span></span>
<span data-ttu-id="7ed85-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ed85-162">If successful, this method returns a `200 OK` response code and an updated [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7ed85-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ed85-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="7ed85-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ed85-164">Request</span></span>
<span data-ttu-id="7ed85-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ed85-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}
Content-type: application/json
Content-length: 418

{
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

### <a name="response"></a><span data-ttu-id="7ed85-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ed85-166">Response</span></span>
<span data-ttu-id="7ed85-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ed85-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








