---
title: Lista androidWorkProfileCompliancePolicies
description: Propiedades de la lista y relaciones de los objetos androidWorkProfileCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 43b4959d3d32535d9e8e22dd9ea5a3dc07a0ca1f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856752"
---
# <a name="list-androidworkprofilecompliancepolicies"></a><span data-ttu-id="b3578-103">Lista androidWorkProfileCompliancePolicies</span><span class="sxs-lookup"><span data-stu-id="b3578-103">List androidWorkProfileCompliancePolicies</span></span>

> <span data-ttu-id="b3578-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3578-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3578-105">Propiedades de la lista y relaciones de los objetos [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="b3578-105">List properties and relationships of the [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b3578-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b3578-106">Prerequisites</span></span>
<span data-ttu-id="b3578-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3578-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b3578-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3578-109">Permission type</span></span>|<span data-ttu-id="b3578-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3578-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b3578-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3578-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b3578-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b3578-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b3578-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3578-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b3578-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3578-114">Not supported.</span></span>|
|<span data-ttu-id="b3578-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3578-115">Application</span></span>|<span data-ttu-id="b3578-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3578-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b3578-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3578-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies
```

## <a name="request-headers"></a><span data-ttu-id="b3578-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3578-118">Request headers</span></span>
|<span data-ttu-id="b3578-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3578-119">Header</span></span>|<span data-ttu-id="b3578-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b3578-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b3578-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b3578-121">Authorization</span></span>|<span data-ttu-id="b3578-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b3578-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b3578-123">Accept</span><span class="sxs-lookup"><span data-stu-id="b3578-123">Accept</span></span>|<span data-ttu-id="b3578-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b3578-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b3578-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3578-125">Request body</span></span>
<span data-ttu-id="b3578-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b3578-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b3578-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3578-127">Response</span></span>
<span data-ttu-id="b3578-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3578-128">If successful, this method returns a `200 OK` response code and a collection of [androidWorkProfileCompliancePolicy](../resources/intune-deviceconfig-androidworkprofilecompliancepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3578-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3578-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b3578-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3578-130">Request</span></span>
<span data-ttu-id="b3578-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3578-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies
```

### <a name="response"></a><span data-ttu-id="b3578-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3578-132">Response</span></span>
<span data-ttu-id="b3578-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b3578-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1487

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidWorkProfileCompliancePolicy",
      "id": "4e385271-5271-4e38-7152-384e7152384e",
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
  ]
}
```



