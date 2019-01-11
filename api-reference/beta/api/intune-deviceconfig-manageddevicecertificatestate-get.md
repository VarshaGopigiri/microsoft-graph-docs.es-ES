---
title: Obtener managedDeviceCertificateState
description: Leer las propiedades y las relaciones del objeto managedDeviceCertificateState.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0ae84915623f17d5b79e933028e57459e5e5addf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822690"
---
# <a name="get-manageddevicecertificatestate"></a><span data-ttu-id="a3998-103">Obtener managedDeviceCertificateState</span><span class="sxs-lookup"><span data-stu-id="a3998-103">Get managedDeviceCertificateState</span></span>

> <span data-ttu-id="a3998-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a3998-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a3998-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a3998-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a3998-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a3998-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a3998-107">Leer las propiedades y las relaciones del objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="a3998-107">Read properties and relationships of the [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a3998-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a3998-108">Prerequisites</span></span>
<span data-ttu-id="a3998-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a3998-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a3998-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a3998-111">Permission type</span></span>|<span data-ttu-id="a3998-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a3998-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a3998-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a3998-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a3998-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a3998-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a3998-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a3998-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a3998-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3998-116">Not supported.</span></span>|
|<span data-ttu-id="a3998-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a3998-117">Application</span></span>|<span data-ttu-id="a3998-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a3998-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a3998-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a3998-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidWorkProfileScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidForWorkImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkScepCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/microsoft.graph.windowsPhone81SCEPCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10PkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows81SCEPCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10ImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windowsPhone81ImportedPFXCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a3998-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a3998-120">Optional query parameters</span></span>
<span data-ttu-id="a3998-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3998-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a3998-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a3998-122">Request headers</span></span>
|<span data-ttu-id="a3998-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3998-123">Header</span></span>|<span data-ttu-id="a3998-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a3998-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a3998-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="a3998-125">Authorization</span></span>|<span data-ttu-id="a3998-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a3998-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a3998-127">Accept</span><span class="sxs-lookup"><span data-stu-id="a3998-127">Accept</span></span>|<span data-ttu-id="a3998-128">application/json</span><span class="sxs-lookup"><span data-stu-id="a3998-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a3998-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a3998-129">Request body</span></span>
<span data-ttu-id="a3998-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a3998-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a3998-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3998-131">Response</span></span>
<span data-ttu-id="a3998-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3998-132">If successful, this method returns a `200 OK` response code and [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a3998-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3998-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="a3998-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a3998-134">Request</span></span>
<span data-ttu-id="a3998-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3998-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates/{managedDeviceCertificateStateId}
```

### <a name="response"></a><span data-ttu-id="a3998-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a3998-136">Response</span></span>
<span data-ttu-id="a3998-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a3998-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1637

{
  "value": {
    "@odata.type": "#microsoft.graph.managedDeviceCertificateState",
    "id": "d99bc884-c884-d99b-84c8-9bd984c89bd9",
    "devicePlatform": "androidForWork",
    "certificateKeyUsage": "digitalSignature",
    "certificateValidityPeriodUnits": "months",
    "certificateIssuanceState": "challengeIssued",
    "certificateKeyStorageProvider": "useTpmKspOtherwiseFail",
    "certificateSubjectNameFormat": "commonNameIncludingEmail",
    "certificateSubjectAlternativeNameFormat": "emailAddress",
    "certificateRevokeStatus": "pending",
    "certificateProfileDisplayName": "Certificate Profile Display Name value",
    "deviceDisplayName": "Device Display Name value",
    "userDisplayName": "User Display Name value",
    "certificateExpirationDateTime": "2017-01-01T00:02:14.9489247-08:00",
    "certificateLastIssuanceStateChangedDateTime": "2017-01-01T00:00:27.7468732-08:00",
    "lastCertificateStateChangeDateTime": "2017-01-01T00:01:10.7144639-08:00",
    "certificateIssuer": "Certificate Issuer value",
    "certificateThumbprint": "Certificate Thumbprint value",
    "certificateSerialNumber": "Certificate Serial Number value",
    "certificateKeyLength": 4,
    "certificateEnhancedKeyUsage": "Certificate Enhanced Key Usage value",
    "certificateValidityPeriod": 9,
    "certificateSubjectNameFormatString": "Certificate Subject Name Format String value",
    "certificateSubjectAlternativeNameFormatString": "Certificate Subject Alternative Name Format String value",
    "certificateIssuanceDateTime": "2016-12-31T23:59:41.5044473-08:00",
    "certificateErrorCode": 4
  }
}
```





