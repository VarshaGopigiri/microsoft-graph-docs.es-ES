---
title: Actualizar softwareUpdateStatusSummary
description: Actualice las propiedades de un objeto softwareUpdateStatusSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c1437e55807e2fba92efb7dab3b908f8bae88487
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837299"
---
# <a name="update-softwareupdatestatussummary"></a><span data-ttu-id="4bb20-103">Actualizar softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="4bb20-103">Update softwareUpdateStatusSummary</span></span>

> <span data-ttu-id="4bb20-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4bb20-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4bb20-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4bb20-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4bb20-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4bb20-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4bb20-107">Actualice las propiedades de un objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="4bb20-107">Update the properties of a [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4bb20-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4bb20-108">Prerequisites</span></span>
<span data-ttu-id="4bb20-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4bb20-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4bb20-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4bb20-111">Permission type</span></span>|<span data-ttu-id="4bb20-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4bb20-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4bb20-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4bb20-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4bb20-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4bb20-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4bb20-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4bb20-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4bb20-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bb20-116">Not supported.</span></span>|
|<span data-ttu-id="4bb20-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4bb20-117">Application</span></span>|<span data-ttu-id="4bb20-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4bb20-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4bb20-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4bb20-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/softwareUpdateStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="4bb20-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4bb20-120">Request headers</span></span>
|<span data-ttu-id="4bb20-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bb20-121">Header</span></span>|<span data-ttu-id="4bb20-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4bb20-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4bb20-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4bb20-123">Authorization</span></span>|<span data-ttu-id="4bb20-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4bb20-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4bb20-125">Accept</span><span class="sxs-lookup"><span data-stu-id="4bb20-125">Accept</span></span>|<span data-ttu-id="4bb20-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4bb20-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4bb20-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4bb20-127">Request body</span></span>
<span data-ttu-id="4bb20-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="4bb20-128">In the request body, supply a JSON representation for the [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object.</span></span>

<span data-ttu-id="4bb20-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="4bb20-129">The following table shows the properties that are required when you create the [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span></span>

|<span data-ttu-id="4bb20-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4bb20-130">Property</span></span>|<span data-ttu-id="4bb20-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bb20-131">Type</span></span>|<span data-ttu-id="4bb20-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bb20-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4bb20-133">id</span><span class="sxs-lookup"><span data-stu-id="4bb20-133">id</span></span>|<span data-ttu-id="4bb20-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="4bb20-134">String</span></span>|<span data-ttu-id="4bb20-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4bb20-135">Key of the entity.</span></span>|
|<span data-ttu-id="4bb20-136">displayName</span><span class="sxs-lookup"><span data-stu-id="4bb20-136">displayName</span></span>|<span data-ttu-id="4bb20-137">String</span><span class="sxs-lookup"><span data-stu-id="4bb20-137">String</span></span>|<span data-ttu-id="4bb20-138">El nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="4bb20-138">The name of the policy.</span></span>|
|<span data-ttu-id="4bb20-139">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-139">compliantDeviceCount</span></span>|<span data-ttu-id="4bb20-140">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-140">Int32</span></span>|<span data-ttu-id="4bb20-141">Número de dispositivos compatibles.</span><span class="sxs-lookup"><span data-stu-id="4bb20-141">Number of compliant devices.</span></span>|
|<span data-ttu-id="4bb20-142">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-142">nonCompliantDeviceCount</span></span>|<span data-ttu-id="4bb20-143">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-143">Int32</span></span>|<span data-ttu-id="4bb20-144">Número de dispositivos no compatibles.</span><span class="sxs-lookup"><span data-stu-id="4bb20-144">Number of non compliant devices.</span></span>|
|<span data-ttu-id="4bb20-145">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-145">remediatedDeviceCount</span></span>|<span data-ttu-id="4bb20-146">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-146">Int32</span></span>|<span data-ttu-id="4bb20-147">Número de dispositivos corregidos.</span><span class="sxs-lookup"><span data-stu-id="4bb20-147">Number of remediated devices.</span></span>|
|<span data-ttu-id="4bb20-148">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-148">errorDeviceCount</span></span>|<span data-ttu-id="4bb20-149">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-149">Int32</span></span>|<span data-ttu-id="4bb20-150">Número de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="4bb20-150">Number of devices had error.</span></span>|
|<span data-ttu-id="4bb20-151">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-151">unknownDeviceCount</span></span>|<span data-ttu-id="4bb20-152">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-152">Int32</span></span>|<span data-ttu-id="4bb20-153">Número de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="4bb20-153">Number of unknown devices.</span></span>|
|<span data-ttu-id="4bb20-154">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-154">conflictDeviceCount</span></span>|<span data-ttu-id="4bb20-155">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-155">Int32</span></span>|<span data-ttu-id="4bb20-156">Número de dispositivos en conflicto.</span><span class="sxs-lookup"><span data-stu-id="4bb20-156">Number of conflict devices.</span></span>|
|<span data-ttu-id="4bb20-157">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-157">notApplicableDeviceCount</span></span>|<span data-ttu-id="4bb20-158">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-158">Int32</span></span>|<span data-ttu-id="4bb20-159">Número de dispositivos no aplicables.</span><span class="sxs-lookup"><span data-stu-id="4bb20-159">Number of not applicable devices.</span></span>|
|<span data-ttu-id="4bb20-160">compliantUserCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-160">compliantUserCount</span></span>|<span data-ttu-id="4bb20-161">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-161">Int32</span></span>|<span data-ttu-id="4bb20-162">Número de usuarios compatibles.</span><span class="sxs-lookup"><span data-stu-id="4bb20-162">Number of compliant users.</span></span>|
|<span data-ttu-id="4bb20-163">nonCompliantUserCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-163">nonCompliantUserCount</span></span>|<span data-ttu-id="4bb20-164">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-164">Int32</span></span>|<span data-ttu-id="4bb20-165">Número de usuarios no compatibles.</span><span class="sxs-lookup"><span data-stu-id="4bb20-165">Number of non compliant users.</span></span>|
|<span data-ttu-id="4bb20-166">remediatedUserCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-166">remediatedUserCount</span></span>|<span data-ttu-id="4bb20-167">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-167">Int32</span></span>|<span data-ttu-id="4bb20-168">Número de usuarios corregidos.</span><span class="sxs-lookup"><span data-stu-id="4bb20-168">Number of remediated users.</span></span>|
|<span data-ttu-id="4bb20-169">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-169">errorUserCount</span></span>|<span data-ttu-id="4bb20-170">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-170">Int32</span></span>|<span data-ttu-id="4bb20-171">Número de usuarios con errores.</span><span class="sxs-lookup"><span data-stu-id="4bb20-171">Number of users had error.</span></span>|
|<span data-ttu-id="4bb20-172">unknownUserCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-172">unknownUserCount</span></span>|<span data-ttu-id="4bb20-173">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-173">Int32</span></span>|<span data-ttu-id="4bb20-174">Número de usuarios desconocidos.</span><span class="sxs-lookup"><span data-stu-id="4bb20-174">Number of unknown users.</span></span>|
|<span data-ttu-id="4bb20-175">conflictUserCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-175">conflictUserCount</span></span>|<span data-ttu-id="4bb20-176">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-176">Int32</span></span>|<span data-ttu-id="4bb20-177">Número de usuarios en conflicto.</span><span class="sxs-lookup"><span data-stu-id="4bb20-177">Number of conflict users.</span></span>|
|<span data-ttu-id="4bb20-178">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="4bb20-178">notApplicableUserCount</span></span>|<span data-ttu-id="4bb20-179">Int32</span><span class="sxs-lookup"><span data-stu-id="4bb20-179">Int32</span></span>|<span data-ttu-id="4bb20-180">Número de usuarios no aplicables.</span><span class="sxs-lookup"><span data-stu-id="4bb20-180">Number of not applicable users.</span></span>|



## <a name="response"></a><span data-ttu-id="4bb20-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bb20-181">Response</span></span>
<span data-ttu-id="4bb20-182">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4bb20-182">If successful, this method returns a `200 OK` response code and an updated [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4bb20-183">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4bb20-183">Example</span></span>
### <a name="request"></a><span data-ttu-id="4bb20-184">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4bb20-184">Request</span></span>
<span data-ttu-id="4bb20-185">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4bb20-185">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/softwareUpdateStatusSummary
Content-type: application/json
Content-length: 452

{
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

### <a name="response"></a><span data-ttu-id="4bb20-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4bb20-186">Response</span></span>
<span data-ttu-id="4bb20-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4bb20-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





