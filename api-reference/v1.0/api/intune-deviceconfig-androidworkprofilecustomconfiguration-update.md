---
title: Actualizar androidWorkProfileCustomConfiguration
description: Actualizar las propiedades de un objeto androidWorkProfileCustomConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e57f91398d87b8019dca00016c47ece1370c828f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860518"
---
# <a name="update-androidworkprofilecustomconfiguration"></a><span data-ttu-id="ea6d6-103">Actualizar androidWorkProfileCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea6d6-103">Update androidWorkProfileCustomConfiguration</span></span>

> <span data-ttu-id="ea6d6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea6d6-105">Actualizar las propiedades de un objeto [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="ea6d6-105">Update the properties of a [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea6d6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea6d6-106">Prerequisites</span></span>
<span data-ttu-id="ea6d6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea6d6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea6d6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea6d6-109">Permission type</span></span>|<span data-ttu-id="ea6d6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea6d6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ea6d6-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea6d6-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ea6d6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea6d6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-114">Not supported.</span></span>|
|<span data-ttu-id="ea6d6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea6d6-115">Application</span></span>|<span data-ttu-id="ea6d6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea6d6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea6d6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ea6d6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6d6-118">Request headers</span></span>
|<span data-ttu-id="ea6d6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea6d6-119">Header</span></span>|<span data-ttu-id="ea6d6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ea6d6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea6d6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ea6d6-121">Authorization</span></span>|<span data-ttu-id="ea6d6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea6d6-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ea6d6-123">Accept</span></span>|<span data-ttu-id="ea6d6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ea6d6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea6d6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6d6-125">Request body</span></span>
<span data-ttu-id="ea6d6-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="ea6d6-126">In the request body, supply a JSON representation for the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>

<span data-ttu-id="ea6d6-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea6d6-127">The following table shows the properties that are required when you create the [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md).</span></span>

|<span data-ttu-id="ea6d6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea6d6-128">Property</span></span>|<span data-ttu-id="ea6d6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea6d6-129">Type</span></span>|<span data-ttu-id="ea6d6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea6d6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea6d6-131">id</span><span class="sxs-lookup"><span data-stu-id="ea6d6-131">id</span></span>|<span data-ttu-id="ea6d6-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea6d6-132">String</span></span>|<span data-ttu-id="ea6d6-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-133">Key of the entity.</span></span> <span data-ttu-id="ea6d6-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea6d6-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ea6d6-135">lastModifiedDateTime</span></span>|<span data-ttu-id="ea6d6-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea6d6-136">DateTimeOffset</span></span>|<span data-ttu-id="ea6d6-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-137">DateTime the object was last modified.</span></span> <span data-ttu-id="ea6d6-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea6d6-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ea6d6-139">createdDateTime</span></span>|<span data-ttu-id="ea6d6-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea6d6-140">DateTimeOffset</span></span>|<span data-ttu-id="ea6d6-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-141">DateTime the object was created.</span></span> <span data-ttu-id="ea6d6-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea6d6-143">descripción</span><span class="sxs-lookup"><span data-stu-id="ea6d6-143">description</span></span>|<span data-ttu-id="ea6d6-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea6d6-144">String</span></span>|<span data-ttu-id="ea6d6-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ea6d6-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea6d6-147">displayName</span><span class="sxs-lookup"><span data-stu-id="ea6d6-147">displayName</span></span>|<span data-ttu-id="ea6d6-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea6d6-148">String</span></span>|<span data-ttu-id="ea6d6-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ea6d6-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea6d6-151">version</span><span class="sxs-lookup"><span data-stu-id="ea6d6-151">version</span></span>|<span data-ttu-id="ea6d6-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ea6d6-152">Int32</span></span>|<span data-ttu-id="ea6d6-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-153">Version of the device configuration.</span></span> <span data-ttu-id="ea6d6-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea6d6-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="ea6d6-155">omaSettings</span></span>|<span data-ttu-id="ea6d6-156">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="ea6d6-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="ea6d6-157">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-157">OMA settings.</span></span> <span data-ttu-id="ea6d6-158">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-158">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="ea6d6-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea6d6-159">Response</span></span>
<span data-ttu-id="ea6d6-160">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-160">If successful, this method returns a `200 OK` response code and an updated [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea6d6-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea6d6-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea6d6-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea6d6-162">Request</span></span>
<span data-ttu-id="ea6d6-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-163">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 413

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
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

### <a name="response"></a><span data-ttu-id="ea6d6-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea6d6-164">Response</span></span>
<span data-ttu-id="ea6d6-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea6d6-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 585

{
  "@odata.type": "#microsoft.graph.androidWorkProfileCustomConfiguration",
  "id": "76c5d59b-d59b-76c5-9bd5-c5769bd5c576",
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



