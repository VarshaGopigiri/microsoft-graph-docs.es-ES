---
title: Crear deviceConfigurationUserStatus
description: Cree un objeto deviceConfigurationUserStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 996e470c97ace1ba56f0a695ff22226e19628e62
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948306"
---
# <a name="create-deviceconfigurationuserstatus"></a><span data-ttu-id="af4ad-103">Crear deviceConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="af4ad-103">Create deviceConfigurationUserStatus</span></span>

> <span data-ttu-id="af4ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af4ad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af4ad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af4ad-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="af4ad-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="af4ad-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="af4ad-107">Cree un objeto [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="af4ad-107">Create a new [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="af4ad-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="af4ad-108">Prerequisites</span></span>
<span data-ttu-id="af4ad-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="af4ad-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="af4ad-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="af4ad-111">Permission type</span></span>|<span data-ttu-id="af4ad-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="af4ad-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="af4ad-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="af4ad-113">Delegated (work or school account)</span></span>|<span data-ttu-id="af4ad-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="af4ad-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="af4ad-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="af4ad-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="af4ad-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="af4ad-116">Not supported.</span></span>|
|<span data-ttu-id="af4ad-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="af4ad-117">Application</span></span>|<span data-ttu-id="af4ad-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="af4ad-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="af4ad-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="af4ad-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/userStatuses
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="af4ad-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="af4ad-120">Request headers</span></span>
|<span data-ttu-id="af4ad-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af4ad-121">Header</span></span>|<span data-ttu-id="af4ad-122">Valor</span><span class="sxs-lookup"><span data-stu-id="af4ad-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="af4ad-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="af4ad-123">Authorization</span></span>|<span data-ttu-id="af4ad-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="af4ad-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="af4ad-125">Accept</span><span class="sxs-lookup"><span data-stu-id="af4ad-125">Accept</span></span>|<span data-ttu-id="af4ad-126">application/json</span><span class="sxs-lookup"><span data-stu-id="af4ad-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="af4ad-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="af4ad-127">Request body</span></span>
<span data-ttu-id="af4ad-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="af4ad-128">In the request body, supply a JSON representation for the deviceConfigurationUserStatus object.</span></span>

<span data-ttu-id="af4ad-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="af4ad-129">The following table shows the properties that are required when you create the deviceConfigurationUserStatus.</span></span>

|<span data-ttu-id="af4ad-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af4ad-130">Property</span></span>|<span data-ttu-id="af4ad-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="af4ad-131">Type</span></span>|<span data-ttu-id="af4ad-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="af4ad-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="af4ad-133">id</span><span class="sxs-lookup"><span data-stu-id="af4ad-133">id</span></span>|<span data-ttu-id="af4ad-134">String</span><span class="sxs-lookup"><span data-stu-id="af4ad-134">String</span></span>|<span data-ttu-id="af4ad-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="af4ad-135">Key of the entity.</span></span>|
|<span data-ttu-id="af4ad-136">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="af4ad-136">userDisplayName</span></span>|<span data-ttu-id="af4ad-137">String</span><span class="sxs-lookup"><span data-stu-id="af4ad-137">String</span></span>|<span data-ttu-id="af4ad-138">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="af4ad-138">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="af4ad-139">devicesCount</span><span class="sxs-lookup"><span data-stu-id="af4ad-139">devicesCount</span></span>|<span data-ttu-id="af4ad-140">Int32</span><span class="sxs-lookup"><span data-stu-id="af4ad-140">Int32</span></span>|<span data-ttu-id="af4ad-141">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="af4ad-141">Devices count for that user.</span></span>|
|<span data-ttu-id="af4ad-142">status</span><span class="sxs-lookup"><span data-stu-id="af4ad-142">status</span></span>|[<span data-ttu-id="af4ad-143">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="af4ad-143">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="af4ad-144">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="af4ad-144">Compliance status of the policy report.</span></span> <span data-ttu-id="af4ad-145">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="af4ad-145">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="af4ad-146">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="af4ad-146">lastReportedDateTime</span></span>|<span data-ttu-id="af4ad-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="af4ad-147">DateTimeOffset</span></span>|<span data-ttu-id="af4ad-148">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="af4ad-148">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="af4ad-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="af4ad-149">userPrincipalName</span></span>|<span data-ttu-id="af4ad-150">String</span><span class="sxs-lookup"><span data-stu-id="af4ad-150">String</span></span>|<span data-ttu-id="af4ad-151">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="af4ad-151">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="af4ad-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af4ad-152">Response</span></span>
<span data-ttu-id="af4ad-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="af4ad-153">If successful, this method returns a `201 Created` response code and a [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="af4ad-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af4ad-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="af4ad-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="af4ad-155">Request</span></span>
<span data-ttu-id="af4ad-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="af4ad-156">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses
Content-type: application/json
Content-length: 290

{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserStatus",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="af4ad-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af4ad-157">Response</span></span>
<span data-ttu-id="af4ad-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="af4ad-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 339

{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserStatus",
  "id": "7e323db2-3db2-7e32-b23d-327eb23d327e",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```





