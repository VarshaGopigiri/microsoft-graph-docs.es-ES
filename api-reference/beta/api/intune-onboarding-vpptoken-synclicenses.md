---
title: Acción syncLicenses
description: Sincroniza las licencias asociadas con un determinado appleVolumePurchaseProgramToken.
ms.openlocfilehash: 36b0e141c398b17319711753928312a1353d2ab5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088847"
---
# <a name="synclicenses-action"></a><span data-ttu-id="bea72-103">Acción syncLicenses</span><span class="sxs-lookup"><span data-stu-id="bea72-103">syncLicenses action</span></span>

> <span data-ttu-id="bea72-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bea72-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bea72-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bea72-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bea72-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bea72-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bea72-107">Sincroniza las licencias asociadas con un appleVolumePurchaseProgramToken específico.</span><span class="sxs-lookup"><span data-stu-id="bea72-107">Syncs licenses associated with a specific appleVolumePurchaseProgramToken</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bea72-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bea72-108">Prerequisites</span></span>
<span data-ttu-id="bea72-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bea72-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bea72-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bea72-111">Permission type</span></span>|<span data-ttu-id="bea72-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bea72-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bea72-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bea72-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bea72-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bea72-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="bea72-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bea72-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bea72-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bea72-116">Not supported.</span></span>|
|<span data-ttu-id="bea72-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bea72-117">Application</span></span>|<span data-ttu-id="bea72-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bea72-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bea72-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bea72-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/vppTokens/{vppTokenId}/syncLicenses
```

## <a name="request-headers"></a><span data-ttu-id="bea72-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bea72-120">Request headers</span></span>
|<span data-ttu-id="bea72-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bea72-121">Header</span></span>|<span data-ttu-id="bea72-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bea72-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bea72-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bea72-123">Authorization</span></span>|<span data-ttu-id="bea72-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bea72-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bea72-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bea72-125">Accept</span></span>|<span data-ttu-id="bea72-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bea72-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bea72-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bea72-127">Request body</span></span>
<span data-ttu-id="bea72-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bea72-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bea72-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bea72-129">Response</span></span>
<span data-ttu-id="bea72-130">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `200 OK` y un [vppToken](../resources/intune-onboarding-vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bea72-130">If successful, this action returns a `200 OK` response code and a [vppToken](../resources/intune-onboarding-vpptoken.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bea72-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bea72-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="bea72-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bea72-132">Request</span></span>
<span data-ttu-id="bea72-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bea72-133">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/vppTokens/{vppTokenId}/syncLicenses
```

### <a name="response"></a><span data-ttu-id="bea72-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bea72-134">Response</span></span>
<span data-ttu-id="bea72-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bea72-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1124

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
    "tokenActionResults": [
      {
        "@odata.type": "microsoft.graph.vppTokenActionResult",
        "actionName": "Action Name value",
        "actionState": "pending",
        "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
        "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
      }
    ],
    "lastSyncStatus": "inProgress",
    "automaticallyUpdateApps": true,
    "countryOrRegion": "Country Or Region value",
    "dataSharingConsentGranted": true,
    "displayName": "Display Name value",
    "locationName": "Location Name value",
    "claimTokenManagementFromExternalMdm": true
  }
}
```





