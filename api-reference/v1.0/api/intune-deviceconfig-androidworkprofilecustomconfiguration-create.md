---
title: Crear androidWorkProfileCustomConfiguration
description: Crear un nuevo objeto androidWorkProfileCustomConfiguration.
ms.openlocfilehash: e814773390fc3dc21f87f1e071b3bbe6439897d5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031323"
---
# <a name="create-androidworkprofilecustomconfiguration"></a><span data-ttu-id="883df-103">Crear androidWorkProfileCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="883df-103">Create androidWorkProfileCustomConfiguration</span></span>

> <span data-ttu-id="883df-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="883df-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="883df-105">Crear un nuevo objeto [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="883df-105">Create a new [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="883df-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="883df-106">Prerequisites</span></span>
<span data-ttu-id="883df-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="883df-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="883df-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="883df-109">Permission type</span></span>|<span data-ttu-id="883df-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="883df-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="883df-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="883df-111">Delegated (work or school account)</span></span>|<span data-ttu-id="883df-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="883df-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="883df-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="883df-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="883df-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="883df-114">Not supported.</span></span>|
|<span data-ttu-id="883df-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="883df-115">Application</span></span>|<span data-ttu-id="883df-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="883df-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="883df-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="883df-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="883df-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="883df-118">Request headers</span></span>
|<span data-ttu-id="883df-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="883df-119">Header</span></span>|<span data-ttu-id="883df-120">Valor</span><span class="sxs-lookup"><span data-stu-id="883df-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="883df-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="883df-121">Authorization</span></span>|<span data-ttu-id="883df-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="883df-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="883df-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="883df-123">Accept</span></span>|<span data-ttu-id="883df-124">application/json</span><span class="sxs-lookup"><span data-stu-id="883df-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="883df-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="883df-125">Request body</span></span>
<span data-ttu-id="883df-126">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidWorkProfileCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="883df-126">In the request body, supply a JSON representation for the androidWorkProfileCustomConfiguration object.</span></span>

<span data-ttu-id="883df-127">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidWorkProfileCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="883df-127">The following table shows the properties that are required when you create the androidWorkProfileCustomConfiguration.</span></span>

|<span data-ttu-id="883df-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="883df-128">Property</span></span>|<span data-ttu-id="883df-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="883df-129">Type</span></span>|<span data-ttu-id="883df-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="883df-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="883df-131">id</span><span class="sxs-lookup"><span data-stu-id="883df-131">id</span></span>|<span data-ttu-id="883df-132">String</span><span class="sxs-lookup"><span data-stu-id="883df-132">String</span></span>|<span data-ttu-id="883df-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="883df-133">Key of the entity.</span></span> <span data-ttu-id="883df-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883df-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="883df-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="883df-135">lastModifiedDateTime</span></span>|<span data-ttu-id="883df-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="883df-136">DateTimeOffset</span></span>|<span data-ttu-id="883df-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="883df-137">DateTime the object was last modified.</span></span> <span data-ttu-id="883df-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883df-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="883df-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="883df-139">createdDateTime</span></span>|<span data-ttu-id="883df-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="883df-140">DateTimeOffset</span></span>|<span data-ttu-id="883df-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="883df-141">DateTime the object was created.</span></span> <span data-ttu-id="883df-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883df-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="883df-143">descripción</span><span class="sxs-lookup"><span data-stu-id="883df-143">description</span></span>|<span data-ttu-id="883df-144">String</span><span class="sxs-lookup"><span data-stu-id="883df-144">String</span></span>|<span data-ttu-id="883df-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="883df-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="883df-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883df-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="883df-147">displayName</span><span class="sxs-lookup"><span data-stu-id="883df-147">displayName</span></span>|<span data-ttu-id="883df-148">String</span><span class="sxs-lookup"><span data-stu-id="883df-148">String</span></span>|<span data-ttu-id="883df-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="883df-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="883df-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883df-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="883df-151">version</span><span class="sxs-lookup"><span data-stu-id="883df-151">version</span></span>|<span data-ttu-id="883df-152">Int32</span><span class="sxs-lookup"><span data-stu-id="883df-152">Int32</span></span>|<span data-ttu-id="883df-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="883df-153">Version of the device configuration.</span></span> <span data-ttu-id="883df-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="883df-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="883df-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="883df-155">omaSettings</span></span>|<span data-ttu-id="883df-156">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="883df-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="883df-157">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="883df-157">OMA settings.</span></span> <span data-ttu-id="883df-158">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="883df-158">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="883df-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="883df-159">Response</span></span>
<span data-ttu-id="883df-160">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="883df-160">If successful, this method returns a `201 Created` response code and a [androidWorkProfileCustomConfiguration](../resources/intune-deviceconfig-androidworkprofilecustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="883df-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="883df-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="883df-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="883df-162">Request</span></span>
<span data-ttu-id="883df-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="883df-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="883df-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="883df-164">Response</span></span>
<span data-ttu-id="883df-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="883df-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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


