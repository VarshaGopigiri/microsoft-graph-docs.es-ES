---
title: acción importAppleDeviceIdentityList
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2c00279ecd56242d3b169a13e7018a6b5da9f182
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959653"
---
# <a name="importappledeviceidentitylist-action"></a><span data-ttu-id="0b5bc-103">acción importAppleDeviceIdentityList</span><span class="sxs-lookup"><span data-stu-id="0b5bc-103">importAppleDeviceIdentityList action</span></span>

> <span data-ttu-id="0b5bc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0b5bc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0b5bc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0b5bc-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0b5bc-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0b5bc-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0b5bc-108">Prerequisites</span></span>
<span data-ttu-id="0b5bc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0b5bc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0b5bc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0b5bc-111">Permission type</span></span>|<span data-ttu-id="0b5bc-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0b5bc-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0b5bc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0b5bc-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0b5bc-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0b5bc-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="0b5bc-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0b5bc-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0b5bc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-116">Not supported.</span></span>|
|<span data-ttu-id="0b5bc-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0b5bc-117">Application</span></span>|<span data-ttu-id="0b5bc-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0b5bc-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b5bc-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/importAppleDeviceIdentityList
```

## <a name="request-headers"></a><span data-ttu-id="0b5bc-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b5bc-120">Request headers</span></span>
|<span data-ttu-id="0b5bc-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b5bc-121">Header</span></span>|<span data-ttu-id="0b5bc-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0b5bc-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0b5bc-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0b5bc-123">Authorization</span></span>|<span data-ttu-id="0b5bc-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0b5bc-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0b5bc-125">Accept</span></span>|<span data-ttu-id="0b5bc-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0b5bc-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0b5bc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0b5bc-127">Request body</span></span>
<span data-ttu-id="0b5bc-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="0b5bc-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="0b5bc-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0b5bc-130">Property</span></span>|<span data-ttu-id="0b5bc-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b5bc-131">Type</span></span>|<span data-ttu-id="0b5bc-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b5bc-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0b5bc-133">importedAppleDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="0b5bc-133">importedAppleDeviceIdentities</span></span>|<span data-ttu-id="0b5bc-134">colección de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="0b5bc-134">[importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) collection</span></span>|<span data-ttu-id="0b5bc-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0b5bc-135">Not yet documented</span></span>|
|<span data-ttu-id="0b5bc-136">overwriteImportedDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="0b5bc-136">overwriteImportedDeviceIdentities</span></span>|<span data-ttu-id="0b5bc-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="0b5bc-137">Boolean</span></span>|<span data-ttu-id="0b5bc-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0b5bc-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="0b5bc-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5bc-139">Response</span></span>
<span data-ttu-id="0b5bc-140">Si tiene éxito, esta acción devuelve un `200 OK` código de respuesta y una colección de [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-140">If successful, this action returns a `200 OK` response code and a [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0b5bc-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b5bc-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="0b5bc-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0b5bc-142">Request</span></span>
<span data-ttu-id="0b5bc-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/importAppleDeviceIdentityList

Content-type: application/json
Content-length: 756

{
  "importedAppleDeviceIdentities": [
    {
      "@odata.type": "#microsoft.graph.importedAppleDeviceIdentity",
      "id": "352e3c2f-3c2f-352e-2f3c-2e352f3c2e35",
      "serialNumber": "Serial Number value",
      "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
      "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
      "isSupervised": true,
      "discoverySource": "adminImport",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
      "description": "Description value",
      "enrollmentState": "enrolled",
      "platform": "ios"
    }
  ],
  "overwriteImportedDeviceIdentities": true
}
```

### <a name="response"></a><span data-ttu-id="0b5bc-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b5bc-144">Response</span></span>
<span data-ttu-id="0b5bc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0b5bc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 715

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.importedAppleDeviceIdentityResult",
      "id": "557cfb4a-fb4a-557c-4afb-7c554afb7c55",
      "serialNumber": "Serial Number value",
      "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
      "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
      "isSupervised": true,
      "discoverySource": "adminImport",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
      "description": "Description value",
      "enrollmentState": "enrolled",
      "platform": "ios",
      "status": true
    }
  ]
}
```





