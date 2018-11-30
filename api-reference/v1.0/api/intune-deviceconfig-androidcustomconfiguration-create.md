---
title: Crear androidCustomConfiguration
description: Cree un objeto androidCustomConfiguration.
ms.openlocfilehash: 7ce26b92d25f062a7dacb44a09ebe2250b680dd1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032334"
---
# <a name="create-androidcustomconfiguration"></a><span data-ttu-id="202db-103">Crear androidCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="202db-103">Create androidCustomConfiguration</span></span>

> <span data-ttu-id="202db-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="202db-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="202db-105">Cree un objeto [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="202db-105">Create a new [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="202db-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="202db-106">Prerequisites</span></span>
<span data-ttu-id="202db-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="202db-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="202db-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="202db-109">Permission type</span></span>|<span data-ttu-id="202db-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="202db-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="202db-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="202db-111">Delegated (work or school account)</span></span>|<span data-ttu-id="202db-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="202db-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="202db-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="202db-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="202db-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="202db-114">Not supported.</span></span>|
|<span data-ttu-id="202db-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="202db-115">Application</span></span>|<span data-ttu-id="202db-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="202db-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="202db-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="202db-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="202db-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="202db-118">Request headers</span></span>
|<span data-ttu-id="202db-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="202db-119">Header</span></span>|<span data-ttu-id="202db-120">Valor</span><span class="sxs-lookup"><span data-stu-id="202db-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="202db-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="202db-121">Authorization</span></span>|<span data-ttu-id="202db-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="202db-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="202db-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="202db-123">Accept</span></span>|<span data-ttu-id="202db-124">application/json</span><span class="sxs-lookup"><span data-stu-id="202db-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="202db-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="202db-125">Request body</span></span>
<span data-ttu-id="202db-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="202db-126">In the request body, supply a JSON representation for the androidCustomConfiguration object.</span></span>

<span data-ttu-id="202db-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="202db-127">The following table shows the properties that are required when you create the androidCustomConfiguration.</span></span>

|<span data-ttu-id="202db-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="202db-128">Property</span></span>|<span data-ttu-id="202db-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="202db-129">Type</span></span>|<span data-ttu-id="202db-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="202db-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="202db-131">id</span><span class="sxs-lookup"><span data-stu-id="202db-131">id</span></span>|<span data-ttu-id="202db-132">String</span><span class="sxs-lookup"><span data-stu-id="202db-132">String</span></span>|<span data-ttu-id="202db-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="202db-133">Key of the entity.</span></span> <span data-ttu-id="202db-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="202db-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="202db-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="202db-135">lastModifiedDateTime</span></span>|<span data-ttu-id="202db-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="202db-136">DateTimeOffset</span></span>|<span data-ttu-id="202db-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="202db-137">DateTime the object was last modified.</span></span> <span data-ttu-id="202db-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="202db-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="202db-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="202db-139">createdDateTime</span></span>|<span data-ttu-id="202db-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="202db-140">DateTimeOffset</span></span>|<span data-ttu-id="202db-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="202db-141">DateTime the object was created.</span></span> <span data-ttu-id="202db-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="202db-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="202db-143">descripción</span><span class="sxs-lookup"><span data-stu-id="202db-143">description</span></span>|<span data-ttu-id="202db-144">String</span><span class="sxs-lookup"><span data-stu-id="202db-144">String</span></span>|<span data-ttu-id="202db-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202db-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="202db-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="202db-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="202db-147">displayName</span><span class="sxs-lookup"><span data-stu-id="202db-147">displayName</span></span>|<span data-ttu-id="202db-148">String</span><span class="sxs-lookup"><span data-stu-id="202db-148">String</span></span>|<span data-ttu-id="202db-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202db-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="202db-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="202db-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="202db-151">version</span><span class="sxs-lookup"><span data-stu-id="202db-151">version</span></span>|<span data-ttu-id="202db-152">Int32</span><span class="sxs-lookup"><span data-stu-id="202db-152">Int32</span></span>|<span data-ttu-id="202db-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="202db-153">Version of the device configuration.</span></span> <span data-ttu-id="202db-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="202db-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="202db-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="202db-155">omaSettings</span></span>|<span data-ttu-id="202db-156">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="202db-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="202db-157">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="202db-157">OMA settings.</span></span> <span data-ttu-id="202db-158">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="202db-158">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="202db-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="202db-159">Response</span></span>
<span data-ttu-id="202db-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="202db-160">If successful, this method returns a `201 Created` response code and a [androidCustomConfiguration](../resources/intune-deviceconfig-androidcustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="202db-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="202db-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="202db-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="202db-162">Request</span></span>
<span data-ttu-id="202db-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="202db-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 402

{
  "@odata.type": "#microsoft.graph.androidCustomConfiguration",
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

### <a name="response"></a><span data-ttu-id="202db-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="202db-164">Response</span></span>
<span data-ttu-id="202db-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="202db-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 574

{
  "@odata.type": "#microsoft.graph.androidCustomConfiguration",
  "id": "619b5e6d-5e6d-619b-6d5e-9b616d5e9b61",
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



