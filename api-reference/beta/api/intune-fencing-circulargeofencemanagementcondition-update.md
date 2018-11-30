---
title: Actualizar circularGeofenceManagementCondition
description: Actualizar las propiedades de un objeto circularGeofenceManagementCondition.
ms.openlocfilehash: d1bf21db47f25834f62241fb66a96bcf176f5d8b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086101"
---
# <a name="update-circulargeofencemanagementcondition"></a><span data-ttu-id="6048b-103">Actualizar circularGeofenceManagementCondition</span><span class="sxs-lookup"><span data-stu-id="6048b-103">Update circularGeofenceManagementCondition</span></span>

> <span data-ttu-id="6048b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6048b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6048b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6048b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6048b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6048b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6048b-107">Actualizar las propiedades de un objeto [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="6048b-107">Update the properties of a [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6048b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6048b-108">Prerequisites</span></span>
<span data-ttu-id="6048b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6048b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6048b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6048b-111">Permission type</span></span>|<span data-ttu-id="6048b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6048b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6048b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6048b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6048b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6048b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6048b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6048b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6048b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6048b-116">Not supported.</span></span>|
|<span data-ttu-id="6048b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6048b-117">Application</span></span>|<span data-ttu-id="6048b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6048b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6048b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6048b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managementConditions/{managementConditionId}
PATCH /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions/{managementConditionId}
```

## <a name="request-headers"></a><span data-ttu-id="6048b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6048b-120">Request headers</span></span>
|<span data-ttu-id="6048b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6048b-121">Header</span></span>|<span data-ttu-id="6048b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6048b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6048b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6048b-123">Authorization</span></span>|<span data-ttu-id="6048b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6048b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6048b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6048b-125">Accept</span></span>|<span data-ttu-id="6048b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6048b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6048b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6048b-127">Request body</span></span>
<span data-ttu-id="6048b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="6048b-128">In the request body, supply a JSON representation for the [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) object.</span></span>

<span data-ttu-id="6048b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md).</span><span class="sxs-lookup"><span data-stu-id="6048b-129">The following table shows the properties that are required when you create the [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md).</span></span>

|<span data-ttu-id="6048b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6048b-130">Property</span></span>|<span data-ttu-id="6048b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6048b-131">Type</span></span>|<span data-ttu-id="6048b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6048b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6048b-133">id</span><span class="sxs-lookup"><span data-stu-id="6048b-133">id</span></span>|<span data-ttu-id="6048b-134">String</span><span class="sxs-lookup"><span data-stu-id="6048b-134">String</span></span>|<span data-ttu-id="6048b-135">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-135">Unique identifier for the management condition.</span></span> <span data-ttu-id="6048b-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="6048b-136">System generated value assigned when created.</span></span> <span data-ttu-id="6048b-137">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-137">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6048b-138">uniqueName</span><span class="sxs-lookup"><span data-stu-id="6048b-138">uniqueName</span></span>|<span data-ttu-id="6048b-139">String</span><span class="sxs-lookup"><span data-stu-id="6048b-139">String</span></span>|<span data-ttu-id="6048b-140">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-140">Unique name for the management condition.</span></span> <span data-ttu-id="6048b-141">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-141">Used in management condition expressions.</span></span> <span data-ttu-id="6048b-142">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-142">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6048b-143">displayName</span><span class="sxs-lookup"><span data-stu-id="6048b-143">displayName</span></span>|<span data-ttu-id="6048b-144">String</span><span class="sxs-lookup"><span data-stu-id="6048b-144">String</span></span>|<span data-ttu-id="6048b-145">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-145">The admin defined name of the management condition.</span></span> <span data-ttu-id="6048b-146">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-146">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6048b-147">descripción</span><span class="sxs-lookup"><span data-stu-id="6048b-147">description</span></span>|<span data-ttu-id="6048b-148">String</span><span class="sxs-lookup"><span data-stu-id="6048b-148">String</span></span>|<span data-ttu-id="6048b-149">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-149">The admin defined description of the management condition.</span></span> <span data-ttu-id="6048b-150">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-150">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6048b-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6048b-151">createdDateTime</span></span>|<span data-ttu-id="6048b-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6048b-152">DateTimeOffset</span></span>|<span data-ttu-id="6048b-153">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-153">The time the management condition was created.</span></span> <span data-ttu-id="6048b-154">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="6048b-154">Generated service side.</span></span> <span data-ttu-id="6048b-155">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-155">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6048b-156">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6048b-156">modifiedDateTime</span></span>|<span data-ttu-id="6048b-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6048b-157">DateTimeOffset</span></span>|<span data-ttu-id="6048b-158">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-158">The time the management condition was last modified.</span></span> <span data-ttu-id="6048b-159">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="6048b-159">Updated service side.</span></span> <span data-ttu-id="6048b-160">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-160">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6048b-161">eTag</span><span class="sxs-lookup"><span data-stu-id="6048b-161">eTag</span></span>|<span data-ttu-id="6048b-162">String</span><span class="sxs-lookup"><span data-stu-id="6048b-162">String</span></span>|<span data-ttu-id="6048b-163">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-163">ETag of the management condition.</span></span> <span data-ttu-id="6048b-164">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="6048b-164">Updated service side.</span></span> <span data-ttu-id="6048b-165">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-165">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6048b-166">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="6048b-166">applicablePlatforms</span></span>|<span data-ttu-id="6048b-167">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="6048b-167">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="6048b-168">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6048b-168">The applicable platforms for this management condition.</span></span> <span data-ttu-id="6048b-169">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md).</span><span class="sxs-lookup"><span data-stu-id="6048b-169">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md).</span></span> <span data-ttu-id="6048b-170">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="6048b-170">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|
|<span data-ttu-id="6048b-171">latitude</span><span class="sxs-lookup"><span data-stu-id="6048b-171">latitude</span></span>|<span data-ttu-id="6048b-172">Doble</span><span class="sxs-lookup"><span data-stu-id="6048b-172">Double</span></span>|<span data-ttu-id="6048b-173">Latitud en grados, entre -90 y + 90 inclusive.</span><span class="sxs-lookup"><span data-stu-id="6048b-173">Latitude in degrees, between -90 and +90 inclusive.</span></span>|
|<span data-ttu-id="6048b-174">longitude</span><span class="sxs-lookup"><span data-stu-id="6048b-174">longitude</span></span>|<span data-ttu-id="6048b-175">Doble</span><span class="sxs-lookup"><span data-stu-id="6048b-175">Double</span></span>|<span data-ttu-id="6048b-176">Longitud en grados, entre -180 y + 180 inclusive.</span><span class="sxs-lookup"><span data-stu-id="6048b-176">Longitude in degrees, between -180 and +180 inclusive.</span></span>|
|<span data-ttu-id="6048b-177">radiusInMeters</span><span class="sxs-lookup"><span data-stu-id="6048b-177">radiusInMeters</span></span>|<span data-ttu-id="6048b-178">Single</span><span class="sxs-lookup"><span data-stu-id="6048b-178">Single</span></span>|<span data-ttu-id="6048b-179">Radio en metros.</span><span class="sxs-lookup"><span data-stu-id="6048b-179">Radius in meters.</span></span>|



## <a name="response"></a><span data-ttu-id="6048b-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6048b-180">Response</span></span>
<span data-ttu-id="6048b-181">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6048b-181">If successful, this method returns a `200 OK` response code and an updated [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6048b-182">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6048b-182">Example</span></span>
### <a name="request"></a><span data-ttu-id="6048b-183">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6048b-183">Request</span></span>
<span data-ttu-id="6048b-184">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6048b-184">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/managementConditions/{managementConditionId}
Content-type: application/json
Content-length: 370

{
  "uniqueName": "Unique Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ],
  "latitude": "<Unknown Primitive Type Edm.Double>",
  "longitude": "<Unknown Primitive Type Edm.Double>",
  "radiusInMeters": "<Unknown Primitive Type Edm.Single>"
}
```

### <a name="response"></a><span data-ttu-id="6048b-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6048b-185">Response</span></span>
<span data-ttu-id="6048b-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6048b-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 612

{
  "@odata.type": "#microsoft.graph.circularGeofenceManagementCondition",
  "id": "30ee27b6-27b6-30ee-b627-ee30b627ee30",
  "uniqueName": "Unique Name value",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ],
  "latitude": "<Unknown Primitive Type Edm.Double>",
  "longitude": "<Unknown Primitive Type Edm.Double>",
  "radiusInMeters": "<Unknown Primitive Type Edm.Single>"
}
```




