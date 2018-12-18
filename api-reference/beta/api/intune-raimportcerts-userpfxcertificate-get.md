---
title: Obtener userPFXCertificate
description: Leer las propiedades y las relaciones del objeto userPFXCertificate.
author: tfitzmac
ms.openlocfilehash: 19dd8ac9216585857524419d3da03a7f9784adb5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304498"
---
# <a name="get-userpfxcertificate"></a><span data-ttu-id="4984c-103">Obtener userPFXCertificate</span><span class="sxs-lookup"><span data-stu-id="4984c-103">Get userPFXCertificate</span></span>

> <span data-ttu-id="4984c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4984c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4984c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4984c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4984c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4984c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4984c-107">Leer las propiedades y las relaciones del objeto [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4984c-107">Read properties and relationships of the [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4984c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4984c-108">Prerequisites</span></span>
<span data-ttu-id="4984c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4984c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4984c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4984c-111">Permission type</span></span>|<span data-ttu-id="4984c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4984c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4984c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4984c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4984c-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="4984c-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="4984c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4984c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4984c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4984c-116">Not supported.</span></span>|
|<span data-ttu-id="4984c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4984c-117">Application</span></span>|<span data-ttu-id="4984c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4984c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4984c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4984c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/userPfxCertificates/{userPFXCertificateId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="4984c-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4984c-120">Optional query parameters</span></span>
<span data-ttu-id="4984c-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4984c-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="4984c-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4984c-122">Request headers</span></span>
|<span data-ttu-id="4984c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4984c-123">Header</span></span>|<span data-ttu-id="4984c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4984c-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4984c-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="4984c-125">Authorization</span></span>|<span data-ttu-id="4984c-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4984c-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4984c-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4984c-127">Accept</span></span>|<span data-ttu-id="4984c-128">application/json</span><span class="sxs-lookup"><span data-stu-id="4984c-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4984c-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4984c-129">Request body</span></span>
<span data-ttu-id="4984c-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4984c-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4984c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4984c-131">Response</span></span>
<span data-ttu-id="4984c-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4984c-132">If successful, this method returns a `200 OK` response code and [userPFXCertificate](../resources/intune-raimportcerts-userpfxcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4984c-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4984c-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="4984c-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4984c-134">Request</span></span>
<span data-ttu-id="4984c-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4984c-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/userPfxCertificates/{userPFXCertificateId}
```

### <a name="response"></a><span data-ttu-id="4984c-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4984c-136">Response</span></span>
<span data-ttu-id="4984c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4984c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 742

{
  "value": {
    "@odata.type": "#microsoft.graph.userPFXCertificate",
    "id": "045c159b-159b-045c-9b15-5c049b155c04",
    "thumbprint": "Thumbprint value",
    "intendedPurpose": "smimeEncryption",
    "userPrincipalName": "User Principal Name value",
    "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "providerName": "Provider Name value",
    "keyName": "Key Name value",
    "paddingScheme": "pkcs1",
    "encryptedPfxBlob": "ZW5jcnlwdGVkUGZ4QmxvYg==",
    "encryptedPfxPassword": "Encrypted Pfx Password value",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
  }
}
```





