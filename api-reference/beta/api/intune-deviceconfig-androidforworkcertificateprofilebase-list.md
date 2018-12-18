---
title: Lista androidForWorkCertificateProfileBases
description: Propiedades de la lista y relaciones de los objetos androidForWorkCertificateProfileBase.
author: tfitzmac
ms.openlocfilehash: 2a0bd2de1408ad6fa41bb8b1e7be9d691460ceb9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318161"
---
# <a name="list-androidforworkcertificateprofilebases"></a><span data-ttu-id="1b7c4-103">Lista androidForWorkCertificateProfileBases</span><span class="sxs-lookup"><span data-stu-id="1b7c4-103">List androidForWorkCertificateProfileBases</span></span>

> <span data-ttu-id="1b7c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1b7c4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1b7c4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1b7c4-107">Propiedades de la lista y relaciones de los objetos [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md) .</span><span class="sxs-lookup"><span data-stu-id="1b7c4-107">List properties and relationships of the [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1b7c4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1b7c4-108">Prerequisites</span></span>
<span data-ttu-id="1b7c4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1b7c4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1b7c4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1b7c4-111">Permission type</span></span>|<span data-ttu-id="1b7c4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1b7c4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1b7c4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1b7c4-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1b7c4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1b7c4-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1b7c4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1b7c4-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1b7c4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-116">Not supported.</span></span>|
|<span data-ttu-id="1b7c4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1b7c4-117">Application</span></span>|<span data-ttu-id="1b7c4-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1b7c4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1b7c4-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="1b7c4-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1b7c4-120">Request headers</span></span>
|<span data-ttu-id="1b7c4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b7c4-121">Header</span></span>|<span data-ttu-id="1b7c4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1b7c4-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1b7c4-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1b7c4-123">Authorization</span></span>|<span data-ttu-id="1b7c4-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1b7c4-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1b7c4-125">Accept</span></span>|<span data-ttu-id="1b7c4-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1b7c4-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1b7c4-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1b7c4-127">Request body</span></span>
<span data-ttu-id="1b7c4-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1b7c4-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b7c4-129">Response</span></span>
<span data-ttu-id="1b7c4-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-130">If successful, this method returns a `200 OK` response code and a collection of [androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1b7c4-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1b7c4-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1b7c4-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1b7c4-132">Request</span></span>
<span data-ttu-id="1b7c4-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="1b7c4-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1b7c4-134">Response</span></span>
<span data-ttu-id="1b7c4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1b7c4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 922

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidForWorkCertificateProfileBase",
      "id": "87f1d53b-d53b-87f1-3bd5-f1873bd5f187",
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
      ]
    }
  ]
}
```





