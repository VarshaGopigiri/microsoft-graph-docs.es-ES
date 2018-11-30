---
title: Actualizar softwareUpdateStatusSummary
description: Actualice las propiedades de un objeto softwareUpdateStatusSummary.
ms.openlocfilehash: 2c3c9688b7f2b7e24188ee6bdaff99dcfbb6605f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030926"
---
# <a name="update-softwareupdatestatussummary"></a><span data-ttu-id="b08c5-103">Actualizar softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="b08c5-103">Update softwareUpdateStatusSummary</span></span>

> <span data-ttu-id="b08c5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b08c5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b08c5-105">Actualice las propiedades de un objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="b08c5-105">Update the properties of a [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b08c5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b08c5-106">Prerequisites</span></span>
<span data-ttu-id="b08c5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b08c5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b08c5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b08c5-109">Permission type</span></span>|<span data-ttu-id="b08c5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b08c5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b08c5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b08c5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b08c5-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b08c5-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b08c5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b08c5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b08c5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b08c5-114">Not supported.</span></span>|
|<span data-ttu-id="b08c5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b08c5-115">Application</span></span>|<span data-ttu-id="b08c5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b08c5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b08c5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b08c5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/softwareUpdateStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="b08c5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b08c5-118">Request headers</span></span>
|<span data-ttu-id="b08c5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b08c5-119">Header</span></span>|<span data-ttu-id="b08c5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b08c5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b08c5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="b08c5-121">Authorization</span></span>|<span data-ttu-id="b08c5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b08c5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b08c5-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b08c5-123">Accept</span></span>|<span data-ttu-id="b08c5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b08c5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b08c5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b08c5-125">Request body</span></span>
<span data-ttu-id="b08c5-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="b08c5-126">In the request body, supply a JSON representation for the [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object.</span></span>

<span data-ttu-id="b08c5-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="b08c5-127">The following table shows the properties that are required when you create the [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span></span>

|<span data-ttu-id="b08c5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b08c5-128">Property</span></span>|<span data-ttu-id="b08c5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b08c5-129">Type</span></span>|<span data-ttu-id="b08c5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b08c5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b08c5-131">id</span><span class="sxs-lookup"><span data-stu-id="b08c5-131">id</span></span>|<span data-ttu-id="b08c5-132">String</span><span class="sxs-lookup"><span data-stu-id="b08c5-132">String</span></span>|<span data-ttu-id="b08c5-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b08c5-133">Key of the entity.</span></span>|
|<span data-ttu-id="b08c5-134">displayName</span><span class="sxs-lookup"><span data-stu-id="b08c5-134">displayName</span></span>|<span data-ttu-id="b08c5-135">String</span><span class="sxs-lookup"><span data-stu-id="b08c5-135">String</span></span>|<span data-ttu-id="b08c5-136">El nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="b08c5-136">The name of the policy.</span></span>|
|<span data-ttu-id="b08c5-137">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-137">compliantDeviceCount</span></span>|<span data-ttu-id="b08c5-138">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-138">Int32</span></span>|<span data-ttu-id="b08c5-139">Número de dispositivos compatibles.</span><span class="sxs-lookup"><span data-stu-id="b08c5-139">Number of compliant devices.</span></span>|
|<span data-ttu-id="b08c5-140">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-140">nonCompliantDeviceCount</span></span>|<span data-ttu-id="b08c5-141">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-141">Int32</span></span>|<span data-ttu-id="b08c5-142">Número de dispositivos no compatibles.</span><span class="sxs-lookup"><span data-stu-id="b08c5-142">Number of non compliant devices.</span></span>|
|<span data-ttu-id="b08c5-143">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-143">remediatedDeviceCount</span></span>|<span data-ttu-id="b08c5-144">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-144">Int32</span></span>|<span data-ttu-id="b08c5-145">Número de dispositivos corregidos.</span><span class="sxs-lookup"><span data-stu-id="b08c5-145">Number of remediated devices.</span></span>|
|<span data-ttu-id="b08c5-146">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-146">errorDeviceCount</span></span>|<span data-ttu-id="b08c5-147">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-147">Int32</span></span>|<span data-ttu-id="b08c5-148">Número de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="b08c5-148">Number of devices had error.</span></span>|
|<span data-ttu-id="b08c5-149">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-149">unknownDeviceCount</span></span>|<span data-ttu-id="b08c5-150">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-150">Int32</span></span>|<span data-ttu-id="b08c5-151">Número de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="b08c5-151">Number of unknown devices.</span></span>|
|<span data-ttu-id="b08c5-152">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-152">conflictDeviceCount</span></span>|<span data-ttu-id="b08c5-153">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-153">Int32</span></span>|<span data-ttu-id="b08c5-154">Número de dispositivos en conflicto.</span><span class="sxs-lookup"><span data-stu-id="b08c5-154">Number of conflict devices.</span></span>|
|<span data-ttu-id="b08c5-155">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-155">notApplicableDeviceCount</span></span>|<span data-ttu-id="b08c5-156">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-156">Int32</span></span>|<span data-ttu-id="b08c5-157">Número de dispositivos no aplicables.</span><span class="sxs-lookup"><span data-stu-id="b08c5-157">Number of not applicable devices.</span></span>|
|<span data-ttu-id="b08c5-158">compliantUserCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-158">compliantUserCount</span></span>|<span data-ttu-id="b08c5-159">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-159">Int32</span></span>|<span data-ttu-id="b08c5-160">Número de usuarios compatibles.</span><span class="sxs-lookup"><span data-stu-id="b08c5-160">Number of compliant users.</span></span>|
|<span data-ttu-id="b08c5-161">nonCompliantUserCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-161">nonCompliantUserCount</span></span>|<span data-ttu-id="b08c5-162">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-162">Int32</span></span>|<span data-ttu-id="b08c5-163">Número de usuarios no compatibles.</span><span class="sxs-lookup"><span data-stu-id="b08c5-163">Number of non compliant users.</span></span>|
|<span data-ttu-id="b08c5-164">remediatedUserCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-164">remediatedUserCount</span></span>|<span data-ttu-id="b08c5-165">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-165">Int32</span></span>|<span data-ttu-id="b08c5-166">Número de usuarios corregidos.</span><span class="sxs-lookup"><span data-stu-id="b08c5-166">Number of remediated users.</span></span>|
|<span data-ttu-id="b08c5-167">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-167">errorUserCount</span></span>|<span data-ttu-id="b08c5-168">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-168">Int32</span></span>|<span data-ttu-id="b08c5-169">Número de usuarios con errores.</span><span class="sxs-lookup"><span data-stu-id="b08c5-169">Number of users had error.</span></span>|
|<span data-ttu-id="b08c5-170">unknownUserCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-170">unknownUserCount</span></span>|<span data-ttu-id="b08c5-171">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-171">Int32</span></span>|<span data-ttu-id="b08c5-172">Número de usuarios desconocidos.</span><span class="sxs-lookup"><span data-stu-id="b08c5-172">Number of unknown users.</span></span>|
|<span data-ttu-id="b08c5-173">conflictUserCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-173">conflictUserCount</span></span>|<span data-ttu-id="b08c5-174">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-174">Int32</span></span>|<span data-ttu-id="b08c5-175">Número de usuarios en conflicto.</span><span class="sxs-lookup"><span data-stu-id="b08c5-175">Number of conflict users.</span></span>|
|<span data-ttu-id="b08c5-176">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="b08c5-176">notApplicableUserCount</span></span>|<span data-ttu-id="b08c5-177">Int32</span><span class="sxs-lookup"><span data-stu-id="b08c5-177">Int32</span></span>|<span data-ttu-id="b08c5-178">Número de usuarios no aplicables.</span><span class="sxs-lookup"><span data-stu-id="b08c5-178">Number of not applicable users.</span></span>|



## <a name="response"></a><span data-ttu-id="b08c5-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b08c5-179">Response</span></span>
<span data-ttu-id="b08c5-180">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b08c5-180">If successful, this method returns a `200 OK` response code and an updated [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b08c5-181">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b08c5-181">Example</span></span>
### <a name="request"></a><span data-ttu-id="b08c5-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b08c5-182">Request</span></span>
<span data-ttu-id="b08c5-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b08c5-183">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/softwareUpdateStatusSummary
Content-type: application/json
Content-length: 518

{
  "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
  "displayName": "Display Name value",
  "compliantDeviceCount": 4,
  "nonCompliantDeviceCount": 7,
  "remediatedDeviceCount": 5,
  "errorDeviceCount": 0,
  "unknownDeviceCount": 2,
  "conflictDeviceCount": 3,
  "notApplicableDeviceCount": 8,
  "compliantUserCount": 2,
  "nonCompliantUserCount": 5,
  "remediatedUserCount": 3,
  "errorUserCount": 14,
  "unknownUserCount": 0,
  "conflictUserCount": 1,
  "notApplicableUserCount": 6
}
```

### <a name="response"></a><span data-ttu-id="b08c5-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b08c5-184">Response</span></span>
<span data-ttu-id="b08c5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b08c5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 567

{
  "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
  "id": "4f71421f-421f-4f71-1f42-714f1f42714f",
  "displayName": "Display Name value",
  "compliantDeviceCount": 4,
  "nonCompliantDeviceCount": 7,
  "remediatedDeviceCount": 5,
  "errorDeviceCount": 0,
  "unknownDeviceCount": 2,
  "conflictDeviceCount": 3,
  "notApplicableDeviceCount": 8,
  "compliantUserCount": 2,
  "nonCompliantUserCount": 5,
  "remediatedUserCount": 3,
  "errorUserCount": 14,
  "unknownUserCount": 0,
  "conflictUserCount": 1,
  "notApplicableUserCount": 6
}
```



