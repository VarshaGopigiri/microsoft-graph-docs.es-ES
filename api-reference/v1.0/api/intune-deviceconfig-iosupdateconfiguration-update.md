---
title: Actualizar iosUpdateConfiguration
description: Actualice las propiedades de un objeto iosUpdateConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f9ecd2a3ac0cee1d7287308f20c88f495391ede7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849010"
---
# <a name="update-iosupdateconfiguration"></a><span data-ttu-id="391b8-103">Actualizar iosUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="391b8-103">Update iosUpdateConfiguration</span></span>

> <span data-ttu-id="391b8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="391b8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="391b8-105">Actualice las propiedades de un objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="391b8-105">Update the properties of a [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="391b8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="391b8-106">Prerequisites</span></span>
<span data-ttu-id="391b8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="391b8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="391b8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="391b8-109">Permission type</span></span>|<span data-ttu-id="391b8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="391b8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="391b8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="391b8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="391b8-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="391b8-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="391b8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="391b8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="391b8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="391b8-114">Not supported.</span></span>|
|<span data-ttu-id="391b8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="391b8-115">Application</span></span>|<span data-ttu-id="391b8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="391b8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="391b8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="391b8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="391b8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="391b8-118">Request headers</span></span>
|<span data-ttu-id="391b8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="391b8-119">Header</span></span>|<span data-ttu-id="391b8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="391b8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="391b8-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="391b8-121">Authorization</span></span>|<span data-ttu-id="391b8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="391b8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="391b8-123">Accept</span><span class="sxs-lookup"><span data-stu-id="391b8-123">Accept</span></span>|<span data-ttu-id="391b8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="391b8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="391b8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="391b8-125">Request body</span></span>
<span data-ttu-id="391b8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="391b8-126">In the request body, supply a JSON representation for the [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) object.</span></span>

<span data-ttu-id="391b8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="391b8-127">The following table shows the properties that are required when you create the [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).</span></span>

|<span data-ttu-id="391b8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="391b8-128">Property</span></span>|<span data-ttu-id="391b8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="391b8-129">Type</span></span>|<span data-ttu-id="391b8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="391b8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="391b8-131">id</span><span class="sxs-lookup"><span data-stu-id="391b8-131">id</span></span>|<span data-ttu-id="391b8-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="391b8-132">String</span></span>|<span data-ttu-id="391b8-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="391b8-133">Key of the entity.</span></span> <span data-ttu-id="391b8-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="391b8-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="391b8-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="391b8-135">lastModifiedDateTime</span></span>|<span data-ttu-id="391b8-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="391b8-136">DateTimeOffset</span></span>|<span data-ttu-id="391b8-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="391b8-137">DateTime the object was last modified.</span></span> <span data-ttu-id="391b8-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="391b8-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="391b8-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="391b8-139">createdDateTime</span></span>|<span data-ttu-id="391b8-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="391b8-140">DateTimeOffset</span></span>|<span data-ttu-id="391b8-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="391b8-141">DateTime the object was created.</span></span> <span data-ttu-id="391b8-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="391b8-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="391b8-143">descripción</span><span class="sxs-lookup"><span data-stu-id="391b8-143">description</span></span>|<span data-ttu-id="391b8-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="391b8-144">String</span></span>|<span data-ttu-id="391b8-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="391b8-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="391b8-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="391b8-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="391b8-147">displayName</span><span class="sxs-lookup"><span data-stu-id="391b8-147">displayName</span></span>|<span data-ttu-id="391b8-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="391b8-148">String</span></span>|<span data-ttu-id="391b8-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="391b8-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="391b8-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="391b8-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="391b8-151">version</span><span class="sxs-lookup"><span data-stu-id="391b8-151">version</span></span>|<span data-ttu-id="391b8-152">Int32</span><span class="sxs-lookup"><span data-stu-id="391b8-152">Int32</span></span>|<span data-ttu-id="391b8-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="391b8-153">Version of the device configuration.</span></span> <span data-ttu-id="391b8-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="391b8-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="391b8-155">activeHoursStart</span><span class="sxs-lookup"><span data-stu-id="391b8-155">activeHoursStart</span></span>|<span data-ttu-id="391b8-156">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="391b8-156">TimeOfDay</span></span>|<span data-ttu-id="391b8-157">Inicio de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="391b8-157">Active Hours Start (active hours mean the time window when updates install should not happen)</span></span>|
|<span data-ttu-id="391b8-158">activeHoursEnd</span><span class="sxs-lookup"><span data-stu-id="391b8-158">activeHoursEnd</span></span>|<span data-ttu-id="391b8-159">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="391b8-159">TimeOfDay</span></span>|<span data-ttu-id="391b8-160">Fin de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="391b8-160">Active Hours End (active hours mean the time window when updates install should not happen)</span></span>|
|<span data-ttu-id="391b8-161">scheduledInstallDays</span><span class="sxs-lookup"><span data-stu-id="391b8-161">scheduledInstallDays</span></span>|<span data-ttu-id="391b8-162">colección de [dayOfWeek](../resources/intune-deviceconfig-dayofweek.md)</span><span class="sxs-lookup"><span data-stu-id="391b8-162">[dayOfWeek](../resources/intune-deviceconfig-dayofweek.md) collection</span></span>|<span data-ttu-id="391b8-163">Días de la semana para los que se configuran las horas activas.</span><span class="sxs-lookup"><span data-stu-id="391b8-163">Days in week for which active hours are configured.</span></span> <span data-ttu-id="391b8-164">Esta colección puede contener un máximo de 7 elementos.</span><span class="sxs-lookup"><span data-stu-id="391b8-164">This collection can contain a maximum of 7 elements.</span></span> <span data-ttu-id="391b8-165">Valores posibles: `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday` y `sunday`.</span><span class="sxs-lookup"><span data-stu-id="391b8-165">Possible values are: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="391b8-166">utcTimeOffsetInMinutes</span><span class="sxs-lookup"><span data-stu-id="391b8-166">utcTimeOffsetInMinutes</span></span>|<span data-ttu-id="391b8-167">Int32</span><span class="sxs-lookup"><span data-stu-id="391b8-167">Int32</span></span>|<span data-ttu-id="391b8-168">Diferencia horaria UTC indicada en minutos</span><span class="sxs-lookup"><span data-stu-id="391b8-168">UTC Time Offset indicated in minutes</span></span>|



## <a name="response"></a><span data-ttu-id="391b8-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="391b8-169">Response</span></span>
<span data-ttu-id="391b8-170">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="391b8-170">If successful, this method returns a `200 OK` response code and an updated [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="391b8-171">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="391b8-171">Example</span></span>
### <a name="request"></a><span data-ttu-id="391b8-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="391b8-172">Request</span></span>
<span data-ttu-id="391b8-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="391b8-173">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 325

{
  "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "activeHoursStart": "12:00:05.5020000",
  "activeHoursEnd": "11:59:00.8990000",
  "scheduledInstallDays": [
    "monday"
  ],
  "utcTimeOffsetInMinutes": 6
}
```

### <a name="response"></a><span data-ttu-id="391b8-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="391b8-174">Response</span></span>
<span data-ttu-id="391b8-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="391b8-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 497

{
  "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
  "id": "321aef09-ef09-321a-09ef-1a3209ef1a32",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "activeHoursStart": "12:00:05.5020000",
  "activeHoursEnd": "11:59:00.8990000",
  "scheduledInstallDays": [
    "monday"
  ],
  "utcTimeOffsetInMinutes": 6
}
```



