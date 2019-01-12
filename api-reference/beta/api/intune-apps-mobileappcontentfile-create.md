---
title: Crear mobileAppContentFile
description: Cree un objeto mobileAppContentFile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 712af333021d02ca043771b79ad88b493a3b1ae3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974987"
---
# <a name="create-mobileappcontentfile"></a><span data-ttu-id="433f3-103">Crear mobileAppContentFile</span><span class="sxs-lookup"><span data-stu-id="433f3-103">Create mobileAppContentFile</span></span>

> <span data-ttu-id="433f3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="433f3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="433f3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="433f3-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="433f3-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="433f3-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="433f3-107">Cree un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md).</span><span class="sxs-lookup"><span data-stu-id="433f3-107">Create a new [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="433f3-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="433f3-108">Prerequisites</span></span>
<span data-ttu-id="433f3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="433f3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="433f3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="433f3-111">Permission type</span></span>|<span data-ttu-id="433f3-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="433f3-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="433f3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="433f3-113">Delegated (work or school account)</span></span>|<span data-ttu-id="433f3-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="433f3-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="433f3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="433f3-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="433f3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="433f3-116">Not supported.</span></span>|
|<span data-ttu-id="433f3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="433f3-117">Application</span></span>|<span data-ttu-id="433f3-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="433f3-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="433f3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="433f3-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
```

## <a name="request-headers"></a><span data-ttu-id="433f3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="433f3-120">Request headers</span></span>
|<span data-ttu-id="433f3-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="433f3-121">Header</span></span>|<span data-ttu-id="433f3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="433f3-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="433f3-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="433f3-123">Authorization</span></span>|<span data-ttu-id="433f3-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="433f3-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="433f3-125">Accept</span><span class="sxs-lookup"><span data-stu-id="433f3-125">Accept</span></span>|<span data-ttu-id="433f3-126">application/json</span><span class="sxs-lookup"><span data-stu-id="433f3-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="433f3-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="433f3-127">Request body</span></span>
<span data-ttu-id="433f3-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="433f3-128">In the request body, supply a JSON representation for the mobileAppContentFile object.</span></span>

<span data-ttu-id="433f3-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="433f3-129">The following table shows the properties that are required when you create the mobileAppContentFile.</span></span>

|<span data-ttu-id="433f3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="433f3-130">Property</span></span>|<span data-ttu-id="433f3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="433f3-131">Type</span></span>|<span data-ttu-id="433f3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="433f3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="433f3-133">azureStorageUri</span><span class="sxs-lookup"><span data-stu-id="433f3-133">azureStorageUri</span></span>|<span data-ttu-id="433f3-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="433f3-134">String</span></span>|<span data-ttu-id="433f3-135">El URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="433f3-135">The Azure Storage URI.</span></span>|
|<span data-ttu-id="433f3-136">isCommitted</span><span class="sxs-lookup"><span data-stu-id="433f3-136">isCommitted</span></span>|<span data-ttu-id="433f3-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="433f3-137">Boolean</span></span>|<span data-ttu-id="433f3-138">Un valor que indica si el archivo está confirmado.</span><span class="sxs-lookup"><span data-stu-id="433f3-138">A value indicating whether the file is committed.</span></span>|
|<span data-ttu-id="433f3-139">id</span><span class="sxs-lookup"><span data-stu-id="433f3-139">id</span></span>|<span data-ttu-id="433f3-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="433f3-140">String</span></span>|<span data-ttu-id="433f3-141">El Id. de archivo.</span><span class="sxs-lookup"><span data-stu-id="433f3-141">The File Id.</span></span>|
|<span data-ttu-id="433f3-142">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="433f3-142">createdDateTime</span></span>|<span data-ttu-id="433f3-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="433f3-143">DateTimeOffset</span></span>|<span data-ttu-id="433f3-144">La hora en que se ha creado el archivo.</span><span class="sxs-lookup"><span data-stu-id="433f3-144">The time the file was created.</span></span>|
|<span data-ttu-id="433f3-145">name</span><span class="sxs-lookup"><span data-stu-id="433f3-145">name</span></span>|<span data-ttu-id="433f3-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="433f3-146">String</span></span>|<span data-ttu-id="433f3-147">El nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="433f3-147">the file name.</span></span>|
|<span data-ttu-id="433f3-148">size</span><span class="sxs-lookup"><span data-stu-id="433f3-148">size</span></span>|<span data-ttu-id="433f3-149">Int64</span><span class="sxs-lookup"><span data-stu-id="433f3-149">Int64</span></span>|<span data-ttu-id="433f3-150">El tamaño del archivo antes del cifrado.</span><span class="sxs-lookup"><span data-stu-id="433f3-150">The size of the file prior to encryption.</span></span>|
|<span data-ttu-id="433f3-151">sizeEncrypted</span><span class="sxs-lookup"><span data-stu-id="433f3-151">sizeEncrypted</span></span>|<span data-ttu-id="433f3-152">Int64</span><span class="sxs-lookup"><span data-stu-id="433f3-152">Int64</span></span>|<span data-ttu-id="433f3-153">El tamaño del archivo después del cifrado.</span><span class="sxs-lookup"><span data-stu-id="433f3-153">The size of the file after encryption.</span></span>|
|<span data-ttu-id="433f3-154">azureStorageUriExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="433f3-154">azureStorageUriExpirationDateTime</span></span>|<span data-ttu-id="433f3-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="433f3-155">DateTimeOffset</span></span>|<span data-ttu-id="433f3-156">La hora en que expira el URI de Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="433f3-156">The time the Azure storage Uri expires.</span></span>|
|<span data-ttu-id="433f3-157">manifiesto</span><span class="sxs-lookup"><span data-stu-id="433f3-157">manifest</span></span>|<span data-ttu-id="433f3-158">Binario</span><span class="sxs-lookup"><span data-stu-id="433f3-158">Binary</span></span>|<span data-ttu-id="433f3-159">La información del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="433f3-159">The manifest information.</span></span>|
|<span data-ttu-id="433f3-160">uploadState</span><span class="sxs-lookup"><span data-stu-id="433f3-160">uploadState</span></span>|[<span data-ttu-id="433f3-161">mobileAppContentFileUploadState</span><span class="sxs-lookup"><span data-stu-id="433f3-161">mobileAppContentFileUploadState</span></span>](../resources/intune-apps-mobileappcontentfileuploadstate.md)|<span data-ttu-id="433f3-162">El estado de la solicitud de carga actual.</span><span class="sxs-lookup"><span data-stu-id="433f3-162">The state of the current upload request.</span></span> <span data-ttu-id="433f3-163">Los valores posibles son: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed` y `commitFileTimedOut`.</span><span class="sxs-lookup"><span data-stu-id="433f3-163">Possible values are: `success`, `transientError`, `error`, `unknown`, `azureStorageUriRequestSuccess`, `azureStorageUriRequestPending`, `azureStorageUriRequestFailed`, `azureStorageUriRequestTimedOut`, `azureStorageUriRenewalSuccess`, `azureStorageUriRenewalPending`, `azureStorageUriRenewalFailed`, `azureStorageUriRenewalTimedOut`, `commitFileSuccess`, `commitFilePending`, `commitFileFailed`, `commitFileTimedOut`.</span></span>|
|<span data-ttu-id="433f3-164">isFrameworkFile</span><span class="sxs-lookup"><span data-stu-id="433f3-164">isFrameworkFile</span></span>|<span data-ttu-id="433f3-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="433f3-165">Boolean</span></span>|<span data-ttu-id="433f3-166">Un valor que indica si el archivo es un archivo de framework.</span><span class="sxs-lookup"><span data-stu-id="433f3-166">A value indicating whether the file is a framework file.</span></span>|
|<span data-ttu-id="433f3-167">isDependency</span><span class="sxs-lookup"><span data-stu-id="433f3-167">isDependency</span></span>|<span data-ttu-id="433f3-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="433f3-168">Boolean</span></span>|<span data-ttu-id="433f3-169">Si el archivo de contenido es una dependencia para el archivo de contenido principal.</span><span class="sxs-lookup"><span data-stu-id="433f3-169">Whether the content file is a dependency for the main content file.</span></span>|



## <a name="response"></a><span data-ttu-id="433f3-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="433f3-170">Response</span></span>
<span data-ttu-id="433f3-171">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="433f3-171">If successful, this method returns a `201 Created` response code and a [mobileAppContentFile](../resources/intune-apps-mobileappcontentfile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="433f3-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="433f3-172">Example</span></span>
### <a name="request"></a><span data-ttu-id="433f3-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="433f3-173">Request</span></span>
<span data-ttu-id="433f3-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="433f3-174">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/files
Content-type: application/json
Content-length: 395

{
  "@odata.type": "#microsoft.graph.mobileAppContentFile",
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

### <a name="response"></a><span data-ttu-id="433f3-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="433f3-175">Response</span></span>
<span data-ttu-id="433f3-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="433f3-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





