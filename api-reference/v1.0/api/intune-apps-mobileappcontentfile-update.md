---
title: Actualizar mobileAppContentFile
description: Actualice las propiedades de un objeto mobileAppContentFile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ee36235a7de5e08b90959b2abaa83ac370371f55
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811252"
---
# <a name="update-mobileappcontentfile"></a><span data-ttu-id="51457-103">Actualizar mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="51457-103">Update mobileAppContentFile</span></span>

> <span data-ttu-id="51457-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="51457-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="51457-105">Actualice las propiedades de un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="51457-105">Update the properties of a [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="51457-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="51457-106">Prerequisites</span></span>
<span data-ttu-id="51457-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="51457-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="51457-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="51457-109">Permission type</span></span>|<span data-ttu-id="51457-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="51457-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="51457-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="51457-111">Delegated (work or school account)</span></span>|<span data-ttu-id="51457-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="51457-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="51457-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="51457-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="51457-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51457-114">Not supported.</span></span>|
|<span data-ttu-id="51457-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="51457-115">Application</span></span>|<span data-ttu-id="51457-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="51457-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="51457-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="51457-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
```

## <a name="request-headers"></a><span data-ttu-id="51457-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="51457-118">Request headers</span></span>
|<span data-ttu-id="51457-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="51457-119">Header</span></span>|<span data-ttu-id="51457-120">Valor</span><span class="sxs-lookup"><span data-stu-id="51457-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="51457-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="51457-121">Authorization</span></span>|<span data-ttu-id="51457-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="51457-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="51457-123">Accept</span><span class="sxs-lookup"><span data-stu-id="51457-123">Accept</span></span>|<span data-ttu-id="51457-124">application/json</span><span class="sxs-lookup"><span data-stu-id="51457-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="51457-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51457-125">Request body</span></span>
<span data-ttu-id="51457-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="51457-126">In the request body, supply a JSON representation for the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>

<span data-ttu-id="51457-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="51457-127">The following table shows the properties that are required when you create the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span></span>

|<span data-ttu-id="51457-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="51457-128">Property</span></span>|<span data-ttu-id="51457-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="51457-129">Type</span></span>|<span data-ttu-id="51457-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="51457-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="51457-131">azureStorageUri</span><span class="sxs-lookup"><span data-stu-id="51457-131">azureStorageUri</span></span>|<span data-ttu-id="51457-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="51457-132">String</span></span>|<span data-ttu-id="51457-133">El URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="51457-133">The Azure Storage URI.</span></span>|
|<span data-ttu-id="51457-134">isCommitted</span><span class="sxs-lookup"><span data-stu-id="51457-134">isCommitted</span></span>|<span data-ttu-id="51457-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="51457-135">Boolean</span></span>|<span data-ttu-id="51457-136">Un valor que indica si el archivo está confirmado.</span><span class="sxs-lookup"><span data-stu-id="51457-136">A value indicating whether the file is committed.</span></span>|
|<span data-ttu-id="51457-137">id</span><span class="sxs-lookup"><span data-stu-id="51457-137">id</span></span>|<span data-ttu-id="51457-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="51457-138">String</span></span>|<span data-ttu-id="51457-139">El Id. de archivo.</span><span class="sxs-lookup"><span data-stu-id="51457-139">The File Id.</span></span>|
|<span data-ttu-id="51457-140">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="51457-140">createdDateTime</span></span>|<span data-ttu-id="51457-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="51457-141">DateTimeOffset</span></span>|<span data-ttu-id="51457-142">La hora en que se ha creado el archivo.</span><span class="sxs-lookup"><span data-stu-id="51457-142">The time the file was created.</span></span>|
|<span data-ttu-id="51457-143">name</span><span class="sxs-lookup"><span data-stu-id="51457-143">name</span></span>|<span data-ttu-id="51457-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="51457-144">String</span></span>|<span data-ttu-id="51457-145">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="51457-145">the file name.</span></span>|
|<span data-ttu-id="51457-146">size</span><span class="sxs-lookup"><span data-stu-id="51457-146">size</span></span>|<span data-ttu-id="51457-147">Int64</span><span class="sxs-lookup"><span data-stu-id="51457-147">Int64</span></span>|<span data-ttu-id="51457-148">El tamaño del archivo antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="51457-148">The size of the file prior to encryption.</span></span>|
|<span data-ttu-id="51457-149">sizeEncrypted</span><span class="sxs-lookup"><span data-stu-id="51457-149">sizeEncrypted</span></span>|<span data-ttu-id="51457-150">Int64</span><span class="sxs-lookup"><span data-stu-id="51457-150">Int64</span></span>|<span data-ttu-id="51457-151">El tamaño del archivo después del cifrado.</span><span class="sxs-lookup"><span data-stu-id="51457-151">The size of the file after encryption.</span></span>|
|<span data-ttu-id="51457-152">azureStorageUriExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="51457-152">azureStorageUriExpirationDateTime</span></span>|<span data-ttu-id="51457-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="51457-153">DateTimeOffset</span></span>|<span data-ttu-id="51457-154">La hora en que expira el URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="51457-154">The time the Azure storage Uri expires.</span></span>|
|<span data-ttu-id="51457-155">manifiesto</span><span class="sxs-lookup"><span data-stu-id="51457-155">manifest</span></span>|<span data-ttu-id="51457-156">Binario</span><span class="sxs-lookup"><span data-stu-id="51457-156">Binary</span></span>|<span data-ttu-id="51457-157">La información del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="51457-157">The manifest information.</span></span>|
|<span data-ttu-id="51457-158">uploadState</span><span class="sxs-lookup"><span data-stu-id="51457-158">uploadState</span></span>|[<span data-ttu-id="51457-159">mobileAppContentFileUploadState</span><span class="sxs-lookup"><span data-stu-id="51457-159">mobileAppContentFileUploadState</span></span>](../resources/intune-apps-mobileappcontentfileuploadstate.md)|<span data-ttu-id="51457-160">El estado de la solicitud de carga actual.</span><span class="sxs-lookup"><span data-stu-id="51457-160">The state of the current upload request.</span></span> <span data-ttu-id="51457-161">Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed` y `commitFileTimedOut`.</span><span class="sxs-lookup"><span data-stu-id="51457-161">Possible values are: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span></span>|



## <a name="response"></a><span data-ttu-id="51457-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51457-162">Response</span></span>
<span data-ttu-id="51457-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="51457-163">If successful, this method returns a `200 OK` response code and an updated [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="51457-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="51457-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="51457-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="51457-165">Request</span></span>
<span data-ttu-id="51457-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="51457-166">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="51457-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="51457-167">Response</span></span>
<span data-ttu-id="51457-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="51457-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



