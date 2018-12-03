---
title: Crear importedDeviceIdentityResult
description: Crear un nuevo objeto importedDeviceIdentityResult.
ms.openlocfilehash: 4dec2ac709274dd30e3412a299bb1b561c9514b7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090093"
---
# <a name="create-importeddeviceidentityresult"></a><span data-ttu-id="2ccd6-103">Crear importedDeviceIdentityResult</span><span class="sxs-lookup"><span data-stu-id="2ccd6-103">Create importedDeviceIdentityResult</span></span>

> <span data-ttu-id="2ccd6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2ccd6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2ccd6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2ccd6-107">Crear un nuevo objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="2ccd6-107">Create a new [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2ccd6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2ccd6-108">Prerequisites</span></span>
<span data-ttu-id="2ccd6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ccd6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2ccd6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ccd6-111">Permission type</span></span>|<span data-ttu-id="2ccd6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2ccd6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2ccd6-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ccd6-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2ccd6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2ccd6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-116">Not supported.</span></span>|
|<span data-ttu-id="2ccd6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ccd6-117">Application</span></span>|<span data-ttu-id="2ccd6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2ccd6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ccd6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/importedDeviceIdentities
```

## <a name="request-headers"></a><span data-ttu-id="2ccd6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ccd6-120">Request headers</span></span>
|<span data-ttu-id="2ccd6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ccd6-121">Header</span></span>|<span data-ttu-id="2ccd6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2ccd6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2ccd6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="2ccd6-123">Authorization</span></span>|<span data-ttu-id="2ccd6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2ccd6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2ccd6-125">Accept</span></span>|<span data-ttu-id="2ccd6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2ccd6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2ccd6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ccd6-127">Request body</span></span>
<span data-ttu-id="2ccd6-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto importedDeviceIdentityResult.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-128">In the request body, supply a JSON representation for the importedDeviceIdentityResult object.</span></span>

<span data-ttu-id="2ccd6-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el importedDeviceIdentityResult.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-129">The following table shows the properties that are required when you create the importedDeviceIdentityResult.</span></span>

|<span data-ttu-id="2ccd6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ccd6-130">Property</span></span>|<span data-ttu-id="2ccd6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ccd6-131">Type</span></span>|<span data-ttu-id="2ccd6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ccd6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2ccd6-133">id</span><span class="sxs-lookup"><span data-stu-id="2ccd6-133">id</span></span>|<span data-ttu-id="2ccd6-134">String</span><span class="sxs-lookup"><span data-stu-id="2ccd6-134">String</span></span>|<span data-ttu-id="2ccd6-135">Identificador de la identidad de dispositivo importada Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-135">Id of the imported device identity Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="2ccd6-136">importedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="2ccd6-136">importedDeviceIdentifier</span></span>|<span data-ttu-id="2ccd6-137">String</span><span class="sxs-lookup"><span data-stu-id="2ccd6-137">String</span></span>|<span data-ttu-id="2ccd6-138">Identificador de dispositivo importada heredado de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-138">Imported Device Identifier Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="2ccd6-139">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="2ccd6-139">importedDeviceIdentityType</span></span>|[<span data-ttu-id="2ccd6-140">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="2ccd6-140">importedDeviceIdentityType</span></span>](../resources/intune-enrollment-importeddeviceidentitytype.md)|<span data-ttu-id="2ccd6-141">Tipo de importados se hereda de identidad del dispositivo de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd6-141">Type of Imported Device Identity Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="2ccd6-142">Los valores posibles son: `unknown`, `imei` y `serialNumber`.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-142">Possible values are: `unknown`, `imei`, `serialNumber`.</span></span>|
|<span data-ttu-id="2ccd6-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2ccd6-143">lastModifiedDateTime</span></span>|<span data-ttu-id="2ccd6-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2ccd6-144">DateTimeOffset</span></span>|<span data-ttu-id="2ccd6-145">DateTime última modificación de la descripción Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-145">Last Modified DateTime of the description Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="2ccd6-146">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2ccd6-146">createdDateTime</span></span>|<span data-ttu-id="2ccd6-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2ccd6-147">DateTimeOffset</span></span>|<span data-ttu-id="2ccd6-148">Crear fecha hora del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-148">Created Date Time of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="2ccd6-149">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="2ccd6-149">lastContactedDateTime</span></span>|<span data-ttu-id="2ccd6-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2ccd6-150">DateTimeOffset</span></span>|<span data-ttu-id="2ccd6-151">Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-151">Last Contacted Date Time of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="2ccd6-152">descripción</span><span class="sxs-lookup"><span data-stu-id="2ccd6-152">description</span></span>|<span data-ttu-id="2ccd6-153">String</span><span class="sxs-lookup"><span data-stu-id="2ccd6-153">String</span></span>|<span data-ttu-id="2ccd6-154">La descripción del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-154">The description of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="2ccd6-155">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="2ccd6-155">enrollmentState</span></span>|[<span data-ttu-id="2ccd6-156">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="2ccd6-156">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="2ccd6-157">El estado del dispositivo en Intune se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd6-157">The state of the device in Intune Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="2ccd6-158">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-158">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="2ccd6-159">platform</span><span class="sxs-lookup"><span data-stu-id="2ccd6-159">platform</span></span>|[<span data-ttu-id="2ccd6-160">plataforma</span><span class="sxs-lookup"><span data-stu-id="2ccd6-160">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="2ccd6-161">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-161">The platform of the Device.</span></span> <span data-ttu-id="2ccd6-162">Se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd6-162">Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="2ccd6-163">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-163">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|
|<span data-ttu-id="2ccd6-164">status</span><span class="sxs-lookup"><span data-stu-id="2ccd6-164">status</span></span>|<span data-ttu-id="2ccd6-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="2ccd6-165">Boolean</span></span>|<span data-ttu-id="2ccd6-166">Estado de identidad de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="2ccd6-166">Status of imported device identity</span></span>|



## <a name="response"></a><span data-ttu-id="2ccd6-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ccd6-167">Response</span></span>
<span data-ttu-id="2ccd6-168">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-168">If successful, this method returns a `201 Created` response code and a [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2ccd6-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ccd6-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="2ccd6-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ccd6-170">Request</span></span>
<span data-ttu-id="2ccd6-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-171">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/importedDeviceIdentities
Content-type: application/json
Content-length: 421

{
  "@odata.type": "#microsoft.graph.importedDeviceIdentityResult",
  "importedDeviceIdentifier": "Imported Device Identifier value",
  "importedDeviceIdentityType": "imei",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```

### <a name="response"></a><span data-ttu-id="2ccd6-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ccd6-172">Response</span></span>
<span data-ttu-id="2ccd6-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 529

{
  "@odata.type": "#microsoft.graph.importedDeviceIdentityResult",
  "id": "9dfd3690-3690-9dfd-9036-fd9d9036fd9d",
  "importedDeviceIdentifier": "Imported Device Identifier value",
  "importedDeviceIdentityType": "imei",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```




