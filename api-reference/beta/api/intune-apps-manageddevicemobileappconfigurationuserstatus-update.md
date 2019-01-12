---
title: Actualizar managedDeviceMobileAppConfigurationUserStatus
description: Actualice las propiedades de un objeto managedDeviceMobileAppConfigurationUserStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 47c6f6831702cf0b86b0b34574392f18ea1bbe50
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930225"
---
# <a name="update-manageddevicemobileappconfigurationuserstatus"></a><span data-ttu-id="9935e-103">Actualizar managedDeviceMobileAppConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="9935e-103">Update managedDeviceMobileAppConfigurationUserStatus</span></span>

> <span data-ttu-id="9935e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9935e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9935e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9935e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9935e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9935e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9935e-107">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9935e-107">Update the properties of a [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9935e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9935e-108">Prerequisites</span></span>
<span data-ttu-id="9935e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9935e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9935e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9935e-111">Permission type</span></span>|<span data-ttu-id="9935e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9935e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9935e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9935e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9935e-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9935e-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="9935e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9935e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9935e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9935e-116">Not supported.</span></span>|
|<span data-ttu-id="9935e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9935e-117">Application</span></span>|<span data-ttu-id="9935e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9935e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9935e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9935e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
PATCH /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="9935e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9935e-120">Request headers</span></span>
|<span data-ttu-id="9935e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9935e-121">Header</span></span>|<span data-ttu-id="9935e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9935e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9935e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9935e-123">Authorization</span></span>|<span data-ttu-id="9935e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9935e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9935e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9935e-125">Accept</span></span>|<span data-ttu-id="9935e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9935e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9935e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9935e-127">Request body</span></span>
<span data-ttu-id="9935e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9935e-128">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) object.</span></span>

<span data-ttu-id="9935e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="9935e-129">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md).</span></span>

|<span data-ttu-id="9935e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9935e-130">Property</span></span>|<span data-ttu-id="9935e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9935e-131">Type</span></span>|<span data-ttu-id="9935e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9935e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9935e-133">id</span><span class="sxs-lookup"><span data-stu-id="9935e-133">id</span></span>|<span data-ttu-id="9935e-134">String</span><span class="sxs-lookup"><span data-stu-id="9935e-134">String</span></span>|<span data-ttu-id="9935e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9935e-135">Key of the entity.</span></span>|
|<span data-ttu-id="9935e-136">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="9935e-136">userDisplayName</span></span>|<span data-ttu-id="9935e-137">String</span><span class="sxs-lookup"><span data-stu-id="9935e-137">String</span></span>|<span data-ttu-id="9935e-138">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="9935e-138">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="9935e-139">devicesCount</span><span class="sxs-lookup"><span data-stu-id="9935e-139">devicesCount</span></span>|<span data-ttu-id="9935e-140">Int32</span><span class="sxs-lookup"><span data-stu-id="9935e-140">Int32</span></span>|<span data-ttu-id="9935e-141">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="9935e-141">Devices count for that user.</span></span>|
|<span data-ttu-id="9935e-142">status</span><span class="sxs-lookup"><span data-stu-id="9935e-142">status</span></span>|[<span data-ttu-id="9935e-143">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="9935e-143">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="9935e-144">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="9935e-144">Compliance status of the policy report.</span></span> <span data-ttu-id="9935e-145">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="9935e-145">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="9935e-146">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="9935e-146">lastReportedDateTime</span></span>|<span data-ttu-id="9935e-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9935e-147">DateTimeOffset</span></span>|<span data-ttu-id="9935e-148">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="9935e-148">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="9935e-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9935e-149">userPrincipalName</span></span>|<span data-ttu-id="9935e-150">String</span><span class="sxs-lookup"><span data-stu-id="9935e-150">String</span></span>|<span data-ttu-id="9935e-151">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="9935e-151">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="9935e-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9935e-152">Response</span></span>
<span data-ttu-id="9935e-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9935e-153">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9935e-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9935e-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="9935e-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9935e-155">Request</span></span>
<span data-ttu-id="9935e-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9935e-156">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="9935e-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9935e-157">Response</span></span>
<span data-ttu-id="9935e-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9935e-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





