---
title: Actualizar windows10CustomConfiguration
description: Actualice las propiedades de un objeto windows10CustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 767b3e9e79c33a631a773658f636d69076fb810f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875092"
---
# <a name="update-windows10customconfiguration"></a><span data-ttu-id="ce922-103">Actualizar windows10CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce922-103">Update windows10CustomConfiguration</span></span>

> <span data-ttu-id="ce922-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ce922-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ce922-105">Actualice las propiedades de un objeto [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ce922-105">Update the properties of a [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ce922-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ce922-106">Prerequisites</span></span>
<span data-ttu-id="ce922-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ce922-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce922-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce922-109">Permission type</span></span>|<span data-ttu-id="ce922-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce922-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ce922-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce922-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ce922-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ce922-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ce922-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce922-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ce922-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce922-114">Not supported.</span></span>|
|<span data-ttu-id="ce922-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce922-115">Application</span></span>|<span data-ttu-id="ce922-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ce922-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ce922-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce922-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ce922-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce922-118">Request headers</span></span>
|<span data-ttu-id="ce922-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce922-119">Header</span></span>|<span data-ttu-id="ce922-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ce922-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ce922-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ce922-121">Authorization</span></span>|<span data-ttu-id="ce922-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ce922-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ce922-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ce922-123">Accept</span></span>|<span data-ttu-id="ce922-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ce922-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ce922-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce922-125">Request body</span></span>
<span data-ttu-id="ce922-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ce922-126">In the request body, supply a JSON representation for the [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) object.</span></span>

<span data-ttu-id="ce922-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ce922-127">The following table shows the properties that are required when you create the [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md).</span></span>

|<span data-ttu-id="ce922-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce922-128">Property</span></span>|<span data-ttu-id="ce922-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce922-129">Type</span></span>|<span data-ttu-id="ce922-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce922-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ce922-131">id</span><span class="sxs-lookup"><span data-stu-id="ce922-131">id</span></span>|<span data-ttu-id="ce922-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="ce922-132">String</span></span>|<span data-ttu-id="ce922-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ce922-133">Key of the entity.</span></span> <span data-ttu-id="ce922-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce922-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce922-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ce922-135">lastModifiedDateTime</span></span>|<span data-ttu-id="ce922-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ce922-136">DateTimeOffset</span></span>|<span data-ttu-id="ce922-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ce922-137">DateTime the object was last modified.</span></span> <span data-ttu-id="ce922-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce922-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce922-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ce922-139">createdDateTime</span></span>|<span data-ttu-id="ce922-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ce922-140">DateTimeOffset</span></span>|<span data-ttu-id="ce922-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ce922-141">DateTime the object was created.</span></span> <span data-ttu-id="ce922-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce922-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce922-143">descripción</span><span class="sxs-lookup"><span data-stu-id="ce922-143">description</span></span>|<span data-ttu-id="ce922-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="ce922-144">String</span></span>|<span data-ttu-id="ce922-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce922-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ce922-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce922-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce922-147">displayName</span><span class="sxs-lookup"><span data-stu-id="ce922-147">displayName</span></span>|<span data-ttu-id="ce922-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="ce922-148">String</span></span>|<span data-ttu-id="ce922-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce922-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ce922-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce922-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce922-151">version</span><span class="sxs-lookup"><span data-stu-id="ce922-151">version</span></span>|<span data-ttu-id="ce922-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ce922-152">Int32</span></span>|<span data-ttu-id="ce922-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce922-153">Version of the device configuration.</span></span> <span data-ttu-id="ce922-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ce922-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ce922-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="ce922-155">omaSettings</span></span>|<span data-ttu-id="ce922-156">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="ce922-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="ce922-157">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="ce922-157">OMA settings.</span></span> <span data-ttu-id="ce922-158">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="ce922-158">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="ce922-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce922-159">Response</span></span>
<span data-ttu-id="ce922-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce922-160">If successful, this method returns a `200 OK` response code and an updated [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ce922-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce922-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="ce922-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce922-162">Request</span></span>
<span data-ttu-id="ce922-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce922-163">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 404

{
  "@odata.type": "#microsoft.graph.windows10CustomConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="ce922-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce922-164">Response</span></span>
<span data-ttu-id="ce922-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce922-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 576

{
  "@odata.type": "#microsoft.graph.windows10CustomConfiguration",
  "id": "d8ae266e-266e-d8ae-6e26-aed86e26aed8",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSettingInteger",
      "displayName": "Display Name value",
      "description": "Description value",
      "omaUri": "Oma Uri value",
      "value": 5
    }
  ]
}
```



