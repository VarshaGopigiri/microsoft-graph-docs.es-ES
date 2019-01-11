---
title: Actualizar windowsOfficeClientConfiguration
description: Una carga de la directiva de seguridad que no son específicos de una revisión.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e13228c6fc467fa49b740c02b4b7068efb1ec42e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863878"
---
# <a name="update-windowsofficeclientconfiguration"></a><span data-ttu-id="5a20b-103">Actualizar windowsOfficeClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a20b-103">Update windowsOfficeClientConfiguration</span></span>

> <span data-ttu-id="5a20b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5a20b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5a20b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5a20b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5a20b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5a20b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5a20b-107">Una carga de la directiva de seguridad que no son específicos de una revisión.</span><span class="sxs-lookup"><span data-stu-id="5a20b-107">Patch a specific non-security policy payload.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5a20b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5a20b-108">Prerequisites</span></span>
<span data-ttu-id="5a20b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5a20b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5a20b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5a20b-111">Permission type</span></span>|<span data-ttu-id="5a20b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5a20b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5a20b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5a20b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5a20b-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5a20b-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5a20b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5a20b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5a20b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a20b-116">Not supported.</span></span>|
|<span data-ttu-id="5a20b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5a20b-117">Application</span></span>|<span data-ttu-id="5a20b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a20b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5a20b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a20b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /officeConfiguration/clientConfigurations/{key}
```

## <a name="request-headers"></a><span data-ttu-id="5a20b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a20b-120">Request headers</span></span>
|<span data-ttu-id="5a20b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a20b-121">Header</span></span>|<span data-ttu-id="5a20b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5a20b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5a20b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5a20b-123">Authorization</span></span>|<span data-ttu-id="5a20b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5a20b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5a20b-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5a20b-125">Accept</span></span>|<span data-ttu-id="5a20b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5a20b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5a20b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a20b-127">Request body</span></span>
<span data-ttu-id="5a20b-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="5a20b-128">In the request body, supply a JSON representation for the [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md) object.</span></span>

<span data-ttu-id="5a20b-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="5a20b-129">The following table shows the properties that are required when you create the [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md).</span></span>

|<span data-ttu-id="5a20b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5a20b-130">Property</span></span>|<span data-ttu-id="5a20b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a20b-131">Type</span></span>|<span data-ttu-id="5a20b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a20b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5a20b-133">id</span><span class="sxs-lookup"><span data-stu-id="5a20b-133">id</span></span>|<span data-ttu-id="5a20b-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5a20b-134">String</span></span>|<span data-ttu-id="5a20b-135">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-135">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="5a20b-136">userPreferencePayload</span><span class="sxs-lookup"><span data-stu-id="5a20b-136">userPreferencePayload</span></span>|<span data-ttu-id="5a20b-137">Stream</span><span class="sxs-lookup"><span data-stu-id="5a20b-137">Stream</span></span>|<span data-ttu-id="5a20b-138">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-138">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="5a20b-139">policyPayload</span><span class="sxs-lookup"><span data-stu-id="5a20b-139">policyPayload</span></span>|<span data-ttu-id="5a20b-140">Stream</span><span class="sxs-lookup"><span data-stu-id="5a20b-140">Stream</span></span>|<span data-ttu-id="5a20b-141">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-141">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="5a20b-142">descripción</span><span class="sxs-lookup"><span data-stu-id="5a20b-142">description</span></span>|<span data-ttu-id="5a20b-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="5a20b-143">String</span></span>|<span data-ttu-id="5a20b-144">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-144">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="5a20b-145">displayName</span><span class="sxs-lookup"><span data-stu-id="5a20b-145">displayName</span></span>|<span data-ttu-id="5a20b-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="5a20b-146">String</span></span>|<span data-ttu-id="5a20b-147">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-147">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="5a20b-148">prioridad</span><span class="sxs-lookup"><span data-stu-id="5a20b-148">priority</span></span>|<span data-ttu-id="5a20b-149">Int32</span><span class="sxs-lookup"><span data-stu-id="5a20b-149">Int32</span></span>|<span data-ttu-id="5a20b-150">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-150">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="5a20b-151">userCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="5a20b-151">userCheckinSummary</span></span>|[<span data-ttu-id="5a20b-152">officeUserCheckinSummary</span><span class="sxs-lookup"><span data-stu-id="5a20b-152">officeUserCheckinSummary</span></span>](../resources/intune-cirrus-officeusercheckinsummary.md)|<span data-ttu-id="5a20b-153">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-153">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|
|<span data-ttu-id="5a20b-154">checkinStatuses</span><span class="sxs-lookup"><span data-stu-id="5a20b-154">checkinStatuses</span></span>|<span data-ttu-id="5a20b-155">colección de [officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-155">[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md) collection</span></span>|<span data-ttu-id="5a20b-156">Aún no se han documentado Inherited desde [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5a20b-156">Not yet documented Inherited from [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="5a20b-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a20b-157">Response</span></span>
<span data-ttu-id="5a20b-158">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a20b-158">If successful, this method returns a `200 OK` response code and an updated [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5a20b-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a20b-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="5a20b-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a20b-160">Request</span></span>
<span data-ttu-id="5a20b-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a20b-161">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="5a20b-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a20b-162">Response</span></span>
<span data-ttu-id="5a20b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5a20b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1069

{
  "@odata.type": "#microsoft.graph.windowsOfficeClientConfiguration",
  "id": "13a5ac73-ac73-13a5-73ac-a51373aca513",
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



