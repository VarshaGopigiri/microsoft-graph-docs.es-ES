---
title: Crear mobileAppContentFile
description: Cree un objeto mobileAppContentFile.
ms.openlocfilehash: 1095e9f5b69cb01416a980a29871423b14bfba80
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032366"
---
# <a name="create-mobileappcontentfile"></a><span data-ttu-id="961bd-103">Crear mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="961bd-103">Create mobileAppContentFile</span></span>

> <span data-ttu-id="961bd-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="961bd-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="961bd-105">Cree un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="961bd-105">Create a new [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="961bd-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="961bd-106">Prerequisites</span></span>
<span data-ttu-id="961bd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="961bd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="961bd-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="961bd-109">Permission type</span></span>|<span data-ttu-id="961bd-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="961bd-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="961bd-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="961bd-111">Delegated (work or school account)</span></span>|<span data-ttu-id="961bd-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="961bd-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="961bd-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="961bd-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="961bd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="961bd-114">Not supported.</span></span>|
|<span data-ttu-id="961bd-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="961bd-115">Application</span></span>|<span data-ttu-id="961bd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="961bd-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="961bd-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="961bd-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
```

## <a name="request-headers"></a><span data-ttu-id="961bd-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="961bd-118">Request headers</span></span>
|<span data-ttu-id="961bd-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="961bd-119">Header</span></span>|<span data-ttu-id="961bd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="961bd-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="961bd-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="961bd-121">Authorization</span></span>|<span data-ttu-id="961bd-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="961bd-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="961bd-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="961bd-123">Accept</span></span>|<span data-ttu-id="961bd-124">application/json</span><span class="sxs-lookup"><span data-stu-id="961bd-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="961bd-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="961bd-125">Request body</span></span>
<span data-ttu-id="961bd-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="961bd-126">In the request body, supply a JSON representation for the mobileAppContentFile object.</span></span>

<span data-ttu-id="961bd-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="961bd-127">The following table shows the properties that are required when you create the mobileAppContentFile.</span></span>

|<span data-ttu-id="961bd-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="961bd-128">Property</span></span>|<span data-ttu-id="961bd-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="961bd-129">Type</span></span>|<span data-ttu-id="961bd-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="961bd-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="961bd-131">azureStorageUri</span><span class="sxs-lookup"><span data-stu-id="961bd-131">azureStorageUri</span></span>|<span data-ttu-id="961bd-132">String</span><span class="sxs-lookup"><span data-stu-id="961bd-132">String</span></span>|<span data-ttu-id="961bd-133">El URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="961bd-133">The Azure Storage URI.</span></span>|
|<span data-ttu-id="961bd-134">isCommitted</span><span class="sxs-lookup"><span data-stu-id="961bd-134">isCommitted</span></span>|<span data-ttu-id="961bd-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="961bd-135">Boolean</span></span>|<span data-ttu-id="961bd-136">Un valor que indica si el archivo está confirmado.</span><span class="sxs-lookup"><span data-stu-id="961bd-136">A value indicating whether the file is committed.</span></span>|
|<span data-ttu-id="961bd-137">id</span><span class="sxs-lookup"><span data-stu-id="961bd-137">id</span></span>|<span data-ttu-id="961bd-138">String</span><span class="sxs-lookup"><span data-stu-id="961bd-138">String</span></span>|<span data-ttu-id="961bd-139">El Id. de archivo.</span><span class="sxs-lookup"><span data-stu-id="961bd-139">The File Id.</span></span>|
|<span data-ttu-id="961bd-140">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="961bd-140">createdDateTime</span></span>|<span data-ttu-id="961bd-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="961bd-141">DateTimeOffset</span></span>|<span data-ttu-id="961bd-142">La hora en que se ha creado el archivo.</span><span class="sxs-lookup"><span data-stu-id="961bd-142">The time the file was created.</span></span>|
|<span data-ttu-id="961bd-143">name</span><span class="sxs-lookup"><span data-stu-id="961bd-143">name</span></span>|<span data-ttu-id="961bd-144">String</span><span class="sxs-lookup"><span data-stu-id="961bd-144">String</span></span>|<span data-ttu-id="961bd-145">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="961bd-145">the file name.</span></span>|
|<span data-ttu-id="961bd-146">size</span><span class="sxs-lookup"><span data-stu-id="961bd-146">size</span></span>|<span data-ttu-id="961bd-147">Int64</span><span class="sxs-lookup"><span data-stu-id="961bd-147">Int64</span></span>|<span data-ttu-id="961bd-148">El tamaño del archivo antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="961bd-148">The size of the file prior to encryption.</span></span>|
|<span data-ttu-id="961bd-149">sizeEncrypted</span><span class="sxs-lookup"><span data-stu-id="961bd-149">sizeEncrypted</span></span>|<span data-ttu-id="961bd-150">Int64</span><span class="sxs-lookup"><span data-stu-id="961bd-150">Int64</span></span>|<span data-ttu-id="961bd-151">El tamaño del archivo después del cifrado.</span><span class="sxs-lookup"><span data-stu-id="961bd-151">The size of the file after encryption.</span></span>|
|<span data-ttu-id="961bd-152">azureStorageUriExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="961bd-152">azureStorageUriExpirationDateTime</span></span>|<span data-ttu-id="961bd-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="961bd-153">DateTimeOffset</span></span>|<span data-ttu-id="961bd-154">La hora en que expira el URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="961bd-154">The time the Azure storage Uri expires.</span></span>|
|<span data-ttu-id="961bd-155">manifiesto</span><span class="sxs-lookup"><span data-stu-id="961bd-155">manifest</span></span>|<span data-ttu-id="961bd-156">Binario</span><span class="sxs-lookup"><span data-stu-id="961bd-156">Binary</span></span>|<span data-ttu-id="961bd-157">La información del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="961bd-157">The manifest information.</span></span>|
|<span data-ttu-id="961bd-158">uploadState</span><span class="sxs-lookup"><span data-stu-id="961bd-158">uploadState</span></span>|[<span data-ttu-id="961bd-159">mobileAppContentFileUploadState</span><span class="sxs-lookup"><span data-stu-id="961bd-159">mobileAppContentFileUploadState</span></span>](../resources/intune-apps-mobileappcontentfileuploadstate.md)|<span data-ttu-id="961bd-160">El estado de la solicitud de carga actual.</span><span class="sxs-lookup"><span data-stu-id="961bd-160">The state of the current upload request.</span></span> <span data-ttu-id="961bd-161">Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed` y `commitFileTimedOut`.</span><span class="sxs-lookup"><span data-stu-id="961bd-161">Possible values are: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span></span>|



## <a name="response"></a><span data-ttu-id="961bd-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="961bd-162">Response</span></span>
<span data-ttu-id="961bd-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="961bd-163">If successful, this method returns a `201 Created` response code and a [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="961bd-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="961bd-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="961bd-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="961bd-165">Request</span></span>
<span data-ttu-id="961bd-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="961bd-166">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="961bd-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="961bd-167">Response</span></span>
<span data-ttu-id="961bd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="961bd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


