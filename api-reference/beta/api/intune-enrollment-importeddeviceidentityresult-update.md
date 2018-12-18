---
title: Actualizar importedDeviceIdentityResult
description: Actualizar las propiedades de un objeto importedDeviceIdentityResult.
author: tfitzmac
ms.openlocfilehash: 4c698810bb3fe88f52d8fcba11d8c29aeb508fe6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332441"
---
# <a name="update-importeddeviceidentityresult"></a><span data-ttu-id="f4516-103">Actualizar importedDeviceIdentityResult</span><span class="sxs-lookup"><span data-stu-id="f4516-103">Update importedDeviceIdentityResult</span></span>

> <span data-ttu-id="f4516-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4516-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4516-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4516-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f4516-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f4516-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f4516-107">Actualizar las propiedades de un objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="f4516-107">Update the properties of a [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f4516-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f4516-108">Prerequisites</span></span>
<span data-ttu-id="f4516-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4516-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f4516-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4516-111">Permission type</span></span>|<span data-ttu-id="f4516-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4516-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f4516-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4516-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f4516-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4516-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f4516-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4516-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f4516-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4516-116">Not supported.</span></span>|
|<span data-ttu-id="f4516-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4516-117">Application</span></span>|<span data-ttu-id="f4516-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4516-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f4516-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4516-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedDeviceIdentities/{importedDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="f4516-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4516-120">Request headers</span></span>
|<span data-ttu-id="f4516-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4516-121">Header</span></span>|<span data-ttu-id="f4516-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f4516-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f4516-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f4516-123">Authorization</span></span>|<span data-ttu-id="f4516-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f4516-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f4516-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f4516-125">Accept</span></span>|<span data-ttu-id="f4516-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f4516-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f4516-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4516-127">Request body</span></span>
<span data-ttu-id="f4516-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) .</span><span class="sxs-lookup"><span data-stu-id="f4516-128">In the request body, supply a JSON representation for the [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object.</span></span>

<span data-ttu-id="f4516-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md).</span><span class="sxs-lookup"><span data-stu-id="f4516-129">The following table shows the properties that are required when you create the [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md).</span></span>

|<span data-ttu-id="f4516-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4516-130">Property</span></span>|<span data-ttu-id="f4516-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4516-131">Type</span></span>|<span data-ttu-id="f4516-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4516-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4516-133">id</span><span class="sxs-lookup"><span data-stu-id="f4516-133">id</span></span>|<span data-ttu-id="f4516-134">String</span><span class="sxs-lookup"><span data-stu-id="f4516-134">String</span></span>|<span data-ttu-id="f4516-135">Identificador de la identidad de dispositivo importada Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="f4516-135">Id of the imported device identity Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="f4516-136">importedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="f4516-136">importedDeviceIdentifier</span></span>|<span data-ttu-id="f4516-137">String</span><span class="sxs-lookup"><span data-stu-id="f4516-137">String</span></span>|<span data-ttu-id="f4516-138">Identificador de dispositivo importada heredado de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="f4516-138">Imported Device Identifier Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="f4516-139">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="f4516-139">importedDeviceIdentityType</span></span>|[<span data-ttu-id="f4516-140">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="f4516-140">importedDeviceIdentityType</span></span>](../resources/intune-enrollment-importeddeviceidentitytype.md)|<span data-ttu-id="f4516-141">Tipo de importados se hereda de identidad del dispositivo de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="f4516-141">Type of Imported Device Identity Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="f4516-142">Los valores posibles son: `unknown`, `imei` y `serialNumber`.</span><span class="sxs-lookup"><span data-stu-id="f4516-142">Possible values are: `unknown`, `imei`, `serialNumber`.</span></span>|
|<span data-ttu-id="f4516-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f4516-143">lastModifiedDateTime</span></span>|<span data-ttu-id="f4516-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4516-144">DateTimeOffset</span></span>|<span data-ttu-id="f4516-145">DateTime última modificación de la descripción Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="f4516-145">Last Modified DateTime of the description Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="f4516-146">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f4516-146">createdDateTime</span></span>|<span data-ttu-id="f4516-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4516-147">DateTimeOffset</span></span>|<span data-ttu-id="f4516-148">Crear fecha hora del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="f4516-148">Created Date Time of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="f4516-149">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="f4516-149">lastContactedDateTime</span></span>|<span data-ttu-id="f4516-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4516-150">DateTimeOffset</span></span>|<span data-ttu-id="f4516-151">Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="f4516-151">Last Contacted Date Time of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="f4516-152">descripción</span><span class="sxs-lookup"><span data-stu-id="f4516-152">description</span></span>|<span data-ttu-id="f4516-153">String</span><span class="sxs-lookup"><span data-stu-id="f4516-153">String</span></span>|<span data-ttu-id="f4516-154">La descripción del dispositivo Inherited desde [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="f4516-154">The description of the device Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md)</span></span>|
|<span data-ttu-id="f4516-155">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="f4516-155">enrollmentState</span></span>|[<span data-ttu-id="f4516-156">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="f4516-156">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="f4516-157">El estado del dispositivo en Intune se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="f4516-157">The state of the device in Intune Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="f4516-158">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="f4516-158">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="f4516-159">platform</span><span class="sxs-lookup"><span data-stu-id="f4516-159">platform</span></span>|[<span data-ttu-id="f4516-160">plataforma</span><span class="sxs-lookup"><span data-stu-id="f4516-160">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="f4516-161">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4516-161">The platform of the Device.</span></span> <span data-ttu-id="f4516-162">Se hereda de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="f4516-162">Inherited from [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span> <span data-ttu-id="f4516-163">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="f4516-163">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|
|<span data-ttu-id="f4516-164">status</span><span class="sxs-lookup"><span data-stu-id="f4516-164">status</span></span>|<span data-ttu-id="f4516-165">Boolean</span><span class="sxs-lookup"><span data-stu-id="f4516-165">Boolean</span></span>|<span data-ttu-id="f4516-166">Estado de identidad de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="f4516-166">Status of imported device identity</span></span>|



## <a name="response"></a><span data-ttu-id="f4516-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4516-167">Response</span></span>
<span data-ttu-id="f4516-168">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4516-168">If successful, this method returns a `200 OK` response code and an updated [importedDeviceIdentityResult](../resources/intune-enrollment-importeddeviceidentityresult.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4516-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4516-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="f4516-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4516-170">Request</span></span>
<span data-ttu-id="f4516-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4516-171">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="f4516-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4516-172">Response</span></span>
<span data-ttu-id="f4516-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4516-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





