---
title: Obtener androidCompliancePolicy
description: Lea las propiedades y las relaciones del objeto androidCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 86c6b8435e32f9dbc36da55e07d8880e5501a002
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932654"
---
# <a name="get-androidcompliancepolicy"></a><span data-ttu-id="65845-103">Obtener androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="65845-103">Get androidCompliancePolicy</span></span>

> <span data-ttu-id="65845-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="65845-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="65845-105">Lea las propiedades y las relaciones del objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="65845-105">Read properties and relationships of the [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="65845-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="65845-106">Prerequisites</span></span>
<span data-ttu-id="65845-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="65845-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="65845-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65845-109">Permission type</span></span>|<span data-ttu-id="65845-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65845-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="65845-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65845-111">Delegated (work or school account)</span></span>|<span data-ttu-id="65845-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="65845-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="65845-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65845-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="65845-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65845-114">Not supported.</span></span>|
|<span data-ttu-id="65845-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65845-115">Application</span></span>|<span data-ttu-id="65845-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="65845-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="65845-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65845-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="65845-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="65845-118">Optional query parameters</span></span>
<span data-ttu-id="65845-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65845-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="65845-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65845-120">Request headers</span></span>
|<span data-ttu-id="65845-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65845-121">Header</span></span>|<span data-ttu-id="65845-122">Valor</span><span class="sxs-lookup"><span data-stu-id="65845-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="65845-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="65845-123">Authorization</span></span>|<span data-ttu-id="65845-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="65845-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="65845-125">Accept</span><span class="sxs-lookup"><span data-stu-id="65845-125">Accept</span></span>|<span data-ttu-id="65845-126">application/json</span><span class="sxs-lookup"><span data-stu-id="65845-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="65845-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65845-127">Request body</span></span>
<span data-ttu-id="65845-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="65845-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="65845-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65845-129">Response</span></span>
<span data-ttu-id="65845-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="65845-130">If successful, this method returns a `200 OK` response code and [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="65845-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65845-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="65845-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65845-132">Request</span></span>
<span data-ttu-id="65845-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="65845-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="65845-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65845-134">Response</span></span>
<span data-ttu-id="65845-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="65845-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1406

{
  "value": {
    "@odata.type": "#microsoft.graph.androidCompliancePolicy",
    "id": "752c820f-820f-752c-0f82-2c750f822c75",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "version": 7,
    "passwordRequired": true,
    "passwordMinimumLength": 5,
    "passwordRequiredType": "alphabetic",
    "passwordMinutesOfInactivityBeforeLock": 5,
    "passwordExpirationDays": 6,
    "passwordPreviousPasswordBlockCount": 2,
    "securityPreventInstallAppsFromUnknownSources": true,
    "securityDisableUsbDebugging": true,
    "securityRequireVerifyApps": true,
    "deviceThreatProtectionEnabled": true,
    "deviceThreatProtectionRequiredSecurityLevel": "secured",
    "securityBlockJailbrokenDevices": true,
    "osMinimumVersion": "Os Minimum Version value",
    "osMaximumVersion": "Os Maximum Version value",
    "minAndroidSecurityPatchLevel": "Min Android Security Patch Level value",
    "storageRequireEncryption": true,
    "securityRequireSafetyNetAttestationBasicIntegrity": true,
    "securityRequireSafetyNetAttestationCertifiedDevice": true,
    "securityRequireGooglePlayServices": true,
    "securityRequireUpToDateSecurityProviders": true,
    "securityRequireCompanyPortalAppIntegrity": true
  }
}
```



