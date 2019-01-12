---
title: Lista androidWorkProfileScepCertificateProfiles
description: Propiedades de la lista y relaciones de los objetos androidWorkProfileScepCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4f5bf49e5eb2930a14c8d0974e2717d285612a91
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958281"
---
# <a name="list-androidworkprofilescepcertificateprofiles"></a><span data-ttu-id="a0613-103">Lista androidWorkProfileScepCertificateProfiles</span><span class="sxs-lookup"><span data-stu-id="a0613-103">List androidWorkProfileScepCertificateProfiles</span></span>

> <span data-ttu-id="a0613-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a0613-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a0613-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a0613-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a0613-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a0613-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a0613-107">Propiedades de la lista y relaciones de los objetos [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a0613-107">List properties and relationships of the [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a0613-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a0613-108">Prerequisites</span></span>
<span data-ttu-id="a0613-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0613-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0613-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0613-111">Permission type</span></span>|<span data-ttu-id="a0613-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0613-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a0613-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0613-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a0613-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a0613-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a0613-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0613-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a0613-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0613-116">Not supported.</span></span>|
|<span data-ttu-id="a0613-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0613-117">Application</span></span>|<span data-ttu-id="a0613-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0613-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a0613-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0613-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a0613-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0613-120">Request headers</span></span>
|<span data-ttu-id="a0613-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0613-121">Header</span></span>|<span data-ttu-id="a0613-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a0613-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a0613-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a0613-123">Authorization</span></span>|<span data-ttu-id="a0613-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a0613-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a0613-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a0613-125">Accept</span></span>|<span data-ttu-id="a0613-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a0613-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a0613-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0613-127">Request body</span></span>
<span data-ttu-id="a0613-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a0613-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a0613-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0613-129">Response</span></span>
<span data-ttu-id="a0613-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0613-130">If successful, this method returns a `200 OK` response code and a collection of [androidWorkProfileScepCertificateProfile](../resources/intune-deviceconfig-androidworkprofilescepcertificateprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a0613-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0613-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="a0613-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0613-132">Request</span></span>
<span data-ttu-id="a0613-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0613-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="a0613-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0613-134">Response</span></span>
<span data-ttu-id="a0613-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0613-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1570

{
  "value": [
    {
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
  ]
}
```





