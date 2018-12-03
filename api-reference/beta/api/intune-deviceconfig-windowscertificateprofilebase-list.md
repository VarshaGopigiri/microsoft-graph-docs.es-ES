---
title: Lista windowsCertificateProfileBases
description: Propiedades de la lista y relaciones de los objetos windowsCertificateProfileBase.
ms.openlocfilehash: 5540502610af7a3f97ef54acbc2bd784efa41ff8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090314"
---
# <a name="list-windowscertificateprofilebases"></a><span data-ttu-id="1d416-103">Lista windowsCertificateProfileBases</span><span class="sxs-lookup"><span data-stu-id="1d416-103">List windowsCertificateProfileBases</span></span>

> <span data-ttu-id="1d416-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1d416-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1d416-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1d416-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1d416-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d416-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d416-107">Propiedades de la lista y relaciones de los objetos [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md) .</span><span class="sxs-lookup"><span data-stu-id="1d416-107">List properties and relationships of the [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d416-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d416-108">Prerequisites</span></span>
<span data-ttu-id="1d416-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d416-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d416-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d416-111">Permission type</span></span>|<span data-ttu-id="1d416-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d416-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d416-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d416-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1d416-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1d416-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1d416-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d416-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d416-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d416-116">Not supported.</span></span>|
|<span data-ttu-id="1d416-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d416-117">Application</span></span>|<span data-ttu-id="1d416-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d416-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d416-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d416-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="1d416-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d416-120">Request headers</span></span>
|<span data-ttu-id="1d416-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d416-121">Header</span></span>|<span data-ttu-id="1d416-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1d416-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d416-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d416-123">Authorization</span></span>|<span data-ttu-id="1d416-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d416-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d416-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1d416-125">Accept</span></span>|<span data-ttu-id="1d416-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1d416-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d416-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d416-127">Request body</span></span>
<span data-ttu-id="1d416-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1d416-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1d416-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d416-129">Response</span></span>
<span data-ttu-id="1d416-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d416-130">If successful, this method returns a `200 OK` response code and a collection of [windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d416-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d416-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d416-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d416-132">Request</span></span>
<span data-ttu-id="1d416-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d416-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="1d416-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d416-134">Response</span></span>
<span data-ttu-id="1d416-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d416-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 809

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsCertificateProfileBase",
      "id": "c0979ce1-9ce1-c097-e19c-97c0e19c97c0",
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
      "keyStorageProvider": "useTpmKspOtherwiseFail",
      "subjectNameFormat": "commonNameIncludingEmail",
      "subjectAlternativeNameType": "emailAddress",
      "certificateValidityPeriodValue": 14,
      "certificateValidityPeriodScale": "months"
    }
  ]
}
```




