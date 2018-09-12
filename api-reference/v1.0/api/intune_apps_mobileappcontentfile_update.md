# <a name="update-mobileappcontentfile"></a><span data-ttu-id="46a24-101">Actualizar mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="46a24-101">Update mobileAppContentFile</span></span>

> <span data-ttu-id="46a24-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46a24-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46a24-103">Actualice las propiedades de un objeto [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="46a24-103">Update the properties of a [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46a24-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="46a24-104">Prerequisites</span></span>
<span data-ttu-id="46a24-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="46a24-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="46a24-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46a24-107">Permission type</span></span>|<span data-ttu-id="46a24-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46a24-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46a24-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46a24-109">Delegated (work or school account)</span></span>|<span data-ttu-id="46a24-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46a24-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="46a24-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46a24-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46a24-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46a24-112">Not supported.</span></span>|
|<span data-ttu-id="46a24-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46a24-113">Application</span></span>|<span data-ttu-id="46a24-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46a24-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46a24-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46a24-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
```

## <a name="request-headers"></a><span data-ttu-id="46a24-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46a24-116">Request headers</span></span>
|<span data-ttu-id="46a24-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46a24-117">Header</span></span>|<span data-ttu-id="46a24-118">Valor</span><span class="sxs-lookup"><span data-stu-id="46a24-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46a24-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="46a24-119">Authorization</span></span>|<span data-ttu-id="46a24-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="46a24-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46a24-121">Accept</span><span class="sxs-lookup"><span data-stu-id="46a24-121">Accept</span></span>|<span data-ttu-id="46a24-122">application/json</span><span class="sxs-lookup"><span data-stu-id="46a24-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46a24-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46a24-123">Request body</span></span>
<span data-ttu-id="46a24-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="46a24-124">In the request body, supply a JSON representation for the [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) object.</span></span>

<span data-ttu-id="46a24-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="46a24-125">The following table shows the properties that are required when you create the [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md).</span></span>

|<span data-ttu-id="46a24-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46a24-126">Property</span></span>|<span data-ttu-id="46a24-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a24-127">Type</span></span>|<span data-ttu-id="46a24-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a24-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46a24-129">azureStorageUri</span><span class="sxs-lookup"><span data-stu-id="46a24-129">azureStorageUri</span></span>|<span data-ttu-id="46a24-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="46a24-130">String</span></span>|<span data-ttu-id="46a24-131">El URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="46a24-131">The Azure Storage URI.</span></span>|
|<span data-ttu-id="46a24-132">isCommitted</span><span class="sxs-lookup"><span data-stu-id="46a24-132">isCommitted</span></span>|<span data-ttu-id="46a24-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="46a24-133">Boolean</span></span>|<span data-ttu-id="46a24-134">Un valor que indica si el archivo está confirmado.</span><span class="sxs-lookup"><span data-stu-id="46a24-134">A value indicating whether the file is committed.</span></span>|
|<span data-ttu-id="46a24-135">id</span><span class="sxs-lookup"><span data-stu-id="46a24-135">id</span></span>|<span data-ttu-id="46a24-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="46a24-136">String</span></span>|<span data-ttu-id="46a24-137">El Id. de archivo.</span><span class="sxs-lookup"><span data-stu-id="46a24-137">The File Id.</span></span>|
|<span data-ttu-id="46a24-138">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="46a24-138">createdDateTime</span></span>|<span data-ttu-id="46a24-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46a24-139">DateTimeOffset</span></span>|<span data-ttu-id="46a24-140">La hora en que se ha creado el archivo.</span><span class="sxs-lookup"><span data-stu-id="46a24-140">The time the file was created.</span></span>|
|<span data-ttu-id="46a24-141">name</span><span class="sxs-lookup"><span data-stu-id="46a24-141">name</span></span>|<span data-ttu-id="46a24-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="46a24-142">String</span></span>|<span data-ttu-id="46a24-143">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="46a24-143">the file name.</span></span>|
|<span data-ttu-id="46a24-144">size</span><span class="sxs-lookup"><span data-stu-id="46a24-144">size</span></span>|<span data-ttu-id="46a24-145">Int64</span><span class="sxs-lookup"><span data-stu-id="46a24-145">Int64</span></span>|<span data-ttu-id="46a24-146">El tamaño del archivo antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="46a24-146">The size of the file prior to encryption.</span></span>|
|<span data-ttu-id="46a24-147">sizeEncrypted</span><span class="sxs-lookup"><span data-stu-id="46a24-147">sizeEncrypted</span></span>|<span data-ttu-id="46a24-148">Int64</span><span class="sxs-lookup"><span data-stu-id="46a24-148">Int64</span></span>|<span data-ttu-id="46a24-149">El tamaño del archivo después del cifrado.</span><span class="sxs-lookup"><span data-stu-id="46a24-149">The size of the file after encryption.</span></span>|
|<span data-ttu-id="46a24-150">azureStorageUriExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="46a24-150">azureStorageUriExpirationDateTime</span></span>|<span data-ttu-id="46a24-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46a24-151">DateTimeOffset</span></span>|<span data-ttu-id="46a24-152">La hora en que expira el URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="46a24-152">The time the Azure storage Uri expires.</span></span>|
|<span data-ttu-id="46a24-153">manifiesto</span><span class="sxs-lookup"><span data-stu-id="46a24-153">manifest</span></span>|<span data-ttu-id="46a24-154">Binario</span><span class="sxs-lookup"><span data-stu-id="46a24-154">Binary</span></span>|<span data-ttu-id="46a24-155">La información del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="46a24-155">The manifest information.</span></span>|
|<span data-ttu-id="46a24-156">uploadState</span><span class="sxs-lookup"><span data-stu-id="46a24-156">uploadState</span></span>|[<span data-ttu-id="46a24-157">mobileAppContentFileUploadState</span><span class="sxs-lookup"><span data-stu-id="46a24-157">mobileAppContentFileUploadState</span></span>](../resources/intune_apps_mobileappcontentfileuploadstate.md)|<span data-ttu-id="46a24-p102">El estado de la solicitud de carga actual. Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span><span class="sxs-lookup"><span data-stu-id="46a24-p102">The state of the current upload request. The possible values are: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span></span>|



## <a name="response"></a><span data-ttu-id="46a24-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46a24-160">Response</span></span>
<span data-ttu-id="46a24-161">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46a24-161">If successful, this method returns a `200 OK` response code and an updated [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46a24-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46a24-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="46a24-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46a24-163">Request</span></span>
<span data-ttu-id="46a24-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46a24-164">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
Content-type: application/json
Content-length: 283

{
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

### <a name="response"></a><span data-ttu-id="46a24-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46a24-165">Response</span></span>
<span data-ttu-id="46a24-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46a24-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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








