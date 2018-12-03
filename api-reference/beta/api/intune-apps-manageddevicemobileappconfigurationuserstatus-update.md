---
title: Actualizar managedDeviceMobileAppConfigurationUserStatus
description: Actualice las propiedades de un objeto managedDeviceMobileAppConfigurationUserStatus.
ms.openlocfilehash: 8fdcb93c01bd2132a69c2bb41de5ff8a5ecf801d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089034"
---
# <a name="update-manageddevicemobileappconfigurationuserstatus"></a><span data-ttu-id="38bcb-103">Actualizar managedDeviceMobileAppConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="38bcb-103">Update managedDeviceMobileAppConfigurationUserStatus</span></span>

> <span data-ttu-id="38bcb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38bcb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38bcb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38bcb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="38bcb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="38bcb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="38bcb-107">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="38bcb-107">Update the properties of a [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="38bcb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="38bcb-108">Prerequisites</span></span>
<span data-ttu-id="38bcb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38bcb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38bcb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38bcb-111">Permission type</span></span>|<span data-ttu-id="38bcb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38bcb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="38bcb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38bcb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="38bcb-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="38bcb-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="38bcb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38bcb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="38bcb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38bcb-116">Not supported.</span></span>|
|<span data-ttu-id="38bcb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38bcb-117">Application</span></span>|<span data-ttu-id="38bcb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38bcb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="38bcb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38bcb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
PATCH /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="38bcb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38bcb-120">Request headers</span></span>
|<span data-ttu-id="38bcb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38bcb-121">Header</span></span>|<span data-ttu-id="38bcb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="38bcb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="38bcb-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="38bcb-123">Authorization</span></span>|<span data-ttu-id="38bcb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="38bcb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="38bcb-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="38bcb-125">Accept</span></span>|<span data-ttu-id="38bcb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="38bcb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="38bcb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38bcb-127">Request body</span></span>
<span data-ttu-id="38bcb-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="38bcb-128">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) object.</span></span>

<span data-ttu-id="38bcb-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="38bcb-129">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span></span>

|<span data-ttu-id="38bcb-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38bcb-130">Property</span></span>|<span data-ttu-id="38bcb-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="38bcb-131">Type</span></span>|<span data-ttu-id="38bcb-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="38bcb-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="38bcb-133">id</span><span class="sxs-lookup"><span data-stu-id="38bcb-133">id</span></span>|<span data-ttu-id="38bcb-134">String</span><span class="sxs-lookup"><span data-stu-id="38bcb-134">String</span></span>|<span data-ttu-id="38bcb-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="38bcb-135">Key of the entity.</span></span>|
|<span data-ttu-id="38bcb-136">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="38bcb-136">userDisplayName</span></span>|<span data-ttu-id="38bcb-137">String</span><span class="sxs-lookup"><span data-stu-id="38bcb-137">String</span></span>|<span data-ttu-id="38bcb-138">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="38bcb-138">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="38bcb-139">devicesCount</span><span class="sxs-lookup"><span data-stu-id="38bcb-139">devicesCount</span></span>|<span data-ttu-id="38bcb-140">Int32</span><span class="sxs-lookup"><span data-stu-id="38bcb-140">Int32</span></span>|<span data-ttu-id="38bcb-141">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="38bcb-141">Devices count for that user.</span></span>|
|<span data-ttu-id="38bcb-142">status</span><span class="sxs-lookup"><span data-stu-id="38bcb-142">status</span></span>|[<span data-ttu-id="38bcb-143">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="38bcb-143">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="38bcb-144">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="38bcb-144">Compliance status of the policy report.</span></span> <span data-ttu-id="38bcb-145">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="38bcb-145">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="38bcb-146">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="38bcb-146">lastReportedDateTime</span></span>|<span data-ttu-id="38bcb-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="38bcb-147">DateTimeOffset</span></span>|<span data-ttu-id="38bcb-148">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="38bcb-148">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="38bcb-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="38bcb-149">userPrincipalName</span></span>|<span data-ttu-id="38bcb-150">String</span><span class="sxs-lookup"><span data-stu-id="38bcb-150">String</span></span>|<span data-ttu-id="38bcb-151">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="38bcb-151">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="38bcb-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38bcb-152">Response</span></span>
<span data-ttu-id="38bcb-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38bcb-153">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38bcb-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38bcb-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="38bcb-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38bcb-155">Request</span></span>
<span data-ttu-id="38bcb-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38bcb-156">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
Content-type: application/json
Content-length: 222

{
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="38bcb-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38bcb-157">Response</span></span>
<span data-ttu-id="38bcb-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38bcb-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 355

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserStatus",
  "id": "44960944-0944-4496-4409-964444099644",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```




