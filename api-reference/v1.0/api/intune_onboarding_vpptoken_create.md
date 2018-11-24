# <a name="create-vpptoken"></a><span data-ttu-id="711a5-101">Crear vppToken</span><span class="sxs-lookup"><span data-stu-id="711a5-101">Create vppToken</span></span>

> <span data-ttu-id="711a5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="711a5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="711a5-103">Crea un nuevo objeto [vppToken](../resources/intune_onboarding_vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="711a5-103">Create a new [vppToken](../resources/intune_onboarding_vpptoken.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="711a5-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="711a5-104">Prerequisites</span></span>
<span data-ttu-id="711a5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="711a5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="711a5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="711a5-107">Permission type</span></span>|<span data-ttu-id="711a5-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="711a5-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="711a5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="711a5-109">Delegated (work or school account)</span></span>|<span data-ttu-id="711a5-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="711a5-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="711a5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="711a5-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="711a5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="711a5-112">Not supported.</span></span>|
|<span data-ttu-id="711a5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="711a5-113">Application</span></span>|<span data-ttu-id="711a5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="711a5-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="711a5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="711a5-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/vppTokens
```

## <a name="request-headers"></a><span data-ttu-id="711a5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="711a5-116">Request headers</span></span>
|<span data-ttu-id="711a5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="711a5-117">Header</span></span>|<span data-ttu-id="711a5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="711a5-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="711a5-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="711a5-119">Authorization</span></span>|<span data-ttu-id="711a5-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="711a5-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="711a5-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="711a5-121">Accept</span></span>|<span data-ttu-id="711a5-122">application/json</span><span class="sxs-lookup"><span data-stu-id="711a5-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="711a5-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="711a5-123">Request body</span></span>
<span data-ttu-id="711a5-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto vppToken.</span><span class="sxs-lookup"><span data-stu-id="711a5-124">In the request body, supply a JSON representation for the vppToken object.</span></span>

<span data-ttu-id="711a5-125">En la tabla siguiente se muestran las propiedades necesarias para crear el vppToken.</span><span class="sxs-lookup"><span data-stu-id="711a5-125">The following table shows the properties that are required when you create the vppToken.</span></span>

|<span data-ttu-id="711a5-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="711a5-126">Property</span></span>|<span data-ttu-id="711a5-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="711a5-127">Type</span></span>|<span data-ttu-id="711a5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="711a5-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="711a5-129">id</span><span class="sxs-lookup"><span data-stu-id="711a5-129">id</span></span>|<span data-ttu-id="711a5-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="711a5-130">String</span></span>|<span data-ttu-id="711a5-131">Esto se genera automáticamente cuando se crea el appleVolumePurchaseProgramToken.</span><span class="sxs-lookup"><span data-stu-id="711a5-131">This is automatically generated when the appleVolumePurchaseProgramToken is created.</span></span> <span data-ttu-id="711a5-132">Es la clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="711a5-132">It is the Key of the entity.</span></span>|
|<span data-ttu-id="711a5-133">organizationName</span><span class="sxs-lookup"><span data-stu-id="711a5-133">organizationName</span></span>|<span data-ttu-id="711a5-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="711a5-134">String</span></span>|<span data-ttu-id="711a5-135">Organización asociada al token del Programa de Compras por Volumen de Apple</span><span class="sxs-lookup"><span data-stu-id="711a5-135">The organization associated with the Apple Volume Purchase Program Token</span></span>|
|<span data-ttu-id="711a5-136">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="711a5-136">vppTokenAccountType</span></span>|[<span data-ttu-id="711a5-137">vppTokenAccountType</span><span class="sxs-lookup"><span data-stu-id="711a5-137">vppTokenAccountType</span></span>](../resources/intune_shared_vpptokenaccounttype.md)|<span data-ttu-id="711a5-138">Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="711a5-138">The type of volume purchase program which the given Apple Volume Purchase Program Token is associated with.</span></span> <span data-ttu-id="711a5-139">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="711a5-139">Possible values are: `business`, `education`.</span></span> <span data-ttu-id="711a5-140">Los valores posibles son: `business` y `education`.</span><span class="sxs-lookup"><span data-stu-id="711a5-140">Possible values are: `business`, `education`.</span></span>|
|<span data-ttu-id="711a5-141">Id. de Apple</span><span class="sxs-lookup"><span data-stu-id="711a5-141">appleId</span></span>|<span data-ttu-id="711a5-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="711a5-142">String</span></span>|<span data-ttu-id="711a5-143">Identificador de Apple asociado al token del Programa de compras por volumen de Apple especificado.</span><span class="sxs-lookup"><span data-stu-id="711a5-143">The apple Id associated with the given Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="711a5-144">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="711a5-144">expirationDateTime</span></span>|<span data-ttu-id="711a5-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="711a5-145">DateTimeOffset</span></span>|<span data-ttu-id="711a5-146">La fecha y hora de vencimiento del token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="711a5-146">The expiration date time of the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="711a5-147">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="711a5-147">lastSyncDateTime</span></span>|<span data-ttu-id="711a5-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="711a5-148">DateTimeOffset</span></span>|<span data-ttu-id="711a5-149">La última vez que se realizó la sincronización de una aplicación con el servicio del programa de compras por volumen de Apple utilizando el token de ese programa de compras.</span><span class="sxs-lookup"><span data-stu-id="711a5-149">The last time when an application sync was done with the Apple volume purchase program service using the the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="711a5-150">token</span><span class="sxs-lookup"><span data-stu-id="711a5-150">token</span></span>|<span data-ttu-id="711a5-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="711a5-151">String</span></span>|<span data-ttu-id="711a5-152">La cadena del token del programa de compras por volumen de Apple descargada desde ese programa de compras.</span><span class="sxs-lookup"><span data-stu-id="711a5-152">The Apple Volume Purchase Program Token string downloaded from the Apple Volume Purchase Program.</span></span>|
|<span data-ttu-id="711a5-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="711a5-153">lastModifiedDateTime</span></span>|<span data-ttu-id="711a5-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="711a5-154">DateTimeOffset</span></span>|<span data-ttu-id="711a5-155">La fecha y hora de modificación asociada con el token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="711a5-155">Last modification date time associated with the Apple Volume Purchase Program Token.</span></span>|
|<span data-ttu-id="711a5-156">estado</span><span class="sxs-lookup"><span data-stu-id="711a5-156">state</span></span>|[<span data-ttu-id="711a5-157">vppTokenState</span><span class="sxs-lookup"><span data-stu-id="711a5-157">vppTokenState</span></span>](../resources/intune_onboarding_vpptokenstate.md)|<span data-ttu-id="711a5-158">Estado actual del token del Programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="711a5-158">Current state of the Apple Volume Purchase Program Token.</span></span> <span data-ttu-id="711a5-159">Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.</span><span class="sxs-lookup"><span data-stu-id="711a5-159">Possible values are: `unknown`, `valid`, `expired`, `invalid`, `assignedToExternalMDM`.</span></span> <span data-ttu-id="711a5-160">Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.</span><span class="sxs-lookup"><span data-stu-id="711a5-160">Possible values are: `unknown`, `valid`, `expired`, `invalid`, `assignedToExternalMDM`.</span></span>|
|<span data-ttu-id="711a5-161">lastSyncStatus</span><span class="sxs-lookup"><span data-stu-id="711a5-161">lastSyncStatus</span></span>|[<span data-ttu-id="711a5-162">vppTokenSyncStatus</span><span class="sxs-lookup"><span data-stu-id="711a5-162">vppTokenSyncStatus</span></span>](../resources/intune_onboarding_vpptokensyncstatus.md)|<span data-ttu-id="711a5-163">Estado de sincronización actual de la última sincronización de la aplicación que se activó con el Token del programa de compras por volumen de Apple.</span><span class="sxs-lookup"><span data-stu-id="711a5-163">Current sync status of the last application sync which was triggered using the Apple Volume Purchase Program Token.</span></span> <span data-ttu-id="711a5-164">Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="711a5-164">Possible values are: `none`, `inProgress`, `completed`, `failed`.</span></span> <span data-ttu-id="711a5-165">Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="711a5-165">Possible values are: `none`, `inProgress`, `completed`, `failed`.</span></span>|
|<span data-ttu-id="711a5-166">automaticallyUpdateApps</span><span class="sxs-lookup"><span data-stu-id="711a5-166">automaticallyUpdateApps</span></span>|<span data-ttu-id="711a5-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="711a5-167">Boolean</span></span>|<span data-ttu-id="711a5-168">Si las aplicaciones para el token VPP se actualizarán automáticamente o no.</span><span class="sxs-lookup"><span data-stu-id="711a5-168">Whether or not apps for the VPP token will be automatically updated.</span></span>|
|<span data-ttu-id="711a5-169">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="711a5-169">countryOrRegion</span></span>|<span data-ttu-id="711a5-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="711a5-170">String</span></span>|<span data-ttu-id="711a5-171">Si las aplicaciones para el token VPP se actualizarán automáticamente o no.</span><span class="sxs-lookup"><span data-stu-id="711a5-171">Whether or not apps for the VPP token will be automatically updated.</span></span>|



## <a name="response"></a><span data-ttu-id="711a5-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="711a5-172">Response</span></span>
<span data-ttu-id="711a5-173">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [vppToken](../resources/intune_onboarding_vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="711a5-173">If successful, this method returns a `201 Created` response code and a [vppToken](../resources/intune_onboarding_vpptoken.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="711a5-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="711a5-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="711a5-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="711a5-175">Request</span></span>
<span data-ttu-id="711a5-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="711a5-176">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/vppTokens
Content-type: application/json
Content-length: 461

{
  "@odata.type": "#microsoft.graph.vppToken",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "state": "valid",
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value"
}
```

### <a name="response"></a><span data-ttu-id="711a5-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="711a5-177">Response</span></span>
<span data-ttu-id="711a5-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="711a5-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 574

{
  "@odata.type": "#microsoft.graph.vppToken",
  "id": "9ceb2f92-2f92-9ceb-922f-eb9c922feb9c",
  "organizationName": "Organization Name value",
  "vppTokenAccountType": "education",
  "appleId": "Apple Id value",
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "token": "Token value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "state": "valid",
  "lastSyncStatus": "inProgress",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "Country Or Region value"
}
```



