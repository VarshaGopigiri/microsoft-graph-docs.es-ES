---
title: Actualizar deviceManagementScriptRunSummary
description: Actualizar las propiedades de un objeto deviceManagementScriptRunSummary.
author: tfitzmac
ms.openlocfilehash: 7acb5406d6806f9c28498f2766b8a92970893af0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338377"
---
# <a name="update-devicemanagementscriptrunsummary"></a><span data-ttu-id="1d841-103">Actualizar deviceManagementScriptRunSummary</span><span class="sxs-lookup"><span data-stu-id="1d841-103">Update deviceManagementScriptRunSummary</span></span>

> <span data-ttu-id="1d841-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d841-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d841-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d841-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d841-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d841-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d841-107">Actualizar las propiedades de un objeto [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="1d841-107">Update the properties of a [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d841-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d841-108">Prerequisites</span></span>
<span data-ttu-id="1d841-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d841-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d841-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d841-111">Permission type</span></span>|<span data-ttu-id="1d841-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d841-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d841-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d841-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1d841-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d841-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="1d841-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d841-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d841-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d841-116">Not supported.</span></span>|
|<span data-ttu-id="1d841-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d841-117">Application</span></span>|<span data-ttu-id="1d841-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d841-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d841-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d841-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/runSummary
```

## <a name="request-headers"></a><span data-ttu-id="1d841-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d841-120">Request headers</span></span>
|<span data-ttu-id="1d841-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d841-121">Header</span></span>|<span data-ttu-id="1d841-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1d841-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d841-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d841-123">Authorization</span></span>|<span data-ttu-id="1d841-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d841-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d841-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1d841-125">Accept</span></span>|<span data-ttu-id="1d841-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1d841-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d841-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d841-127">Request body</span></span>
<span data-ttu-id="1d841-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="1d841-128">In the request body, supply a JSON representation for the [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) object.</span></span>

<span data-ttu-id="1d841-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md).</span><span class="sxs-lookup"><span data-stu-id="1d841-129">The following table shows the properties that are required when you create the [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md).</span></span>

|<span data-ttu-id="1d841-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d841-130">Property</span></span>|<span data-ttu-id="1d841-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d841-131">Type</span></span>|<span data-ttu-id="1d841-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d841-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1d841-133">id</span><span class="sxs-lookup"><span data-stu-id="1d841-133">id</span></span>|<span data-ttu-id="1d841-134">String</span><span class="sxs-lookup"><span data-stu-id="1d841-134">String</span></span>|<span data-ttu-id="1d841-135">Clave de la secuencia de comandos de administración de dispositivo ejecute entidad resumen.</span><span class="sxs-lookup"><span data-stu-id="1d841-135">Key of the device management script run summary entity.</span></span>|
|<span data-ttu-id="1d841-136">successDeviceCount</span><span class="sxs-lookup"><span data-stu-id="1d841-136">successDeviceCount</span></span>|<span data-ttu-id="1d841-137">Int32</span><span class="sxs-lookup"><span data-stu-id="1d841-137">Int32</span></span>|<span data-ttu-id="1d841-138">Recuento de éxito de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d841-138">Success device count.</span></span>|
|<span data-ttu-id="1d841-139">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="1d841-139">errorDeviceCount</span></span>|<span data-ttu-id="1d841-140">Int32</span><span class="sxs-lookup"><span data-stu-id="1d841-140">Int32</span></span>|<span data-ttu-id="1d841-141">Recuento de error de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d841-141">Error device count.</span></span>|
|<span data-ttu-id="1d841-142">successUserCount</span><span class="sxs-lookup"><span data-stu-id="1d841-142">successUserCount</span></span>|<span data-ttu-id="1d841-143">Int32</span><span class="sxs-lookup"><span data-stu-id="1d841-143">Int32</span></span>|<span data-ttu-id="1d841-144">Recuento de usuario correcto.</span><span class="sxs-lookup"><span data-stu-id="1d841-144">Success user count.</span></span>|
|<span data-ttu-id="1d841-145">errorUserCount</span><span class="sxs-lookup"><span data-stu-id="1d841-145">errorUserCount</span></span>|<span data-ttu-id="1d841-146">Int32</span><span class="sxs-lookup"><span data-stu-id="1d841-146">Int32</span></span>|<span data-ttu-id="1d841-147">Recuento de usuario de error.</span><span class="sxs-lookup"><span data-stu-id="1d841-147">Error user count.</span></span>|



## <a name="response"></a><span data-ttu-id="1d841-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d841-148">Response</span></span>
<span data-ttu-id="1d841-149">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d841-149">If successful, this method returns a `200 OK` response code and an updated [deviceManagementScriptRunSummary](../resources/intune-devices-devicemanagementscriptrunsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d841-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d841-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d841-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d841-151">Request</span></span>
<span data-ttu-id="1d841-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d841-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/runSummary
Content-type: application/json
Content-length: 108

{
  "successDeviceCount": 2,
  "errorDeviceCount": 0,
  "successUserCount": 0,
  "errorUserCount": 14
}
```

### <a name="response"></a><span data-ttu-id="1d841-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d841-153">Response</span></span>
<span data-ttu-id="1d841-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d841-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 228

{
  "@odata.type": "#microsoft.graph.deviceManagementScriptRunSummary",
  "id": "514d5d38-5d38-514d-385d-4d51385d4d51",
  "successDeviceCount": 2,
  "errorDeviceCount": 0,
  "successUserCount": 0,
  "errorUserCount": 14
}
```





