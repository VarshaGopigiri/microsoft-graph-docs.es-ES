---
title: acción importAppleDeviceIdentityList
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 75a40be8d2ea3ddafadb78f95662dcadf7a9ac01
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890604"
---
# <a name="importappledeviceidentitylist-action"></a><span data-ttu-id="2cd26-103">acción importAppleDeviceIdentityList</span><span class="sxs-lookup"><span data-stu-id="2cd26-103">importAppleDeviceIdentityList action</span></span>

> <span data-ttu-id="2cd26-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2cd26-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2cd26-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2cd26-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2cd26-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2cd26-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2cd26-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2cd26-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2cd26-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2cd26-108">Prerequisites</span></span>
<span data-ttu-id="2cd26-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2cd26-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2cd26-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2cd26-111">Permission type</span></span>|<span data-ttu-id="2cd26-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2cd26-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2cd26-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2cd26-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2cd26-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cd26-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2cd26-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2cd26-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2cd26-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2cd26-116">Not supported.</span></span>|
|<span data-ttu-id="2cd26-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2cd26-117">Application</span></span>|<span data-ttu-id="2cd26-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2cd26-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2cd26-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2cd26-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities/importAppleDeviceIdentityList
```

## <a name="request-headers"></a><span data-ttu-id="2cd26-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2cd26-120">Request headers</span></span>
|<span data-ttu-id="2cd26-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cd26-121">Header</span></span>|<span data-ttu-id="2cd26-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2cd26-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2cd26-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2cd26-123">Authorization</span></span>|<span data-ttu-id="2cd26-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2cd26-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2cd26-125">Accept</span><span class="sxs-lookup"><span data-stu-id="2cd26-125">Accept</span></span>|<span data-ttu-id="2cd26-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2cd26-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2cd26-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2cd26-127">Request body</span></span>
<span data-ttu-id="2cd26-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="2cd26-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="2cd26-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="2cd26-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="2cd26-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2cd26-130">Property</span></span>|<span data-ttu-id="2cd26-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cd26-131">Type</span></span>|<span data-ttu-id="2cd26-132">Description</span><span class="sxs-lookup"><span data-stu-id="2cd26-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2cd26-133">importedAppleDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="2cd26-133">importedAppleDeviceIdentities</span></span>|<span data-ttu-id="2cd26-134">colección de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)</span><span class="sxs-lookup"><span data-stu-id="2cd26-134">[importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md) collection</span></span>|<span data-ttu-id="2cd26-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2cd26-135">Not yet documented</span></span>|
|<span data-ttu-id="2cd26-136">overwriteImportedDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="2cd26-136">overwriteImportedDeviceIdentities</span></span>|<span data-ttu-id="2cd26-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="2cd26-137">Boolean</span></span>|<span data-ttu-id="2cd26-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2cd26-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="2cd26-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cd26-139">Response</span></span>
<span data-ttu-id="2cd26-140">Si tiene éxito, esta acción devuelve un `200 OK` código de respuesta y una colección de [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cd26-140">If successful, this action returns a `200 OK` response code and a [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2cd26-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cd26-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="2cd26-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2cd26-142">Request</span></span>
<span data-ttu-id="2cd26-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2cd26-143">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="2cd26-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cd26-144">Response</span></span>
<span data-ttu-id="2cd26-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2cd26-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





