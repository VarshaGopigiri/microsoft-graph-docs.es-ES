---
title: Enumerar vppTokens
description: Enumera las propiedades y las relaciones de los objetos vppToken.
ms.openlocfilehash: 577213da304d77b171470f52f43a187edba4ad24
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029618"
---
# <a name="list-vpptokens"></a><span data-ttu-id="88306-103">Enumerar vppTokens</span><span class="sxs-lookup"><span data-stu-id="88306-103">List vppTokens</span></span>

> <span data-ttu-id="88306-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="88306-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="88306-105">Enumera las propiedades y las relaciones de los objetos [vppToken](../resources/intune-onboarding-vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="88306-105">List properties and relationships of the [vppToken](../resources/intune-onboarding-vpptoken.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="88306-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="88306-106">Prerequisites</span></span>
<span data-ttu-id="88306-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88306-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="88306-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88306-109">Permission type</span></span>|<span data-ttu-id="88306-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88306-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="88306-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88306-111">Delegated (work or school account)</span></span>|<span data-ttu-id="88306-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="88306-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="88306-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88306-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="88306-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88306-114">Not supported.</span></span>|
|<span data-ttu-id="88306-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88306-115">Application</span></span>|<span data-ttu-id="88306-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88306-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="88306-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88306-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/vppTokens
```

## <a name="request-headers"></a><span data-ttu-id="88306-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88306-118">Request headers</span></span>
|<span data-ttu-id="88306-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88306-119">Header</span></span>|<span data-ttu-id="88306-120">Valor</span><span class="sxs-lookup"><span data-stu-id="88306-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="88306-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="88306-121">Authorization</span></span>|<span data-ttu-id="88306-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="88306-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="88306-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="88306-123">Accept</span></span>|<span data-ttu-id="88306-124">application/json</span><span class="sxs-lookup"><span data-stu-id="88306-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="88306-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88306-125">Request body</span></span>
<span data-ttu-id="88306-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="88306-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="88306-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88306-127">Response</span></span>
<span data-ttu-id="88306-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [vppToken](../resources/intune-onboarding-vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88306-128">If successful, this method returns a `200 OK` response code and a collection of [vppToken](../resources/intune-onboarding-vpptoken.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88306-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88306-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="88306-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88306-130">Request</span></span>
<span data-ttu-id="88306-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88306-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/vppTokens
```

### <a name="response"></a><span data-ttu-id="88306-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88306-132">Response</span></span>
<span data-ttu-id="88306-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88306-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 659

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.vppToken",
      "id": "9ceb2f92-2f92-9ceb-922f-eb9c922feb9c",
      "organizationName": "Organization Name value",
      "vppTokenAccountType": "education",
      "appleId": "Apple Id value",
      "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "token": "Token value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "state": "valid",
      "lastSyncStatus": "inProgress",
      "automaticallyUpdateApps": true,
      "countryOrRegion": "Country Or Region value"
    }
  ]
}
```



