---
title: Crear deviceComplianceSettingState
description: Cree un objeto deviceComplianceSettingState.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f1914c143bc4c5c7bb40acfcdd4b57cead1070a8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956986"
---
# <a name="create-devicecompliancesettingstate"></a><span data-ttu-id="5e1b7-103">Crear deviceComplianceSettingState</span><span class="sxs-lookup"><span data-stu-id="5e1b7-103">Create deviceComplianceSettingState</span></span>

> <span data-ttu-id="5e1b7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5e1b7-105">Cree un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).</span><span class="sxs-lookup"><span data-stu-id="5e1b7-105">Create a new [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5e1b7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5e1b7-106">Prerequisites</span></span>
<span data-ttu-id="5e1b7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5e1b7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5e1b7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5e1b7-109">Permission type</span></span>|<span data-ttu-id="5e1b7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5e1b7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5e1b7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5e1b7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="5e1b7-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5e1b7-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5e1b7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5e1b7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5e1b7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-114">Not supported.</span></span>|
|<span data-ttu-id="5e1b7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5e1b7-115">Application</span></span>|<span data-ttu-id="5e1b7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5e1b7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5e1b7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

## <a name="request-headers"></a><span data-ttu-id="5e1b7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5e1b7-118">Request headers</span></span>
|<span data-ttu-id="5e1b7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e1b7-119">Header</span></span>|<span data-ttu-id="5e1b7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5e1b7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5e1b7-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e1b7-121">Authorization</span></span>|<span data-ttu-id="5e1b7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5e1b7-123">Accept</span><span class="sxs-lookup"><span data-stu-id="5e1b7-123">Accept</span></span>|<span data-ttu-id="5e1b7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="5e1b7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5e1b7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5e1b7-125">Request body</span></span>
<span data-ttu-id="5e1b7-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceSettingState.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-126">In the request body, supply a JSON representation for the deviceComplianceSettingState object.</span></span>

<span data-ttu-id="5e1b7-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceSettingState.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-127">The following table shows the properties that are required when you create the deviceComplianceSettingState.</span></span>

|<span data-ttu-id="5e1b7-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5e1b7-128">Property</span></span>|<span data-ttu-id="5e1b7-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e1b7-129">Type</span></span>|<span data-ttu-id="5e1b7-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e1b7-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5e1b7-131">id</span><span class="sxs-lookup"><span data-stu-id="5e1b7-131">id</span></span>|<span data-ttu-id="5e1b7-132">String</span><span class="sxs-lookup"><span data-stu-id="5e1b7-132">String</span></span>|<span data-ttu-id="5e1b7-133">Clave de la entidad</span><span class="sxs-lookup"><span data-stu-id="5e1b7-133">Key of the entity</span></span>|
|<span data-ttu-id="5e1b7-134">ajustes</span><span class="sxs-lookup"><span data-stu-id="5e1b7-134">setting</span></span>|<span data-ttu-id="5e1b7-135">String</span><span class="sxs-lookup"><span data-stu-id="5e1b7-135">String</span></span>|<span data-ttu-id="5e1b7-136">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-136">The setting class name and property name.</span></span>|
|<span data-ttu-id="5e1b7-137">settingName</span><span class="sxs-lookup"><span data-stu-id="5e1b7-137">settingName</span></span>|<span data-ttu-id="5e1b7-138">String</span><span class="sxs-lookup"><span data-stu-id="5e1b7-138">String</span></span>|<span data-ttu-id="5e1b7-139">El nombre de configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-139">The Setting Name that is being reported</span></span>|
|<span data-ttu-id="5e1b7-140">deviceId</span><span class="sxs-lookup"><span data-stu-id="5e1b7-140">deviceId</span></span>|<span data-ttu-id="5e1b7-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e1b7-141">String</span></span>|<span data-ttu-id="5e1b7-142">El identificador del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-142">The Device Id that is being reported</span></span>|
|<span data-ttu-id="5e1b7-143">deviceName</span><span class="sxs-lookup"><span data-stu-id="5e1b7-143">deviceName</span></span>|<span data-ttu-id="5e1b7-144">String</span><span class="sxs-lookup"><span data-stu-id="5e1b7-144">String</span></span>|<span data-ttu-id="5e1b7-145">El nombre del dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-145">The Device Name that is being reported</span></span>|
|<span data-ttu-id="5e1b7-146">userId</span><span class="sxs-lookup"><span data-stu-id="5e1b7-146">userId</span></span>|<span data-ttu-id="5e1b7-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e1b7-147">String</span></span>|<span data-ttu-id="5e1b7-148">El identificador del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-148">The user Id that is being reported</span></span>|
|<span data-ttu-id="5e1b7-149">userEmail</span><span class="sxs-lookup"><span data-stu-id="5e1b7-149">userEmail</span></span>|<span data-ttu-id="5e1b7-150">String</span><span class="sxs-lookup"><span data-stu-id="5e1b7-150">String</span></span>|<span data-ttu-id="5e1b7-151">La dirección de correo electrónico del usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-151">The User email address that is being reported</span></span>|
|<span data-ttu-id="5e1b7-152">userName</span><span class="sxs-lookup"><span data-stu-id="5e1b7-152">userName</span></span>|<span data-ttu-id="5e1b7-153">String</span><span class="sxs-lookup"><span data-stu-id="5e1b7-153">String</span></span>|<span data-ttu-id="5e1b7-154">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-154">The User Name that is being reported</span></span>|
|<span data-ttu-id="5e1b7-155">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5e1b7-155">userPrincipalName</span></span>|<span data-ttu-id="5e1b7-156">String</span><span class="sxs-lookup"><span data-stu-id="5e1b7-156">String</span></span>|<span data-ttu-id="5e1b7-157">El nombre principal de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-157">The User PrincipalName that is being reported</span></span>|
|<span data-ttu-id="5e1b7-158">deviceModel</span><span class="sxs-lookup"><span data-stu-id="5e1b7-158">deviceModel</span></span>|<span data-ttu-id="5e1b7-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="5e1b7-159">String</span></span>|<span data-ttu-id="5e1b7-160">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="5e1b7-160">The device model that is being reported</span></span>|
|<span data-ttu-id="5e1b7-161">estado</span><span class="sxs-lookup"><span data-stu-id="5e1b7-161">state</span></span>|[<span data-ttu-id="5e1b7-162">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="5e1b7-162">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="5e1b7-163">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-163">The compliance state of the setting.</span></span> <span data-ttu-id="5e1b7-164">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-164">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="5e1b7-165">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="5e1b7-165">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="5e1b7-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5e1b7-166">DateTimeOffset</span></span>|<span data-ttu-id="5e1b7-167">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5e1b7-167">The DateTime when device compliance grace period expires</span></span>|



## <a name="response"></a><span data-ttu-id="5e1b7-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e1b7-168">Response</span></span>
<span data-ttu-id="5e1b7-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-169">If successful, this method returns a `201 Created` response code and a [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5e1b7-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5e1b7-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="5e1b7-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5e1b7-171">Request</span></span>
<span data-ttu-id="5e1b7-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-172">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="5e1b7-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5e1b7-173">Response</span></span>
<span data-ttu-id="5e1b7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5e1b7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



