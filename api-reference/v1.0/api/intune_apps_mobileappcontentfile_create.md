# <a name="create-mobileappcontentfile"></a><span data-ttu-id="c628d-101">Crear mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="c628d-101">Create mobileAppContentFile</span></span>

> <span data-ttu-id="c628d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c628d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c628d-103">Cree un objeto [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="c628d-103">Create a new [plannerBucket](../resources/intune_apps_mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c628d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c628d-104">Prerequisites</span></span>
<span data-ttu-id="c628d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c628d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c628d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c628d-107">Permission type</span></span>|<span data-ttu-id="c628d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c628d-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c628d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c628d-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c628d-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c628d-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c628d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c628d-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c628d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c628d-112">Not supported.</span></span>|
|<span data-ttu-id="c628d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c628d-113">Application</span></span>|<span data-ttu-id="c628d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c628d-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c628d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c628d-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
```

## <a name="request-headers"></a><span data-ttu-id="c628d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c628d-116">Request headers</span></span>
|<span data-ttu-id="c628d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c628d-117">Header</span></span>|<span data-ttu-id="c628d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c628d-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c628d-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="c628d-119">Authorization</span></span>|<span data-ttu-id="c628d-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c628d-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="c628d-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c628d-121">Accept</span></span>|<span data-ttu-id="c628d-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c628d-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c628d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c628d-123">Request body</span></span>
<span data-ttu-id="c628d-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="c628d-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="c628d-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="c628d-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="c628d-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c628d-126">Property</span></span>|<span data-ttu-id="c628d-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c628d-127">Type</span></span>|<span data-ttu-id="c628d-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c628d-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c628d-129">azureStorageUri</span><span class="sxs-lookup"><span data-stu-id="c628d-129">azureStorageUri</span></span>|<span data-ttu-id="c628d-130">String</span><span class="sxs-lookup"><span data-stu-id="c628d-130">String</span></span>|<span data-ttu-id="c628d-131">El URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c628d-131">The Azure Storage URI.</span></span>|
|<span data-ttu-id="c628d-132">isCommitted</span><span class="sxs-lookup"><span data-stu-id="c628d-132">isCommitted</span></span>|<span data-ttu-id="c628d-133">Boolean</span><span class="sxs-lookup"><span data-stu-id="c628d-133">Boolean</span></span>|<span data-ttu-id="c628d-134">Un valor que indica si el archivo está confirmado.</span><span class="sxs-lookup"><span data-stu-id="c628d-134">A value indicating whether the file is committed.</span></span>|
|<span data-ttu-id="c628d-135">id</span><span class="sxs-lookup"><span data-stu-id="c628d-135">id</span></span>|<span data-ttu-id="c628d-136">String</span><span class="sxs-lookup"><span data-stu-id="c628d-136">String</span></span>|<span data-ttu-id="c628d-137">El Id. de archivo.</span><span class="sxs-lookup"><span data-stu-id="c628d-137">The File Id.</span></span>|
|<span data-ttu-id="c628d-138">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c628d-138">createdDateTime</span></span>|<span data-ttu-id="c628d-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c628d-139">DateTimeOffset</span></span>|<span data-ttu-id="c628d-140">La hora en que se ha creado el archivo.</span><span class="sxs-lookup"><span data-stu-id="c628d-140">The time the file was created.</span></span>|
|<span data-ttu-id="c628d-141">name</span><span class="sxs-lookup"><span data-stu-id="c628d-141">name</span></span>|<span data-ttu-id="c628d-142">String</span><span class="sxs-lookup"><span data-stu-id="c628d-142">String</span></span>|<span data-ttu-id="c628d-143">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="c628d-143">The file name.</span></span>|
|<span data-ttu-id="c628d-144">size</span><span class="sxs-lookup"><span data-stu-id="c628d-144">size</span></span>|<span data-ttu-id="c628d-145">Int64</span><span class="sxs-lookup"><span data-stu-id="c628d-145">Int64</span></span>|<span data-ttu-id="c628d-146">El tamaño del archivo antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="c628d-146">The size of the file prior to encryption.</span></span>|
|<span data-ttu-id="c628d-147">sizeEncrypted</span><span class="sxs-lookup"><span data-stu-id="c628d-147">sizeEncrypted</span></span>|<span data-ttu-id="c628d-148">Int64</span><span class="sxs-lookup"><span data-stu-id="c628d-148">Int64</span></span>|<span data-ttu-id="c628d-149">El tamaño del archivo después del cifrado.</span><span class="sxs-lookup"><span data-stu-id="c628d-149">The size of the file after encryption.</span></span>|
|<span data-ttu-id="c628d-150">azureStorageUriExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="c628d-150">azureStorageUriExpirationDateTime</span></span>|<span data-ttu-id="c628d-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c628d-151">DateTimeOffset</span></span>|<span data-ttu-id="c628d-152">La hora en que expira el URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="c628d-152">The time the Azure storage Uri expires.</span></span>|
|<span data-ttu-id="c628d-153">manifiesto</span><span class="sxs-lookup"><span data-stu-id="c628d-153">manifest</span></span>|<span data-ttu-id="c628d-154">Binario</span><span class="sxs-lookup"><span data-stu-id="c628d-154">Binary</span></span>|<span data-ttu-id="c628d-155">La información del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="c628d-155">The manifest information.</span></span>|
|<span data-ttu-id="c628d-156">uploadState</span><span class="sxs-lookup"><span data-stu-id="c628d-156">uploadState</span></span>|<span data-ttu-id="c628d-157">String</span><span class="sxs-lookup"><span data-stu-id="c628d-157">String</span></span>|<span data-ttu-id="c628d-158">El estado de la solicitud de carga actual.</span><span class="sxs-lookup"><span data-stu-id="c628d-158">The state of the current upload request.</span></span> <span data-ttu-id="c628d-159">Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed` y `commitFileTimedOut`.</span><span class="sxs-lookup"><span data-stu-id="c628d-159">Possible values are: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span></span>|



## <a name="response"></a><span data-ttu-id="c628d-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c628d-160">Response</span></span>
<span data-ttu-id="c628d-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c628d-161">If successful, this method returns a `201 Created` response code and [Contract](../resources/intune_apps_mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c628d-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c628d-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="c628d-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c628d-163">Request</span></span>
<span data-ttu-id="c628d-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c628d-164">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
Content-type: application/json
Content-length: 342

{
  "@odata.type": "#microsoft.graph.mobileAppContentFile",
  "azureStorageUri": "Azure Storage Uri value",
  "isCommitted": true,
  "name": "Name value",
  "size": 4,
  "sizeEncrypted": 13,
  "azureStorageUriExpirationDateTime": "2017-01-01T00:00:08.4940464-08:00",
  "manifest": "bWFuaWZlc3Q=",
  "uploadState": "transientError"
}
```

### <a name="response"></a><span data-ttu-id="c628d-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c628d-165">Response</span></span>
<span data-ttu-id="c628d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c628d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 450

{
  "@odata.type": "#microsoft.graph.mobileAppContentFile",
  "azureStorageUri": "Azure Storage Uri value",
  "isCommitted": true,
  "id": "eab2e29b-e29b-eab2-9be2-b2ea9be2b2ea",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "name": "Name value",
  "size": 4,
  "sizeEncrypted": 13,
  "azureStorageUriExpirationDateTime": "2017-01-01T00:00:08.4940464-08:00",
  "manifest": "bWFuaWZlc3Q=",
  "uploadState": "transientError"
}
```



