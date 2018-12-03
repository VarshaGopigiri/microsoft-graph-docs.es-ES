---
title: Lista androidDeviceOwnerEnrollmentProfiles
description: Propiedades de la lista y relaciones de los objetos androidDeviceOwnerEnrollmentProfile.
ms.openlocfilehash: cba0ec4d450e866eaf849536f905dfdc3e00a20c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086893"
---
# <a name="list-androiddeviceownerenrollmentprofiles"></a><span data-ttu-id="1118b-103">Lista androidDeviceOwnerEnrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="1118b-103">List androidDeviceOwnerEnrollmentProfiles</span></span>

> <span data-ttu-id="1118b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1118b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1118b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1118b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1118b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1118b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1118b-107">Propiedades de la lista y relaciones de los objetos [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="1118b-107">List properties and relationships of the [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1118b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1118b-108">Prerequisites</span></span>
<span data-ttu-id="1118b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1118b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1118b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1118b-111">Permission type</span></span>|<span data-ttu-id="1118b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1118b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1118b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1118b-113">Delegated (work or school account)</span></span>|<span data-ttu-id="1118b-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1118b-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1118b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1118b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1118b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1118b-116">Not supported.</span></span>|
|<span data-ttu-id="1118b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1118b-117">Application</span></span>|<span data-ttu-id="1118b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1118b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1118b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1118b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/androidDeviceOwnerEnrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="1118b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1118b-120">Request headers</span></span>
|<span data-ttu-id="1118b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1118b-121">Header</span></span>|<span data-ttu-id="1118b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1118b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1118b-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="1118b-123">Authorization</span></span>|<span data-ttu-id="1118b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1118b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1118b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1118b-125">Accept</span></span>|<span data-ttu-id="1118b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1118b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1118b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1118b-127">Request body</span></span>
<span data-ttu-id="1118b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1118b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1118b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1118b-129">Response</span></span>
<span data-ttu-id="1118b-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1118b-130">If successful, this method returns a `200 OK` response code and a collection of [androidDeviceOwnerEnrollmentProfile](../resources/intune-androidforwork-androiddeviceownerenrollmentprofile.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1118b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1118b-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1118b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1118b-132">Request</span></span>
<span data-ttu-id="1118b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1118b-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/androidDeviceOwnerEnrollmentProfiles
```

### <a name="response"></a><span data-ttu-id="1118b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1118b-134">Response</span></span>
<span data-ttu-id="1118b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1118b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 838

{
  "value": [
    {
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
  ]
}
```




