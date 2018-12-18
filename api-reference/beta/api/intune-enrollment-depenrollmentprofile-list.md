---
title: Lista depEnrollmentProfiles
description: Propiedades de la lista y relaciones de los objetos depEnrollmentProfile.
author: tfitzmac
ms.openlocfilehash: 13347a0b662f9a8f662ce45f08f11ffbf27788e8
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321822"
---
# <a name="list-depenrollmentprofiles"></a><span data-ttu-id="41bca-103">Lista depEnrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="41bca-103">List depEnrollmentProfiles</span></span>

> <span data-ttu-id="41bca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="41bca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41bca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="41bca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="41bca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41bca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41bca-107">Propiedades de la lista y relaciones de los objetos [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="41bca-107">List properties and relationships of the [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="41bca-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="41bca-108">Prerequisites</span></span>
<span data-ttu-id="41bca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41bca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="41bca-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41bca-111">Permission type</span></span>|<span data-ttu-id="41bca-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41bca-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="41bca-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41bca-113">Delegated (work or school account)</span></span>|<span data-ttu-id="41bca-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="41bca-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="41bca-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41bca-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="41bca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41bca-116">Not supported.</span></span>|
|<span data-ttu-id="41bca-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41bca-117">Application</span></span>|<span data-ttu-id="41bca-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41bca-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="41bca-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41bca-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="41bca-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41bca-120">Request headers</span></span>
|<span data-ttu-id="41bca-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41bca-121">Header</span></span>|<span data-ttu-id="41bca-122">Valor</span><span class="sxs-lookup"><span data-stu-id="41bca-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="41bca-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="41bca-123">Authorization</span></span>|<span data-ttu-id="41bca-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="41bca-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="41bca-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="41bca-125">Accept</span></span>|<span data-ttu-id="41bca-126">application/json</span><span class="sxs-lookup"><span data-stu-id="41bca-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="41bca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41bca-127">Request body</span></span>
<span data-ttu-id="41bca-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="41bca-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="41bca-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41bca-129">Response</span></span>
<span data-ttu-id="41bca-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41bca-130">If successful, this method returns a `200 OK` response code and a collection of [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41bca-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41bca-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="41bca-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41bca-132">Request</span></span>
<span data-ttu-id="41bca-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41bca-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

### <a name="response"></a><span data-ttu-id="41bca-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41bca-134">Response</span></span>
<span data-ttu-id="41bca-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41bca-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1520

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.depEnrollmentProfile",
      "id": "3d4534f7-34f7-3d45-f734-453df734453d",
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
      "iTunesPairingMode": "allow",
      "profileRemovalDisabled": true,
      "managementCertificates": [
        {
          "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
          "thumbprint": "Thumbprint value",
          "certificate": "Certificate value"
        }
      ],
      "restoreBlocked": true,
      "restoreFromAndroidDisabled": true,
      "appleIdDisabled": true,
      "termsAndConditionsDisabled": true,
      "touchIdDisabled": true,
      "applePayDisabled": true,
      "zoomDisabled": true,
      "siriDisabled": true,
      "diagnosticsDisabled": true,
      "macOSRegistrationDisabled": true,
      "macOSFileVaultDisabled": true,
      "awaitDeviceConfiguredConfirmation": true,
      "sharedIPadMaximumUserCount": 10,
      "enableSharedIPad": true
    }
  ]
}
```





