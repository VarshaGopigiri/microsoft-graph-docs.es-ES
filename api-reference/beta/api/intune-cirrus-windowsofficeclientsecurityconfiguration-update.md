---
title: Actualizar windowsOfficeClientSecurityConfiguration
description: Actualizar las propiedades de un objeto windowsOfficeClientSecurityConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 52db50c1014833468b9eee435e06c96153aa5fc5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853392"
---
# <a name="update-windowsofficeclientsecurityconfiguration"></a><span data-ttu-id="3b892-103">Actualizar windowsOfficeClientSecurityConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b892-103">Update windowsOfficeClientSecurityConfiguration</span></span>

> <span data-ttu-id="3b892-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3b892-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b892-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3b892-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3b892-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3b892-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3b892-107">Actualizar las propiedades de un objeto [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="3b892-107">Update the properties of a [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3b892-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3b892-108">Prerequisites</span></span>
<span data-ttu-id="3b892-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3b892-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3b892-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3b892-111">Permission type</span></span>|<span data-ttu-id="3b892-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3b892-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3b892-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3b892-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3b892-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b892-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="3b892-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3b892-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3b892-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b892-116">Not supported.</span></span>|
|<span data-ttu-id="3b892-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3b892-117">Application</span></span>|<span data-ttu-id="3b892-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3b892-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3b892-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3b892-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /officeConfiguration/clientConfigurations/{officeClientConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="3b892-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3b892-120">Request headers</span></span>
|<span data-ttu-id="3b892-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b892-121">Header</span></span>|<span data-ttu-id="3b892-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3b892-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3b892-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3b892-123">Authorization</span></span>|<span data-ttu-id="3b892-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3b892-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3b892-125">Accept</span><span class="sxs-lookup"><span data-stu-id="3b892-125">Accept</span></span>|<span data-ttu-id="3b892-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3b892-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3b892-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3b892-127">Request body</span></span>
<span data-ttu-id="3b892-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="3b892-128">In the request body, supply a JSON representation for the [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md) object.</span></span>

<span data-ttu-id="3b892-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="3b892-129">The following table shows the properties that are required when you create the [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md).</span></span>

|<span data-ttu-id="3b892-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3b892-130">Property</span></span>|<span data-ttu-id="3b892-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b892-131">Type</span></span>|<span data-ttu-id="3b892-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b892-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3b892-133">id</span><span class="sxs-lookup"><span data-stu-id="3b892-133">id</span></span>|<span data-ttu-id="3b892-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="3b892-134">String</span></span>|<span data-ttu-id="3b892-135">Identificador de la directiva de configuración de cliente de office.</span><span class="sxs-lookup"><span data-stu-id="3b892-135">Id of the office client configuration policy.</span></span> <span data-ttu-id="3b892-136">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-136">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-137">userPreferencePayload</span><span class="sxs-lookup"><span data-stu-id="3b892-137">userPreferencePayload</span></span>|<span data-ttu-id="3b892-138">Stream</span><span class="sxs-lookup"><span data-stu-id="3b892-138">Stream</span></span>|<span data-ttu-id="3b892-139">Configuración de preferencias de JSON de cadenas en formato binario, estos valores pueden ser anulados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3b892-139">Preference settings JSON string in binary format, these values can be overridden by the user.</span></span> <span data-ttu-id="3b892-140">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-140">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-141">policyPayload</span><span class="sxs-lookup"><span data-stu-id="3b892-141">policyPayload</span></span>|<span data-ttu-id="3b892-142">Stream</span><span class="sxs-lookup"><span data-stu-id="3b892-142">Stream</span></span>|<span data-ttu-id="3b892-143">Configuración de la directiva JSON de cadenas en formato binario, no se puede cambiar estos valores por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3b892-143">Policy settings JSON string in binary format, these values cannot be changed by the user.</span></span> <span data-ttu-id="3b892-144">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-144">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-145">descripción</span><span class="sxs-lookup"><span data-stu-id="3b892-145">description</span></span>|<span data-ttu-id="3b892-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="3b892-146">String</span></span>|<span data-ttu-id="3b892-147">Administración descripción proporcionada por el del cliente de office de directiva de configuración.</span><span class="sxs-lookup"><span data-stu-id="3b892-147">Admin provided description of the office client configuration policy.</span></span> <span data-ttu-id="3b892-148">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-148">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-149">displayName</span><span class="sxs-lookup"><span data-stu-id="3b892-149">displayName</span></span>|<span data-ttu-id="3b892-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="3b892-150">String</span></span>|<span data-ttu-id="3b892-151">Admin proporcionada el nombre de la directiva de configuración de cliente de office.</span><span class="sxs-lookup"><span data-stu-id="3b892-151">Admin provided name of the office client configuration policy.</span></span> <span data-ttu-id="3b892-152">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-152">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-153">asignaciones</span><span class="sxs-lookup"><span data-stu-id="3b892-153">assignments</span></span>|<span data-ttu-id="3b892-154">colección de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-154">[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md) collection</span></span>|<span data-ttu-id="3b892-155">La lista de las asignaciones de grupo para la directiva..</span><span class="sxs-lookup"><span data-stu-id="3b892-155">The list of group assignments for the policy..</span></span> <span data-ttu-id="3b892-156">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-156">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-157">prioridad</span><span class="sxs-lookup"><span data-stu-id="3b892-157">priority</span></span>|<span data-ttu-id="3b892-158">Int32</span><span class="sxs-lookup"><span data-stu-id="3b892-158">Int32</span></span>|<span data-ttu-id="3b892-159">Valor de prioridad debe ser un valor único para cada directiva de un inquilino y se usará para la resolución de conflictos, los valores más bajos significan prioridad sea alta.</span><span class="sxs-lookup"><span data-stu-id="3b892-159">Priority value should be unique value for each policy under a tenant and will be used for conflict resolution, lower values mean priority is high.</span></span> <span data-ttu-id="3b892-160">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-160">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-161">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3b892-161">lastModifiedDateTime</span></span>|<span data-ttu-id="3b892-162">DateTime</span><span class="sxs-lookup"><span data-stu-id="3b892-162">DateTime</span></span>|<span data-ttu-id="3b892-163">Última marca de datetime modificada de la directiva.</span><span class="sxs-lookup"><span data-stu-id="3b892-163">Last modified datetime stamp of the policy.</span></span> <span data-ttu-id="3b892-164">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-164">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-165">userCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="3b892-165">userCheckinSummary</span></span>|[<span data-ttu-id="3b892-166">officeUserCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="3b892-166">officeUserCheckinSummary</span></span>](../resources/intune-cirrus-officeusercheckinsummary.md)|<span data-ttu-id="3b892-167">Protección de resumen de usuario para la directiva.</span><span class="sxs-lookup"><span data-stu-id="3b892-167">User check-in summary for the policy.</span></span> <span data-ttu-id="3b892-168">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-168">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="3b892-169">checkinStatuses</span><span class="sxs-lookup"><span data-stu-id="3b892-169">checkinStatuses</span></span>|<span data-ttu-id="3b892-170">colección de [officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-170">[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md) collection</span></span>|<span data-ttu-id="3b892-171">Lista de comprobación de estado del cliente de office.</span><span class="sxs-lookup"><span data-stu-id="3b892-171">List of office Client check-in status.</span></span> <span data-ttu-id="3b892-172">Se hereda de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="3b892-172">Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="3b892-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b892-173">Response</span></span>
<span data-ttu-id="3b892-174">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3b892-174">If successful, this method returns a `200 OK` response code and an updated [windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3b892-175">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3b892-175">Example</span></span>
### <a name="request"></a><span data-ttu-id="3b892-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3b892-176">Request</span></span>
<span data-ttu-id="3b892-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3b892-177">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{officeClientConfigurationId}
Content-type: application/json
Content-length: 949

{
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "Description value",
  "displayName": "Display Name value",
  "priority": 8,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 2,
    "failedUserCount": 15
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "User Principal Name value",
      "deviceName": "Device Name value",
      "devicePlatform": "Device Platform value",
      "devicePlatformVersion": "Device Platform Version value",
      "wasSuccessful": true,
      "userId": "User Id value",
      "checkinDateTime": "2016-12-31T23:56:33.9571764-08:00",
      "errorMessage": "Error Message value",
      "appliedPolicies": [
        "Applied Policies value"
      ]
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="3b892-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3b892-178">Response</span></span>
<span data-ttu-id="3b892-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3b892-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1077

{
  "@odata.type": "#microsoft.graph.windowsOfficeClientSecurityConfiguration",
  "id": "f90ca1a5-a1a5-f90c-a5a1-0cf9a5a10cf9",
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "Description value",
  "displayName": "Display Name value",
  "priority": 8,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 2,
    "failedUserCount": 15
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "User Principal Name value",
      "deviceName": "Device Name value",
      "devicePlatform": "Device Platform value",
      "devicePlatformVersion": "Device Platform Version value",
      "wasSuccessful": true,
      "userId": "User Id value",
      "checkinDateTime": "2016-12-31T23:56:33.9571764-08:00",
      "errorMessage": "Error Message value",
      "appliedPolicies": [
        "Applied Policies value"
      ]
    }
  ]
}
```



