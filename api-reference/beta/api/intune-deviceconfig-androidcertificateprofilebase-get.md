---
title: Obtener androidCertificateProfileBase
description: Leer las propiedades y las relaciones del objeto androidCertificateProfileBase.
author: tfitzmac
ms.openlocfilehash: c2b0ef9f1dd5e4dd608b0fb7042af86d68ed2c4c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340183"
---
# <a name="get-androidcertificateprofilebase"></a><span data-ttu-id="d1815-103">Obtener androidCertificateProfileBase</span><span class="sxs-lookup"><span data-stu-id="d1815-103">Get androidCertificateProfileBase</span></span>

> <span data-ttu-id="d1815-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1815-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1815-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1815-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d1815-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d1815-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d1815-107">Leer las propiedades y las relaciones del objeto [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md) .</span><span class="sxs-lookup"><span data-stu-id="d1815-107">Read properties and relationships of the [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d1815-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d1815-108">Prerequisites</span></span>
<span data-ttu-id="d1815-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d1815-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d1815-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d1815-111">Permission type</span></span>|<span data-ttu-id="d1815-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d1815-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d1815-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d1815-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d1815-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="d1815-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="d1815-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d1815-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d1815-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1815-116">Not supported.</span></span>|
|<span data-ttu-id="d1815-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d1815-117">Application</span></span>|<span data-ttu-id="d1815-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1815-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d1815-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d1815-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidVpnConfiguration/identityCertificate
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidEasEmailProfileConfiguration/identityCertificate
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidEasEmailProfileConfiguration/smimeSigningCertificate
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidEnterpriseWiFiConfiguration/identityCertificateForClientAuthentication
```

## <a name="optional-query-parameters"></a><span data-ttu-id="d1815-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="d1815-120">Optional query parameters</span></span>
<span data-ttu-id="d1815-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d1815-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="d1815-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d1815-122">Request headers</span></span>
|<span data-ttu-id="d1815-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1815-123">Header</span></span>|<span data-ttu-id="d1815-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d1815-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d1815-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="d1815-125">Authorization</span></span>|<span data-ttu-id="d1815-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d1815-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d1815-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d1815-127">Accept</span></span>|<span data-ttu-id="d1815-128">application/json</span><span class="sxs-lookup"><span data-stu-id="d1815-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d1815-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d1815-129">Request body</span></span>
<span data-ttu-id="d1815-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d1815-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d1815-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1815-131">Response</span></span>
<span data-ttu-id="d1815-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d1815-132">If successful, this method returns a `200 OK` response code and [androidCertificateProfileBase](../resources/intune-deviceconfig-androidcertificateprofilebase.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d1815-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1815-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="d1815-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d1815-134">Request</span></span>
<span data-ttu-id="d1815-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1815-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidVpnConfiguration/identityCertificate
```

### <a name="response"></a><span data-ttu-id="d1815-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1815-136">Response</span></span>
<span data-ttu-id="d1815-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d1815-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 908

{
  "value": {
    "@odata.type": "#microsoft.graph.androidCertificateProfileBase",
    "id": "76cf241d-241d-76cf-1d24-cf761d24cf76",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "renewalThresholdPercentage": 10,
    "subjectNameFormat": "commonNameIncludingEmail",
    "subjectAlternativeNameType": "emailAddress",
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months",
    "extendedKeyUsages": [
      {
        "@odata.type": "microsoft.graph.extendedKeyUsage",
        "name": "Name value",
        "objectIdentifier": "Object Identifier value"
      }
    ]
  }
}
```





