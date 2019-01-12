---
title: Crear circularGeofenceManagementCondition
description: Crear un nuevo objeto circularGeofenceManagementCondition.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6ca3d469280b3419700e6948d66e8e3ed1640b22
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979596"
---
# <a name="create-circulargeofencemanagementcondition"></a><span data-ttu-id="6eb05-103">Crear circularGeofenceManagementCondition</span><span class="sxs-lookup"><span data-stu-id="6eb05-103">Create circularGeofenceManagementCondition</span></span>

> <span data-ttu-id="6eb05-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6eb05-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6eb05-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6eb05-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6eb05-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6eb05-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6eb05-107">Crear un nuevo objeto [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="6eb05-107">Create a new [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6eb05-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6eb05-108">Prerequisites</span></span>
<span data-ttu-id="6eb05-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6eb05-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6eb05-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6eb05-111">Permission type</span></span>|<span data-ttu-id="6eb05-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6eb05-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6eb05-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6eb05-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6eb05-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6eb05-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6eb05-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6eb05-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6eb05-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6eb05-116">Not supported.</span></span>|
|<span data-ttu-id="6eb05-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6eb05-117">Application</span></span>|<span data-ttu-id="6eb05-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6eb05-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6eb05-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6eb05-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/managementConditions
POST /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements/{managementConditionStatementId}/managementConditions
```

## <a name="request-headers"></a><span data-ttu-id="6eb05-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6eb05-120">Request headers</span></span>
|<span data-ttu-id="6eb05-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6eb05-121">Header</span></span>|<span data-ttu-id="6eb05-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6eb05-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6eb05-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6eb05-123">Authorization</span></span>|<span data-ttu-id="6eb05-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6eb05-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6eb05-125">Accept</span><span class="sxs-lookup"><span data-stu-id="6eb05-125">Accept</span></span>|<span data-ttu-id="6eb05-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6eb05-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6eb05-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6eb05-127">Request body</span></span>
<span data-ttu-id="6eb05-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto circularGeofenceManagementCondition.</span><span class="sxs-lookup"><span data-stu-id="6eb05-128">In the request body, supply a JSON representation for the circularGeofenceManagementCondition object.</span></span>

<span data-ttu-id="6eb05-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el circularGeofenceManagementCondition.</span><span class="sxs-lookup"><span data-stu-id="6eb05-129">The following table shows the properties that are required when you create the circularGeofenceManagementCondition.</span></span>

|<span data-ttu-id="6eb05-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6eb05-130">Property</span></span>|<span data-ttu-id="6eb05-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6eb05-131">Type</span></span>|<span data-ttu-id="6eb05-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6eb05-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6eb05-133">id</span><span class="sxs-lookup"><span data-stu-id="6eb05-133">id</span></span>|<span data-ttu-id="6eb05-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="6eb05-134">String</span></span>|<span data-ttu-id="6eb05-135">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-135">Unique identifier for the management condition.</span></span> <span data-ttu-id="6eb05-136">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="6eb05-136">System generated value assigned when created.</span></span> <span data-ttu-id="6eb05-137">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-137">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6eb05-138">uniqueName</span><span class="sxs-lookup"><span data-stu-id="6eb05-138">uniqueName</span></span>|<span data-ttu-id="6eb05-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="6eb05-139">String</span></span>|<span data-ttu-id="6eb05-140">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-140">Unique name for the management condition.</span></span> <span data-ttu-id="6eb05-141">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-141">Used in management condition expressions.</span></span> <span data-ttu-id="6eb05-142">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-142">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6eb05-143">displayName</span><span class="sxs-lookup"><span data-stu-id="6eb05-143">displayName</span></span>|<span data-ttu-id="6eb05-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="6eb05-144">String</span></span>|<span data-ttu-id="6eb05-145">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-145">The admin defined name of the management condition.</span></span> <span data-ttu-id="6eb05-146">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-146">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6eb05-147">descripción</span><span class="sxs-lookup"><span data-stu-id="6eb05-147">description</span></span>|<span data-ttu-id="6eb05-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="6eb05-148">String</span></span>|<span data-ttu-id="6eb05-149">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-149">The admin defined description of the management condition.</span></span> <span data-ttu-id="6eb05-150">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-150">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6eb05-151">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="6eb05-151">createdDateTime</span></span>|<span data-ttu-id="6eb05-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6eb05-152">DateTimeOffset</span></span>|<span data-ttu-id="6eb05-153">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-153">The time the management condition was created.</span></span> <span data-ttu-id="6eb05-154">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="6eb05-154">Generated service side.</span></span> <span data-ttu-id="6eb05-155">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-155">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6eb05-156">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="6eb05-156">modifiedDateTime</span></span>|<span data-ttu-id="6eb05-157">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6eb05-157">DateTimeOffset</span></span>|<span data-ttu-id="6eb05-158">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-158">The time the management condition was last modified.</span></span> <span data-ttu-id="6eb05-159">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="6eb05-159">Updated service side.</span></span> <span data-ttu-id="6eb05-160">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-160">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6eb05-161">eTag</span><span class="sxs-lookup"><span data-stu-id="6eb05-161">eTag</span></span>|<span data-ttu-id="6eb05-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="6eb05-162">String</span></span>|<span data-ttu-id="6eb05-163">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-163">ETag of the management condition.</span></span> <span data-ttu-id="6eb05-164">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="6eb05-164">Updated service side.</span></span> <span data-ttu-id="6eb05-165">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-165">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="6eb05-166">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="6eb05-166">applicablePlatforms</span></span>|<span data-ttu-id="6eb05-167">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="6eb05-167">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="6eb05-168">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="6eb05-168">The applicable platforms for this management condition.</span></span> <span data-ttu-id="6eb05-169">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md).</span><span class="sxs-lookup"><span data-stu-id="6eb05-169">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md).</span></span> <span data-ttu-id="6eb05-170">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.</span><span class="sxs-lookup"><span data-stu-id="6eb05-170">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`.</span></span>|
|<span data-ttu-id="6eb05-171">latitude</span><span class="sxs-lookup"><span data-stu-id="6eb05-171">latitude</span></span>|<span data-ttu-id="6eb05-172">Doble</span><span class="sxs-lookup"><span data-stu-id="6eb05-172">Double</span></span>|<span data-ttu-id="6eb05-173">Latitud en grados, entre -90 y + 90 inclusive.</span><span class="sxs-lookup"><span data-stu-id="6eb05-173">Latitude in degrees, between -90 and +90 inclusive.</span></span>|
|<span data-ttu-id="6eb05-174">longitude</span><span class="sxs-lookup"><span data-stu-id="6eb05-174">longitude</span></span>|<span data-ttu-id="6eb05-175">Doble</span><span class="sxs-lookup"><span data-stu-id="6eb05-175">Double</span></span>|<span data-ttu-id="6eb05-176">Longitud en grados, entre -180 y + 180 inclusive.</span><span class="sxs-lookup"><span data-stu-id="6eb05-176">Longitude in degrees, between -180 and +180 inclusive.</span></span>|
|<span data-ttu-id="6eb05-177">radiusInMeters</span><span class="sxs-lookup"><span data-stu-id="6eb05-177">radiusInMeters</span></span>|<span data-ttu-id="6eb05-178">Single</span><span class="sxs-lookup"><span data-stu-id="6eb05-178">Single</span></span>|<span data-ttu-id="6eb05-179">Radio en metros.</span><span class="sxs-lookup"><span data-stu-id="6eb05-179">Radius in meters.</span></span>|



## <a name="response"></a><span data-ttu-id="6eb05-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6eb05-180">Response</span></span>
<span data-ttu-id="6eb05-181">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6eb05-181">If successful, this method returns a `201 Created` response code and a [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6eb05-182">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6eb05-182">Example</span></span>
### <a name="request"></a><span data-ttu-id="6eb05-183">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6eb05-183">Request</span></span>
<span data-ttu-id="6eb05-184">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6eb05-184">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/managementConditions
Content-type: application/json
Content-length: 444

{
  "@odata.type": "#microsoft.graph.circularGeofenceManagementCondition",
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

### <a name="response"></a><span data-ttu-id="6eb05-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6eb05-185">Response</span></span>
<span data-ttu-id="6eb05-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6eb05-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





