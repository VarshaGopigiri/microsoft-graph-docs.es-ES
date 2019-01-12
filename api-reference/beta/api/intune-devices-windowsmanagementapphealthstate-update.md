---
title: Actualizar windowsManagementAppHealthState
description: Actualizar las propiedades de un objeto windowsManagementAppHealthState.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b52762bf13a7ff534c3c76b8b0c94561744b15fe
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924233"
---
# <a name="update-windowsmanagementapphealthstate"></a><span data-ttu-id="15064-103">Actualizar windowsManagementAppHealthState</span><span class="sxs-lookup"><span data-stu-id="15064-103">Update windowsManagementAppHealthState</span></span>

> <span data-ttu-id="15064-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="15064-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="15064-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="15064-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="15064-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="15064-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="15064-107">Actualizar las propiedades de un objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .</span><span class="sxs-lookup"><span data-stu-id="15064-107">Update the properties of a [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="15064-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="15064-108">Prerequisites</span></span>
<span data-ttu-id="15064-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="15064-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="15064-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15064-111">Permission type</span></span>|<span data-ttu-id="15064-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15064-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="15064-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15064-113">Delegated (work or school account)</span></span>|<span data-ttu-id="15064-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="15064-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="15064-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15064-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="15064-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15064-116">Not supported.</span></span>|
|<span data-ttu-id="15064-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15064-117">Application</span></span>|<span data-ttu-id="15064-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15064-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="15064-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15064-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/windowsManagementApp/healthStates/{windowsManagementAppHealthStateId}
```

## <a name="request-headers"></a><span data-ttu-id="15064-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15064-120">Request headers</span></span>
|<span data-ttu-id="15064-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15064-121">Header</span></span>|<span data-ttu-id="15064-122">Valor</span><span class="sxs-lookup"><span data-stu-id="15064-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="15064-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="15064-123">Authorization</span></span>|<span data-ttu-id="15064-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="15064-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="15064-125">Accept</span><span class="sxs-lookup"><span data-stu-id="15064-125">Accept</span></span>|<span data-ttu-id="15064-126">application/json</span><span class="sxs-lookup"><span data-stu-id="15064-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="15064-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15064-127">Request body</span></span>
<span data-ttu-id="15064-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .</span><span class="sxs-lookup"><span data-stu-id="15064-128">In the request body, supply a JSON representation for the [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) object.</span></span>

<span data-ttu-id="15064-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md).</span><span class="sxs-lookup"><span data-stu-id="15064-129">The following table shows the properties that are required when you create the [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md).</span></span>

|<span data-ttu-id="15064-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15064-130">Property</span></span>|<span data-ttu-id="15064-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="15064-131">Type</span></span>|<span data-ttu-id="15064-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="15064-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="15064-133">id</span><span class="sxs-lookup"><span data-stu-id="15064-133">id</span></span>|<span data-ttu-id="15064-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="15064-134">String</span></span>|<span data-ttu-id="15064-135">Identificador único para el estado de mantenimiento de aplicación de administración de Windows</span><span class="sxs-lookup"><span data-stu-id="15064-135">Unique Identifier for the Windows management app health state</span></span>|
|<span data-ttu-id="15064-136">healthState</span><span class="sxs-lookup"><span data-stu-id="15064-136">healthState</span></span>|[<span data-ttu-id="15064-137">healthState</span><span class="sxs-lookup"><span data-stu-id="15064-137">healthState</span></span>](../resources/intune-devices-healthstate.md)|<span data-ttu-id="15064-138">Estado de mantenimiento de aplicación de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="15064-138">Windows management app health state.</span></span> <span data-ttu-id="15064-139">Los valores posibles son: `unknown`, `healthy` y `unhealthy`.</span><span class="sxs-lookup"><span data-stu-id="15064-139">Possible values are: `unknown`, `healthy`, `unhealthy`.</span></span>|
|<span data-ttu-id="15064-140">installedVersion</span><span class="sxs-lookup"><span data-stu-id="15064-140">installedVersion</span></span>|<span data-ttu-id="15064-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="15064-141">String</span></span>|<span data-ttu-id="15064-142">La versión instalada de aplicación de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="15064-142">Windows management app installed version.</span></span>|
|<span data-ttu-id="15064-143">lastCheckInDateTime</span><span class="sxs-lookup"><span data-stu-id="15064-143">lastCheckInDateTime</span></span>|<span data-ttu-id="15064-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="15064-144">DateTimeOffset</span></span>|<span data-ttu-id="15064-145">Aplicación de administración de Windows última hora de protección.</span><span class="sxs-lookup"><span data-stu-id="15064-145">Windows management app last check-in time.</span></span>|
|<span data-ttu-id="15064-146">deviceName</span><span class="sxs-lookup"><span data-stu-id="15064-146">deviceName</span></span>|<span data-ttu-id="15064-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="15064-147">String</span></span>|<span data-ttu-id="15064-148">Nombre del dispositivo con Windows está instalada la aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="15064-148">Name of the device on which Windows management app is installed.</span></span>|
|<span data-ttu-id="15064-149">deviceOSVersion</span><span class="sxs-lookup"><span data-stu-id="15064-149">deviceOSVersion</span></span>|<span data-ttu-id="15064-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="15064-150">String</span></span>|<span data-ttu-id="15064-151">Versión de sistema operativo de Windows 10 del dispositivo con Windows está instalada la aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="15064-151">Windows 10 OS version of the device on which Windows management app is installed.</span></span>|



## <a name="response"></a><span data-ttu-id="15064-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15064-152">Response</span></span>
<span data-ttu-id="15064-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15064-153">If successful, this method returns a `200 OK` response code and an updated [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="15064-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15064-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="15064-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15064-155">Request</span></span>
<span data-ttu-id="15064-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15064-156">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/windowsManagementApp/healthStates/{windowsManagementAppHealthStateId}
Content-type: application/json
Content-length: 230

{
  "healthState": "healthy",
  "installedVersion": "Installed Version value",
  "lastCheckInDateTime": "2016-12-31T23:59:56.413532-08:00",
  "deviceName": "Device Name value",
  "deviceOSVersion": "Device OSVersion value"
}
```

### <a name="response"></a><span data-ttu-id="15064-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15064-157">Response</span></span>
<span data-ttu-id="15064-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="15064-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 349

{
  "@odata.type": "#microsoft.graph.windowsManagementAppHealthState",
  "id": "5c7e50fb-50fb-5c7e-fb50-7e5cfb507e5c",
  "healthState": "healthy",
  "installedVersion": "Installed Version value",
  "lastCheckInDateTime": "2016-12-31T23:59:56.413532-08:00",
  "deviceName": "Device Name value",
  "deviceOSVersion": "Device OSVersion value"
}
```





