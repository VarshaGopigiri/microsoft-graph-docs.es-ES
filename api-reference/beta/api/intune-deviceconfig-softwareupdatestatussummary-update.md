---
title: Actualizar softwareUpdateStatusSummary
description: Actualice las propiedades de un objeto softwareUpdateStatusSummary.
author: tfitzmac
ms.openlocfilehash: 6cb95a9bfb28e0488148d1f8773c87209c585b70
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302285"
---
# <a name="update-softwareupdatestatussummary"></a><span data-ttu-id="90643-103">Actualizar softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="90643-103">Update softwareUpdateStatusSummary</span></span>

> <span data-ttu-id="90643-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="90643-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="90643-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="90643-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="90643-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="90643-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="90643-107">Actualice las propiedades de un objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="90643-107">Update the properties of a [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="90643-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="90643-108">Prerequisites</span></span>
<span data-ttu-id="90643-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="90643-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="90643-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="90643-111">Permission type</span></span>|<span data-ttu-id="90643-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="90643-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="90643-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="90643-113">Delegated (work or school account)</span></span>|<span data-ttu-id="90643-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="90643-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="90643-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="90643-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="90643-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90643-116">Not supported.</span></span>|
|<span data-ttu-id="90643-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="90643-117">Application</span></span>|<span data-ttu-id="90643-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="90643-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="90643-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90643-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/softwareUpdateStatusSummary
```

## <a name="request-headers"></a><span data-ttu-id="90643-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90643-120">Request headers</span></span>
|<span data-ttu-id="90643-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90643-121">Header</span></span>|<span data-ttu-id="90643-122">Valor</span><span class="sxs-lookup"><span data-stu-id="90643-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="90643-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="90643-123">Authorization</span></span>|<span data-ttu-id="90643-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="90643-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="90643-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="90643-125">Accept</span></span>|<span data-ttu-id="90643-126">application/json</span><span class="sxs-lookup"><span data-stu-id="90643-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="90643-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="90643-127">Request body</span></span>
<span data-ttu-id="90643-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="90643-128">In the request body, supply a JSON representation for the [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object.</span></span>

<span data-ttu-id="90643-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="90643-129">The following table shows the properties that are required when you create the [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span></span>

|<span data-ttu-id="90643-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90643-130">Property</span></span>|<span data-ttu-id="90643-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="90643-131">Type</span></span>|<span data-ttu-id="90643-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="90643-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="90643-133">id</span><span class="sxs-lookup"><span data-stu-id="90643-133">id</span></span>|<span data-ttu-id="90643-134">String</span><span class="sxs-lookup"><span data-stu-id="90643-134">String</span></span>|<span data-ttu-id="90643-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="90643-135">Key of the entity.</span></span>|
|<span data-ttu-id="90643-136">displayName</span><span class="sxs-lookup"><span data-stu-id="90643-136">displayName</span></span>|<span data-ttu-id="90643-137">String</span><span class="sxs-lookup"><span data-stu-id="90643-137">String</span></span>|<span data-ttu-id="90643-138">El nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="90643-138">The name of the policy.</span></span>|
|<span data-ttu-id="90643-139">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="90643-139">compliantDeviceCount</span></span>|<span data-ttu-id="90643-140">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-140">Int32</span></span>|<span data-ttu-id="90643-141">Número de dispositivos compatibles.</span><span class="sxs-lookup"><span data-stu-id="90643-141">Number of compliant devices.</span></span>|
|<span data-ttu-id="90643-142">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="90643-142">nonCompliantDeviceCount</span></span>|<span data-ttu-id="90643-143">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-143">Int32</span></span>|<span data-ttu-id="90643-144">Número de dispositivos no compatibles.</span><span class="sxs-lookup"><span data-stu-id="90643-144">Number of non compliant devices.</span></span>|
|<span data-ttu-id="90643-145">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="90643-145">remediatedDeviceCount</span></span>|<span data-ttu-id="90643-146">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-146">Int32</span></span>|<span data-ttu-id="90643-147">Número de dispositivos corregidos.</span><span class="sxs-lookup"><span data-stu-id="90643-147">Number of remediated devices.</span></span>|
|<span data-ttu-id="90643-148">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="90643-148">errorDeviceCount</span></span>|<span data-ttu-id="90643-149">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-149">Int32</span></span>|<span data-ttu-id="90643-150">Número de dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="90643-150">Number of devices had error.</span></span>|
|<span data-ttu-id="90643-151">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="90643-151">unknownDeviceCount</span></span>|<span data-ttu-id="90643-152">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-152">Int32</span></span>|<span data-ttu-id="90643-153">Número de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="90643-153">Number of unknown devices.</span></span>|
|<span data-ttu-id="90643-154">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="90643-154">conflictDeviceCount</span></span>|<span data-ttu-id="90643-155">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-155">Int32</span></span>|<span data-ttu-id="90643-156">Número de dispositivos en conflicto.</span><span class="sxs-lookup"><span data-stu-id="90643-156">Number of conflict devices.</span></span>|
|<span data-ttu-id="90643-157">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="90643-157">notApplicableDeviceCount</span></span>|<span data-ttu-id="90643-158">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-158">Int32</span></span>|<span data-ttu-id="90643-159">Número de dispositivos no aplicables.</span><span class="sxs-lookup"><span data-stu-id="90643-159">Number of not applicable devices.</span></span>|
|<span data-ttu-id="90643-160">compliantUserCount</span><span class="sxs-lookup"><span data-stu-id="90643-160">compliantUserCount</span></span>|<span data-ttu-id="90643-161">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-161">Int32</span></span>|<span data-ttu-id="90643-162">Número de usuarios compatibles.</span><span class="sxs-lookup"><span data-stu-id="90643-162">Number of compliant users.</span></span>|
|<span data-ttu-id="90643-163">nonCompliantUserCount</span><span class="sxs-lookup"><span data-stu-id="90643-163">nonCompliantUserCount</span></span>|<span data-ttu-id="90643-164">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-164">Int32</span></span>|<span data-ttu-id="90643-165">Número de usuarios no compatibles.</span><span class="sxs-lookup"><span data-stu-id="90643-165">Number of non compliant users.</span></span>|
|<span data-ttu-id="90643-166">remediatedUserCount</span><span class="sxs-lookup"><span data-stu-id="90643-166">remediatedUserCount</span></span>|<span data-ttu-id="90643-167">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-167">Int32</span></span>|<span data-ttu-id="90643-168">Número de usuarios corregidos.</span><span class="sxs-lookup"><span data-stu-id="90643-168">Number of remediated users.</span></span>|
|<span data-ttu-id="90643-169">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="90643-169">errorUserCount</span></span>|<span data-ttu-id="90643-170">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-170">Int32</span></span>|<span data-ttu-id="90643-171">Número de usuarios con errores.</span><span class="sxs-lookup"><span data-stu-id="90643-171">Number of users had error.</span></span>|
|<span data-ttu-id="90643-172">unknownUserCount</span><span class="sxs-lookup"><span data-stu-id="90643-172">unknownUserCount</span></span>|<span data-ttu-id="90643-173">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-173">Int32</span></span>|<span data-ttu-id="90643-174">Número de usuarios desconocidos.</span><span class="sxs-lookup"><span data-stu-id="90643-174">Number of unknown users.</span></span>|
|<span data-ttu-id="90643-175">conflictUserCount</span><span class="sxs-lookup"><span data-stu-id="90643-175">conflictUserCount</span></span>|<span data-ttu-id="90643-176">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-176">Int32</span></span>|<span data-ttu-id="90643-177">Número de usuarios en conflicto.</span><span class="sxs-lookup"><span data-stu-id="90643-177">Number of conflict users.</span></span>|
|<span data-ttu-id="90643-178">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="90643-178">notApplicableUserCount</span></span>|<span data-ttu-id="90643-179">Int32</span><span class="sxs-lookup"><span data-stu-id="90643-179">Int32</span></span>|<span data-ttu-id="90643-180">Número de usuarios no aplicables.</span><span class="sxs-lookup"><span data-stu-id="90643-180">Number of not applicable users.</span></span>|



## <a name="response"></a><span data-ttu-id="90643-181">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90643-181">Response</span></span>
<span data-ttu-id="90643-182">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90643-182">If successful, this method returns a `200 OK` response code and an updated [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90643-183">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90643-183">Example</span></span>
### <a name="request"></a><span data-ttu-id="90643-184">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90643-184">Request</span></span>
<span data-ttu-id="90643-185">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90643-185">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="90643-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90643-186">Response</span></span>
<span data-ttu-id="90643-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90643-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





