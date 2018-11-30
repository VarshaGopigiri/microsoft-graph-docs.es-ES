---
title: Actualizar mobileAppContentFile
description: Actualice las propiedades de un objeto mobileAppContentFile.
ms.openlocfilehash: b3a25c3ccce6598f12d6742546cca0f61679a138
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029277"
---
# <a name="update-mobileappcontentfile"></a><span data-ttu-id="f87fc-103">Actualizar mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="f87fc-103">Update mobileAppContentFile</span></span>

> <span data-ttu-id="f87fc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f87fc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f87fc-105">Actualice las propiedades de un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="f87fc-105">Update the properties of a [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f87fc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f87fc-106">Prerequisites</span></span>
<span data-ttu-id="f87fc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f87fc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f87fc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f87fc-109">Permission type</span></span>|<span data-ttu-id="f87fc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f87fc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f87fc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f87fc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f87fc-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f87fc-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f87fc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f87fc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f87fc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f87fc-114">Not supported.</span></span>|
|<span data-ttu-id="f87fc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f87fc-115">Application</span></span>|<span data-ttu-id="f87fc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f87fc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f87fc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f87fc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
```

## <a name="request-headers"></a><span data-ttu-id="f87fc-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f87fc-118">Request headers</span></span>
|<span data-ttu-id="f87fc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f87fc-119">Header</span></span>|<span data-ttu-id="f87fc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f87fc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f87fc-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f87fc-121">Authorization</span></span>|<span data-ttu-id="f87fc-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f87fc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f87fc-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f87fc-123">Accept</span></span>|<span data-ttu-id="f87fc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f87fc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f87fc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f87fc-125">Request body</span></span>
<span data-ttu-id="f87fc-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="f87fc-126">In the request body, supply a JSON representation for the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>

<span data-ttu-id="f87fc-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="f87fc-127">The following table shows the properties that are required when you create the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span></span>

|<span data-ttu-id="f87fc-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f87fc-128">Property</span></span>|<span data-ttu-id="f87fc-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f87fc-129">Type</span></span>|<span data-ttu-id="f87fc-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f87fc-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f87fc-131">azureStorageUri</span><span class="sxs-lookup"><span data-stu-id="f87fc-131">azureStorageUri</span></span>|<span data-ttu-id="f87fc-132">String</span><span class="sxs-lookup"><span data-stu-id="f87fc-132">String</span></span>|<span data-ttu-id="f87fc-133">El URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f87fc-133">The Azure Storage URI.</span></span>|
|<span data-ttu-id="f87fc-134">isCommitted</span><span class="sxs-lookup"><span data-stu-id="f87fc-134">isCommitted</span></span>|<span data-ttu-id="f87fc-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="f87fc-135">Boolean</span></span>|<span data-ttu-id="f87fc-136">Un valor que indica si el archivo está confirmado.</span><span class="sxs-lookup"><span data-stu-id="f87fc-136">A value indicating whether the file is committed.</span></span>|
|<span data-ttu-id="f87fc-137">id</span><span class="sxs-lookup"><span data-stu-id="f87fc-137">id</span></span>|<span data-ttu-id="f87fc-138">String</span><span class="sxs-lookup"><span data-stu-id="f87fc-138">String</span></span>|<span data-ttu-id="f87fc-139">El Id. de archivo.</span><span class="sxs-lookup"><span data-stu-id="f87fc-139">The File Id.</span></span>|
|<span data-ttu-id="f87fc-140">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f87fc-140">createdDateTime</span></span>|<span data-ttu-id="f87fc-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f87fc-141">DateTimeOffset</span></span>|<span data-ttu-id="f87fc-142">La hora en que se ha creado el archivo.</span><span class="sxs-lookup"><span data-stu-id="f87fc-142">The time the file was created.</span></span>|
|<span data-ttu-id="f87fc-143">name</span><span class="sxs-lookup"><span data-stu-id="f87fc-143">name</span></span>|<span data-ttu-id="f87fc-144">String</span><span class="sxs-lookup"><span data-stu-id="f87fc-144">String</span></span>|<span data-ttu-id="f87fc-145">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="f87fc-145">the file name.</span></span>|
|<span data-ttu-id="f87fc-146">size</span><span class="sxs-lookup"><span data-stu-id="f87fc-146">size</span></span>|<span data-ttu-id="f87fc-147">Int64</span><span class="sxs-lookup"><span data-stu-id="f87fc-147">Int64</span></span>|<span data-ttu-id="f87fc-148">El tamaño del archivo antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="f87fc-148">The size of the file prior to encryption.</span></span>|
|<span data-ttu-id="f87fc-149">sizeEncrypted</span><span class="sxs-lookup"><span data-stu-id="f87fc-149">sizeEncrypted</span></span>|<span data-ttu-id="f87fc-150">Int64</span><span class="sxs-lookup"><span data-stu-id="f87fc-150">Int64</span></span>|<span data-ttu-id="f87fc-151">El tamaño del archivo después del cifrado.</span><span class="sxs-lookup"><span data-stu-id="f87fc-151">The size of the file after encryption.</span></span>|
|<span data-ttu-id="f87fc-152">azureStorageUriExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="f87fc-152">azureStorageUriExpirationDateTime</span></span>|<span data-ttu-id="f87fc-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f87fc-153">DateTimeOffset</span></span>|<span data-ttu-id="f87fc-154">La hora en que expira el URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="f87fc-154">The time the Azure storage Uri expires.</span></span>|
|<span data-ttu-id="f87fc-155">manifiesto</span><span class="sxs-lookup"><span data-stu-id="f87fc-155">manifest</span></span>|<span data-ttu-id="f87fc-156">Binario</span><span class="sxs-lookup"><span data-stu-id="f87fc-156">Binary</span></span>|<span data-ttu-id="f87fc-157">La información del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="f87fc-157">The manifest information.</span></span>|
|<span data-ttu-id="f87fc-158">uploadState</span><span class="sxs-lookup"><span data-stu-id="f87fc-158">uploadState</span></span>|[<span data-ttu-id="f87fc-159">mobileAppContentFileUploadState</span><span class="sxs-lookup"><span data-stu-id="f87fc-159">mobileAppContentFileUploadState</span></span>](../resources/intune-apps-mobileappcontentfileuploadstate.md)|<span data-ttu-id="f87fc-160">El estado de la solicitud de carga actual.</span><span class="sxs-lookup"><span data-stu-id="f87fc-160">The state of the current upload request.</span></span> <span data-ttu-id="f87fc-161">Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed` y `commitFileTimedOut`.</span><span class="sxs-lookup"><span data-stu-id="f87fc-161">Possible values are: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span></span>|



## <a name="response"></a><span data-ttu-id="f87fc-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f87fc-162">Response</span></span>
<span data-ttu-id="f87fc-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f87fc-163">If successful, this method returns a `200 OK` response code and an updated [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f87fc-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f87fc-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="f87fc-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f87fc-165">Request</span></span>
<span data-ttu-id="f87fc-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f87fc-166">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
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

### <a name="response"></a><span data-ttu-id="f87fc-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f87fc-167">Response</span></span>
<span data-ttu-id="f87fc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f87fc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



