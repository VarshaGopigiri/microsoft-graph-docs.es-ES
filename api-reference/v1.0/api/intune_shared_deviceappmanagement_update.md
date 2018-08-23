# <a name="update-deviceappmanagement"></a><span data-ttu-id="a3826-101">Actualizar deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a3826-101">Update deviceAppManagement</span></span>

> <span data-ttu-id="a3826-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a3826-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a3826-103">Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a3826-103">Update the properties of a [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a3826-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a3826-104">Prerequisites</span></span>
<span data-ttu-id="a3826-105">Se requiere uno de los siguientes permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a3826-105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see Permissions.</span></span> <span data-ttu-id="a3826-106">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a3826-106">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>  <span data-ttu-id="a3826-107">Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a3826-107">Note that the appropriate permission varies according to the workflow.</span></span>

|<span data-ttu-id="a3826-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a3826-108">Permission type</span></span>|<span data-ttu-id="a3826-109">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a3826-109">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a3826-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a3826-110">Delegated (work or school account)</span></span>|<span data-ttu-id="a3826-111">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a3826-111">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a3826-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a3826-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a3826-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3826-113">Not supported.</span></span>|
|<span data-ttu-id="a3826-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a3826-114">Application</span></span>|<span data-ttu-id="a3826-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3826-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a3826-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3826-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement
```

## <a name="request-headers"></a><span data-ttu-id="a3826-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3826-117">Request headers</span></span>
|<span data-ttu-id="a3826-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3826-118">Header</span></span>|<span data-ttu-id="a3826-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a3826-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a3826-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="a3826-120">Authorization</span></span>|<span data-ttu-id="a3826-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a3826-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a3826-122">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a3826-122">Accept</span></span>|<span data-ttu-id="a3826-123">application/json</span><span class="sxs-lookup"><span data-stu-id="a3826-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a3826-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a3826-124">Request body</span></span>
<span data-ttu-id="a3826-125">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a3826-125">In the request body, supply a JSON representation for the [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md) object.</span></span>

<span data-ttu-id="a3826-126">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a3826-126">The following table shows the properties that are required when you create the [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md).</span></span>

|<span data-ttu-id="a3826-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a3826-127">Property</span></span>|<span data-ttu-id="a3826-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3826-128">Type</span></span>|<span data-ttu-id="a3826-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3826-129">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a3826-130">id</span><span class="sxs-lookup"><span data-stu-id="a3826-130">id</span></span>|<span data-ttu-id="a3826-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="a3826-131">String</span></span>|<span data-ttu-id="a3826-132">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a3826-132">Key of the entity.</span></span>|
|<span data-ttu-id="a3826-133">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="a3826-133">**On-boarding**</span></span>|
|<span data-ttu-id="a3826-134">isEnabledForMicrosoftStoreForBusiness</span><span class="sxs-lookup"><span data-stu-id="a3826-134">isEnabledForMicrosoftStoreForBusiness</span></span>|<span data-ttu-id="a3826-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="a3826-135">Boolean</span></span>|<span data-ttu-id="a3826-136">Indica si la cuenta está habilitada para la sincronización de aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="a3826-136">Whether the account is enabled for syncing applications from the Microsoft Store for Business.</span></span>|
|<span data-ttu-id="a3826-137">microsoftStoreForBusinessLanguage</span><span class="sxs-lookup"><span data-stu-id="a3826-137">microsoftStoreForBusinessLanguage</span></span>|<span data-ttu-id="a3826-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="a3826-138">String</span></span>|<span data-ttu-id="a3826-139">Información local que se usa para sincronizar las aplicaciones de Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="a3826-139">The locale information used to sync applications from the Microsoft Store for Business.</span></span> <span data-ttu-id="a3826-140">Referencias culturales que son específicas de un país o región.</span><span class="sxs-lookup"><span data-stu-id="a3826-140">Cultures that are specific to a country/region.</span></span> <span data-ttu-id="a3826-141">Los nombres de dichas referencias culturales siguen RFC 4646 (Windows Vista y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="a3826-141">The names of these cultures follow RFC 4646 (Windows Vista and later).</span></span> <span data-ttu-id="a3826-142">El formato es <languagecode2>-<country/regioncode2>, donde <languagecode2> es un código de dos letras en minúsculas proveniente de ISO 639-1 y <country/regioncode2> es un código de dos letras en mayúsculas derivado de ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="a3826-142">The format is <languagecode2>-<country/regioncode2>, where <languagecode2> is a lowercase two-letter code derived from ISO 639-1 and <country/regioncode2> is an uppercase two-letter code derived from ISO 3166.</span></span> <span data-ttu-id="a3826-143">Por ejemplo, en-US para inglés (Estados Unidos) es una referencia cultural específica.</span><span class="sxs-lookup"><span data-stu-id="a3826-143">For example, en-US for English (United States) is a specific culture.</span></span>|
|<span data-ttu-id="a3826-144">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span><span class="sxs-lookup"><span data-stu-id="a3826-144">microsoftStoreForBusinessLastCompletedApplicationSyncTime</span></span>|<span data-ttu-id="a3826-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a3826-145">DateTimeOffset</span></span>|<span data-ttu-id="a3826-146">La última vez que se completó una sincronización de aplicaciones desde Microsoft Store para Empresas.</span><span class="sxs-lookup"><span data-stu-id="a3826-146">The last time an application sync from the Microsoft Store for Business was completed.</span></span>|
|<span data-ttu-id="a3826-147">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="a3826-147">microsoftStoreForBusinessLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="a3826-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a3826-148">DateTimeOffset</span></span>|<span data-ttu-id="a3826-149">Última vez que se sincronizaron correctamente las aplicaciones de Microsoft Store para Empresas en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="a3826-149">The last time the apps from the Microsoft Store for Business were synced successfully for the account.</span></span>|

## <a name="response"></a><span data-ttu-id="a3826-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3826-150">Response</span></span>
<span data-ttu-id="a3826-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3826-151">If successful, this method returns a `200 OK` response code and an updated [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a3826-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3826-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="a3826-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a3826-153">Request</span></span>
<span data-ttu-id="a3826-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3826-154">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="a3826-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3826-155">Response</span></span>
<span data-ttu-id="a3826-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a3826-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 110

{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
}
```



