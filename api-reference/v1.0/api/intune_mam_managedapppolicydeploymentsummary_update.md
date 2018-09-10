# <a name="update-managedapppolicydeploymentsummary"></a><span data-ttu-id="86885-101">Actualizar managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="86885-101">Update managedAppPolicyDeploymentSummary</span></span>

> <span data-ttu-id="86885-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="86885-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="86885-103">Actualice las propiedades de un objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="86885-103">Update the properties of a [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="86885-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="86885-104">Prerequisites</span></span>
<span data-ttu-id="86885-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="86885-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="86885-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="86885-107">Permission type</span></span>|<span data-ttu-id="86885-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="86885-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="86885-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="86885-109">Delegated (work or school account)</span></span>|<span data-ttu-id="86885-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="86885-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="86885-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="86885-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="86885-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="86885-112">Not supported.</span></span>|
|<span data-ttu-id="86885-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="86885-113">Application</span></span>|<span data-ttu-id="86885-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="86885-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="86885-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86885-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
PATCH /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/deploymentSummary
PATCH /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/deploymentSummary
PATCH /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/deploymentSummary
```

## <a name="request-headers"></a><span data-ttu-id="86885-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86885-116">Request headers</span></span>
|<span data-ttu-id="86885-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86885-117">Header</span></span>|<span data-ttu-id="86885-118">Valor</span><span class="sxs-lookup"><span data-stu-id="86885-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="86885-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="86885-119">Authorization</span></span>|<span data-ttu-id="86885-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="86885-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="86885-121">Accept</span><span class="sxs-lookup"><span data-stu-id="86885-121">Accept</span></span>|<span data-ttu-id="86885-122">application/json</span><span class="sxs-lookup"><span data-stu-id="86885-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="86885-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="86885-123">Request body</span></span>
<span data-ttu-id="86885-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="86885-124">In the request body, supply a JSON representation for the [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md) object.</span></span>

<span data-ttu-id="86885-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="86885-125">The following table shows the properties that are required when you create the [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).</span></span>

|<span data-ttu-id="86885-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="86885-126">Property</span></span>|<span data-ttu-id="86885-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="86885-127">Type</span></span>|<span data-ttu-id="86885-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="86885-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="86885-129">displayName</span><span class="sxs-lookup"><span data-stu-id="86885-129">displayName</span></span>|<span data-ttu-id="86885-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="86885-130">String</span></span>|<span data-ttu-id="86885-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="86885-131">Not yet documented</span></span>|
|<span data-ttu-id="86885-132">configurationDeployedUserCount</span><span class="sxs-lookup"><span data-stu-id="86885-132">configurationDeployedUserCount</span></span>|<span data-ttu-id="86885-133">Int32</span><span class="sxs-lookup"><span data-stu-id="86885-133">Int32</span></span>|<span data-ttu-id="86885-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="86885-134">Not yet documented</span></span>|
|<span data-ttu-id="86885-135">lastRefreshTime</span><span class="sxs-lookup"><span data-stu-id="86885-135">lastRefreshTime</span></span>|<span data-ttu-id="86885-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="86885-136">DateTimeOffset</span></span>|<span data-ttu-id="86885-137">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="86885-137">Not yet documented</span></span>|
|<span data-ttu-id="86885-138">configurationDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="86885-138">configurationDeploymentSummaryPerApp</span></span>|<span data-ttu-id="86885-139">Colección [managedAppPolicyDeploymentSummaryPerApp](../resources/intune_mam_managedapppolicydeploymentsummaryperapp.md)</span><span class="sxs-lookup"><span data-stu-id="86885-139">[managedAppPolicyDeploymentSummaryPerApp](../resources/intune_mam_managedapppolicydeploymentsummaryperapp.md) collection</span></span>|<span data-ttu-id="86885-140">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="86885-140">Not yet documented</span></span>|
|<span data-ttu-id="86885-141">id</span><span class="sxs-lookup"><span data-stu-id="86885-141">id</span></span>|<span data-ttu-id="86885-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="86885-142">String</span></span>|<span data-ttu-id="86885-143">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="86885-143">Key of the entity.</span></span>|
|<span data-ttu-id="86885-144">version</span><span class="sxs-lookup"><span data-stu-id="86885-144">version</span></span>|<span data-ttu-id="86885-145">Cadena</span><span class="sxs-lookup"><span data-stu-id="86885-145">String</span></span>|<span data-ttu-id="86885-146">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="86885-146">Version of the entity.</span></span>|



## <a name="response"></a><span data-ttu-id="86885-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86885-147">Response</span></span>
<span data-ttu-id="86885-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86885-148">If successful, this method returns a `200 OK` response code and an updated [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="86885-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86885-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="86885-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="86885-150">Request</span></span>
<span data-ttu-id="86885-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86885-151">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
Content-type: application/json
Content-length: 516

{
  "displayName": "Display Name value",
  "configurationDeployedUserCount": 14,
  "lastRefreshTime": "2017-01-01T00:01:30.1240368-08:00",
  "configurationDeploymentSummaryPerApp": [
    {
      "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
        "packageId": "Package Id value"
      },
      "configurationAppliedUserCount": 13
    }
  ],
  "version": "Version value"
}
```

### <a name="response"></a><span data-ttu-id="86885-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86885-152">Response</span></span>
<span data-ttu-id="86885-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="86885-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 637

{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummary",
  "displayName": "Display Name value",
  "configurationDeployedUserCount": 14,
  "lastRefreshTime": "2017-01-01T00:01:30.1240368-08:00",
  "configurationDeploymentSummaryPerApp": [
    {
      "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
        "packageId": "Package Id value"
      },
      "configurationAppliedUserCount": 13
    }
  ],
  "id": "61f2f688-f688-61f2-88f6-f26188f6f261",
  "version": "Version value"
}
```








