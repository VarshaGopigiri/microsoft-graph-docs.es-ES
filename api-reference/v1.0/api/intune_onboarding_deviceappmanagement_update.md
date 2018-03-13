# <a name="update-deviceappmanagement"></a><span data-ttu-id="0629b-101">Actualizar deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="0629b-101">Update deviceAppManagement</span></span>

> <span data-ttu-id="0629b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0629b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0629b-103">Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0629b-103">Update the properties of a [calendar](../resources/intune_onboarding_deviceappmanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0629b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0629b-104">Prerequisites</span></span>
<span data-ttu-id="0629b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0629b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0629b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0629b-107">Permission type</span></span>|<span data-ttu-id="0629b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0629b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0629b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0629b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0629b-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0629b-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0629b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0629b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0629b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0629b-112">Not supported.</span></span>|
|<span data-ttu-id="0629b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0629b-113">Application</span></span>|<span data-ttu-id="0629b-114">No compatible.</span><span class="sxs-lookup"><span data-stu-id="0629b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0629b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0629b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement
```

## <a name="request-headers"></a><span data-ttu-id="0629b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0629b-116">Request headers</span></span>
|<span data-ttu-id="0629b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0629b-117">Header</span></span>|<span data-ttu-id="0629b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0629b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0629b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0629b-119">Authorization</span></span>|<span data-ttu-id="0629b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0629b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="0629b-121">Accept</span><span class="sxs-lookup"><span data-stu-id="0629b-121">Accept</span></span>|<span data-ttu-id="0629b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0629b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0629b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0629b-123">Request body</span></span>
<span data-ttu-id="0629b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0629b-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_onboarding_deviceappmanagement.md) object.</span></span>

<span data-ttu-id="0629b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="0629b-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="0629b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0629b-126">Property</span></span>|<span data-ttu-id="0629b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0629b-127">Type</span></span>|<span data-ttu-id="0629b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0629b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0629b-129">id</span><span class="sxs-lookup"><span data-stu-id="0629b-129">id</span></span>|<span data-ttu-id="0629b-130">String</span><span class="sxs-lookup"><span data-stu-id="0629b-130">String</span></span>|<span data-ttu-id="0629b-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0629b-131">Not yet documented</span></span>|
|<span data-ttu-id="0629b-132">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="0629b-132">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="0629b-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0629b-133">DateTimeOffset</span></span>|<span data-ttu-id="0629b-134">Última vez que se sincronizaron correctamente las aplicaciones de Microsoft Store para Empresas en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="0629b-134">The last time the apps from the Microsoft Store for Business were synced successfully for the account.</span></span>|
|<span data-ttu-id="0629b-135">isEnabledForMicrosoftStoreForBusiness</span><span class="sxs-lookup"><span data-stu-id="0629b-135">isEnabledForMicrosoftStoreForBusiness</span></span>|<span data-ttu-id="0629b-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="0629b-136">Boolean</span></span>|<span data-ttu-id="0629b-137">Indica si la cuenta está habilitada para la sincronización de aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="0629b-137">Whether the account is enabled for syncing applications from the Microsoft Store for Business.</span></span>|
|<span data-ttu-id="0629b-138">microsoftStoreForBusinessLanguage</span><span class="sxs-lookup"><span data-stu-id="0629b-138">microsoftStoreForBusinessLanguage</span></span>|<span data-ttu-id="0629b-139">String</span><span class="sxs-lookup"><span data-stu-id="0629b-139">String</span></span>|<span data-ttu-id="0629b-140">Información local que se usa para sincronizar las aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="0629b-140">The locale information used to sync applications from the Microsoft Store for Business.</span></span> <span data-ttu-id="0629b-141">Referencias culturales que son específicas de un país o región.</span><span class="sxs-lookup"><span data-stu-id="0629b-141">Cultures that are specific to a country/region.</span></span> <span data-ttu-id="0629b-142">Los nombres de dichas referencias culturales siguen RFC 4646 (Windows Vista y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="0629b-142">The names of these cultures follow RFC 4646 (Windows Vista and later).</span></span> <span data-ttu-id="0629b-143">El formato es <languagecode2>-<country/regioncode2>, donde <languagecode2> es un código de dos letras en minúsculas proveniente de ISO 639-1 y <country/regioncode2> es un código de dos letras en mayúsculas derivado de ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="0629b-143">The format is <languagecode2>-<country/regioncode2>, where <languagecode2> is a lowercase two-letter code derived from ISO 639-1 and <country/regioncode2> is an uppercase two-letter code derived from ISO 3166.</span></span> <span data-ttu-id="0629b-144">Por ejemplo, en-US para inglés (Estados Unidos) es una referencia cultural específica.</span><span class="sxs-lookup"><span data-stu-id="0629b-144">For example, en-US for English (United States) is a specific culture.</span></span>|
|<span data-ttu-id="0629b-145">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span><span class="sxs-lookup"><span data-stu-id="0629b-145">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span></span>|<span data-ttu-id="0629b-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0629b-146">DateTimeOffset</span></span>|<span data-ttu-id="0629b-147">Última vez que se completó una sincronización de aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="0629b-147">The last time an application sync from the Microsoft Store for Business was completed.</span></span>|



## <a name="response"></a><span data-ttu-id="0629b-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0629b-148">Response</span></span>
<span data-ttu-id="0629b-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune_onboarding_deviceappmanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0629b-149">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_onboarding_deviceappmanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0629b-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0629b-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="0629b-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0629b-151">Request</span></span>
<span data-ttu-id="0629b-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0629b-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement
Content-type: application/json
Content-length: 336

{
  "microsoftStoreForBusinessLastSuccessfulSyncDateTime": "2016-12-31T23:57:45.2453148-08:00",
  "isEnabledForMicrosoftStoreForBusiness": true,
  "microsoftStoreForBusinessLanguage": "Microsoft Store For Business Language value",
  "microsoftStoreForBusinessLastCompletedApplicationSyncTime": "2017-01-01T00:02:00.0421137-08:00"
}
```

### <a name="response"></a><span data-ttu-id="0629b-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0629b-153">Response</span></span>
<span data-ttu-id="0629b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0629b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 443

{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb",
  "microsoftStoreForBusinessLastSuccessfulSyncDateTime": "2016-12-31T23:57:45.2453148-08:00",
  "isEnabledForMicrosoftStoreForBusiness": true,
  "microsoftStoreForBusinessLanguage": "Microsoft Store For Business Language value",
  "microsoftStoreForBusinessLastCompletedApplicationSyncTime": "2017-01-01T00:02:00.0421137-08:00"
}
```



