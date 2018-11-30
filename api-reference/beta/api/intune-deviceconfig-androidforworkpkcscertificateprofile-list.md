---
title: Lista androidForWorkPkcsCertificateProfiles
description: Propiedades de la lista y relaciones de los objetos androidForWorkPkcsCertificateProfile.
ms.openlocfilehash: 44abac7cdb9cc453e901b9365b55c736f7041c6f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089983"
---
# <a name="list-androidforworkpkcscertificateprofiles"></a><span data-ttu-id="f2d77-103">Lista androidForWorkPkcsCertificateProfiles</span><span class="sxs-lookup"><span data-stu-id="f2d77-103">List androidForWorkPkcsCertificateProfiles</span></span>

> <span data-ttu-id="f2d77-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f2d77-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f2d77-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f2d77-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f2d77-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f2d77-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f2d77-107">Propiedades de la lista y relaciones de los objetos [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f2d77-107">List properties and relationships of the [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f2d77-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2d77-108">Prerequisites</span></span>
<span data-ttu-id="f2d77-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f2d77-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f2d77-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f2d77-111">Permission type</span></span>|<span data-ttu-id="f2d77-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f2d77-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f2d77-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f2d77-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f2d77-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f2d77-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f2d77-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f2d77-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f2d77-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2d77-116">Not supported.</span></span>|
|<span data-ttu-id="f2d77-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f2d77-117">Application</span></span>|<span data-ttu-id="f2d77-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2d77-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f2d77-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2d77-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="f2d77-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2d77-120">Request headers</span></span>
|<span data-ttu-id="f2d77-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2d77-121">Header</span></span>|<span data-ttu-id="f2d77-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f2d77-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f2d77-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f2d77-123">Authorization</span></span>|<span data-ttu-id="f2d77-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f2d77-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f2d77-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f2d77-125">Accept</span></span>|<span data-ttu-id="f2d77-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f2d77-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f2d77-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2d77-127">Request body</span></span>
<span data-ttu-id="f2d77-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f2d77-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f2d77-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2d77-129">Response</span></span>
<span data-ttu-id="f2d77-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2d77-130">If successful, this method returns a `200 OK` response code and a collection of [androidForWorkPkcsCertificateProfile](../resources/intune-deviceconfig-androidforworkpkcscertificateprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f2d77-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2d77-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f2d77-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2d77-132">Request</span></span>
<span data-ttu-id="f2d77-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2d77-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="f2d77-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2d77-134">Response</span></span>
<span data-ttu-id="f2d77-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f2d77-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1278

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidForWorkPkcsCertificateProfile",
      "id": "0a2d7691-7691-0a2d-9176-2d0a91762d0a",
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
      "certificationAuthority": "Certification Authority value",
      "certificationAuthorityName": "Certification Authority Name value",
      "certificateTemplateName": "Certificate Template Name value",
      "subjectAlternativeNameFormatString": "Subject Alternative Name Format String value",
      "subjectAlternativeNameType": "emailAddress"
    }
  ]
}
```





