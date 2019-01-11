---
title: Obtener androidDeviceOwnerEnrollmentProfile
description: Leer las propiedades y las relaciones del objeto androidDeviceOwnerEnrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6947171c5d7a366cc5c5fab30bf3143e002c92a7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818602"
---
# <a name="get-androiddeviceownerenrollmentprofile"></a><span data-ttu-id="38ef5-103">Obtener androidDeviceOwnerEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="38ef5-103">Get androidDeviceOwnerEnrollmentProfile</span></span>

> <span data-ttu-id="38ef5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38ef5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38ef5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38ef5-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="38ef5-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="38ef5-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="38ef5-107">Leer las propiedades y las relaciones del objeto [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="38ef5-107">Read properties and relationships of the [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="38ef5-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="38ef5-108">Prerequisites</span></span>
<span data-ttu-id="38ef5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38ef5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38ef5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38ef5-111">Permission type</span></span>|<span data-ttu-id="38ef5-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38ef5-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="38ef5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38ef5-113">Delegated (work or school account)</span></span>|<span data-ttu-id="38ef5-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="38ef5-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="38ef5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38ef5-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="38ef5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38ef5-116">Not supported.</span></span>|
|<span data-ttu-id="38ef5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38ef5-117">Application</span></span>|<span data-ttu-id="38ef5-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38ef5-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="38ef5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38ef5-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/androidDeviceOwnerEnrollmentProfiles/{androidDeviceOwnerEnrollmentProfileId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="38ef5-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="38ef5-120">Optional query parameters</span></span>
<span data-ttu-id="38ef5-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38ef5-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="38ef5-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38ef5-122">Request headers</span></span>
|<span data-ttu-id="38ef5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38ef5-123">Header</span></span>|<span data-ttu-id="38ef5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="38ef5-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="38ef5-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="38ef5-125">Authorization</span></span>|<span data-ttu-id="38ef5-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="38ef5-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="38ef5-127">Accept</span><span class="sxs-lookup"><span data-stu-id="38ef5-127">Accept</span></span>|<span data-ttu-id="38ef5-128">application/json</span><span class="sxs-lookup"><span data-stu-id="38ef5-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="38ef5-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38ef5-129">Request body</span></span>
<span data-ttu-id="38ef5-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="38ef5-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="38ef5-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38ef5-131">Response</span></span>
<span data-ttu-id="38ef5-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38ef5-132">If successful, this method returns a `200 OK` response code and [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38ef5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38ef5-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="38ef5-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38ef5-134">Request</span></span>
<span data-ttu-id="38ef5-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38ef5-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/androidDeviceOwnerEnrollmentProfiles/{androidDeviceOwnerEnrollmentProfileId}
```

### <a name="response"></a><span data-ttu-id="38ef5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38ef5-136">Response</span></span>
<span data-ttu-id="38ef5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38ef5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 790

{
  "value": {
    "@odata.type": "#microsoft.graph.androidDeviceOwnerEnrollmentProfile",
    "accountId": "Account Id value",
    "id": "a8d0245e-245e-a8d0-5e24-d0a85e24d0a8",
    "displayName": "Display Name value",
    "description": "Description value",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "tokenValue": "Token Value value",
    "tokenCreationDateTime": "2017-01-01T00:01:38.5314127-08:00",
    "tokenExpirationDateTime": "2016-12-31T23:59:54.0590989-08:00",
    "enrolledDeviceCount": 3,
    "qrCodeContent": "Qr Code Content value",
    "qrCodeImage": {
      "@odata.type": "microsoft.graph.mimeContent",
      "type": "Type value",
      "value": "dmFsdWU="
    }
  }
}
```





