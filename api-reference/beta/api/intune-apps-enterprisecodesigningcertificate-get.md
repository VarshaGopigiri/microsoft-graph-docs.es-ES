---
title: Obtener enterpriseCodeSigningCertificate
description: Leer las propiedades y las relaciones del objeto enterpriseCodeSigningCertificate.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 35e919fbce3c02748eb17c722d910fe717200140
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990505"
---
# <a name="get-enterprisecodesigningcertificate"></a><span data-ttu-id="77314-103">Obtener enterpriseCodeSigningCertificate</span><span class="sxs-lookup"><span data-stu-id="77314-103">Get enterpriseCodeSigningCertificate</span></span>

> <span data-ttu-id="77314-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77314-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77314-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77314-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="77314-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="77314-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="77314-107">Leer las propiedades y las relaciones del objeto [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="77314-107">Read properties and relationships of the [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="77314-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="77314-108">Prerequisites</span></span>
<span data-ttu-id="77314-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77314-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="77314-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77314-111">Permission type</span></span>|<span data-ttu-id="77314-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77314-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="77314-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77314-113">Delegated (work or school account)</span></span>|<span data-ttu-id="77314-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="77314-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="77314-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77314-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="77314-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77314-116">Not supported.</span></span>|
|<span data-ttu-id="77314-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77314-117">Application</span></span>|<span data-ttu-id="77314-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77314-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="77314-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77314-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/enterpriseCodeSigningCertificates/{enterpriseCodeSigningCertificateId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="77314-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="77314-120">Optional query parameters</span></span>
<span data-ttu-id="77314-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77314-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="77314-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77314-122">Request headers</span></span>
|<span data-ttu-id="77314-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77314-123">Header</span></span>|<span data-ttu-id="77314-124">Valor</span><span class="sxs-lookup"><span data-stu-id="77314-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="77314-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="77314-125">Authorization</span></span>|<span data-ttu-id="77314-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="77314-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="77314-127">Accept</span><span class="sxs-lookup"><span data-stu-id="77314-127">Accept</span></span>|<span data-ttu-id="77314-128">application/json</span><span class="sxs-lookup"><span data-stu-id="77314-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="77314-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="77314-129">Request body</span></span>
<span data-ttu-id="77314-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="77314-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="77314-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77314-131">Response</span></span>
<span data-ttu-id="77314-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77314-132">If successful, this method returns a `200 OK` response code and [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77314-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77314-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="77314-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77314-134">Request</span></span>
<span data-ttu-id="77314-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77314-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/enterpriseCodeSigningCertificates/{enterpriseCodeSigningCertificateId}
```

### <a name="response"></a><span data-ttu-id="77314-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77314-136">Response</span></span>
<span data-ttu-id="77314-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77314-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 478

{
  "value": {
    "@odata.type": "#microsoft.graph.enterpriseCodeSigningCertificate",
    "id": "b20d3703-3703-b20d-0337-0db203370db2",
    "content": "Y29udGVudA==",
    "status": "provisioned",
    "subjectName": "Subject Name value",
    "subject": "Subject value",
    "issuerName": "Issuer Name value",
    "issuer": "Issuer value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "uploadDateTime": "2016-12-31T23:58:46.5747426-08:00"
  }
}
```





