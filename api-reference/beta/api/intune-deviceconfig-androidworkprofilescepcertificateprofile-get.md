---
title: Obtener androidWorkProfileScepCertificateProfile
description: Leer las propiedades y las relaciones del objeto androidWorkProfileScepCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: af689ca6e1c9258be94439331ce8622367c03db9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916869"
---
# <a name="get-androidworkprofilescepcertificateprofile"></a><span data-ttu-id="63114-103">Obtener androidWorkProfileScepCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="63114-103">Get androidWorkProfileScepCertificateProfile</span></span>

> <span data-ttu-id="63114-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63114-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63114-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63114-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="63114-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63114-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63114-107">Leer las propiedades y las relaciones del objeto [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="63114-107">Read properties and relationships of the [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63114-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63114-108">Prerequisites</span></span>
<span data-ttu-id="63114-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="63114-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="63114-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63114-111">Permission type</span></span>|<span data-ttu-id="63114-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63114-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63114-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63114-113">Delegated (work or school account)</span></span>|<span data-ttu-id="63114-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="63114-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="63114-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63114-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63114-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63114-116">Not supported.</span></span>|
|<span data-ttu-id="63114-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63114-117">Application</span></span>|<span data-ttu-id="63114-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63114-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63114-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63114-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="63114-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="63114-120">Optional query parameters</span></span>
<span data-ttu-id="63114-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63114-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="63114-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63114-122">Request headers</span></span>
|<span data-ttu-id="63114-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63114-123">Header</span></span>|<span data-ttu-id="63114-124">Valor</span><span class="sxs-lookup"><span data-stu-id="63114-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63114-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="63114-125">Authorization</span></span>|<span data-ttu-id="63114-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63114-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="63114-127">Accept</span><span class="sxs-lookup"><span data-stu-id="63114-127">Accept</span></span>|<span data-ttu-id="63114-128">application/json</span><span class="sxs-lookup"><span data-stu-id="63114-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63114-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63114-129">Request body</span></span>
<span data-ttu-id="63114-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="63114-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="63114-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63114-131">Response</span></span>
<span data-ttu-id="63114-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63114-132">If successful, this method returns a `200 OK` response code and [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63114-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63114-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="63114-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63114-134">Request</span></span>
<span data-ttu-id="63114-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63114-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="63114-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63114-136">Response</span></span>
<span data-ttu-id="63114-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63114-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1478

{
  "value": {
    "@odata.type": "#microsoft.graph.androidWorkProfileScepCertificateProfile",
    "id": "6f494abf-4abf-6f49-bf4a-496fbf4a496f",
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
    "certificateValidityPeriodValue": 14,
    "certificateValidityPeriodScale": "months",
    "extendedKeyUsages": [
      {
        "@odata.type": "microsoft.graph.extendedKeyUsage",
        "name": "Name value",
        "objectIdentifier": "Object Identifier value"
      }
    ],
    "scepServerUrls": [
      "Scep Server Urls value"
    ],
    "subjectNameFormatString": "Subject Name Format String value",
    "keyUsage": "digitalSignature",
    "keySize": "size2048",
    "hashAlgorithm": "sha2",
    "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
    "certificateStore": "machine",
    "customSubjectAlternativeNames": [
      {
        "@odata.type": "microsoft.graph.customSubjectAlternativeName",
        "sanType": "emailAddress",
        "name": "Name value"
      }
    ],
    "subjectAlternativeNameType": "emailAddress"
  }
}
```





