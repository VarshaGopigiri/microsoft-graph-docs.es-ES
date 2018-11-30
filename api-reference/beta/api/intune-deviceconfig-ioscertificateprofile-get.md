---
title: Obtener iosCertificateProfile
description: Lea las propiedades y las relaciones del objeto iosCertificateProfile.
ms.openlocfilehash: c4ea3241dc5c49bc54490651831c5cc0b068670c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089751"
---
# <a name="get-ioscertificateprofile"></a><span data-ttu-id="8cdb8-103">Obtener iosCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="8cdb8-103">Get iosCertificateProfile</span></span>

> <span data-ttu-id="8cdb8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8cdb8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8cdb8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8cdb8-107">Lea las propiedades y las relaciones del objeto [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="8cdb8-107">Read properties and relationships of the [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8cdb8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8cdb8-108">Prerequisites</span></span>
<span data-ttu-id="8cdb8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8cdb8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8cdb8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8cdb8-111">Permission type</span></span>|<span data-ttu-id="8cdb8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8cdb8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8cdb8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8cdb8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8cdb8-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="8cdb8-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="8cdb8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8cdb8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8cdb8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-116">Not supported.</span></span>|
|<span data-ttu-id="8cdb8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8cdb8-117">Application</span></span>|<span data-ttu-id="8cdb8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8cdb8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8cdb8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosEasEmailProfileConfiguration/smimeSigningCertificate
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosEasEmailProfileConfiguration/smimeEncryptionCertificate
```

## <a name="optional-query-parameters"></a><span data-ttu-id="8cdb8-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8cdb8-120">Optional query parameters</span></span>
<span data-ttu-id="8cdb8-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="8cdb8-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8cdb8-122">Request headers</span></span>
|<span data-ttu-id="8cdb8-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cdb8-123">Header</span></span>|<span data-ttu-id="8cdb8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8cdb8-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8cdb8-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="8cdb8-125">Authorization</span></span>|<span data-ttu-id="8cdb8-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8cdb8-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8cdb8-127">Accept</span></span>|<span data-ttu-id="8cdb8-128">application/json</span><span class="sxs-lookup"><span data-stu-id="8cdb8-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8cdb8-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8cdb8-129">Request body</span></span>
<span data-ttu-id="8cdb8-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8cdb8-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8cdb8-131">Response</span></span>
<span data-ttu-id="8cdb8-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-132">If successful, this method returns a `200 OK` response code and [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8cdb8-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8cdb8-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="8cdb8-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8cdb8-134">Request</span></span>
<span data-ttu-id="8cdb8-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosEasEmailProfileConfiguration/smimeSigningCertificate
```

### <a name="response"></a><span data-ttu-id="8cdb8-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8cdb8-136">Response</span></span>
<span data-ttu-id="8cdb8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8cdb8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 464

{
  "value": {
    "@odata.type": "#microsoft.graph.iosCertificateProfile",
    "id": "0ea4f39a-f39a-0ea4-9af3-a40e9af3a40e",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7
  }
}
```





