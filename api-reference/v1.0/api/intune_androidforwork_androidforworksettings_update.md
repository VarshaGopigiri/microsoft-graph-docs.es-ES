# <a name="update-androidforworksettings"></a><span data-ttu-id="7ddd8-101">Actualizar androidForWorkSettings</span><span class="sxs-lookup"><span data-stu-id="7ddd8-101">Update androidForWorkSettings</span></span>

> <span data-ttu-id="7ddd8-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7ddd8-103">Actualice las propiedades de un objeto [androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md).</span><span class="sxs-lookup"><span data-stu-id="7ddd8-103">Update the properties of a [calendar](../resources/intune_androidforwork_androidforworksettings.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7ddd8-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7ddd8-104">Prerequisites</span></span>
<span data-ttu-id="7ddd8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7ddd8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7ddd8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7ddd8-107">Permission type</span></span>|<span data-ttu-id="7ddd8-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7ddd8-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7ddd8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7ddd8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7ddd8-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7ddd8-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7ddd8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7ddd8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7ddd8-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-112">Not supported.</span></span>|
|<span data-ttu-id="7ddd8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7ddd8-113">Application</span></span>|<span data-ttu-id="7ddd8-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7ddd8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7ddd8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/androidForWorkSettings
```

## <a name="request-headers"></a><span data-ttu-id="7ddd8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ddd8-116">Request headers</span></span>
|<span data-ttu-id="7ddd8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ddd8-117">Header</span></span>|<span data-ttu-id="7ddd8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7ddd8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7ddd8-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="7ddd8-119">Authorization</span></span>|<span data-ttu-id="7ddd8-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="7ddd8-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7ddd8-121">Accept</span></span>|<span data-ttu-id="7ddd8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="7ddd8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7ddd8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7ddd8-123">Request body</span></span>
<span data-ttu-id="7ddd8-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md).</span><span class="sxs-lookup"><span data-stu-id="7ddd8-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_androidforwork_androidforworksettings.md) object.</span></span>

<span data-ttu-id="7ddd8-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md).</span><span class="sxs-lookup"><span data-stu-id="7ddd8-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="7ddd8-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7ddd8-126">Property</span></span>|<span data-ttu-id="7ddd8-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ddd8-127">Type</span></span>|<span data-ttu-id="7ddd8-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ddd8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7ddd8-129">id</span><span class="sxs-lookup"><span data-stu-id="7ddd8-129">id</span></span>|<span data-ttu-id="7ddd8-130">String</span><span class="sxs-lookup"><span data-stu-id="7ddd8-130">String</span></span>|<span data-ttu-id="7ddd8-131">Identificador de la configuración de Android for Work</span><span class="sxs-lookup"><span data-stu-id="7ddd8-131">The Android for Work settings identifier</span></span>|
|<span data-ttu-id="7ddd8-132">bindStatus</span><span class="sxs-lookup"><span data-stu-id="7ddd8-132">bindStatus</span></span>|<span data-ttu-id="7ddd8-133">String</span><span class="sxs-lookup"><span data-stu-id="7ddd8-133">String</span></span>|<span data-ttu-id="7ddd8-134">Estado de enlace del espacio empresarial con la API del EMM de Google. Los valores posibles son: `notBound`, `bound`, `boundAndValidated` y `unbinding`.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-134">Bind status of the tenant with the Google EMM API Possible values are: `notBound`, `bound`, `boundAndValidated`, `unbinding`.</span></span>|
|<span data-ttu-id="7ddd8-135">lastAppSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="7ddd8-135">lastAppSyncDateTime</span></span>|<span data-ttu-id="7ddd8-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ddd8-136">DateTimeOffset</span></span>|<span data-ttu-id="7ddd8-137">Última hora de finalización para la sincronización de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7ddd8-137">Last completion time for app sync</span></span>|
|<span data-ttu-id="7ddd8-138">lastAppSyncStatus</span><span class="sxs-lookup"><span data-stu-id="7ddd8-138">lastAppSyncStatus</span></span>|<span data-ttu-id="7ddd8-139">String</span><span class="sxs-lookup"><span data-stu-id="7ddd8-139">String</span></span>|<span data-ttu-id="7ddd8-140">Resultado de la última sincronización de la aplicación. Los valores posibles son: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError` y `none`.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-140">Last application sync result Possible values are: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.</span></span>|
|<span data-ttu-id="7ddd8-141">ownerUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7ddd8-141">ownerUserPrincipalName</span></span>|<span data-ttu-id="7ddd8-142">String</span><span class="sxs-lookup"><span data-stu-id="7ddd8-142">String</span></span>|<span data-ttu-id="7ddd8-143">UPN del propietario que creó la empresa</span><span class="sxs-lookup"><span data-stu-id="7ddd8-143">Owner UPN that created the enterprise</span></span>|
|<span data-ttu-id="7ddd8-144">ownerOrganizationName</span><span class="sxs-lookup"><span data-stu-id="7ddd8-144">ownerOrganizationName</span></span>|<span data-ttu-id="7ddd8-145">String</span><span class="sxs-lookup"><span data-stu-id="7ddd8-145">String</span></span>|<span data-ttu-id="7ddd8-146">Nombre de organización usado al incorporar Android for Work</span><span class="sxs-lookup"><span data-stu-id="7ddd8-146">Organization name used when onboarding Android for Work</span></span>|
|<span data-ttu-id="7ddd8-147">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7ddd8-147">lastModifiedDateTime</span></span>|<span data-ttu-id="7ddd8-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7ddd8-148">DateTimeOffset</span></span>|<span data-ttu-id="7ddd8-149">Última hora de modificación para la configuración de Android for Work</span><span class="sxs-lookup"><span data-stu-id="7ddd8-149">Last modification time for Android for Work settings</span></span>|
|<span data-ttu-id="7ddd8-150">enrollmentTarget</span><span class="sxs-lookup"><span data-stu-id="7ddd8-150">enrollmentTarget</span></span>|<span data-ttu-id="7ddd8-151">String</span><span class="sxs-lookup"><span data-stu-id="7ddd8-151">String</span></span>|<span data-ttu-id="7ddd8-152">Indica los usuarios que pueden inscribir dispositivos en la administración de dispositivos de Android for Work. Los valores posibles son: `none`, `all`, `targeted` y `targetedAsEnrollmentRestrictions`.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-152">Indicates which users can enroll devices in Android for Work device management Possible values are: `none`, `all`, `targeted`, `targetedAsEnrollmentRestrictions`.</span></span>|
|<span data-ttu-id="7ddd8-153">targetGroupIds</span><span class="sxs-lookup"><span data-stu-id="7ddd8-153">targetGroupIds</span></span>|<span data-ttu-id="7ddd8-154">Colección String</span><span class="sxs-lookup"><span data-stu-id="7ddd8-154">String collection</span></span>|<span data-ttu-id="7ddd8-155">Especifica los grupos de AAD que pueden inscribir dispositivos en la administración de dispositivos de Android for Work si se establece enrollmentTarget en "Dirigido"</span><span class="sxs-lookup"><span data-stu-id="7ddd8-155">Specifies which AAD groups can enroll devices in Android for Work device management if enrollmentTarget is set to 'Targeted'</span></span>|



## <a name="response"></a><span data-ttu-id="7ddd8-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ddd8-156">Response</span></span>
<span data-ttu-id="7ddd8-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-157">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_androidforwork_androidforworksettings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7ddd8-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ddd8-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="7ddd8-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ddd8-159">Request</span></span>
<span data-ttu-id="7ddd8-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-160">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/androidForWorkSettings
Content-type: application/json
Content-length: 417

{
  "bindStatus": "bound",
  "lastAppSyncDateTime": "2016-12-31T23:57:22.8606813-08:00",
  "lastAppSyncStatus": "credentialsNotValid",
  "ownerUserPrincipalName": "Owner User Principal Name value",
  "ownerOrganizationName": "Owner Organization Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "enrollmentTarget": "all",
  "targetGroupIds": [
    "Target Group Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="7ddd8-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ddd8-161">Response</span></span>
<span data-ttu-id="7ddd8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7ddd8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 527

{
  "@odata.type": "#microsoft.graph.androidForWorkSettings",
  "id": "97adc169-c169-97ad-69c1-ad9769c1ad97",
  "bindStatus": "bound",
  "lastAppSyncDateTime": "2016-12-31T23:57:22.8606813-08:00",
  "lastAppSyncStatus": "credentialsNotValid",
  "ownerUserPrincipalName": "Owner User Principal Name value",
  "ownerOrganizationName": "Owner Organization Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "enrollmentTarget": "all",
  "targetGroupIds": [
    "Target Group Ids value"
  ]
}
```



