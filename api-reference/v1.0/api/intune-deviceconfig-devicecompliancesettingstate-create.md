---
title: Crear deviceComplianceSettingState
description: Cree un objeto deviceComplianceSettingState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1da7aed12ae0c2c3f77a066295d7f98f55b55f8c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27819855"
---
# <a name="create-devicecompliancesettingstate"></a><span data-ttu-id="652d4-103">Crear deviceComplianceSettingState</span><span class="sxs-lookup"><span data-stu-id="652d4-103">Create deviceComplianceSettingState</span></span>

> <span data-ttu-id="652d4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="652d4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="652d4-105">Cree un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="652d4-105">Create a new [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="652d4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="652d4-106">Prerequisites</span></span>
<span data-ttu-id="652d4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="652d4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="652d4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="652d4-109">Permission type</span></span>|<span data-ttu-id="652d4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="652d4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="652d4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="652d4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="652d4-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="652d4-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="652d4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="652d4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="652d4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="652d4-114">Not supported.</span></span>|
|<span data-ttu-id="652d4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="652d4-115">Application</span></span>|<span data-ttu-id="652d4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="652d4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="652d4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="652d4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

## <a name="request-headers"></a><span data-ttu-id="652d4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="652d4-118">Request headers</span></span>
|<span data-ttu-id="652d4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="652d4-119">Header</span></span>|<span data-ttu-id="652d4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="652d4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="652d4-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="652d4-121">Authorization</span></span>|<span data-ttu-id="652d4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="652d4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="652d4-123">Accept</span><span class="sxs-lookup"><span data-stu-id="652d4-123">Accept</span></span>|<span data-ttu-id="652d4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="652d4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="652d4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="652d4-125">Request body</span></span>
<span data-ttu-id="652d4-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceSettingState.</span><span class="sxs-lookup"><span data-stu-id="652d4-126">In the request body, supply a JSON representation for the deviceComplianceSettingState object.</span></span>

<span data-ttu-id="652d4-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceSettingState.</span><span class="sxs-lookup"><span data-stu-id="652d4-127">The following table shows the properties that are required when you create the deviceComplianceSettingState.</span></span>

|<span data-ttu-id="652d4-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="652d4-128">Property</span></span>|<span data-ttu-id="652d4-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="652d4-129">Type</span></span>|<span data-ttu-id="652d4-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="652d4-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="652d4-131">id</span><span class="sxs-lookup"><span data-stu-id="652d4-131">id</span></span>|<span data-ttu-id="652d4-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-132">String</span></span>|<span data-ttu-id="652d4-133">Clave de la entidad</span><span class="sxs-lookup"><span data-stu-id="652d4-133">Key of the entity</span></span>|
|<span data-ttu-id="652d4-134">ajustes</span><span class="sxs-lookup"><span data-stu-id="652d4-134">setting</span></span>|<span data-ttu-id="652d4-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-135">String</span></span>|<span data-ttu-id="652d4-136">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="652d4-136">The setting class name and property name.</span></span>|
|<span data-ttu-id="652d4-137">settingName</span><span class="sxs-lookup"><span data-stu-id="652d4-137">settingName</span></span>|<span data-ttu-id="652d4-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-138">String</span></span>|<span data-ttu-id="652d4-139">El nombre de configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-139">The Setting Name that is being reported</span></span>|
|<span data-ttu-id="652d4-140">deviceId</span><span class="sxs-lookup"><span data-stu-id="652d4-140">deviceId</span></span>|<span data-ttu-id="652d4-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-141">String</span></span>|<span data-ttu-id="652d4-142">El identificador del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-142">The Device Id that is being reported</span></span>|
|<span data-ttu-id="652d4-143">deviceName</span><span class="sxs-lookup"><span data-stu-id="652d4-143">deviceName</span></span>|<span data-ttu-id="652d4-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-144">String</span></span>|<span data-ttu-id="652d4-145">El nombre del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-145">The Device Name that is being reported</span></span>|
|<span data-ttu-id="652d4-146">userId</span><span class="sxs-lookup"><span data-stu-id="652d4-146">userId</span></span>|<span data-ttu-id="652d4-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-147">String</span></span>|<span data-ttu-id="652d4-148">El identificador del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-148">The user Id that is being reported</span></span>|
|<span data-ttu-id="652d4-149">userEmail</span><span class="sxs-lookup"><span data-stu-id="652d4-149">userEmail</span></span>|<span data-ttu-id="652d4-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-150">String</span></span>|<span data-ttu-id="652d4-151">La dirección de correo electrónico del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-151">The User email address that is being reported</span></span>|
|<span data-ttu-id="652d4-152">userName</span><span class="sxs-lookup"><span data-stu-id="652d4-152">userName</span></span>|<span data-ttu-id="652d4-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-153">String</span></span>|<span data-ttu-id="652d4-154">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-154">The User Name that is being reported</span></span>|
|<span data-ttu-id="652d4-155">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="652d4-155">userPrincipalName</span></span>|<span data-ttu-id="652d4-156">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-156">String</span></span>|<span data-ttu-id="652d4-157">El nombre principal de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-157">The User PrincipalName that is being reported</span></span>|
|<span data-ttu-id="652d4-158">deviceModel</span><span class="sxs-lookup"><span data-stu-id="652d4-158">deviceModel</span></span>|<span data-ttu-id="652d4-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="652d4-159">String</span></span>|<span data-ttu-id="652d4-160">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="652d4-160">The device model that is being reported</span></span>|
|<span data-ttu-id="652d4-161">state</span><span class="sxs-lookup"><span data-stu-id="652d4-161">state</span></span>|[<span data-ttu-id="652d4-162">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="652d4-162">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="652d4-163">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="652d4-163">The compliance state of the setting.</span></span> <span data-ttu-id="652d4-164">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="652d4-164">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="652d4-165">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="652d4-165">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="652d4-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="652d4-166">DateTimeOffset</span></span>|<span data-ttu-id="652d4-167">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="652d4-167">The DateTime when device compliance grace period expires</span></span>|



## <a name="response"></a><span data-ttu-id="652d4-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="652d4-168">Response</span></span>
<span data-ttu-id="652d4-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="652d4-169">If successful, this method returns a `201 Created` response code and a [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="652d4-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="652d4-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="652d4-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="652d4-171">Request</span></span>
<span data-ttu-id="652d4-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="652d4-172">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
Content-type: application/json
Content-length: 517

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```

### <a name="response"></a><span data-ttu-id="652d4-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="652d4-173">Response</span></span>
<span data-ttu-id="652d4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="652d4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 566

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "id": "9905f955-f955-9905-55f9-059955f90599",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```



