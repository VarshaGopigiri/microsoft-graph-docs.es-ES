---
title: Actualizar windowsManagementAppHealthSummary
description: Actualizar las propiedades de un objeto windowsManagementAppHealthSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 068e99b09d2204c3e33955a2407e9bbac3ff31b4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887195"
---
# <a name="update-windowsmanagementapphealthsummary"></a><span data-ttu-id="d2450-103">Actualizar windowsManagementAppHealthSummary</span><span class="sxs-lookup"><span data-stu-id="d2450-103">Update windowsManagementAppHealthSummary</span></span>

> <span data-ttu-id="d2450-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2450-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2450-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2450-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d2450-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2450-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2450-107">Actualizar las propiedades de un objeto [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="d2450-107">Update the properties of a [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2450-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2450-108">Prerequisites</span></span>
<span data-ttu-id="d2450-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2450-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2450-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2450-111">Permission type</span></span>|<span data-ttu-id="d2450-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2450-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2450-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2450-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d2450-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2450-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="d2450-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2450-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2450-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2450-116">Not supported.</span></span>|
|<span data-ttu-id="d2450-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2450-117">Application</span></span>|<span data-ttu-id="d2450-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2450-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2450-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2450-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsManagementApp/healthSummary
```

## <a name="request-headers"></a><span data-ttu-id="d2450-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2450-120">Request headers</span></span>
|<span data-ttu-id="d2450-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2450-121">Header</span></span>|<span data-ttu-id="d2450-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2450-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2450-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2450-123">Authorization</span></span>|<span data-ttu-id="d2450-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2450-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2450-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d2450-125">Accept</span></span>|<span data-ttu-id="d2450-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d2450-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2450-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2450-127">Request body</span></span>
<span data-ttu-id="d2450-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="d2450-128">In the request body, supply a JSON representation for the [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) object.</span></span>

<span data-ttu-id="d2450-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md).</span><span class="sxs-lookup"><span data-stu-id="d2450-129">The following table shows the properties that are required when you create the [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md).</span></span>

|<span data-ttu-id="d2450-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2450-130">Property</span></span>|<span data-ttu-id="d2450-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2450-131">Type</span></span>|<span data-ttu-id="d2450-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2450-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2450-133">id</span><span class="sxs-lookup"><span data-stu-id="d2450-133">id</span></span>|<span data-ttu-id="d2450-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d2450-134">String</span></span>|<span data-ttu-id="d2450-135">Clave de la entidad resumen del estado de aplicación de Windows management.</span><span class="sxs-lookup"><span data-stu-id="d2450-135">Key of the Windows management app health summary entity.</span></span>|
|<span data-ttu-id="d2450-136">healthyDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d2450-136">healthyDeviceCount</span></span>|<span data-ttu-id="d2450-137">Int32</span><span class="sxs-lookup"><span data-stu-id="d2450-137">Int32</span></span>|<span data-ttu-id="d2450-138">Recuento de dispositivo correcto.</span><span class="sxs-lookup"><span data-stu-id="d2450-138">Healthy device count.</span></span>|
|<span data-ttu-id="d2450-139">unhealthyDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d2450-139">unhealthyDeviceCount</span></span>|<span data-ttu-id="d2450-140">Int32</span><span class="sxs-lookup"><span data-stu-id="d2450-140">Int32</span></span>|<span data-ttu-id="d2450-141">Recuento de dispositivo mal estado.</span><span class="sxs-lookup"><span data-stu-id="d2450-141">Unhealthy device count.</span></span>|
|<span data-ttu-id="d2450-142">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d2450-142">unknownDeviceCount</span></span>|<span data-ttu-id="d2450-143">Int32</span><span class="sxs-lookup"><span data-stu-id="d2450-143">Int32</span></span>|<span data-ttu-id="d2450-144">Recuento de dispositivo desconocido.</span><span class="sxs-lookup"><span data-stu-id="d2450-144">Unknown device count.</span></span>|



## <a name="response"></a><span data-ttu-id="d2450-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2450-145">Response</span></span>
<span data-ttu-id="d2450-146">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2450-146">If successful, this method returns a `200 OK` response code and an updated [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2450-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2450-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="d2450-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2450-148">Request</span></span>
<span data-ttu-id="d2450-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2450-149">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/windowsManagementApp/healthSummary
Content-type: application/json
Content-length: 89

{
  "healthyDeviceCount": 2,
  "unhealthyDeviceCount": 4,
  "unknownDeviceCount": 2
}
```

### <a name="response"></a><span data-ttu-id="d2450-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2450-150">Response</span></span>
<span data-ttu-id="d2450-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2450-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 210

{
  "@odata.type": "#microsoft.graph.windowsManagementAppHealthSummary",
  "id": "a9d38a9e-8a9e-a9d3-9e8a-d3a99e8ad3a9",
  "healthyDeviceCount": 2,
  "unhealthyDeviceCount": 4,
  "unknownDeviceCount": 2
}
```





