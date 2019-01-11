---
title: Actualizar deviceComplianceUserStatus
description: Actualice las propiedades de un objeto deviceComplianceUserStatus.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 40d58158ca3a0e17f7f92b15a35f1b730d2511c4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852804"
---
# <a name="update-devicecomplianceuserstatus"></a><span data-ttu-id="5d1d7-103">Actualizar deviceComplianceUserStatus</span><span class="sxs-lookup"><span data-stu-id="5d1d7-103">Update deviceComplianceUserStatus</span></span>

> <span data-ttu-id="5d1d7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5d1d7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5d1d7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5d1d7-107">Actualice las propiedades de un objeto [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="5d1d7-107">Update the properties of a [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5d1d7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5d1d7-108">Prerequisites</span></span>
<span data-ttu-id="5d1d7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5d1d7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5d1d7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d1d7-111">Permission type</span></span>|<span data-ttu-id="5d1d7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d1d7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5d1d7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d1d7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5d1d7-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5d1d7-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5d1d7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d1d7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5d1d7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-116">Not supported.</span></span>|
|<span data-ttu-id="5d1d7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d1d7-117">Application</span></span>|<span data-ttu-id="5d1d7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5d1d7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d1d7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses/{deviceComplianceUserStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="5d1d7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d1d7-120">Request headers</span></span>
|<span data-ttu-id="5d1d7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d1d7-121">Header</span></span>|<span data-ttu-id="5d1d7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5d1d7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5d1d7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5d1d7-123">Authorization</span></span>|<span data-ttu-id="5d1d7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5d1d7-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5d1d7-125">Accept</span></span>|<span data-ttu-id="5d1d7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5d1d7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5d1d7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d1d7-127">Request body</span></span>
<span data-ttu-id="5d1d7-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="5d1d7-128">In the request body, supply a JSON representation for the [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) object.</span></span>

<span data-ttu-id="5d1d7-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="5d1d7-129">The following table shows the properties that are required when you create the [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md).</span></span>

|<span data-ttu-id="5d1d7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5d1d7-130">Property</span></span>|<span data-ttu-id="5d1d7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d1d7-131">Type</span></span>|<span data-ttu-id="5d1d7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d1d7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5d1d7-133">id</span><span class="sxs-lookup"><span data-stu-id="5d1d7-133">id</span></span>|<span data-ttu-id="5d1d7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d1d7-134">String</span></span>|<span data-ttu-id="5d1d7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-135">Key of the entity.</span></span>|
|<span data-ttu-id="5d1d7-136">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="5d1d7-136">userDisplayName</span></span>|<span data-ttu-id="5d1d7-137">String</span><span class="sxs-lookup"><span data-stu-id="5d1d7-137">String</span></span>|<span data-ttu-id="5d1d7-138">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-138">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="5d1d7-139">devicesCount</span><span class="sxs-lookup"><span data-stu-id="5d1d7-139">devicesCount</span></span>|<span data-ttu-id="5d1d7-140">Int32</span><span class="sxs-lookup"><span data-stu-id="5d1d7-140">Int32</span></span>|<span data-ttu-id="5d1d7-141">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-141">Devices count for that user.</span></span>|
|<span data-ttu-id="5d1d7-142">status</span><span class="sxs-lookup"><span data-stu-id="5d1d7-142">status</span></span>|[<span data-ttu-id="5d1d7-143">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="5d1d7-143">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="5d1d7-144">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-144">Compliance status of the policy report.</span></span> <span data-ttu-id="5d1d7-145">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-145">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="5d1d7-146">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="5d1d7-146">lastReportedDateTime</span></span>|<span data-ttu-id="5d1d7-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5d1d7-147">DateTimeOffset</span></span>|<span data-ttu-id="5d1d7-148">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-148">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="5d1d7-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5d1d7-149">userPrincipalName</span></span>|<span data-ttu-id="5d1d7-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d1d7-150">String</span></span>|<span data-ttu-id="5d1d7-151">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-151">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="5d1d7-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d1d7-152">Response</span></span>
<span data-ttu-id="5d1d7-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-153">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5d1d7-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d1d7-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="5d1d7-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d1d7-155">Request</span></span>
<span data-ttu-id="5d1d7-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-156">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses/{deviceComplianceUserStatusId}
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

### <a name="response"></a><span data-ttu-id="5d1d7-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d1d7-157">Response</span></span>
<span data-ttu-id="5d1d7-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d1d7-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 336

{
  "@odata.type": "#microsoft.graph.deviceComplianceUserStatus",
  "id": "a0b566cd-66cd-a0b5-cd66-b5a0cd66b5a0",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```





