---
title: Enumerar vppTokens
description: Enumera las propiedades y las relaciones de los objetos vppToken.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 993e7f8917ed60185159303dffc2be957816d4c5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976200"
---
# <a name="list-vpptokens"></a><span data-ttu-id="e6893-103">Enumerar vppTokens</span><span class="sxs-lookup"><span data-stu-id="e6893-103">List vppTokens</span></span>

> <span data-ttu-id="e6893-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e6893-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e6893-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e6893-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e6893-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6893-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6893-107">Enumera las propiedades y las relaciones de los objetos [vppToken](../resources/intune-onboarding-vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="e6893-107">List properties and relationships of the [vppToken](../resources/intune-onboarding-vpptoken.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6893-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6893-108">Prerequisites</span></span>
<span data-ttu-id="e6893-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6893-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6893-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6893-111">Permission type</span></span>|<span data-ttu-id="e6893-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6893-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6893-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6893-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e6893-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="e6893-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="e6893-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6893-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6893-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6893-116">Not supported.</span></span>|
|<span data-ttu-id="e6893-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6893-117">Application</span></span>|<span data-ttu-id="e6893-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6893-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6893-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6893-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/vppTokens
```

## <a name="request-headers"></a><span data-ttu-id="e6893-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6893-120">Request headers</span></span>
|<span data-ttu-id="e6893-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6893-121">Header</span></span>|<span data-ttu-id="e6893-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e6893-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6893-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e6893-123">Authorization</span></span>|<span data-ttu-id="e6893-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6893-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e6893-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e6893-125">Accept</span></span>|<span data-ttu-id="e6893-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e6893-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6893-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6893-127">Request body</span></span>
<span data-ttu-id="e6893-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6893-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6893-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6893-129">Response</span></span>
<span data-ttu-id="e6893-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [vppToken](../resources/intune-onboarding-vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6893-130">If successful, this method returns a `200 OK` response code and a collection of [vppToken](../resources/intune-onboarding-vpptoken.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6893-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6893-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6893-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6893-132">Request</span></span>
<span data-ttu-id="e6893-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6893-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/vppTokens
```

### <a name="response"></a><span data-ttu-id="e6893-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6893-134">Response</span></span>
<span data-ttu-id="e6893-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6893-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1190

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
  ]
}
```





