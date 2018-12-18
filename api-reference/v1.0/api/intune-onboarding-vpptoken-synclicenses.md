---
title: Acción syncLicenses
description: Sincroniza las licencias asociadas con un determinado appleVolumePurchaseProgramToken.
author: tfitzmac
ms.openlocfilehash: 541d974666988a165293f8e4241d0a15d712209a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336606"
---
# <a name="synclicenses-action"></a><span data-ttu-id="b9be2-103">Acción syncLicenses</span><span class="sxs-lookup"><span data-stu-id="b9be2-103">syncLicenses action</span></span>

> <span data-ttu-id="b9be2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9be2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9be2-105">Sincroniza las licencias asociadas con un appleVolumePurchaseProgramToken específico.</span><span class="sxs-lookup"><span data-stu-id="b9be2-105">Syncs licenses associated with a specific appleVolumePurchaseProgramToken</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b9be2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b9be2-106">Prerequisites</span></span>
<span data-ttu-id="b9be2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b9be2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b9be2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b9be2-109">Permission type</span></span>|<span data-ttu-id="b9be2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b9be2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b9be2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b9be2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b9be2-112">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b9be2-112">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="b9be2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b9be2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b9be2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9be2-114">Not supported.</span></span>|
|<span data-ttu-id="b9be2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b9be2-115">Application</span></span>|<span data-ttu-id="b9be2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9be2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b9be2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9be2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/vppTokens/{vppTokenId}/syncLicenses
```

## <a name="request-headers"></a><span data-ttu-id="b9be2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9be2-118">Request headers</span></span>
|<span data-ttu-id="b9be2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9be2-119">Header</span></span>|<span data-ttu-id="b9be2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b9be2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b9be2-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b9be2-121">Authorization</span></span>|<span data-ttu-id="b9be2-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b9be2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b9be2-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b9be2-123">Accept</span></span>|<span data-ttu-id="b9be2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b9be2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b9be2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9be2-125">Request body</span></span>
<span data-ttu-id="b9be2-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b9be2-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b9be2-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9be2-127">Response</span></span>
<span data-ttu-id="b9be2-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un [vppToken](../resources/intune-onboarding-vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9be2-128">If successful, this action returns a `200 OK` response code and a [vppToken](../resources/intune-onboarding-vpptoken.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b9be2-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9be2-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b9be2-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9be2-130">Request</span></span>
<span data-ttu-id="b9be2-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9be2-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/vppTokens/{vppTokenId}/syncLicenses
```

### <a name="response"></a><span data-ttu-id="b9be2-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9be2-132">Response</span></span>
<span data-ttu-id="b9be2-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9be2-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



