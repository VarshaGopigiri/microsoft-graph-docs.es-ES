---
title: Obtener androidCompliancePolicy
description: Lea las propiedades y las relaciones del objeto androidCompliancePolicy.
author: tfitzmac
ms.openlocfilehash: a3e9657e472a58a41e335321685c7a6cb7ac8bb9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354309"
---
# <a name="get-androidcompliancepolicy"></a><span data-ttu-id="43827-103">Obtener androidCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="43827-103">Get androidCompliancePolicy</span></span>

> <span data-ttu-id="43827-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="43827-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="43827-105">Lea las propiedades y las relaciones del objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="43827-105">Read properties and relationships of the [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="43827-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="43827-106">Prerequisites</span></span>
<span data-ttu-id="43827-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43827-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43827-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43827-109">Permission type</span></span>|<span data-ttu-id="43827-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43827-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="43827-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43827-111">Delegated (work or school account)</span></span>|<span data-ttu-id="43827-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="43827-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="43827-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43827-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="43827-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43827-114">Not supported.</span></span>|
|<span data-ttu-id="43827-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43827-115">Application</span></span>|<span data-ttu-id="43827-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43827-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="43827-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43827-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="43827-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="43827-118">Optional query parameters</span></span>
<span data-ttu-id="43827-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43827-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="43827-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43827-120">Request headers</span></span>
|<span data-ttu-id="43827-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43827-121">Header</span></span>|<span data-ttu-id="43827-122">Valor</span><span class="sxs-lookup"><span data-stu-id="43827-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="43827-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="43827-123">Authorization</span></span>|<span data-ttu-id="43827-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="43827-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="43827-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="43827-125">Accept</span></span>|<span data-ttu-id="43827-126">application/json</span><span class="sxs-lookup"><span data-stu-id="43827-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="43827-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43827-127">Request body</span></span>
<span data-ttu-id="43827-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="43827-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="43827-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43827-129">Response</span></span>
<span data-ttu-id="43827-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43827-130">If successful, this method returns a `200 OK` response code and [androidCompliancePolicy](../resources/intune-deviceconfig-androidcompliancepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="43827-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43827-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="43827-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43827-132">Request</span></span>
<span data-ttu-id="43827-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43827-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

### <a name="response"></a><span data-ttu-id="43827-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43827-134">Response</span></span>
<span data-ttu-id="43827-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="43827-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



