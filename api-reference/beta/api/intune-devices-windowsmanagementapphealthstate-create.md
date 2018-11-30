---
title: Crear windowsManagementAppHealthState
description: Crear un nuevo objeto windowsManagementAppHealthState.
ms.openlocfilehash: e815a86001e75e2350e0ea1b5bb73a8dfd87f58a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085629"
---
# <a name="create-windowsmanagementapphealthstate"></a><span data-ttu-id="0f39b-103">Crear windowsManagementAppHealthState</span><span class="sxs-lookup"><span data-stu-id="0f39b-103">Create windowsManagementAppHealthState</span></span>

> <span data-ttu-id="0f39b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0f39b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0f39b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0f39b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0f39b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0f39b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0f39b-107">Crear un nuevo objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .</span><span class="sxs-lookup"><span data-stu-id="0f39b-107">Create a new [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0f39b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0f39b-108">Prerequisites</span></span>
<span data-ttu-id="0f39b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0f39b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0f39b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0f39b-111">Permission type</span></span>|<span data-ttu-id="0f39b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0f39b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0f39b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0f39b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0f39b-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0f39b-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="0f39b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0f39b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0f39b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f39b-116">Not supported.</span></span>|
|<span data-ttu-id="0f39b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0f39b-117">Application</span></span>|<span data-ttu-id="0f39b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f39b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0f39b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0f39b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/windowsManagementApp/healthStates
```

## <a name="request-headers"></a><span data-ttu-id="0f39b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0f39b-120">Request headers</span></span>
|<span data-ttu-id="0f39b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f39b-121">Header</span></span>|<span data-ttu-id="0f39b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0f39b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0f39b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="0f39b-123">Authorization</span></span>|<span data-ttu-id="0f39b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0f39b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0f39b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0f39b-125">Accept</span></span>|<span data-ttu-id="0f39b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0f39b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0f39b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0f39b-127">Request body</span></span>
<span data-ttu-id="0f39b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsManagementAppHealthState.</span><span class="sxs-lookup"><span data-stu-id="0f39b-128">In the request body, supply a JSON representation for the windowsManagementAppHealthState object.</span></span>

<span data-ttu-id="0f39b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsManagementAppHealthState.</span><span class="sxs-lookup"><span data-stu-id="0f39b-129">The following table shows the properties that are required when you create the windowsManagementAppHealthState.</span></span>

|<span data-ttu-id="0f39b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0f39b-130">Property</span></span>|<span data-ttu-id="0f39b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f39b-131">Type</span></span>|<span data-ttu-id="0f39b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f39b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0f39b-133">id</span><span class="sxs-lookup"><span data-stu-id="0f39b-133">id</span></span>|<span data-ttu-id="0f39b-134">String</span><span class="sxs-lookup"><span data-stu-id="0f39b-134">String</span></span>|<span data-ttu-id="0f39b-135">Identificador único para el estado de mantenimiento de aplicación de administración de Windows</span><span class="sxs-lookup"><span data-stu-id="0f39b-135">Unique Identifier for the Windows management app health state</span></span>|
|<span data-ttu-id="0f39b-136">healthState</span><span class="sxs-lookup"><span data-stu-id="0f39b-136">healthState</span></span>|[<span data-ttu-id="0f39b-137">healthState</span><span class="sxs-lookup"><span data-stu-id="0f39b-137">healthState</span></span>](../resources/intune-devices-healthstate.md)|<span data-ttu-id="0f39b-138">Estado de mantenimiento de aplicación de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="0f39b-138">Windows management app health state.</span></span> <span data-ttu-id="0f39b-139">Los valores posibles son: `unknown`, `healthy` y `unhealthy`.</span><span class="sxs-lookup"><span data-stu-id="0f39b-139">Possible values are: `unknown`, `healthy`, `unhealthy`.</span></span>|
|<span data-ttu-id="0f39b-140">installedVersion</span><span class="sxs-lookup"><span data-stu-id="0f39b-140">installedVersion</span></span>|<span data-ttu-id="0f39b-141">String</span><span class="sxs-lookup"><span data-stu-id="0f39b-141">String</span></span>|<span data-ttu-id="0f39b-142">La versión instalada de aplicación de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="0f39b-142">Windows management app installed version.</span></span>|
|<span data-ttu-id="0f39b-143">lastCheckInDateTime</span><span class="sxs-lookup"><span data-stu-id="0f39b-143">lastCheckInDateTime</span></span>|<span data-ttu-id="0f39b-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0f39b-144">DateTimeOffset</span></span>|<span data-ttu-id="0f39b-145">Aplicación de administración de Windows última hora de protección.</span><span class="sxs-lookup"><span data-stu-id="0f39b-145">Windows management app last check-in time.</span></span>|
|<span data-ttu-id="0f39b-146">deviceName</span><span class="sxs-lookup"><span data-stu-id="0f39b-146">deviceName</span></span>|<span data-ttu-id="0f39b-147">String</span><span class="sxs-lookup"><span data-stu-id="0f39b-147">String</span></span>|<span data-ttu-id="0f39b-148">Nombre del dispositivo con Windows está instalada la aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="0f39b-148">Name of the device on which Windows management app is installed.</span></span>|
|<span data-ttu-id="0f39b-149">deviceOSVersion</span><span class="sxs-lookup"><span data-stu-id="0f39b-149">deviceOSVersion</span></span>|<span data-ttu-id="0f39b-150">String</span><span class="sxs-lookup"><span data-stu-id="0f39b-150">String</span></span>|<span data-ttu-id="0f39b-151">Versión de sistema operativo de Windows 10 del dispositivo con Windows está instalada la aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="0f39b-151">Windows 10 OS version of the device on which Windows management app is installed.</span></span>|



## <a name="response"></a><span data-ttu-id="0f39b-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f39b-152">Response</span></span>
<span data-ttu-id="0f39b-153">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0f39b-153">If successful, this method returns a `201 Created` response code and a [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0f39b-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f39b-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="0f39b-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0f39b-155">Request</span></span>
<span data-ttu-id="0f39b-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f39b-156">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/windowsManagementApp/healthStates
Content-type: application/json
Content-length: 300

{
  "@odata.type": "#microsoft.graph.windowsManagementAppHealthState",
  "healthState": "healthy",
  "installedVersion": "Installed Version value",
  "lastCheckInDateTime": "2016-12-31T23:59:56.413532-08:00",
  "deviceName": "Device Name value",
  "deviceOSVersion": "Device OSVersion value"
}
```

### <a name="response"></a><span data-ttu-id="0f39b-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f39b-157">Response</span></span>
<span data-ttu-id="0f39b-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0f39b-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





