---
title: Crear windowsPhone81CustomConfiguration
description: Cree un objeto windowsPhone81CustomConfiguration.
author: tfitzmac
ms.openlocfilehash: 02701baa092b32ecdb2519780d05de42c6c73447
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301354"
---
# <a name="create-windowsphone81customconfiguration"></a><span data-ttu-id="f1cfc-103">Crear windowsPhone81CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1cfc-103">Create windowsPhone81CustomConfiguration</span></span>

> <span data-ttu-id="f1cfc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f1cfc-105">Cree un objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f1cfc-105">Create a new [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f1cfc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f1cfc-106">Prerequisites</span></span>
<span data-ttu-id="f1cfc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f1cfc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f1cfc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f1cfc-109">Permission type</span></span>|<span data-ttu-id="f1cfc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f1cfc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f1cfc-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f1cfc-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f1cfc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f1cfc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-114">Not supported.</span></span>|
|<span data-ttu-id="f1cfc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f1cfc-115">Application</span></span>|<span data-ttu-id="f1cfc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f1cfc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1cfc-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="f1cfc-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1cfc-118">Request headers</span></span>
|<span data-ttu-id="f1cfc-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1cfc-119">Header</span></span>|<span data-ttu-id="f1cfc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f1cfc-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f1cfc-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f1cfc-121">Authorization</span></span>|<span data-ttu-id="f1cfc-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f1cfc-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f1cfc-123">Accept</span></span>|<span data-ttu-id="f1cfc-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f1cfc-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f1cfc-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1cfc-125">Request body</span></span>
<span data-ttu-id="f1cfc-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsPhone81CustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-126">In the request body, supply a JSON representation for the windowsPhone81CustomConfiguration object.</span></span>

<span data-ttu-id="f1cfc-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsPhone81CustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-127">The following table shows the properties that are required when you create the windowsPhone81CustomConfiguration.</span></span>

|<span data-ttu-id="f1cfc-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f1cfc-128">Property</span></span>|<span data-ttu-id="f1cfc-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1cfc-129">Type</span></span>|<span data-ttu-id="f1cfc-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1cfc-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f1cfc-131">id</span><span class="sxs-lookup"><span data-stu-id="f1cfc-131">id</span></span>|<span data-ttu-id="f1cfc-132">String</span><span class="sxs-lookup"><span data-stu-id="f1cfc-132">String</span></span>|<span data-ttu-id="f1cfc-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-133">Key of the entity.</span></span> <span data-ttu-id="f1cfc-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f1cfc-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f1cfc-135">lastModifiedDateTime</span></span>|<span data-ttu-id="f1cfc-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f1cfc-136">DateTimeOffset</span></span>|<span data-ttu-id="f1cfc-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-137">DateTime the object was last modified.</span></span> <span data-ttu-id="f1cfc-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f1cfc-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f1cfc-139">createdDateTime</span></span>|<span data-ttu-id="f1cfc-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f1cfc-140">DateTimeOffset</span></span>|<span data-ttu-id="f1cfc-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-141">DateTime the object was created.</span></span> <span data-ttu-id="f1cfc-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f1cfc-143">descripción</span><span class="sxs-lookup"><span data-stu-id="f1cfc-143">description</span></span>|<span data-ttu-id="f1cfc-144">String</span><span class="sxs-lookup"><span data-stu-id="f1cfc-144">String</span></span>|<span data-ttu-id="f1cfc-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="f1cfc-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f1cfc-147">displayName</span><span class="sxs-lookup"><span data-stu-id="f1cfc-147">displayName</span></span>|<span data-ttu-id="f1cfc-148">String</span><span class="sxs-lookup"><span data-stu-id="f1cfc-148">String</span></span>|<span data-ttu-id="f1cfc-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="f1cfc-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f1cfc-151">version</span><span class="sxs-lookup"><span data-stu-id="f1cfc-151">version</span></span>|<span data-ttu-id="f1cfc-152">Int32</span><span class="sxs-lookup"><span data-stu-id="f1cfc-152">Int32</span></span>|<span data-ttu-id="f1cfc-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-153">Version of the device configuration.</span></span> <span data-ttu-id="f1cfc-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f1cfc-155">omaSettings</span><span class="sxs-lookup"><span data-stu-id="f1cfc-155">omaSettings</span></span>|<span data-ttu-id="f1cfc-156">Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)</span><span class="sxs-lookup"><span data-stu-id="f1cfc-156">[omaSetting](../resources/intune-deviceconfig-omasetting.md) collection</span></span>|<span data-ttu-id="f1cfc-157">Configuración de OMA.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-157">OMA settings.</span></span> <span data-ttu-id="f1cfc-158">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-158">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="f1cfc-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1cfc-159">Response</span></span>
<span data-ttu-id="f1cfc-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-160">If successful, this method returns a `201 Created` response code and a [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f1cfc-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1cfc-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="f1cfc-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f1cfc-162">Request</span></span>
<span data-ttu-id="f1cfc-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-163">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 409

{
  "@odata.type": "#microsoft.graph.windowsPhone81CustomConfiguration",
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

### <a name="response"></a><span data-ttu-id="f1cfc-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1cfc-164">Response</span></span>
<span data-ttu-id="f1cfc-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f1cfc-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 581

{
  "@odata.type": "#microsoft.graph.windowsPhone81CustomConfiguration",
  "id": "0d98693c-693c-0d98-3c69-980d3c69980d",
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



