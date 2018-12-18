---
title: Actualizar deviceConfigurationDeviceStateSummary
description: Actualice las propiedades de un objeto deviceConfigurationDeviceStateSummary.
author: tfitzmac
ms.openlocfilehash: 9dd5e96762a750b015d6eb8dea7d1778ac36f66b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354260"
---
# <a name="update-deviceconfigurationdevicestatesummary"></a><span data-ttu-id="b275e-103">Actualizar deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="b275e-103">Update deviceConfigurationDeviceStateSummary</span></span>

> <span data-ttu-id="b275e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b275e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b275e-105">Actualice las propiedades de un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="b275e-105">Update the properties of a [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b275e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b275e-106">Prerequisites</span></span>
<span data-ttu-id="b275e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b275e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b275e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b275e-109">Permission type</span></span>|<span data-ttu-id="b275e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b275e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b275e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b275e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b275e-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b275e-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b275e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b275e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b275e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b275e-114">Not supported.</span></span>|
|<span data-ttu-id="b275e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b275e-115">Application</span></span>|<span data-ttu-id="b275e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b275e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b275e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b275e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationDeviceStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="b275e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b275e-118">Request headers</span></span>
|<span data-ttu-id="b275e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b275e-119">Header</span></span>|<span data-ttu-id="b275e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b275e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b275e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b275e-121">Authorization</span></span>|<span data-ttu-id="b275e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b275e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b275e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b275e-123">Accept</span></span>|<span data-ttu-id="b275e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b275e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b275e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b275e-125">Request body</span></span>
<span data-ttu-id="b275e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="b275e-126">In the request body, supply a JSON representation for the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>

<span data-ttu-id="b275e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="b275e-127">The following table shows the properties that are required when you create the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span></span>

|<span data-ttu-id="b275e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b275e-128">Property</span></span>|<span data-ttu-id="b275e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b275e-129">Type</span></span>|<span data-ttu-id="b275e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b275e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b275e-131">id</span><span class="sxs-lookup"><span data-stu-id="b275e-131">id</span></span>|<span data-ttu-id="b275e-132">String</span><span class="sxs-lookup"><span data-stu-id="b275e-132">String</span></span>|<span data-ttu-id="b275e-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b275e-133">Key of the entity.</span></span>|
|<span data-ttu-id="b275e-134">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b275e-134">unknownDeviceCount</span></span>|<span data-ttu-id="b275e-135">Int32</span><span class="sxs-lookup"><span data-stu-id="b275e-135">Int32</span></span>|<span data-ttu-id="b275e-136">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="b275e-136">Number of unknown devices</span></span>|
|<span data-ttu-id="b275e-137">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b275e-137">notApplicableDeviceCount</span></span>|<span data-ttu-id="b275e-138">Int32</span><span class="sxs-lookup"><span data-stu-id="b275e-138">Int32</span></span>|<span data-ttu-id="b275e-139">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="b275e-139">Number of not applicable devices</span></span>|
|<span data-ttu-id="b275e-140">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b275e-140">compliantDeviceCount</span></span>|<span data-ttu-id="b275e-141">Int32</span><span class="sxs-lookup"><span data-stu-id="b275e-141">Int32</span></span>|<span data-ttu-id="b275e-142">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="b275e-142">Number of compliant devices</span></span>|
|<span data-ttu-id="b275e-143">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b275e-143">remediatedDeviceCount</span></span>|<span data-ttu-id="b275e-144">Int32</span><span class="sxs-lookup"><span data-stu-id="b275e-144">Int32</span></span>|<span data-ttu-id="b275e-145">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="b275e-145">Number of remediated devices</span></span>|
|<span data-ttu-id="b275e-146">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b275e-146">nonCompliantDeviceCount</span></span>|<span data-ttu-id="b275e-147">Int32</span><span class="sxs-lookup"><span data-stu-id="b275e-147">Int32</span></span>|<span data-ttu-id="b275e-148">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="b275e-148">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="b275e-149">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b275e-149">errorDeviceCount</span></span>|<span data-ttu-id="b275e-150">Int32</span><span class="sxs-lookup"><span data-stu-id="b275e-150">Int32</span></span>|<span data-ttu-id="b275e-151">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="b275e-151">Number of error devices</span></span>|
|<span data-ttu-id="b275e-152">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b275e-152">conflictDeviceCount</span></span>|<span data-ttu-id="b275e-153">Int32</span><span class="sxs-lookup"><span data-stu-id="b275e-153">Int32</span></span>|<span data-ttu-id="b275e-154">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="b275e-154">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="b275e-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b275e-155">Response</span></span>
<span data-ttu-id="b275e-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b275e-156">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b275e-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b275e-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="b275e-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b275e-158">Request</span></span>
<span data-ttu-id="b275e-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b275e-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurationDeviceStateSummaries
Content-type: application/json
Content-length: 290

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="b275e-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b275e-160">Response</span></span>
<span data-ttu-id="b275e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b275e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 339

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
  "id": "5db26f5a-6f5a-5db2-5a6f-b25d5a6fb25d",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```



