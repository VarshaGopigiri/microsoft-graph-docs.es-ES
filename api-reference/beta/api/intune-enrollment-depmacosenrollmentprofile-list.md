---
title: Lista depMacOSEnrollmentProfiles
description: Propiedades de la lista y relaciones de los objetos depMacOSEnrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 262d17b29bc1dd0c8a0a1a25ec6b077a33be22c2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822480"
---
# <a name="list-depmacosenrollmentprofiles"></a><span data-ttu-id="21459-103">Lista depMacOSEnrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="21459-103">List depMacOSEnrollmentProfiles</span></span>

> <span data-ttu-id="21459-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="21459-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="21459-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="21459-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="21459-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="21459-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="21459-107">Propiedades de la lista y relaciones de los objetos [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="21459-107">List properties and relationships of the [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="21459-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="21459-108">Prerequisites</span></span>
<span data-ttu-id="21459-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21459-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="21459-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21459-111">Permission type</span></span>|<span data-ttu-id="21459-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21459-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="21459-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21459-113">Delegated (work or school account)</span></span>|<span data-ttu-id="21459-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="21459-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="21459-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21459-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="21459-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21459-116">Not supported.</span></span>|
|<span data-ttu-id="21459-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21459-117">Application</span></span>|<span data-ttu-id="21459-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21459-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="21459-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21459-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="21459-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21459-120">Request headers</span></span>
|<span data-ttu-id="21459-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21459-121">Header</span></span>|<span data-ttu-id="21459-122">Valor</span><span class="sxs-lookup"><span data-stu-id="21459-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="21459-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="21459-123">Authorization</span></span>|<span data-ttu-id="21459-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="21459-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="21459-125">Accept</span><span class="sxs-lookup"><span data-stu-id="21459-125">Accept</span></span>|<span data-ttu-id="21459-126">application/json</span><span class="sxs-lookup"><span data-stu-id="21459-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="21459-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="21459-127">Request body</span></span>
<span data-ttu-id="21459-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="21459-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="21459-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21459-129">Response</span></span>
<span data-ttu-id="21459-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21459-130">If successful, this method returns a `200 OK` response code and a collection of [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="21459-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21459-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="21459-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21459-132">Request</span></span>
<span data-ttu-id="21459-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21459-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

### <a name="response"></a><span data-ttu-id="21459-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21459-134">Response</span></span>
<span data-ttu-id="21459-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="21459-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1114

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.depMacOSEnrollmentProfile",
      "id": "e433c95c-c95c-e433-5cc9-33e45cc933e4",
      "displayName": "Display Name value",
      "description": "Description value",
      "requiresUserAuthentication": true,
      "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
      "enableAuthenticationViaCompanyPortal": true,
      "isDefault": true,
      "supervisedModeEnabled": true,
      "supportDepartment": "Support Department value",
      "passCodeDisabled": true,
      "isMandatory": true,
      "locationDisabled": true,
      "supportPhoneNumber": "Support Phone Number value",
      "profileRemovalDisabled": true,
      "restoreBlocked": true,
      "appleIdDisabled": true,
      "termsAndConditionsDisabled": true,
      "touchIdDisabled": true,
      "applePayDisabled": true,
      "zoomDisabled": true,
      "siriDisabled": true,
      "diagnosticsDisabled": true,
      "registrationDisabled": true,
      "fileVaultDisabled": true,
      "iCloudDiagnosticsDisabled": true
    }
  ]
}
```





