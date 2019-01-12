---
title: Crear deviceConfigurationUserStatus
description: Cree un objeto deviceConfigurationUserStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f45158eff675f27f67cc17c36198b530438134bd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27971546"
---
# <a name="create-deviceconfigurationuserstatus"></a><span data-ttu-id="ebe1e-103">Crear deviceConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="ebe1e-103">Create deviceConfigurationUserStatus</span></span>

> <span data-ttu-id="ebe1e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ebe1e-105">Cree un objeto [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="ebe1e-105">Create a new [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ebe1e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ebe1e-106">Prerequisites</span></span>
<span data-ttu-id="ebe1e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ebe1e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ebe1e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebe1e-109">Permission type</span></span>|<span data-ttu-id="ebe1e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebe1e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ebe1e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebe1e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ebe1e-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ebe1e-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ebe1e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebe1e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ebe1e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-114">Not supported.</span></span>|
|<span data-ttu-id="ebe1e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebe1e-115">Application</span></span>|<span data-ttu-id="ebe1e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ebe1e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebe1e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="ebe1e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebe1e-118">Request headers</span></span>
|<span data-ttu-id="ebe1e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebe1e-119">Header</span></span>|<span data-ttu-id="ebe1e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ebe1e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ebe1e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ebe1e-121">Authorization</span></span>|<span data-ttu-id="ebe1e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ebe1e-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ebe1e-123">Accept</span></span>|<span data-ttu-id="ebe1e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ebe1e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ebe1e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebe1e-125">Request body</span></span>
<span data-ttu-id="ebe1e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-126">In the request body, supply a JSON representation for the deviceConfigurationUserStatus object.</span></span>

<span data-ttu-id="ebe1e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceConfigurationUserStatus.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-127">The following table shows the properties that are required when you create the deviceConfigurationUserStatus.</span></span>

|<span data-ttu-id="ebe1e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebe1e-128">Property</span></span>|<span data-ttu-id="ebe1e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebe1e-129">Type</span></span>|<span data-ttu-id="ebe1e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebe1e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ebe1e-131">id</span><span class="sxs-lookup"><span data-stu-id="ebe1e-131">id</span></span>|<span data-ttu-id="ebe1e-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="ebe1e-132">String</span></span>|<span data-ttu-id="ebe1e-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-133">Key of the entity.</span></span>|
|<span data-ttu-id="ebe1e-134">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="ebe1e-134">userDisplayName</span></span>|<span data-ttu-id="ebe1e-135">String</span><span class="sxs-lookup"><span data-stu-id="ebe1e-135">String</span></span>|<span data-ttu-id="ebe1e-136">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-136">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="ebe1e-137">devicesCount</span><span class="sxs-lookup"><span data-stu-id="ebe1e-137">devicesCount</span></span>|<span data-ttu-id="ebe1e-138">Int32</span><span class="sxs-lookup"><span data-stu-id="ebe1e-138">Int32</span></span>|<span data-ttu-id="ebe1e-139">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-139">Devices count for that user.</span></span>|
|<span data-ttu-id="ebe1e-140">status</span><span class="sxs-lookup"><span data-stu-id="ebe1e-140">status</span></span>|[<span data-ttu-id="ebe1e-141">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="ebe1e-141">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="ebe1e-142">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-142">Compliance status of the policy report.</span></span> <span data-ttu-id="ebe1e-143">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-143">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="ebe1e-144">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="ebe1e-144">lastReportedDateTime</span></span>|<span data-ttu-id="ebe1e-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ebe1e-145">DateTimeOffset</span></span>|<span data-ttu-id="ebe1e-146">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-146">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="ebe1e-147">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ebe1e-147">userPrincipalName</span></span>|<span data-ttu-id="ebe1e-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="ebe1e-148">String</span></span>|<span data-ttu-id="ebe1e-149">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-149">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="ebe1e-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebe1e-150">Response</span></span>
<span data-ttu-id="ebe1e-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-151">If successful, this method returns a `201 Created` response code and a [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ebe1e-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebe1e-152">Example</span></span>
### <a name="request"></a><span data-ttu-id="ebe1e-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebe1e-153">Request</span></span>
<span data-ttu-id="ebe1e-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-154">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses
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

### <a name="response"></a><span data-ttu-id="ebe1e-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebe1e-155">Response</span></span>
<span data-ttu-id="ebe1e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ebe1e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



