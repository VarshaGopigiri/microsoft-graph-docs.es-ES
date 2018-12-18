---
title: Crear defaultDeviceCompliancePolicy
description: Crear un nuevo objeto defaultDeviceCompliancePolicy.
author: tfitzmac
ms.openlocfilehash: 7e58ac41c1839429d2a15a4590a6ce765a5341a3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327100"
---
# <a name="create-defaultdevicecompliancepolicy"></a><span data-ttu-id="c0e63-103">Crear defaultDeviceCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="c0e63-103">Create defaultDeviceCompliancePolicy</span></span>

> <span data-ttu-id="c0e63-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c0e63-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c0e63-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c0e63-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c0e63-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c0e63-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c0e63-107">Crear un nuevo objeto [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="c0e63-107">Create a new [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c0e63-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c0e63-108">Prerequisites</span></span>
<span data-ttu-id="c0e63-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c0e63-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c0e63-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c0e63-111">Permission type</span></span>|<span data-ttu-id="c0e63-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c0e63-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c0e63-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c0e63-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c0e63-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c0e63-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c0e63-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c0e63-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c0e63-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0e63-116">Not supported.</span></span>|
|<span data-ttu-id="c0e63-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c0e63-117">Application</span></span>|<span data-ttu-id="c0e63-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c0e63-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c0e63-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0e63-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="c0e63-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0e63-120">Request headers</span></span>
|<span data-ttu-id="c0e63-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0e63-121">Header</span></span>|<span data-ttu-id="c0e63-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c0e63-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c0e63-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="c0e63-123">Authorization</span></span>|<span data-ttu-id="c0e63-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c0e63-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c0e63-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c0e63-125">Accept</span></span>|<span data-ttu-id="c0e63-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c0e63-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c0e63-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0e63-127">Request body</span></span>
<span data-ttu-id="c0e63-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto defaultDeviceCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="c0e63-128">In the request body, supply a JSON representation for the defaultDeviceCompliancePolicy object.</span></span>

<span data-ttu-id="c0e63-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el defaultDeviceCompliancePolicy.</span><span class="sxs-lookup"><span data-stu-id="c0e63-129">The following table shows the properties that are required when you create the defaultDeviceCompliancePolicy.</span></span>

|<span data-ttu-id="c0e63-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c0e63-130">Property</span></span>|<span data-ttu-id="c0e63-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0e63-131">Type</span></span>|<span data-ttu-id="c0e63-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0e63-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c0e63-133">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="c0e63-133">roleScopeTagIds</span></span>|<span data-ttu-id="c0e63-134">Colección String</span><span class="sxs-lookup"><span data-stu-id="c0e63-134">String collection</span></span>|<span data-ttu-id="c0e63-135">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="c0e63-135">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="c0e63-136">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c0e63-136">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c0e63-137">id</span><span class="sxs-lookup"><span data-stu-id="c0e63-137">id</span></span>|<span data-ttu-id="c0e63-138">String</span><span class="sxs-lookup"><span data-stu-id="c0e63-138">String</span></span>|<span data-ttu-id="c0e63-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c0e63-139">Key of the entity.</span></span> <span data-ttu-id="c0e63-140">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c0e63-140">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c0e63-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c0e63-141">createdDateTime</span></span>|<span data-ttu-id="c0e63-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c0e63-142">DateTimeOffset</span></span>|<span data-ttu-id="c0e63-143">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="c0e63-143">DateTime the object was created.</span></span> <span data-ttu-id="c0e63-144">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c0e63-144">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c0e63-145">descripción</span><span class="sxs-lookup"><span data-stu-id="c0e63-145">description</span></span>|<span data-ttu-id="c0e63-146">String</span><span class="sxs-lookup"><span data-stu-id="c0e63-146">String</span></span>|<span data-ttu-id="c0e63-147">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0e63-147">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="c0e63-148">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c0e63-148">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c0e63-149">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c0e63-149">lastModifiedDateTime</span></span>|<span data-ttu-id="c0e63-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c0e63-150">DateTimeOffset</span></span>|<span data-ttu-id="c0e63-151">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="c0e63-151">DateTime the object was last modified.</span></span> <span data-ttu-id="c0e63-152">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c0e63-152">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c0e63-153">displayName</span><span class="sxs-lookup"><span data-stu-id="c0e63-153">displayName</span></span>|<span data-ttu-id="c0e63-154">String</span><span class="sxs-lookup"><span data-stu-id="c0e63-154">String</span></span>|<span data-ttu-id="c0e63-155">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0e63-155">Admin provided name of the device configuration.</span></span> <span data-ttu-id="c0e63-156">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c0e63-156">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|
|<span data-ttu-id="c0e63-157">version</span><span class="sxs-lookup"><span data-stu-id="c0e63-157">version</span></span>|<span data-ttu-id="c0e63-158">Int32</span><span class="sxs-lookup"><span data-stu-id="c0e63-158">Int32</span></span>|<span data-ttu-id="c0e63-159">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0e63-159">Version of the device configuration.</span></span> <span data-ttu-id="c0e63-160">Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c0e63-160">Inherited from [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span></span>|



## <a name="response"></a><span data-ttu-id="c0e63-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0e63-161">Response</span></span>
<span data-ttu-id="c0e63-162">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0e63-162">If successful, this method returns a `201 Created` response code and a [defaultDeviceCompliancePolicy](../resources/intune-deviceconfig-defaultdevicecompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c0e63-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0e63-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="c0e63-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0e63-164">Request</span></span>
<span data-ttu-id="c0e63-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0e63-165">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="c0e63-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0e63-166">Response</span></span>
<span data-ttu-id="c0e63-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c0e63-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





