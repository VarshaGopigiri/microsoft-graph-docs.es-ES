---
title: Lista depIOSEnrollmentProfiles
description: Propiedades de la lista y relaciones de los objetos depIOSEnrollmentProfile.
ms.openlocfilehash: f3cf1c7107351315cfc1ee8586ad23f4f53dfc91
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082914"
---
# <a name="list-depiosenrollmentprofiles"></a><span data-ttu-id="bb655-103">Lista depIOSEnrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="bb655-103">List depIOSEnrollmentProfiles</span></span>

> <span data-ttu-id="bb655-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb655-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb655-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb655-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bb655-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bb655-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bb655-107">Propiedades de la lista y relaciones de los objetos [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="bb655-107">List properties and relationships of the [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bb655-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bb655-108">Prerequisites</span></span>
<span data-ttu-id="bb655-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bb655-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bb655-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bb655-111">Permission type</span></span>|<span data-ttu-id="bb655-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bb655-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb655-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bb655-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bb655-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="bb655-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="bb655-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bb655-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb655-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb655-116">Not supported.</span></span>|
|<span data-ttu-id="bb655-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bb655-117">Application</span></span>|<span data-ttu-id="bb655-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bb655-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb655-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bb655-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="bb655-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb655-120">Request headers</span></span>
|<span data-ttu-id="bb655-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb655-121">Header</span></span>|<span data-ttu-id="bb655-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bb655-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb655-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bb655-123">Authorization</span></span>|<span data-ttu-id="bb655-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bb655-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bb655-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bb655-125">Accept</span></span>|<span data-ttu-id="bb655-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bb655-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb655-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bb655-127">Request body</span></span>
<span data-ttu-id="bb655-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bb655-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bb655-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb655-129">Response</span></span>
<span data-ttu-id="bb655-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb655-130">If successful, this method returns a `200 OK` response code and a collection of [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb655-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bb655-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="bb655-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bb655-132">Request</span></span>
<span data-ttu-id="bb655-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bb655-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

### <a name="response"></a><span data-ttu-id="bb655-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bb655-134">Response</span></span>
<span data-ttu-id="bb655-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bb655-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1559

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.depIOSEnrollmentProfile",
      "id": "1ec10a60-0a60-1ec1-600a-c11e600ac11e",
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
      "iTunesPairingMode": "allow",
      "managementCertificates": [
        {
          "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
          "thumbprint": "Thumbprint value",
          "certificate": "Certificate value"
        }
      ],
      "restoreFromAndroidDisabled": true,
      "awaitDeviceConfiguredConfirmation": true,
      "sharedIPadMaximumUserCount": 10,
      "enableSharedIPad": true,
      "companyPortalVppTokenId": "Company Portal Vpp Token Id value",
      "enableSingleAppEnrollmentMode": true
    }
  ]
}
```





