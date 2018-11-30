---
title: Acción syncLicenses
description: Sincroniza las licencias asociadas con un determinado appleVolumePurchaseProgramToken.
ms.openlocfilehash: 167fbb16b9377e3134c1a4403433449341e21562
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032644"
---
# <a name="synclicenses-action"></a><span data-ttu-id="97b5e-103">Acción syncLicenses</span><span class="sxs-lookup"><span data-stu-id="97b5e-103">syncLicenses action</span></span>

> <span data-ttu-id="97b5e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97b5e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97b5e-105">Sincroniza las licencias asociadas con un appleVolumePurchaseProgramToken específico.</span><span class="sxs-lookup"><span data-stu-id="97b5e-105">Syncs licenses associated with a specific appleVolumePurchaseProgramToken</span></span>
## <a name="prerequisites"></a><span data-ttu-id="97b5e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="97b5e-106">Prerequisites</span></span>
<span data-ttu-id="97b5e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="97b5e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="97b5e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97b5e-109">Permission type</span></span>|<span data-ttu-id="97b5e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97b5e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="97b5e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97b5e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="97b5e-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97b5e-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="97b5e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97b5e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="97b5e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97b5e-114">Not supported.</span></span>|
|<span data-ttu-id="97b5e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97b5e-115">Application</span></span>|<span data-ttu-id="97b5e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97b5e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="97b5e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97b5e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/vppTokens/{vppTokenId}/syncLicenses
```

## <a name="request-headers"></a><span data-ttu-id="97b5e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="97b5e-118">Request headers</span></span>
|<span data-ttu-id="97b5e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97b5e-119">Header</span></span>|<span data-ttu-id="97b5e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="97b5e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="97b5e-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="97b5e-121">Authorization</span></span>|<span data-ttu-id="97b5e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="97b5e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="97b5e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="97b5e-123">Accept</span></span>|<span data-ttu-id="97b5e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="97b5e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="97b5e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97b5e-125">Request body</span></span>
<span data-ttu-id="97b5e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="97b5e-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="97b5e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97b5e-127">Response</span></span>
<span data-ttu-id="97b5e-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un [vppToken](../resources/intune-onboarding-vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97b5e-128">If successful, this action returns a `200 OK` response code and a [vppToken](../resources/intune-onboarding-vpptoken.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="97b5e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97b5e-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="97b5e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="97b5e-130">Request</span></span>
<span data-ttu-id="97b5e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97b5e-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/vppTokens/{vppTokenId}/syncLicenses
```

### <a name="response"></a><span data-ttu-id="97b5e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97b5e-132">Response</span></span>
<span data-ttu-id="97b5e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="97b5e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 619

{
  "value": {
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
}
```



