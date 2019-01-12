---
title: Actualizar deviceComplianceDeviceStatus
description: Actualice las propiedades de un objeto deviceComplianceDeviceStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 28643c5e308f026f6aca0b0c600387a35acf4f4f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968998"
---
# <a name="update-devicecompliancedevicestatus"></a><span data-ttu-id="0d4cb-103">Actualizar deviceComplianceDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="0d4cb-103">Update deviceComplianceDeviceStatus</span></span>

> <span data-ttu-id="0d4cb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0d4cb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0d4cb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0d4cb-107">Actualice las propiedades de un objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="0d4cb-107">Update the properties of a [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0d4cb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0d4cb-108">Prerequisites</span></span>
<span data-ttu-id="0d4cb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0d4cb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0d4cb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0d4cb-111">Permission type</span></span>|<span data-ttu-id="0d4cb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0d4cb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0d4cb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0d4cb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0d4cb-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0d4cb-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0d4cb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0d4cb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0d4cb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-116">Not supported.</span></span>|
|<span data-ttu-id="0d4cb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0d4cb-117">Application</span></span>|<span data-ttu-id="0d4cb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0d4cb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0d4cb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses/{deviceComplianceDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="0d4cb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d4cb-120">Request headers</span></span>
|<span data-ttu-id="0d4cb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d4cb-121">Header</span></span>|<span data-ttu-id="0d4cb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0d4cb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0d4cb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0d4cb-123">Authorization</span></span>|<span data-ttu-id="0d4cb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0d4cb-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0d4cb-125">Accept</span></span>|<span data-ttu-id="0d4cb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0d4cb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0d4cb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0d4cb-127">Request body</span></span>
<span data-ttu-id="0d4cb-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="0d4cb-128">In the request body, supply a JSON representation for the [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) object.</span></span>

<span data-ttu-id="0d4cb-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="0d4cb-129">The following table shows the properties that are required when you create the [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md).</span></span>

|<span data-ttu-id="0d4cb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0d4cb-130">Property</span></span>|<span data-ttu-id="0d4cb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d4cb-131">Type</span></span>|<span data-ttu-id="0d4cb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d4cb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0d4cb-133">id</span><span class="sxs-lookup"><span data-stu-id="0d4cb-133">id</span></span>|<span data-ttu-id="0d4cb-134">String</span><span class="sxs-lookup"><span data-stu-id="0d4cb-134">String</span></span>|<span data-ttu-id="0d4cb-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-135">Key of the entity.</span></span>|
|<span data-ttu-id="0d4cb-136">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="0d4cb-136">deviceDisplayName</span></span>|<span data-ttu-id="0d4cb-137">String</span><span class="sxs-lookup"><span data-stu-id="0d4cb-137">String</span></span>|<span data-ttu-id="0d4cb-138">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-138">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="0d4cb-139">userName</span><span class="sxs-lookup"><span data-stu-id="0d4cb-139">userName</span></span>|<span data-ttu-id="0d4cb-140">String</span><span class="sxs-lookup"><span data-stu-id="0d4cb-140">String</span></span>|<span data-ttu-id="0d4cb-141">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="0d4cb-141">The User Name that is being reported</span></span>|
|<span data-ttu-id="0d4cb-142">deviceModel</span><span class="sxs-lookup"><span data-stu-id="0d4cb-142">deviceModel</span></span>|<span data-ttu-id="0d4cb-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="0d4cb-143">String</span></span>|<span data-ttu-id="0d4cb-144">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="0d4cb-144">The device model that is being reported</span></span>|
|<span data-ttu-id="0d4cb-145">platform</span><span class="sxs-lookup"><span data-stu-id="0d4cb-145">platform</span></span>|<span data-ttu-id="0d4cb-146">Int32</span><span class="sxs-lookup"><span data-stu-id="0d4cb-146">Int32</span></span>|<span data-ttu-id="0d4cb-147">Plataforma del dispositivo que se notifica</span><span class="sxs-lookup"><span data-stu-id="0d4cb-147">Platform of the device that is being reported</span></span>|
|<span data-ttu-id="0d4cb-148">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="0d4cb-148">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="0d4cb-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0d4cb-149">DateTimeOffset</span></span>|<span data-ttu-id="0d4cb-150">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="0d4cb-150">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="0d4cb-151">status</span><span class="sxs-lookup"><span data-stu-id="0d4cb-151">status</span></span>|[<span data-ttu-id="0d4cb-152">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="0d4cb-152">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="0d4cb-153">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-153">Compliance status of the policy report.</span></span> <span data-ttu-id="0d4cb-154">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-154">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="0d4cb-155">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="0d4cb-155">lastReportedDateTime</span></span>|<span data-ttu-id="0d4cb-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0d4cb-156">DateTimeOffset</span></span>|<span data-ttu-id="0d4cb-157">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-157">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="0d4cb-158">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0d4cb-158">userPrincipalName</span></span>|<span data-ttu-id="0d4cb-159">String</span><span class="sxs-lookup"><span data-stu-id="0d4cb-159">String</span></span>|<span data-ttu-id="0d4cb-160">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-160">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="0d4cb-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d4cb-161">Response</span></span>
<span data-ttu-id="0d4cb-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-162">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0d4cb-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d4cb-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="0d4cb-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0d4cb-164">Request</span></span>
<span data-ttu-id="0d4cb-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses/{deviceComplianceDeviceStatusId}
Content-type: application/json
Content-length: 377

{
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "platform": 8,
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="0d4cb-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d4cb-166">Response</span></span>
<span data-ttu-id="0d4cb-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0d4cb-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 493

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceStatus",
  "id": "c6c78124-8124-c6c7-2481-c7c62481c7c6",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "platform": 8,
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```





