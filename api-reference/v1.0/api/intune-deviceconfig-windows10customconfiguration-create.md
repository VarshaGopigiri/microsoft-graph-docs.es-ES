---
title: Crear windows10CustomConfiguration
description: Cree un objeto windows10CustomConfiguration.
ms.openlocfilehash: c7c180b26cd5e25aba9ff36d0190ab455000f839
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030736"
---
# <a name="create-windows10customconfiguration"></a><span data-ttu-id="7e030-103">Crear windows10CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e030-103">Create windows10CustomConfiguration</span></span>

> <span data-ttu-id="7e030-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7e030-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7e030-105">Cree un objeto [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="7e030-105">Create a new [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7e030-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7e030-106">Prerequisites</span></span>
<span data-ttu-id="7e030-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7e030-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7e030-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e030-109">Permission type</span></span>|<span data-ttu-id="7e030-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e030-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7e030-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e030-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7e030-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e030-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="7e030-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e030-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7e030-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e030-114">Not supported.</span></span>|
|<span data-ttu-id="7e030-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e030-115">Application</span></span>|<span data-ttu-id="7e030-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e030-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7e030-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e030-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="7e030-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e030-118">Request headers</span></span>
|<span data-ttu-id="7e030-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e030-119">Header</span></span>|<span data-ttu-id="7e030-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7e030-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7e030-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="7e030-121">Authorization</span></span>|<span data-ttu-id="7e030-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7e030-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7e030-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7e030-123">Accept</span></span>|<span data-ttu-id="7e030-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7e030-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7e030-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e030-125">Request body</span></span>
<span data-ttu-id="7e030-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10CustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7e030-126">In the request body, supply a JSON representation for the windows10CustomConfiguration object.</span></span>

<span data-ttu-id="7e030-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10CustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7e030-127">The following table shows the properties that are required when you create the windows10CustomConfiguration.</span></span>

|<span data-ttu-id="7e030-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e030-128">Property</span></span>|<span data-ttu-id="7e030-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e030-129">Type</span></span>|<span data-ttu-id="7e030-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e030-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e030-131">id</span><span class="sxs-lookup"><span data-stu-id="7e030-131">id</span></span>|<span data-ttu-id="7e030-132">String</span><span class="sxs-lookup"><span data-stu-id="7e030-132">String</span></span>|<span data-ttu-id="7e030-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7e030-133">Key of the entity.</span></span> <span data-ttu-id="7e030-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7e030-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7e030-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7e030-135">lastModifiedDateTime</span></span>|<span data-ttu-id="7e030-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e030-136">DateTimeOffset</span></span>|<span data-ttu-id="7e030-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="7e030-137">DateTime the object was last modified.</span></span> <span data-ttu-id="7e030-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7e030-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7e030-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7e030-139">createdDateTime</span></span>|<span data-ttu-id="7e030-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e030-140">DateTimeOffset</span></span>|<span data-ttu-id="7e030-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e030-141">DateTime the object was created.</span></span> <span data-ttu-id="7e030-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7e030-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7e030-143">descripción</span><span class="sxs-lookup"><span data-stu-id="7e030-143">description</span></span>|<span data-ttu-id="7e030-144">String</span><span class="sxs-lookup"><span data-stu-id="7e030-144">String</span></span>|<span data-ttu-id="7e030-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e030-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="7e030-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7e030-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7e030-147">displayName</span><span class="sxs-lookup"><span data-stu-id="7e030-147">displayName</span></span>|<span data-ttu-id="7e030-148">String</span><span class="sxs-lookup"><span data-stu-id="7e030-148">String</span></span>|<span data-ttu-id="7e030-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e030-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="7e030-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7e030-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7e030-151">version</span><span class="sxs-lookup"><span data-stu-id="7e030-151">version</span></span>|<span data-ttu-id="7e030-152">Int32</span><span class="sxs-lookup"><span data-stu-id="7e030-152">Int32</span></span>|<span data-ttu-id="7e030-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e030-153">Version of the device configuration.</span></span> <span data-ttu-id="7e030-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="7e030-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="7e030-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="7e030-155">omaSettings</span></span>|<span data-ttu-id="7e030-156">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="7e030-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="7e030-157">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="7e030-157">OMA settings.</span></span> <span data-ttu-id="7e030-158">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="7e030-158">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="7e030-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e030-159">Response</span></span>
<span data-ttu-id="7e030-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e030-160">If successful, this method returns a `201 Created` response code and a [windows10CustomConfiguration](../resources/intune-deviceconfig-windows10customconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7e030-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e030-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="7e030-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e030-162">Request</span></span>
<span data-ttu-id="7e030-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e030-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="7e030-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e030-164">Response</span></span>
<span data-ttu-id="7e030-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e030-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



