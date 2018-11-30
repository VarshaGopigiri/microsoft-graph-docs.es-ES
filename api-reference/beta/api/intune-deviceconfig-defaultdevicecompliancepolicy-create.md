---
title: Crear defaultDeviceCompliancePolicy
description: Crear un nuevo objeto defaultDeviceCompliancePolicy.
ms.openlocfilehash: 8c05cc7eedc1249175b6738ea241dea37fa5cad4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083896"
---
# <a name="create-defaultdevicecompliancepolicy"></a><span data-ttu-id="8e570-103">Crear defaultDeviceCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="8e570-103">Create defaultDeviceCompliancePolicy</span></span>

> <span data-ttu-id="8e570-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8e570-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8e570-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8e570-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8e570-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8e570-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8e570-107">Crear un nuevo objeto [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="8e570-107">Create a new [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8e570-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8e570-108">Prerequisites</span></span>
<span data-ttu-id="8e570-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8e570-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8e570-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8e570-111">Permission type</span></span>|<span data-ttu-id="8e570-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8e570-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8e570-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8e570-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8e570-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8e570-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8e570-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8e570-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8e570-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e570-116">Not supported.</span></span>|
|<span data-ttu-id="8e570-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8e570-117">Application</span></span>|<span data-ttu-id="8e570-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8e570-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8e570-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8e570-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="8e570-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8e570-120">Request headers</span></span>
|<span data-ttu-id="8e570-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e570-121">Header</span></span>|<span data-ttu-id="8e570-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8e570-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8e570-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8e570-123">Authorization</span></span>|<span data-ttu-id="8e570-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8e570-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8e570-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8e570-125">Accept</span></span>|<span data-ttu-id="8e570-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8e570-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8e570-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8e570-127">Request body</span></span>
<span data-ttu-id="8e570-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto defaultDeviceCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="8e570-128">In the request body, supply a JSON representation for the defaultDeviceCompliancePolicy object.</span></span>

<span data-ttu-id="8e570-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el defaultDeviceCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="8e570-129">The following table shows the properties that are required when you create the defaultDeviceCompliancePolicy.</span></span>

|<span data-ttu-id="8e570-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8e570-130">Property</span></span>|<span data-ttu-id="8e570-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e570-131">Type</span></span>|<span data-ttu-id="8e570-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e570-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8e570-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="8e570-133">roleScopeTagIds</span></span>|<span data-ttu-id="8e570-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="8e570-134">String collection</span></span>|<span data-ttu-id="8e570-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="8e570-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="8e570-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8e570-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8e570-137">id</span><span class="sxs-lookup"><span data-stu-id="8e570-137">id</span></span>|<span data-ttu-id="8e570-138">String</span><span class="sxs-lookup"><span data-stu-id="8e570-138">String</span></span>|<span data-ttu-id="8e570-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8e570-139">Key of the entity.</span></span> <span data-ttu-id="8e570-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8e570-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8e570-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8e570-141">createdDateTime</span></span>|<span data-ttu-id="8e570-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8e570-142">DateTimeOffset</span></span>|<span data-ttu-id="8e570-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8e570-143">DateTime the object was created.</span></span> <span data-ttu-id="8e570-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8e570-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8e570-145">descripción</span><span class="sxs-lookup"><span data-stu-id="8e570-145">description</span></span>|<span data-ttu-id="8e570-146">String</span><span class="sxs-lookup"><span data-stu-id="8e570-146">String</span></span>|<span data-ttu-id="8e570-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e570-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8e570-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8e570-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8e570-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8e570-149">lastModifiedDateTime</span></span>|<span data-ttu-id="8e570-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8e570-150">DateTimeOffset</span></span>|<span data-ttu-id="8e570-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8e570-151">DateTime the object was last modified.</span></span> <span data-ttu-id="8e570-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8e570-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8e570-153">displayName</span><span class="sxs-lookup"><span data-stu-id="8e570-153">displayName</span></span>|<span data-ttu-id="8e570-154">String</span><span class="sxs-lookup"><span data-stu-id="8e570-154">String</span></span>|<span data-ttu-id="8e570-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e570-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8e570-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8e570-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="8e570-157">version</span><span class="sxs-lookup"><span data-stu-id="8e570-157">version</span></span>|<span data-ttu-id="8e570-158">Int32</span><span class="sxs-lookup"><span data-stu-id="8e570-158">Int32</span></span>|<span data-ttu-id="8e570-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e570-159">Version of the device configuration.</span></span> <span data-ttu-id="8e570-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="8e570-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|



## <a name="response"></a><span data-ttu-id="8e570-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e570-161">Response</span></span>
<span data-ttu-id="8e570-162">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8e570-162">If successful, this method returns a `201 Created` response code and a [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8e570-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e570-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="8e570-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8e570-164">Request</span></span>
<span data-ttu-id="8e570-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8e570-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies
Content-type: application/json
Content-length: 293

{
  "@odata.type": "#microsoft.graph.defaultDeviceCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="8e570-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8e570-166">Response</span></span>
<span data-ttu-id="8e570-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8e570-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 401

{
  "@odata.type": "#microsoft.graph.defaultDeviceCompliancePolicy",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "id": "a285f027-f027-a285-27f0-85a227f085a2",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7
}
```





