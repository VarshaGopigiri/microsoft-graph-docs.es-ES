---
title: Lista managedDeviceCertificateStates
description: Propiedades de la lista y relaciones de los objetos managedDeviceCertificateState.
author: tfitzmac
ms.openlocfilehash: 7e5ac9bde17c20fe0a9aab2d5d88149a8c578cef
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308235"
---
# <a name="list-manageddevicecertificatestates"></a><span data-ttu-id="b29ec-103">Lista managedDeviceCertificateStates</span><span class="sxs-lookup"><span data-stu-id="b29ec-103">List managedDeviceCertificateStates</span></span>

> <span data-ttu-id="b29ec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b29ec-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b29ec-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b29ec-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b29ec-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b29ec-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b29ec-107">Propiedades de la lista y relaciones de los objetos [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="b29ec-107">List properties and relationships of the [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b29ec-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b29ec-108">Prerequisites</span></span>
<span data-ttu-id="b29ec-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b29ec-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b29ec-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b29ec-111">Permission type</span></span>|<span data-ttu-id="b29ec-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b29ec-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b29ec-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b29ec-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b29ec-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b29ec-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b29ec-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b29ec-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b29ec-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b29ec-116">Not supported.</span></span>|
|<span data-ttu-id="b29ec-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b29ec-117">Application</span></span>|<span data-ttu-id="b29ec-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b29ec-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b29ec-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b29ec-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidPkcsCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidScepCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosImportedPFXCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSImportedPFXCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidImportedPFXCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidWorkProfileScepCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidForWorkImportedPFXCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkPkcsCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/microsoft.graph.androidForWorkScepCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/microsoft.graph.windowsPhone81SCEPCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10PkcsCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows81SCEPCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows10ImportedPFXCertificateProfile/managedDeviceCertificateStates
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windowsPhone81ImportedPFXCertificateProfile/managedDeviceCertificateStates
```

## <a name="request-headers"></a><span data-ttu-id="b29ec-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b29ec-120">Request headers</span></span>
|<span data-ttu-id="b29ec-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b29ec-121">Header</span></span>|<span data-ttu-id="b29ec-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b29ec-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b29ec-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b29ec-123">Authorization</span></span>|<span data-ttu-id="b29ec-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b29ec-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b29ec-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b29ec-125">Accept</span></span>|<span data-ttu-id="b29ec-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b29ec-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b29ec-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b29ec-127">Request body</span></span>
<span data-ttu-id="b29ec-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b29ec-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b29ec-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29ec-129">Response</span></span>
<span data-ttu-id="b29ec-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b29ec-130">If successful, this method returns a `200 OK` response code and a collection of [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b29ec-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b29ec-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="b29ec-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b29ec-132">Request</span></span>
<span data-ttu-id="b29ec-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b29ec-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosPkcsCertificateProfile/managedDeviceCertificateStates
```

### <a name="response"></a><span data-ttu-id="b29ec-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29ec-134">Response</span></span>
<span data-ttu-id="b29ec-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b29ec-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1703

{
  "value": [
    {
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
  ]
}
```





