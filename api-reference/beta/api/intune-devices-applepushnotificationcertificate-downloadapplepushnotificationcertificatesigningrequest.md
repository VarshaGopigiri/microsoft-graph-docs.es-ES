---
title: Función downloadApplePushNotificationCertificateSigningRequest
description: Descargar solicitud de firma de certificado de notificación de inserción de Apple
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 94126d7372497abfc2318ad5029eab27b64d0087
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953654"
---
# <a name="downloadapplepushnotificationcertificatesigningrequest-function"></a><span data-ttu-id="1e4cb-103">Función downloadApplePushNotificationCertificateSigningRequest</span><span class="sxs-lookup"><span data-stu-id="1e4cb-103">downloadApplePushNotificationCertificateSigningRequest function</span></span>

> <span data-ttu-id="1e4cb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e4cb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1e4cb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1e4cb-107">Descargar solicitud de firma de certificado de notificación de inserción de Apple</span><span class="sxs-lookup"><span data-stu-id="1e4cb-107">Download Apple push notification certificate signing request</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1e4cb-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1e4cb-108">Prerequisites</span></span>
<span data-ttu-id="1e4cb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1e4cb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1e4cb-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e4cb-111">Permission type</span></span>|<span data-ttu-id="1e4cb-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e4cb-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1e4cb-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e4cb-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1e4cb-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1e4cb-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="1e4cb-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e4cb-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1e4cb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-116">Not supported.</span></span>|
|<span data-ttu-id="1e4cb-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e4cb-117">Application</span></span>|<span data-ttu-id="1e4cb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1e4cb-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e4cb-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/applePushNotificationCertificate/downloadApplePushNotificationCertificateSigningRequest
```

## <a name="request-headers"></a><span data-ttu-id="1e4cb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1e4cb-120">Request headers</span></span>
|<span data-ttu-id="1e4cb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e4cb-121">Header</span></span>|<span data-ttu-id="1e4cb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1e4cb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1e4cb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1e4cb-123">Authorization</span></span>|<span data-ttu-id="1e4cb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1e4cb-125">Accept</span><span class="sxs-lookup"><span data-stu-id="1e4cb-125">Accept</span></span>|<span data-ttu-id="1e4cb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1e4cb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1e4cb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1e4cb-127">Request body</span></span>
<span data-ttu-id="1e4cb-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1e4cb-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e4cb-129">Response</span></span>
<span data-ttu-id="1e4cb-130">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un objeto String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-130">If successful, this function returns a `200 OK` response code and a String in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1e4cb-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e4cb-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1e4cb-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e4cb-132">Request</span></span>
<span data-ttu-id="1e4cb-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/applePushNotificationCertificate/downloadApplePushNotificationCertificateSigningRequest
```

### <a name="response"></a><span data-ttu-id="1e4cb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e4cb-134">Response</span></span>
<span data-ttu-id="1e4cb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1e4cb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 85

{
  "value": "Download Apple Push Notification Certificate Signing Request value"
}
```





