---
title: Actualizar mobileAppContentFile
description: Actualice las propiedades de un objeto mobileAppContentFile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8db4e9544e044f004e3524bf0a0df9af9360f342
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27944547"
---
# <a name="update-mobileappcontentfile"></a><span data-ttu-id="e3b88-103">Actualizar mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="e3b88-103">Update mobileAppContentFile</span></span>

> <span data-ttu-id="e3b88-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e3b88-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e3b88-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e3b88-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e3b88-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e3b88-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e3b88-107">Actualice las propiedades de un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="e3b88-107">Update the properties of a [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e3b88-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e3b88-108">Prerequisites</span></span>
<span data-ttu-id="e3b88-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3b88-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e3b88-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3b88-111">Permission type</span></span>|<span data-ttu-id="e3b88-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3b88-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e3b88-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3b88-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e3b88-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3b88-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="e3b88-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3b88-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e3b88-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3b88-116">Not supported.</span></span>|
|<span data-ttu-id="e3b88-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3b88-117">Application</span></span>|<span data-ttu-id="e3b88-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3b88-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e3b88-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3b88-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
```

## <a name="request-headers"></a><span data-ttu-id="e3b88-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3b88-120">Request headers</span></span>
|<span data-ttu-id="e3b88-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3b88-121">Header</span></span>|<span data-ttu-id="e3b88-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e3b88-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e3b88-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e3b88-123">Authorization</span></span>|<span data-ttu-id="e3b88-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e3b88-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e3b88-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e3b88-125">Accept</span></span>|<span data-ttu-id="e3b88-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e3b88-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e3b88-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3b88-127">Request body</span></span>
<span data-ttu-id="e3b88-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="e3b88-128">In the request body, supply a JSON representation for the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>

<span data-ttu-id="e3b88-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="e3b88-129">The following table shows the properties that are required when you create the [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span></span>

|<span data-ttu-id="e3b88-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3b88-130">Property</span></span>|<span data-ttu-id="e3b88-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3b88-131">Type</span></span>|<span data-ttu-id="e3b88-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3b88-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e3b88-133">azureStorageUri</span><span class="sxs-lookup"><span data-stu-id="e3b88-133">azureStorageUri</span></span>|<span data-ttu-id="e3b88-134">String</span><span class="sxs-lookup"><span data-stu-id="e3b88-134">String</span></span>|<span data-ttu-id="e3b88-135">El URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e3b88-135">The Azure Storage URI.</span></span>|
|<span data-ttu-id="e3b88-136">isCommitted</span><span class="sxs-lookup"><span data-stu-id="e3b88-136">isCommitted</span></span>|<span data-ttu-id="e3b88-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3b88-137">Boolean</span></span>|<span data-ttu-id="e3b88-138">Un valor que indica si el archivo está confirmado.</span><span class="sxs-lookup"><span data-stu-id="e3b88-138">A value indicating whether the file is committed.</span></span>|
|<span data-ttu-id="e3b88-139">id</span><span class="sxs-lookup"><span data-stu-id="e3b88-139">id</span></span>|<span data-ttu-id="e3b88-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="e3b88-140">String</span></span>|<span data-ttu-id="e3b88-141">El Id. de archivo.</span><span class="sxs-lookup"><span data-stu-id="e3b88-141">The File Id.</span></span>|
|<span data-ttu-id="e3b88-142">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e3b88-142">createdDateTime</span></span>|<span data-ttu-id="e3b88-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3b88-143">DateTimeOffset</span></span>|<span data-ttu-id="e3b88-144">La hora en que se ha creado el archivo.</span><span class="sxs-lookup"><span data-stu-id="e3b88-144">The time the file was created.</span></span>|
|<span data-ttu-id="e3b88-145">name</span><span class="sxs-lookup"><span data-stu-id="e3b88-145">name</span></span>|<span data-ttu-id="e3b88-146">String</span><span class="sxs-lookup"><span data-stu-id="e3b88-146">String</span></span>|<span data-ttu-id="e3b88-147">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="e3b88-147">the file name.</span></span>|
|<span data-ttu-id="e3b88-148">size</span><span class="sxs-lookup"><span data-stu-id="e3b88-148">size</span></span>|<span data-ttu-id="e3b88-149">Int64</span><span class="sxs-lookup"><span data-stu-id="e3b88-149">Int64</span></span>|<span data-ttu-id="e3b88-150">El tamaño del archivo antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="e3b88-150">The size of the file prior to encryption.</span></span>|
|<span data-ttu-id="e3b88-151">sizeEncrypted</span><span class="sxs-lookup"><span data-stu-id="e3b88-151">sizeEncrypted</span></span>|<span data-ttu-id="e3b88-152">Int64</span><span class="sxs-lookup"><span data-stu-id="e3b88-152">Int64</span></span>|<span data-ttu-id="e3b88-153">El tamaño del archivo después del cifrado.</span><span class="sxs-lookup"><span data-stu-id="e3b88-153">The size of the file after encryption.</span></span>|
|<span data-ttu-id="e3b88-154">azureStorageUriExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e3b88-154">azureStorageUriExpirationDateTime</span></span>|<span data-ttu-id="e3b88-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3b88-155">DateTimeOffset</span></span>|<span data-ttu-id="e3b88-156">La hora en que expira el URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="e3b88-156">The time the Azure storage Uri expires.</span></span>|
|<span data-ttu-id="e3b88-157">manifiesto</span><span class="sxs-lookup"><span data-stu-id="e3b88-157">manifest</span></span>|<span data-ttu-id="e3b88-158">Binario</span><span class="sxs-lookup"><span data-stu-id="e3b88-158">Binary</span></span>|<span data-ttu-id="e3b88-159">La información del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="e3b88-159">The manifest information.</span></span>|
|<span data-ttu-id="e3b88-160">uploadState</span><span class="sxs-lookup"><span data-stu-id="e3b88-160">uploadState</span></span>|[<span data-ttu-id="e3b88-161">mobileAppContentFileUploadState</span><span class="sxs-lookup"><span data-stu-id="e3b88-161">mobileAppContentFileUploadState</span></span>](../resources/intune-apps-mobileappcontentfileuploadstate.md)|<span data-ttu-id="e3b88-162">El estado de la solicitud de carga actual.</span><span class="sxs-lookup"><span data-stu-id="e3b88-162">The state of the current upload request.</span></span> <span data-ttu-id="e3b88-163">Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed` y `commitFileTimedOut`.</span><span class="sxs-lookup"><span data-stu-id="e3b88-163">Possible values are: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span></span>|
|<span data-ttu-id="e3b88-164">isFrameworkFile</span><span class="sxs-lookup"><span data-stu-id="e3b88-164">isFrameworkFile</span></span>|<span data-ttu-id="e3b88-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3b88-165">Boolean</span></span>|<span data-ttu-id="e3b88-166">Un valor que indica si el archivo es un archivo de framework.</span><span class="sxs-lookup"><span data-stu-id="e3b88-166">A value indicating whether the file is a framework file.</span></span>|
|<span data-ttu-id="e3b88-167">isDependency</span><span class="sxs-lookup"><span data-stu-id="e3b88-167">isDependency</span></span>|<span data-ttu-id="e3b88-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3b88-168">Boolean</span></span>|<span data-ttu-id="e3b88-169">Si el archivo de contenido es una dependencia para el archivo de contenido principal.</span><span class="sxs-lookup"><span data-stu-id="e3b88-169">Whether the content file is a dependency for the main content file.</span></span>|



## <a name="response"></a><span data-ttu-id="e3b88-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3b88-170">Response</span></span>
<span data-ttu-id="e3b88-171">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3b88-171">If successful, this method returns a `200 OK` response code and an updated [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3b88-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3b88-172">Example</span></span>
### <a name="request"></a><span data-ttu-id="e3b88-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3b88-173">Request</span></span>
<span data-ttu-id="e3b88-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3b88-174">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files/{mobileAppContentFileId}
Content-type: application/json
Content-length: 336

{
  "azureStorageUri": "Azure Storage Uri value",
  "isCommitted": true,
  "name": "Name value",
  "size": 4,
  "sizeEncrypted": 13,
  "azureStorageUriExpirationDateTime": "2017-01-01T00:00:08.4940464-08:00",
  "manifest": "bWFuaWZlc3Q=",
  "uploadState": "transientError",
  "isFrameworkFile": true,
  "isDependency": true
}
```

### <a name="response"></a><span data-ttu-id="e3b88-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3b88-175">Response</span></span>
<span data-ttu-id="e3b88-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e3b88-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 503

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
  "uploadState": "transientError",
  "isFrameworkFile": true,
  "isDependency": true
}
```





