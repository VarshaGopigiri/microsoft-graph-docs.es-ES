---
title: Crear deviceComplianceDeviceStatus
description: Cree un objeto deviceComplianceDeviceStatus.
ms.openlocfilehash: c3c43b6c6ee49f0c4b962cd35d0cead9d4900bf6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030356"
---
# <a name="create-devicecompliancedevicestatus"></a><span data-ttu-id="457c2-103">Crear deviceComplianceDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="457c2-103">Create deviceComplianceDeviceStatus</span></span>

> <span data-ttu-id="457c2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="457c2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="457c2-105">Cree un objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="457c2-105">Create a new [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="457c2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="457c2-106">Prerequisites</span></span>
<span data-ttu-id="457c2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="457c2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="457c2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="457c2-109">Permission type</span></span>|<span data-ttu-id="457c2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="457c2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="457c2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="457c2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="457c2-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="457c2-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="457c2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="457c2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="457c2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="457c2-114">Not supported.</span></span>|
|<span data-ttu-id="457c2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="457c2-115">Application</span></span>|<span data-ttu-id="457c2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="457c2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="457c2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="457c2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="457c2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="457c2-118">Request headers</span></span>
|<span data-ttu-id="457c2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="457c2-119">Header</span></span>|<span data-ttu-id="457c2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="457c2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="457c2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="457c2-121">Authorization</span></span>|<span data-ttu-id="457c2-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="457c2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="457c2-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="457c2-123">Accept</span></span>|<span data-ttu-id="457c2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="457c2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="457c2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="457c2-125">Request body</span></span>
<span data-ttu-id="457c2-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="457c2-126">In the request body, supply a JSON representation for the deviceComplianceDeviceStatus object.</span></span>

<span data-ttu-id="457c2-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="457c2-127">The following table shows the properties that are required when you create the deviceComplianceDeviceStatus.</span></span>

|<span data-ttu-id="457c2-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="457c2-128">Property</span></span>|<span data-ttu-id="457c2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="457c2-129">Type</span></span>|<span data-ttu-id="457c2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="457c2-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="457c2-131">id</span><span class="sxs-lookup"><span data-stu-id="457c2-131">id</span></span>|<span data-ttu-id="457c2-132">String</span><span class="sxs-lookup"><span data-stu-id="457c2-132">String</span></span>|<span data-ttu-id="457c2-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="457c2-133">Key of the entity.</span></span>|
|<span data-ttu-id="457c2-134">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="457c2-134">deviceDisplayName</span></span>|<span data-ttu-id="457c2-135">String</span><span class="sxs-lookup"><span data-stu-id="457c2-135">String</span></span>|<span data-ttu-id="457c2-136">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="457c2-136">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="457c2-137">userName</span><span class="sxs-lookup"><span data-stu-id="457c2-137">userName</span></span>|<span data-ttu-id="457c2-138">String</span><span class="sxs-lookup"><span data-stu-id="457c2-138">String</span></span>|<span data-ttu-id="457c2-139">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="457c2-139">The User Name that is being reported</span></span>|
|<span data-ttu-id="457c2-140">deviceModel</span><span class="sxs-lookup"><span data-stu-id="457c2-140">deviceModel</span></span>|<span data-ttu-id="457c2-141">String</span><span class="sxs-lookup"><span data-stu-id="457c2-141">String</span></span>|<span data-ttu-id="457c2-142">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="457c2-142">The device model that is being reported</span></span>|
|<span data-ttu-id="457c2-143">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="457c2-143">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="457c2-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="457c2-144">DateTimeOffset</span></span>|<span data-ttu-id="457c2-145">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="457c2-145">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="457c2-146">status</span><span class="sxs-lookup"><span data-stu-id="457c2-146">status</span></span>|[<span data-ttu-id="457c2-147">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="457c2-147">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="457c2-148">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="457c2-148">Compliance status of the policy report.</span></span> <span data-ttu-id="457c2-149">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="457c2-149">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="457c2-150">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="457c2-150">lastReportedDateTime</span></span>|<span data-ttu-id="457c2-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="457c2-151">DateTimeOffset</span></span>|<span data-ttu-id="457c2-152">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="457c2-152">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="457c2-153">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="457c2-153">userPrincipalName</span></span>|<span data-ttu-id="457c2-154">String</span><span class="sxs-lookup"><span data-stu-id="457c2-154">String</span></span>|<span data-ttu-id="457c2-155">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="457c2-155">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="457c2-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="457c2-156">Response</span></span>
<span data-ttu-id="457c2-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="457c2-157">If successful, this method returns a `201 Created` response code and a [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="457c2-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="457c2-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="457c2-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="457c2-159">Request</span></span>
<span data-ttu-id="457c2-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="457c2-160">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses
Content-type: application/json
Content-length: 426

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceStatus",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="457c2-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="457c2-161">Response</span></span>
<span data-ttu-id="457c2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="457c2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 475

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceStatus",
  "id": "c6c78124-8124-c6c7-2481-c7c62481c7c6",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```



