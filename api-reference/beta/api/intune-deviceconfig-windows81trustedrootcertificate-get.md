---
title: Obtener windows81TrustedRootCertificate
description: Leer las propiedades y las relaciones del objeto windows81TrustedRootCertificate.
ms.openlocfilehash: 17ad19e1c0cac90a268f63d67256dc34bfc6fd87
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082915"
---
# <a name="get-windows81trustedrootcertificate"></a><span data-ttu-id="1db0f-103">Obtener windows81TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1db0f-103">Get windows81TrustedRootCertificate</span></span>

> <span data-ttu-id="1db0f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1db0f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1db0f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1db0f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1db0f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1db0f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1db0f-107">Leer las propiedades y las relaciones del objeto [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="1db0f-107">Read properties and relationships of the [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1db0f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1db0f-108">Prerequisites</span></span>
<span data-ttu-id="1db0f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1db0f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1db0f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1db0f-111">Permission type</span></span>|<span data-ttu-id="1db0f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1db0f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1db0f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1db0f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1db0f-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1db0f-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1db0f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1db0f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1db0f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1db0f-116">Not supported.</span></span>|
|<span data-ttu-id="1db0f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1db0f-117">Application</span></span>|<span data-ttu-id="1db0f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1db0f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1db0f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1db0f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/microsoft.graph.windows81SCEPCertificateProfile/rootCertificate
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1db0f-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1db0f-120">Optional query parameters</span></span>
<span data-ttu-id="1db0f-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1db0f-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1db0f-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1db0f-122">Request headers</span></span>
|<span data-ttu-id="1db0f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1db0f-123">Header</span></span>|<span data-ttu-id="1db0f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1db0f-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1db0f-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="1db0f-125">Authorization</span></span>|<span data-ttu-id="1db0f-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1db0f-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1db0f-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1db0f-127">Accept</span></span>|<span data-ttu-id="1db0f-128">application/json</span><span class="sxs-lookup"><span data-stu-id="1db0f-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1db0f-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1db0f-129">Request body</span></span>
<span data-ttu-id="1db0f-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1db0f-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1db0f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1db0f-131">Response</span></span>
<span data-ttu-id="1db0f-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1db0f-132">If successful, this method returns a `200 OK` response code and [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1db0f-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1db0f-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="1db0f-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1db0f-134">Request</span></span>
<span data-ttu-id="1db0f-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1db0f-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}
```

### <a name="response"></a><span data-ttu-id="1db0f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1db0f-136">Response</span></span>
<span data-ttu-id="1db0f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1db0f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 644

{
  "value": {
    "@odata.type": "#microsoft.graph.windows81TrustedRootCertificate",
    "id": "3fb588f9-88f9-3fb5-f988-b53ff988b53f",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "trustedRootCertificate": "dHJ1c3RlZFJvb3RDZXJ0aWZpY2F0ZQ==",
    "certFileName": "Cert File Name value",
    "destinationStore": "computerCertStoreIntermediate"
  }
}
```




