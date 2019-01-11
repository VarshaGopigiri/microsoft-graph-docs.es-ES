---
title: Obtener depEnrollmentProfile
description: Leer las propiedades y las relaciones del objeto depEnrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: aa3c9da25c4afa0b8ba4130f6cc7afb869aa33f0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878970"
---
# <a name="get-depenrollmentprofile"></a><span data-ttu-id="ba66f-103">Obtener depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="ba66f-103">Get depEnrollmentProfile</span></span>

> <span data-ttu-id="ba66f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ba66f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ba66f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ba66f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ba66f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ba66f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ba66f-107">Leer las propiedades y las relaciones del objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="ba66f-107">Read properties and relationships of the [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ba66f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ba66f-108">Prerequisites</span></span>
<span data-ttu-id="ba66f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba66f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba66f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba66f-111">Permission type</span></span>|<span data-ttu-id="ba66f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba66f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ba66f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba66f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ba66f-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="ba66f-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="ba66f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba66f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ba66f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba66f-116">Not supported.</span></span>|
|<span data-ttu-id="ba66f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba66f-117">Application</span></span>|<span data-ttu-id="ba66f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba66f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ba66f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba66f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ba66f-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ba66f-120">Optional query parameters</span></span>
<span data-ttu-id="ba66f-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba66f-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ba66f-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba66f-122">Request headers</span></span>
|<span data-ttu-id="ba66f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba66f-123">Header</span></span>|<span data-ttu-id="ba66f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ba66f-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ba66f-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="ba66f-125">Authorization</span></span>|<span data-ttu-id="ba66f-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ba66f-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ba66f-127">Accept</span><span class="sxs-lookup"><span data-stu-id="ba66f-127">Accept</span></span>|<span data-ttu-id="ba66f-128">application/json</span><span class="sxs-lookup"><span data-stu-id="ba66f-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ba66f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba66f-129">Request body</span></span>
<span data-ttu-id="ba66f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ba66f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ba66f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba66f-131">Response</span></span>
<span data-ttu-id="ba66f-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba66f-132">If successful, this method returns a `200 OK` response code and [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ba66f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba66f-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="ba66f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba66f-134">Request</span></span>
<span data-ttu-id="ba66f-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba66f-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}
```

### <a name="response"></a><span data-ttu-id="ba66f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba66f-136">Response</span></span>
<span data-ttu-id="ba66f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba66f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1432

{
  "value": {
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
}
```





