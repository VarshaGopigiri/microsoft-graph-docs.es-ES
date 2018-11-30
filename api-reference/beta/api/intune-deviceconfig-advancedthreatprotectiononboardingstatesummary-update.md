---
title: Actualizar advancedThreatProtectionOnboardingStateSummary
description: Actualizar las propiedades de un objeto advancedThreatProtectionOnboardingStateSummary.
ms.openlocfilehash: e39a6086f78db393a3e75a99b475cc5db02ddb3d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089723"
---
# <a name="update-advancedthreatprotectiononboardingstatesummary"></a><span data-ttu-id="a7537-103">Actualizar advancedThreatProtectionOnboardingStateSummary</span><span class="sxs-lookup"><span data-stu-id="a7537-103">Update advancedThreatProtectionOnboardingStateSummary</span></span>

> <span data-ttu-id="a7537-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a7537-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a7537-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a7537-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a7537-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a7537-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a7537-107">Actualizar las propiedades de un objeto [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) .</span><span class="sxs-lookup"><span data-stu-id="a7537-107">Update the properties of a [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a7537-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a7537-108">Prerequisites</span></span>
<span data-ttu-id="a7537-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7537-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7537-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7537-111">Permission type</span></span>|<span data-ttu-id="a7537-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7537-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a7537-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7537-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a7537-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a7537-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a7537-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7537-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a7537-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7537-116">Not supported.</span></span>|
|<span data-ttu-id="a7537-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7537-117">Application</span></span>|<span data-ttu-id="a7537-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a7537-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a7537-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7537-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/advancedThreatProtectionOnboardingStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="a7537-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7537-120">Request headers</span></span>
|<span data-ttu-id="a7537-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7537-121">Header</span></span>|<span data-ttu-id="a7537-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a7537-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a7537-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7537-123">Authorization</span></span>|<span data-ttu-id="a7537-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a7537-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a7537-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a7537-125">Accept</span></span>|<span data-ttu-id="a7537-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a7537-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a7537-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7537-127">Request body</span></span>
<span data-ttu-id="a7537-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) .</span><span class="sxs-lookup"><span data-stu-id="a7537-128">In the request body, supply a JSON representation for the [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) object.</span></span>

<span data-ttu-id="a7537-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="a7537-129">The following table shows the properties that are required when you create the [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md).</span></span>

|<span data-ttu-id="a7537-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a7537-130">Property</span></span>|<span data-ttu-id="a7537-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7537-131">Type</span></span>|<span data-ttu-id="a7537-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7537-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a7537-133">id</span><span class="sxs-lookup"><span data-stu-id="a7537-133">id</span></span>|<span data-ttu-id="a7537-134">String</span><span class="sxs-lookup"><span data-stu-id="a7537-134">String</span></span>|<span data-ttu-id="a7537-135">Identificador único</span><span class="sxs-lookup"><span data-stu-id="a7537-135">Unique Identifier</span></span>|
|<span data-ttu-id="a7537-136">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-136">unknownDeviceCount</span></span>|<span data-ttu-id="a7537-137">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-137">Int32</span></span>|<span data-ttu-id="a7537-138">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="a7537-138">Number of unknown devices</span></span>|
|<span data-ttu-id="a7537-139">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-139">notApplicableDeviceCount</span></span>|<span data-ttu-id="a7537-140">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-140">Int32</span></span>|<span data-ttu-id="a7537-141">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="a7537-141">Number of not applicable devices</span></span>|
|<span data-ttu-id="a7537-142">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-142">compliantDeviceCount</span></span>|<span data-ttu-id="a7537-143">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-143">Int32</span></span>|<span data-ttu-id="a7537-144">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="a7537-144">Number of compliant devices</span></span>|
|<span data-ttu-id="a7537-145">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-145">remediatedDeviceCount</span></span>|<span data-ttu-id="a7537-146">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-146">Int32</span></span>|<span data-ttu-id="a7537-147">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="a7537-147">Number of remediated devices</span></span>|
|<span data-ttu-id="a7537-148">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-148">nonCompliantDeviceCount</span></span>|<span data-ttu-id="a7537-149">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-149">Int32</span></span>|<span data-ttu-id="a7537-150">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="a7537-150">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="a7537-151">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-151">errorDeviceCount</span></span>|<span data-ttu-id="a7537-152">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-152">Int32</span></span>|<span data-ttu-id="a7537-153">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="a7537-153">Number of error devices</span></span>|
|<span data-ttu-id="a7537-154">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-154">conflictDeviceCount</span></span>|<span data-ttu-id="a7537-155">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-155">Int32</span></span>|<span data-ttu-id="a7537-156">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="a7537-156">Number of conflict devices</span></span>|
|<span data-ttu-id="a7537-157">notAssignedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a7537-157">notAssignedDeviceCount</span></span>|<span data-ttu-id="a7537-158">Int32</span><span class="sxs-lookup"><span data-stu-id="a7537-158">Int32</span></span>|<span data-ttu-id="a7537-159">Número de dispositivos no asignados</span><span class="sxs-lookup"><span data-stu-id="a7537-159">Number of not assigned devices</span></span>|



## <a name="response"></a><span data-ttu-id="a7537-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7537-160">Response</span></span>
<span data-ttu-id="a7537-161">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7537-161">If successful, this method returns a `200 OK` response code and an updated [advancedThreatProtectionOnboardingStateSummary](../resources/intune-deviceconfig-advancedthreatprotectiononboardingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7537-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7537-162">Example</span></span>
### <a name="request"></a><span data-ttu-id="a7537-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7537-163">Request</span></span>
<span data-ttu-id="a7537-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7537-164">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/advancedThreatProtectionOnboardingStateSummary
Content-type: application/json
Content-length: 246

{
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3,
  "notAssignedDeviceCount": 6
}
```

### <a name="response"></a><span data-ttu-id="a7537-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7537-165">Response</span></span>
<span data-ttu-id="a7537-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7537-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 380

{
  "@odata.type": "#microsoft.graph.advancedThreatProtectionOnboardingStateSummary",
  "id": "74089602-9602-7408-0296-087402960874",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3,
  "notAssignedDeviceCount": 6
}
```




