---
title: Actualizar windows10EnterpriseModernAppManagementConfiguration
description: Actualice las propiedades de un objeto windows10EnterpriseModernAppManagementConfiguration.
ms.openlocfilehash: 6eb9259be829723b66e7b8b2136bceb8b7449c45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031088"
---
# <a name="update-windows10enterprisemodernappmanagementconfiguration"></a><span data-ttu-id="25253-103">Actualizar windows10EnterpriseModernAppManagementConfiguration</span><span class="sxs-lookup"><span data-stu-id="25253-103">Update windows10EnterpriseModernAppManagementConfiguration</span></span>

> <span data-ttu-id="25253-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25253-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25253-105">Actualice las propiedades de un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="25253-105">Update the properties of a [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="25253-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25253-106">Prerequisites</span></span>
<span data-ttu-id="25253-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25253-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25253-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25253-109">Permission type</span></span>|<span data-ttu-id="25253-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25253-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="25253-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25253-111">Delegated (work or school account)</span></span>|<span data-ttu-id="25253-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25253-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="25253-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25253-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="25253-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25253-114">Not supported.</span></span>|
|<span data-ttu-id="25253-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25253-115">Application</span></span>|<span data-ttu-id="25253-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25253-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="25253-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25253-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="25253-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25253-118">Request headers</span></span>
|<span data-ttu-id="25253-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25253-119">Header</span></span>|<span data-ttu-id="25253-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25253-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="25253-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="25253-121">Authorization</span></span>|<span data-ttu-id="25253-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="25253-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="25253-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="25253-123">Accept</span></span>|<span data-ttu-id="25253-124">application/json</span><span class="sxs-lookup"><span data-stu-id="25253-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="25253-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25253-125">Request body</span></span>
<span data-ttu-id="25253-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="25253-126">In the request body, supply a JSON representation for the [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object.</span></span>

<span data-ttu-id="25253-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="25253-127">The following table shows the properties that are required when you create the [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md).</span></span>

|<span data-ttu-id="25253-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25253-128">Property</span></span>|<span data-ttu-id="25253-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="25253-129">Type</span></span>|<span data-ttu-id="25253-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="25253-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25253-131">id</span><span class="sxs-lookup"><span data-stu-id="25253-131">id</span></span>|<span data-ttu-id="25253-132">String</span><span class="sxs-lookup"><span data-stu-id="25253-132">String</span></span>|<span data-ttu-id="25253-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="25253-133">Key of the entity.</span></span> <span data-ttu-id="25253-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25253-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25253-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="25253-135">lastModifiedDateTime</span></span>|<span data-ttu-id="25253-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="25253-136">DateTimeOffset</span></span>|<span data-ttu-id="25253-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="25253-137">DateTime the object was last modified.</span></span> <span data-ttu-id="25253-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25253-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25253-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="25253-139">createdDateTime</span></span>|<span data-ttu-id="25253-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="25253-140">DateTimeOffset</span></span>|<span data-ttu-id="25253-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="25253-141">DateTime the object was created.</span></span> <span data-ttu-id="25253-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25253-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25253-143">descripción</span><span class="sxs-lookup"><span data-stu-id="25253-143">description</span></span>|<span data-ttu-id="25253-144">String</span><span class="sxs-lookup"><span data-stu-id="25253-144">String</span></span>|<span data-ttu-id="25253-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25253-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="25253-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25253-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25253-147">displayName</span><span class="sxs-lookup"><span data-stu-id="25253-147">displayName</span></span>|<span data-ttu-id="25253-148">String</span><span class="sxs-lookup"><span data-stu-id="25253-148">String</span></span>|<span data-ttu-id="25253-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25253-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="25253-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25253-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25253-151">version</span><span class="sxs-lookup"><span data-stu-id="25253-151">version</span></span>|<span data-ttu-id="25253-152">Int32</span><span class="sxs-lookup"><span data-stu-id="25253-152">Int32</span></span>|<span data-ttu-id="25253-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25253-153">Version of the device configuration.</span></span> <span data-ttu-id="25253-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25253-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25253-155">uninstallBuiltInApps</span><span class="sxs-lookup"><span data-stu-id="25253-155">uninstallBuiltInApps</span></span>|<span data-ttu-id="25253-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="25253-156">Boolean</span></span>|<span data-ttu-id="25253-157">Indica si se desinstalará o no una lista fija de aplicaciones integradas de Windows.</span><span class="sxs-lookup"><span data-stu-id="25253-157">Indicates whether or not to uninstall a fixed list of built-in Windows apps.</span></span>|



## <a name="response"></a><span data-ttu-id="25253-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25253-158">Response</span></span>
<span data-ttu-id="25253-159">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25253-159">If successful, this method returns a `200 OK` response code and an updated [windows10EnterpriseModernAppManagementConfiguration](../resources/intune-deviceconfig-windows10enterprisemodernappmanagementconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25253-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25253-160">Example</span></span>
### <a name="request"></a><span data-ttu-id="25253-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25253-161">Request</span></span>
<span data-ttu-id="25253-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25253-162">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 222

{
  "@odata.type": "#microsoft.graph.windows10EnterpriseModernAppManagementConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "uninstallBuiltInApps": true
}
```

### <a name="response"></a><span data-ttu-id="25253-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25253-163">Response</span></span>
<span data-ttu-id="25253-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25253-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 394

{
  "@odata.type": "#microsoft.graph.windows10EnterpriseModernAppManagementConfiguration",
  "id": "d6577687-7687-d657-8776-57d6877657d6",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "uninstallBuiltInApps": true
}
```



