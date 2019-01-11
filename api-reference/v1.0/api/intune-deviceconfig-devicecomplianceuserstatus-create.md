---
title: Crear deviceComplianceUserStatus
description: Cree un objeto deviceComplianceUserStatus.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b4e82a3ead9e4ab36fd5f94a71afc5558f7482de
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849325"
---
# <a name="create-devicecomplianceuserstatus"></a><span data-ttu-id="4d2a7-103">Crear deviceComplianceUserStatus</span><span class="sxs-lookup"><span data-stu-id="4d2a7-103">Create deviceComplianceUserStatus</span></span>

> <span data-ttu-id="4d2a7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4d2a7-105">Cree un objeto [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="4d2a7-105">Create a new [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4d2a7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4d2a7-106">Prerequisites</span></span>
<span data-ttu-id="4d2a7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d2a7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4d2a7-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d2a7-109">Permission type</span></span>|<span data-ttu-id="4d2a7-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d2a7-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4d2a7-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d2a7-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4d2a7-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d2a7-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4d2a7-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d2a7-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4d2a7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-114">Not supported.</span></span>|
|<span data-ttu-id="4d2a7-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d2a7-115">Application</span></span>|<span data-ttu-id="4d2a7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4d2a7-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d2a7-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="4d2a7-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2a7-118">Request headers</span></span>
|<span data-ttu-id="4d2a7-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d2a7-119">Header</span></span>|<span data-ttu-id="4d2a7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4d2a7-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4d2a7-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="4d2a7-121">Authorization</span></span>|<span data-ttu-id="4d2a7-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4d2a7-123">Accept</span><span class="sxs-lookup"><span data-stu-id="4d2a7-123">Accept</span></span>|<span data-ttu-id="4d2a7-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4d2a7-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4d2a7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2a7-125">Request body</span></span>
<span data-ttu-id="4d2a7-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceUserStatus.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-126">In the request body, supply a JSON representation for the deviceComplianceUserStatus object.</span></span>

<span data-ttu-id="4d2a7-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceUserStatus.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-127">The following table shows the properties that are required when you create the deviceComplianceUserStatus.</span></span>

|<span data-ttu-id="4d2a7-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d2a7-128">Property</span></span>|<span data-ttu-id="4d2a7-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d2a7-129">Type</span></span>|<span data-ttu-id="4d2a7-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d2a7-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4d2a7-131">id</span><span class="sxs-lookup"><span data-stu-id="4d2a7-131">id</span></span>|<span data-ttu-id="4d2a7-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="4d2a7-132">String</span></span>|<span data-ttu-id="4d2a7-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-133">Key of the entity.</span></span>|
|<span data-ttu-id="4d2a7-134">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="4d2a7-134">userDisplayName</span></span>|<span data-ttu-id="4d2a7-135">String</span><span class="sxs-lookup"><span data-stu-id="4d2a7-135">String</span></span>|<span data-ttu-id="4d2a7-136">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-136">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="4d2a7-137">devicesCount</span><span class="sxs-lookup"><span data-stu-id="4d2a7-137">devicesCount</span></span>|<span data-ttu-id="4d2a7-138">Int32</span><span class="sxs-lookup"><span data-stu-id="4d2a7-138">Int32</span></span>|<span data-ttu-id="4d2a7-139">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-139">Devices count for that user.</span></span>|
|<span data-ttu-id="4d2a7-140">status</span><span class="sxs-lookup"><span data-stu-id="4d2a7-140">status</span></span>|[<span data-ttu-id="4d2a7-141">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="4d2a7-141">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="4d2a7-142">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-142">Compliance status of the policy report.</span></span> <span data-ttu-id="4d2a7-143">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-143">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="4d2a7-144">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="4d2a7-144">lastReportedDateTime</span></span>|<span data-ttu-id="4d2a7-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4d2a7-145">DateTimeOffset</span></span>|<span data-ttu-id="4d2a7-146">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-146">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="4d2a7-147">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4d2a7-147">userPrincipalName</span></span>|<span data-ttu-id="4d2a7-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="4d2a7-148">String</span></span>|<span data-ttu-id="4d2a7-149">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-149">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="4d2a7-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d2a7-150">Response</span></span>
<span data-ttu-id="4d2a7-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-151">If successful, this method returns a `201 Created` response code and a [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d2a7-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d2a7-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="4d2a7-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d2a7-153">Request</span></span>
<span data-ttu-id="4d2a7-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-154">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatuses
Content-type: application/json
Content-length: 287

{
  "@odata.type": "#microsoft.graph.deviceComplianceUserStatus",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="4d2a7-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d2a7-155">Response</span></span>
<span data-ttu-id="4d2a7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4d2a7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



