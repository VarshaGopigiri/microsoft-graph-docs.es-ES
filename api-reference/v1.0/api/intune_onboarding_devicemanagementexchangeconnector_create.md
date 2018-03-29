# <a name="create-devicemanagementexchangeconnector"></a><span data-ttu-id="d31c1-101">Crear deviceManagementExchangeConnector</span><span class="sxs-lookup"><span data-stu-id="d31c1-101">Create deviceManagementExchangeConnector</span></span>

> <span data-ttu-id="d31c1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d31c1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d31c1-103">Cree un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md).</span><span class="sxs-lookup"><span data-stu-id="d31c1-103">Create a new [plannerBucket](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d31c1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d31c1-104">Prerequisites</span></span>
<span data-ttu-id="d31c1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d31c1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d31c1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d31c1-107">Permission type</span></span>|<span data-ttu-id="d31c1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d31c1-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d31c1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d31c1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d31c1-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d31c1-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="d31c1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d31c1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d31c1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d31c1-112">Not supported.</span></span>|
|<span data-ttu-id="d31c1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d31c1-113">Application</span></span>|<span data-ttu-id="d31c1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d31c1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d31c1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d31c1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/exchangeConnectors
```

## <a name="request-headers"></a><span data-ttu-id="d31c1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d31c1-116">Request headers</span></span>
|<span data-ttu-id="d31c1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d31c1-117">Header</span></span>|<span data-ttu-id="d31c1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d31c1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d31c1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d31c1-119">Authorization</span></span>|<span data-ttu-id="d31c1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d31c1-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="d31c1-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d31c1-121">Accept</span></span>|<span data-ttu-id="d31c1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d31c1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d31c1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d31c1-123">Request body</span></span>
<span data-ttu-id="d31c1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceManagementExchangeConnector.</span><span class="sxs-lookup"><span data-stu-id="d31c1-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="d31c1-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceManagementExchangeConnector.</span><span class="sxs-lookup"><span data-stu-id="d31c1-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="d31c1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d31c1-126">Property</span></span>|<span data-ttu-id="d31c1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d31c1-127">Type</span></span>|<span data-ttu-id="d31c1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d31c1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d31c1-129">id</span><span class="sxs-lookup"><span data-stu-id="d31c1-129">id</span></span>|<span data-ttu-id="d31c1-130">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-130">String</span></span>|<span data-ttu-id="d31c1-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d31c1-131">Not yet documented</span></span>|
|<span data-ttu-id="d31c1-132">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="d31c1-132">lastSyncDateTime</span></span>|<span data-ttu-id="d31c1-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d31c1-133">DateTimeOffset</span></span>|<span data-ttu-id="d31c1-134">Última hora de sincronización para Exchange Connector</span><span class="sxs-lookup"><span data-stu-id="d31c1-134">Last sync time for the Exchange Connector</span></span>|
|<span data-ttu-id="d31c1-135">status</span><span class="sxs-lookup"><span data-stu-id="d31c1-135">status</span></span>|<span data-ttu-id="d31c1-136">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-136">String</span></span>|<span data-ttu-id="d31c1-137">Estado de Exchange Connector Los valores posibles son: `none`, `connectionPending`, `connected` y `disconnected`.</span><span class="sxs-lookup"><span data-stu-id="d31c1-137">Exchange Connector Status Possible values are: `none`, `connectionPending`, `connected`, `disconnected`.</span></span>|
|<span data-ttu-id="d31c1-138">primarySmtpAddress</span><span class="sxs-lookup"><span data-stu-id="d31c1-138">primarySmtpAddress</span></span>|<span data-ttu-id="d31c1-139">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-139">String</span></span>|<span data-ttu-id="d31c1-140">Dirección de correo electrónico que se usó para configurar el Exchange Connector de Service To Service.</span><span class="sxs-lookup"><span data-stu-id="d31c1-140">Email address used to configure the Service To Service Exchange Connector.</span></span>|
|<span data-ttu-id="d31c1-141">serverName</span><span class="sxs-lookup"><span data-stu-id="d31c1-141">ServerName</span></span>|<span data-ttu-id="d31c1-142">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-142">String</span></span>|<span data-ttu-id="d31c1-143">El nombre del servidor que hospeda el Exchange Connector.</span><span class="sxs-lookup"><span data-stu-id="d31c1-143">The name of the server hosting the Exchange Connector.</span></span>|
|<span data-ttu-id="d31c1-144">exchangeConnectorType</span><span class="sxs-lookup"><span data-stu-id="d31c1-144">exchangeConnectorType</span></span>|<span data-ttu-id="d31c1-145">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-145">String</span></span>|<span data-ttu-id="d31c1-146">El tipo de Exchange Connector configurado.</span><span class="sxs-lookup"><span data-stu-id="d31c1-146">The type of Exchange Connector Configured.</span></span> <span data-ttu-id="d31c1-147">Los valores posibles son: `onPremises`, `hosted`, `serviceToService` y `dedicated`.</span><span class="sxs-lookup"><span data-stu-id="d31c1-147">Possible values are: `onPremises`, `hosted`, `serviceToService`, `dedicated`.</span></span>|
|<span data-ttu-id="d31c1-148">version</span><span class="sxs-lookup"><span data-stu-id="d31c1-148">version</span></span>|<span data-ttu-id="d31c1-149">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-149">String</span></span>|<span data-ttu-id="d31c1-150">La versión del ExchangeConnectorAgent</span><span class="sxs-lookup"><span data-stu-id="d31c1-150">The version of the message.</span></span>|
|<span data-ttu-id="d31c1-151">exchangeAlias</span><span class="sxs-lookup"><span data-stu-id="d31c1-151">exchangeAlias</span></span>|<span data-ttu-id="d31c1-152">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-152">String</span></span>|<span data-ttu-id="d31c1-153">Un alias asignado al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="d31c1-153">An alias assigned to the Exchange server</span></span>|
|<span data-ttu-id="d31c1-154">exchangeOrganization</span><span class="sxs-lookup"><span data-stu-id="d31c1-154">exchangeOrganization</span></span>|<span data-ttu-id="d31c1-155">String</span><span class="sxs-lookup"><span data-stu-id="d31c1-155">String</span></span>|<span data-ttu-id="d31c1-156">Organización de Exchange al servidor de Exchange</span><span class="sxs-lookup"><span data-stu-id="d31c1-156">Exchange Organization to the Exchange server</span></span>|



## <a name="response"></a><span data-ttu-id="d31c1-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d31c1-157">Response</span></span>
<span data-ttu-id="d31c1-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceManagementExchangeConnector](../resources/intune_onboarding_devicemanagementexchangeconnector.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d31c1-158">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_onboarding_devicemanagementexchangeconnector.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d31c1-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d31c1-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="d31c1-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d31c1-160">Request</span></span>
<span data-ttu-id="d31c1-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d31c1-161">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/exchangeConnectors
Content-type: application/json
Content-length: 433

{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "status": "connectionPending",
  "primarySmtpAddress": "Primary Smtp Address value",
  "serverName": "Server Name value",
  "exchangeConnectorType": "hosted",
  "version": "Version value",
  "exchangeAlias": "Exchange Alias value",
  "exchangeOrganization": "Exchange Organization value"
}
```

### <a name="response"></a><span data-ttu-id="d31c1-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d31c1-162">Response</span></span>
<span data-ttu-id="d31c1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d31c1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 482

{
  "@odata.type": "#microsoft.graph.deviceManagementExchangeConnector",
  "id": "e11c1de8-1de8-e11c-e81d-1ce1e81d1ce1",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "status": "connectionPending",
  "primarySmtpAddress": "Primary Smtp Address value",
  "serverName": "Server Name value",
  "exchangeConnectorType": "hosted",
  "version": "Version value",
  "exchangeAlias": "Exchange Alias value",
  "exchangeOrganization": "Exchange Organization value"
}
```



