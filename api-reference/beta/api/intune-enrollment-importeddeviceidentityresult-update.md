---
title: Actualizar importedDeviceIdentityResult
description: Actualizar las propiedades de un objeto importedDeviceIdentityResult.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7fe9472b0f63ada966c61dd8fc56a7865cf94408
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827576"
---
# <a name="update-importeddeviceidentityresult"></a><span data-ttu-id="ab576-103">Actualizar importedDeviceIdentityResult</span><span class="sxs-lookup"><span data-stu-id="ab576-103">Update importedDeviceIdentityResult</span></span>

> <span data-ttu-id="ab576-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab576-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab576-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab576-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ab576-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ab576-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ab576-107">Actualizar las propiedades de un objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="ab576-107">Update the properties of a [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ab576-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ab576-108">Prerequisites</span></span>
<span data-ttu-id="ab576-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab576-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ab576-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab576-111">Permission type</span></span>|<span data-ttu-id="ab576-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab576-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ab576-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab576-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ab576-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab576-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="ab576-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab576-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ab576-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab576-116">Not supported.</span></span>|
|<span data-ttu-id="ab576-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab576-117">Application</span></span>|<span data-ttu-id="ab576-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab576-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ab576-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab576-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedDeviceIdentities/{importedDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="ab576-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab576-120">Request headers</span></span>
|<span data-ttu-id="ab576-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab576-121">Header</span></span>|<span data-ttu-id="ab576-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ab576-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ab576-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ab576-123">Authorization</span></span>|<span data-ttu-id="ab576-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ab576-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ab576-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ab576-125">Accept</span></span>|<span data-ttu-id="ab576-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ab576-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ab576-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ab576-127">Request body</span></span>
<span data-ttu-id="ab576-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="ab576-128">In the request body, supply a JSON representation for the [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object.</span></span>

<span data-ttu-id="ab576-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md).</span><span class="sxs-lookup"><span data-stu-id="ab576-129">The following table shows the properties that are required when you create the [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md).</span></span>

|<span data-ttu-id="ab576-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab576-130">Property</span></span>|<span data-ttu-id="ab576-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab576-131">Type</span></span>|<span data-ttu-id="ab576-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab576-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ab576-133">id</span><span class="sxs-lookup"><span data-stu-id="ab576-133">id</span></span>|<span data-ttu-id="ab576-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab576-134">String</span></span>|<span data-ttu-id="ab576-135">Identificador de la identidad de dispositivo importada Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="ab576-135">Id of the imported device identity Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="ab576-136">importedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="ab576-136">importedDeviceIdentifier</span></span>|<span data-ttu-id="ab576-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab576-137">String</span></span>|<span data-ttu-id="ab576-138">Identificador de dispositivo importada heredado de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="ab576-138">Imported Device Identifier Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="ab576-139">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="ab576-139">importedDeviceIdentityType</span></span>|[<span data-ttu-id="ab576-140">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="ab576-140">importedDeviceIdentityType</span></span>](../resources/intune-enrollment-importeddeviceidentitytype.md)|<span data-ttu-id="ab576-141">Tipo de importados se hereda de identidad del dispositivo de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="ab576-141">Type of Imported Device Identity Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="ab576-142">Los valores posibles son: `unknown`, `imei` y `serialNumber`.</span><span class="sxs-lookup"><span data-stu-id="ab576-142">Possible values are: `unknown`, `imei`, `serialNumber`.</span></span>|
|<span data-ttu-id="ab576-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ab576-143">lastModifiedDateTime</span></span>|<span data-ttu-id="ab576-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ab576-144">DateTimeOffset</span></span>|<span data-ttu-id="ab576-145">DateTime última modificación de la descripción Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="ab576-145">Last Modified DateTime of the description Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="ab576-146">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ab576-146">createdDateTime</span></span>|<span data-ttu-id="ab576-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ab576-147">DateTimeOffset</span></span>|<span data-ttu-id="ab576-148">Crear fecha hora del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="ab576-148">Created Date Time of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="ab576-149">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="ab576-149">lastContactedDateTime</span></span>|<span data-ttu-id="ab576-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ab576-150">DateTimeOffset</span></span>|<span data-ttu-id="ab576-151">Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="ab576-151">Last Contacted Date Time of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="ab576-152">descripción</span><span class="sxs-lookup"><span data-stu-id="ab576-152">description</span></span>|<span data-ttu-id="ab576-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="ab576-153">String</span></span>|<span data-ttu-id="ab576-154">La descripción del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="ab576-154">The description of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="ab576-155">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="ab576-155">enrollmentState</span></span>|[<span data-ttu-id="ab576-156">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="ab576-156">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="ab576-157">El estado del dispositivo en Intune se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="ab576-157">The state of the device in Intune Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="ab576-158">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="ab576-158">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="ab576-159">platform</span><span class="sxs-lookup"><span data-stu-id="ab576-159">platform</span></span>|[<span data-ttu-id="ab576-160">plataforma</span><span class="sxs-lookup"><span data-stu-id="ab576-160">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="ab576-161">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab576-161">The platform of the Device.</span></span> <span data-ttu-id="ab576-162">Se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="ab576-162">Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="ab576-163">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="ab576-163">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|
|<span data-ttu-id="ab576-164">status</span><span class="sxs-lookup"><span data-stu-id="ab576-164">status</span></span>|<span data-ttu-id="ab576-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="ab576-165">Boolean</span></span>|<span data-ttu-id="ab576-166">Estado de identidad de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="ab576-166">Status of imported device identity</span></span>|



## <a name="response"></a><span data-ttu-id="ab576-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab576-167">Response</span></span>
<span data-ttu-id="ab576-168">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab576-168">If successful, this method returns a `200 OK` response code and an updated [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ab576-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab576-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="ab576-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab576-170">Request</span></span>
<span data-ttu-id="ab576-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab576-171">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/importedDeviceIdentities/{importedDeviceIdentityId}
Content-type: application/json
Content-length: 354

{
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

### <a name="response"></a><span data-ttu-id="ab576-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab576-172">Response</span></span>
<span data-ttu-id="ab576-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab576-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





