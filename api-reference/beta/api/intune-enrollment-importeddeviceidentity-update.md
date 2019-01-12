---
title: Actualizar importedDeviceIdentity
description: Actualizar las propiedades de un objeto importedDeviceIdentity.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a66ceb575363f8a48dd0d23e61a6ecbc994ea582
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973492"
---
# <a name="update-importeddeviceidentity"></a><span data-ttu-id="88b2f-103">Actualizar importedDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="88b2f-103">Update importedDeviceIdentity</span></span>

> <span data-ttu-id="88b2f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88b2f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88b2f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88b2f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="88b2f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="88b2f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="88b2f-107">Actualizar las propiedades de un objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="88b2f-107">Update the properties of a [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="88b2f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="88b2f-108">Prerequisites</span></span>
<span data-ttu-id="88b2f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88b2f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88b2f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88b2f-111">Permission type</span></span>|<span data-ttu-id="88b2f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88b2f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="88b2f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88b2f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="88b2f-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="88b2f-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="88b2f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88b2f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="88b2f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88b2f-116">Not supported.</span></span>|
|<span data-ttu-id="88b2f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88b2f-117">Application</span></span>|<span data-ttu-id="88b2f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88b2f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="88b2f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88b2f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedDeviceIdentities/{importedDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="88b2f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88b2f-120">Request headers</span></span>
|<span data-ttu-id="88b2f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88b2f-121">Header</span></span>|<span data-ttu-id="88b2f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="88b2f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="88b2f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="88b2f-123">Authorization</span></span>|<span data-ttu-id="88b2f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="88b2f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="88b2f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="88b2f-125">Accept</span></span>|<span data-ttu-id="88b2f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="88b2f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="88b2f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88b2f-127">Request body</span></span>
<span data-ttu-id="88b2f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="88b2f-128">In the request body, supply a JSON representation for the [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object.</span></span>

<span data-ttu-id="88b2f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="88b2f-129">The following table shows the properties that are required when you create the [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md).</span></span>

|<span data-ttu-id="88b2f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="88b2f-130">Property</span></span>|<span data-ttu-id="88b2f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="88b2f-131">Type</span></span>|<span data-ttu-id="88b2f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="88b2f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="88b2f-133">id</span><span class="sxs-lookup"><span data-stu-id="88b2f-133">id</span></span>|<span data-ttu-id="88b2f-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="88b2f-134">String</span></span>|<span data-ttu-id="88b2f-135">Identificador de la identidad del dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="88b2f-135">Id of the imported device identity</span></span>|
|<span data-ttu-id="88b2f-136">importedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="88b2f-136">importedDeviceIdentifier</span></span>|<span data-ttu-id="88b2f-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="88b2f-137">String</span></span>|<span data-ttu-id="88b2f-138">Identificador de dispositivo importada</span><span class="sxs-lookup"><span data-stu-id="88b2f-138">Imported Device Identifier</span></span>|
|<span data-ttu-id="88b2f-139">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="88b2f-139">importedDeviceIdentityType</span></span>|[<span data-ttu-id="88b2f-140">importedDeviceIdentityType</span><span class="sxs-lookup"><span data-stu-id="88b2f-140">importedDeviceIdentityType</span></span>](../resources/intune-enrollment-importeddeviceidentitytype.md)|<span data-ttu-id="88b2f-141">Tipo de identidad de dispositivo importada.</span><span class="sxs-lookup"><span data-stu-id="88b2f-141">Type of Imported Device Identity.</span></span> <span data-ttu-id="88b2f-142">Los valores posibles son: `unknown`, `imei` y `serialNumber`.</span><span class="sxs-lookup"><span data-stu-id="88b2f-142">Possible values are: `unknown`, `imei`, `serialNumber`.</span></span>|
|<span data-ttu-id="88b2f-143">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="88b2f-143">lastModifiedDateTime</span></span>|<span data-ttu-id="88b2f-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88b2f-144">DateTimeOffset</span></span>|<span data-ttu-id="88b2f-145">DateTime última modificación de la descripción</span><span class="sxs-lookup"><span data-stu-id="88b2f-145">Last Modified DateTime of the description</span></span>|
|<span data-ttu-id="88b2f-146">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="88b2f-146">createdDateTime</span></span>|<span data-ttu-id="88b2f-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88b2f-147">DateTimeOffset</span></span>|<span data-ttu-id="88b2f-148">Crear fecha hora del dispositivo</span><span class="sxs-lookup"><span data-stu-id="88b2f-148">Created Date Time of the device</span></span>|
|<span data-ttu-id="88b2f-149">lastContactedDateTime</span><span class="sxs-lookup"><span data-stu-id="88b2f-149">lastContactedDateTime</span></span>|<span data-ttu-id="88b2f-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="88b2f-150">DateTimeOffset</span></span>|<span data-ttu-id="88b2f-151">Última vez fecha ponerse en contacto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="88b2f-151">Last Contacted Date Time of the device</span></span>|
|<span data-ttu-id="88b2f-152">descripción</span><span class="sxs-lookup"><span data-stu-id="88b2f-152">description</span></span>|<span data-ttu-id="88b2f-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="88b2f-153">String</span></span>|<span data-ttu-id="88b2f-154">La descripción del dispositivo</span><span class="sxs-lookup"><span data-stu-id="88b2f-154">The description of the device</span></span>|
|<span data-ttu-id="88b2f-155">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="88b2f-155">enrollmentState</span></span>|[<span data-ttu-id="88b2f-156">enrollmentState</span><span class="sxs-lookup"><span data-stu-id="88b2f-156">enrollmentState</span></span>](../resources/intune-enrollment-enrollmentstate.md)|<span data-ttu-id="88b2f-157">El estado del dispositivo en Intune.</span><span class="sxs-lookup"><span data-stu-id="88b2f-157">The state of the device in Intune.</span></span> <span data-ttu-id="88b2f-158">Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span><span class="sxs-lookup"><span data-stu-id="88b2f-158">Possible values are: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.</span></span>|
|<span data-ttu-id="88b2f-159">platform</span><span class="sxs-lookup"><span data-stu-id="88b2f-159">platform</span></span>|[<span data-ttu-id="88b2f-160">plataforma</span><span class="sxs-lookup"><span data-stu-id="88b2f-160">platform</span></span>](../resources/intune-enrollment-platform.md)|<span data-ttu-id="88b2f-161">La plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88b2f-161">The platform of the Device.</span></span> <span data-ttu-id="88b2f-162">Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span><span class="sxs-lookup"><span data-stu-id="88b2f-162">Possible values are: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.</span></span>|



## <a name="response"></a><span data-ttu-id="88b2f-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88b2f-163">Response</span></span>
<span data-ttu-id="88b2f-164">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88b2f-164">If successful, this method returns a `200 OK` response code and an updated [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88b2f-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88b2f-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="88b2f-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88b2f-166">Request</span></span>
<span data-ttu-id="88b2f-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88b2f-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/importedDeviceIdentities/{importedDeviceIdentityId}
Content-type: application/json
Content-length: 335

{
  "importedDeviceIdentifier": "Imported Device Identifier value",
  "importedDeviceIdentityType": "imei",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios"
}
```

### <a name="response"></a><span data-ttu-id="88b2f-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88b2f-168">Response</span></span>
<span data-ttu-id="88b2f-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88b2f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





