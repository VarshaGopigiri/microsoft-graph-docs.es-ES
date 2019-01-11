---
title: Lista enterpriseCodeSigningCertificates
description: Propiedades de la lista y relaciones de los objetos enterpriseCodeSigningCertificate.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 648b58e12ebd314366ff171ee5a4304b8aac59bc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27824439"
---
# <a name="list-enterprisecodesigningcertificates"></a><span data-ttu-id="eb6a9-103">Lista enterpriseCodeSigningCertificates</span><span class="sxs-lookup"><span data-stu-id="eb6a9-103">List enterpriseCodeSigningCertificates</span></span>

> <span data-ttu-id="eb6a9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb6a9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eb6a9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb6a9-107">Propiedades de la lista y relaciones de los objetos [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6a9-107">List properties and relationships of the [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eb6a9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eb6a9-108">Prerequisites</span></span>
<span data-ttu-id="eb6a9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb6a9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb6a9-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb6a9-111">Permission type</span></span>|<span data-ttu-id="eb6a9-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb6a9-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eb6a9-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb6a9-113">Delegated (work or school account)</span></span>|<span data-ttu-id="eb6a9-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="eb6a9-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="eb6a9-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb6a9-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eb6a9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-116">Not supported.</span></span>|
|<span data-ttu-id="eb6a9-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb6a9-117">Application</span></span>|<span data-ttu-id="eb6a9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eb6a9-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb6a9-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/enterpriseCodeSigningCertificates
```

## <a name="request-headers"></a><span data-ttu-id="eb6a9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb6a9-120">Request headers</span></span>
|<span data-ttu-id="eb6a9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb6a9-121">Header</span></span>|<span data-ttu-id="eb6a9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eb6a9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eb6a9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="eb6a9-123">Authorization</span></span>|<span data-ttu-id="eb6a9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eb6a9-125">Accept</span><span class="sxs-lookup"><span data-stu-id="eb6a9-125">Accept</span></span>|<span data-ttu-id="eb6a9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="eb6a9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eb6a9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb6a9-127">Request body</span></span>
<span data-ttu-id="eb6a9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eb6a9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb6a9-129">Response</span></span>
<span data-ttu-id="eb6a9-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-130">If successful, this method returns a `200 OK` response code and a collection of [enterpriseCodeSigningCertificate](../resources/intune-apps-enterprisecodesigningcertificate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eb6a9-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb6a9-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="eb6a9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb6a9-132">Request</span></span>
<span data-ttu-id="eb6a9-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/enterpriseCodeSigningCertificates
```

### <a name="response"></a><span data-ttu-id="eb6a9-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb6a9-134">Response</span></span>
<span data-ttu-id="eb6a9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb6a9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 512

{
  "value": [
    {
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
  ]
}
```





