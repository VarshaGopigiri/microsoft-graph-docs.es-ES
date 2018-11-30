---
title: Obtener androidForWorkTrustedRootCertificate
description: Leer las propiedades y las relaciones del objeto androidForWorkTrustedRootCertificate.
ms.openlocfilehash: ae3db38cea96c2e895b32d03df7f4f2e5cbde6c5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086906"
---
# <a name="get-androidforworktrustedrootcertificate"></a><span data-ttu-id="ea0be-103">Obtener androidForWorkTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ea0be-103">Get androidForWorkTrustedRootCertificate</span></span>

> <span data-ttu-id="ea0be-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea0be-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea0be-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea0be-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ea0be-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea0be-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea0be-107">Leer las propiedades y las relaciones del objeto [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="ea0be-107">Read properties and relationships of the [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea0be-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea0be-108">Prerequisites</span></span>
<span data-ttu-id="ea0be-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea0be-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea0be-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea0be-111">Permission type</span></span>|<span data-ttu-id="ea0be-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea0be-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea0be-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea0be-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ea0be-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="ea0be-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="ea0be-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea0be-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea0be-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea0be-116">Not supported.</span></span>|
|<span data-ttu-id="ea0be-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea0be-117">Application</span></span>|<span data-ttu-id="ea0be-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea0be-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea0be-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea0be-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.androidForWorkEnterpriseWiFiConfiguration/rootCertificateForServerValidation
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ea0be-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ea0be-120">Optional query parameters</span></span>
<span data-ttu-id="ea0be-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea0be-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ea0be-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea0be-122">Request headers</span></span>
|<span data-ttu-id="ea0be-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea0be-123">Header</span></span>|<span data-ttu-id="ea0be-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0be-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea0be-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea0be-125">Authorization</span></span>|<span data-ttu-id="ea0be-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea0be-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea0be-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ea0be-127">Accept</span></span>|<span data-ttu-id="ea0be-128">application/json</span><span class="sxs-lookup"><span data-stu-id="ea0be-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea0be-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea0be-129">Request body</span></span>
<span data-ttu-id="ea0be-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ea0be-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea0be-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea0be-131">Response</span></span>
<span data-ttu-id="ea0be-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea0be-132">If successful, this method returns a `200 OK` response code and [androidForWorkTrustedRootCertificate](../resources/intune-deviceconfig-androidforworktrustedrootcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea0be-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea0be-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea0be-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea0be-134">Request</span></span>
<span data-ttu-id="ea0be-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea0be-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate
```

### <a name="response"></a><span data-ttu-id="ea0be-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea0be-136">Response</span></span>
<span data-ttu-id="ea0be-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea0be-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 591

{
  "value": {
    "@odata.type": "#microsoft.graph.androidForWorkTrustedRootCertificate",
    "id": "2f78834c-834c-2f78-4c83-782f4c83782f",
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
    "certFileName": "Cert File Name value"
  }
}
```





