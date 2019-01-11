---
title: Actualizar deviceConfigurationDeviceStateSummary
description: Actualice las propiedades de un objeto deviceConfigurationDeviceStateSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1963e00e5f2cf6719932b1b26b388a72fff0fb28
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832540"
---
# <a name="update-deviceconfigurationdevicestatesummary"></a><span data-ttu-id="bb5b6-103">Actualizar deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="bb5b6-103">Update deviceConfigurationDeviceStateSummary</span></span>

> <span data-ttu-id="bb5b6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb5b6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bb5b6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bb5b6-107">Actualice las propiedades de un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-107">Update the properties of a [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bb5b6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bb5b6-108">Prerequisites</span></span>
<span data-ttu-id="bb5b6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb5b6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb5b6-111">Permission type</span></span>|<span data-ttu-id="bb5b6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb5b6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb5b6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb5b6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bb5b6-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bb5b6-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="bb5b6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb5b6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb5b6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-116">Not supported.</span></span>|
|<span data-ttu-id="bb5b6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb5b6-117">Application</span></span>|<span data-ttu-id="bb5b6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb5b6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb5b6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationDeviceStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="bb5b6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb5b6-120">Request headers</span></span>
|<span data-ttu-id="bb5b6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb5b6-121">Header</span></span>|<span data-ttu-id="bb5b6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bb5b6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb5b6-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="bb5b6-123">Authorization</span></span>|<span data-ttu-id="bb5b6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb5b6-125">Accept</span><span class="sxs-lookup"><span data-stu-id="bb5b6-125">Accept</span></span>|<span data-ttu-id="bb5b6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bb5b6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb5b6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb5b6-127">Request body</span></span>
<span data-ttu-id="bb5b6-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-128">In the request body, supply a JSON representation for the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object.</span></span>

<span data-ttu-id="bb5b6-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="bb5b6-129">The following table shows the properties that are required when you create the [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md).</span></span>

|<span data-ttu-id="bb5b6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb5b6-130">Property</span></span>|<span data-ttu-id="bb5b6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb5b6-131">Type</span></span>|<span data-ttu-id="bb5b6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb5b6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bb5b6-133">id</span><span class="sxs-lookup"><span data-stu-id="bb5b6-133">id</span></span>|<span data-ttu-id="bb5b6-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="bb5b6-134">String</span></span>|<span data-ttu-id="bb5b6-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-135">Key of the entity.</span></span>|
|<span data-ttu-id="bb5b6-136">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bb5b6-136">unknownDeviceCount</span></span>|<span data-ttu-id="bb5b6-137">Int32</span><span class="sxs-lookup"><span data-stu-id="bb5b6-137">Int32</span></span>|<span data-ttu-id="bb5b6-138">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="bb5b6-138">Number of unknown devices</span></span>|
|<span data-ttu-id="bb5b6-139">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bb5b6-139">notApplicableDeviceCount</span></span>|<span data-ttu-id="bb5b6-140">Int32</span><span class="sxs-lookup"><span data-stu-id="bb5b6-140">Int32</span></span>|<span data-ttu-id="bb5b6-141">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="bb5b6-141">Number of not applicable devices</span></span>|
|<span data-ttu-id="bb5b6-142">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bb5b6-142">compliantDeviceCount</span></span>|<span data-ttu-id="bb5b6-143">Int32</span><span class="sxs-lookup"><span data-stu-id="bb5b6-143">Int32</span></span>|<span data-ttu-id="bb5b6-144">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="bb5b6-144">Number of compliant devices</span></span>|
|<span data-ttu-id="bb5b6-145">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bb5b6-145">remediatedDeviceCount</span></span>|<span data-ttu-id="bb5b6-146">Int32</span><span class="sxs-lookup"><span data-stu-id="bb5b6-146">Int32</span></span>|<span data-ttu-id="bb5b6-147">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="bb5b6-147">Number of remediated devices</span></span>|
|<span data-ttu-id="bb5b6-148">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bb5b6-148">nonCompliantDeviceCount</span></span>|<span data-ttu-id="bb5b6-149">Int32</span><span class="sxs-lookup"><span data-stu-id="bb5b6-149">Int32</span></span>|<span data-ttu-id="bb5b6-150">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="bb5b6-150">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="bb5b6-151">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bb5b6-151">errorDeviceCount</span></span>|<span data-ttu-id="bb5b6-152">Int32</span><span class="sxs-lookup"><span data-stu-id="bb5b6-152">Int32</span></span>|<span data-ttu-id="bb5b6-153">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="bb5b6-153">Number of error devices</span></span>|
|<span data-ttu-id="bb5b6-154">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="bb5b6-154">conflictDeviceCount</span></span>|<span data-ttu-id="bb5b6-155">Int32</span><span class="sxs-lookup"><span data-stu-id="bb5b6-155">Int32</span></span>|<span data-ttu-id="bb5b6-156">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="bb5b6-156">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="bb5b6-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb5b6-157">Response</span></span>
<span data-ttu-id="bb5b6-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-158">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationDeviceStateSummary](../resources/intune-deviceconfig-deviceconfigurationdevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb5b6-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb5b6-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="bb5b6-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb5b6-160">Request</span></span>
<span data-ttu-id="bb5b6-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurationDeviceStateSummaries
Content-type: application/json
Content-length: 214

{
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="bb5b6-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb5b6-162">Response</span></span>
<span data-ttu-id="bb5b6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb5b6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





