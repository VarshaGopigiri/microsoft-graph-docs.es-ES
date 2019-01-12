---
title: Crear importedDeviceIdentity
description: Crear un nuevo objeto importedDeviceIdentity.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9e0efa7cdccd24f01539840beb3d0a53342323a7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930142"
---
# <a name="create-importeddeviceidentity"></a><span data-ttu-id="d776d-103">Crear importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="d776d-103">Create importedDeviceIdentity</span></span>

> <span data-ttu-id="d776d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d776d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d776d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d776d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d776d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d776d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d776d-107">Crear un nuevo objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="d776d-107">Create a new [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d776d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d776d-108">Prerequisites</span></span>
<span data-ttu-id="d776d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d776d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d776d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d776d-111">Permission type</span></span>|<span data-ttu-id="d776d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d776d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d776d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d776d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d776d-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d776d-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="d776d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d776d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d776d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d776d-116">Not supported.</span></span>|
|<span data-ttu-id="d776d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d776d-117">Application</span></span>|<span data-ttu-id="d776d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d776d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d776d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d776d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/importedDeviceIdentities
```

## <a name="request-headers"></a><span data-ttu-id="d776d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d776d-120">Request headers</span></span>
|<span data-ttu-id="d776d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d776d-121">Header</span></span>|<span data-ttu-id="d776d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d776d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d776d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="d776d-123">Authorization</span></span>|<span data-ttu-id="d776d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d776d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d776d-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d776d-125">Accept</span></span>|<span data-ttu-id="d776d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d776d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d776d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d776d-127">Request body</span></span>
<span data-ttu-id="d776d-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto importedDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="d776d-128">In the request body, supply a JSON representation for the importedDeviceIdentity object.</span></span>

<span data-ttu-id="d776d-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el importedDeviceIdentity.</span><span class="sxs-lookup"><span data-stu-id="d776d-129">The following table shows the properties that are required when you create the importedDeviceIdentity.</span></span>

|<span data-ttu-id="d776d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d776d-130">Property</span></span>|<span data-ttu-id="d776d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d776d-131">Type</span></span>|<span data-ttu-id="d776d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d776d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d776d-133">id</span><span class="sxs-lookup"><span data-stu-id="d776d-133">id</span></span>|<span data-ttu-id="d776d-134">String</span><span class="sxs-lookup"><span data-stu-id="d776d-134">String</span></span>|<span data-ttu-id="d776d-135">Identificador de la identidad del dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="d776d-135">Id of the imported device identity</span></span>|
|<span data-ttu-id="d776d-136">importedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="d776d-136">importedDeviceIdentifier</span></span>|<span data-ttu-id="d776d-137">String</span><span class="sxs-lookup"><span data-stu-id="d776d-137">String</span></span>|<span data-ttu-id="d776d-138">Identificador de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="d776d-138">Imported Device Identifier</span></span>|
|<span data-ttu-id="d776d-139">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="d776d-139">importedDeviceIdentityType</span></span>|[<span data-ttu-id="d776d-140">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="d776d-140">importedDeviceIdentityType</span></span>](../resources/intune-enrollment-importeddeviceidentitytype.md)|<span data-ttu-id="d776d-141">Tipo de identidad de dispositivo importada.</span><span class="sxs-lookup"><span data-stu-id="d776d-141">Type of Imported Device Identity.</span></span> <span data-ttu-id="d776d-142">Los valores posibles son: `unknown`, `imei` y `serialNumber`.</span><span class="sxs-lookup"><span data-stu-id="d776d-142">Possible values are: `unknown`, `imei`, `serialNumber`.</span></span>|
|<span data-ttu-id="d776d-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d776d-143">lastModifiedDateTime</span></span>|<span data-ttu-id="d776d-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d776d-144">DateTimeOffset</span></span>|<span data-ttu-id="d776d-145">DateTime última modificación de la descripción</span><span class="sxs-lookup"><span data-stu-id="d776d-145">Last Modified DateTime of the description</span></span>|
|<span data-ttu-id="d776d-146">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d776d-146">createdDateTime</span></span>|<span data-ttu-id="d776d-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d776d-147">DateTimeOffset</span></span>|<span data-ttu-id="d776d-148">Crear fecha hora del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d776d-148">Created Date Time of the device</span></span>|
|<span data-ttu-id="d776d-149">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="d776d-149">lastContactedDateTime</span></span>|<span data-ttu-id="d776d-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d776d-150">DateTimeOffset</span></span>|<span data-ttu-id="d776d-151">Última vez fecha ponerse en contacto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d776d-151">Last Contacted Date Time of the device</span></span>|
|<span data-ttu-id="d776d-152">descripción</span><span class="sxs-lookup"><span data-stu-id="d776d-152">description</span></span>|<span data-ttu-id="d776d-153">String</span><span class="sxs-lookup"><span data-stu-id="d776d-153">String</span></span>|<span data-ttu-id="d776d-154">La descripción del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d776d-154">The description of the device</span></span>|
|<span data-ttu-id="d776d-155">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="d776d-155">enrollmentState</span></span>|[<span data-ttu-id="d776d-156">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="d776d-156">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="d776d-157">El estado del dispositivo en Intune.</span><span class="sxs-lookup"><span data-stu-id="d776d-157">The state of the device in Intune.</span></span> <span data-ttu-id="d776d-158">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="d776d-158">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="d776d-159">platform</span><span class="sxs-lookup"><span data-stu-id="d776d-159">platform</span></span>|[<span data-ttu-id="d776d-160">plataforma</span><span class="sxs-lookup"><span data-stu-id="d776d-160">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="d776d-161">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d776d-161">The platform of the Device.</span></span> <span data-ttu-id="d776d-162">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="d776d-162">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|



## <a name="response"></a><span data-ttu-id="d776d-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d776d-163">Response</span></span>
<span data-ttu-id="d776d-164">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d776d-164">If successful, this method returns a `201 Created` response code and a [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d776d-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d776d-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="d776d-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d776d-166">Request</span></span>
<span data-ttu-id="d776d-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d776d-167">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/importedDeviceIdentities
Content-type: application/json
Content-length: 396

{
  "@odata.type": "#microsoft.graph.importedDeviceIdentity",
  "importedDeviceIdentifier": "Imported Device Identifier value",
  "importedDeviceIdentityType": "imei",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios"
}
```

### <a name="response"></a><span data-ttu-id="d776d-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d776d-168">Response</span></span>
<span data-ttu-id="d776d-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d776d-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 504

{
  "@odata.type": "#microsoft.graph.importedDeviceIdentity",
  "id": "9f70a12f-a12f-9f70-2fa1-709f2fa1709f",
  "importedDeviceIdentifier": "Imported Device Identifier value",
  "importedDeviceIdentityType": "imei",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios"
}
```





