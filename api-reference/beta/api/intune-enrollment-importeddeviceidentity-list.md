---
title: Lista importedDeviceIdentities
description: Propiedades de la lista y relaciones de los objetos importedDeviceIdentity.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 11f40baaa839229c483dab70f0483be7e61f979c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27939276"
---
# <a name="list-importeddeviceidentities"></a><span data-ttu-id="5629a-103">Lista importedDeviceIdentities</span><span class="sxs-lookup"><span data-stu-id="5629a-103">List importedDeviceIdentities</span></span>

> <span data-ttu-id="5629a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5629a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5629a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5629a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5629a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5629a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5629a-107">Propiedades de la lista y relaciones de los objetos [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="5629a-107">List properties and relationships of the [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5629a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5629a-108">Prerequisites</span></span>
<span data-ttu-id="5629a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5629a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5629a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5629a-111">Permission type</span></span>|<span data-ttu-id="5629a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5629a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5629a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5629a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5629a-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="5629a-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="5629a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5629a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5629a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5629a-116">Not supported.</span></span>|
|<span data-ttu-id="5629a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5629a-117">Application</span></span>|<span data-ttu-id="5629a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5629a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5629a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5629a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/importedDeviceIdentities
```

## <a name="request-headers"></a><span data-ttu-id="5629a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5629a-120">Request headers</span></span>
|<span data-ttu-id="5629a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5629a-121">Header</span></span>|<span data-ttu-id="5629a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5629a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5629a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5629a-123">Authorization</span></span>|<span data-ttu-id="5629a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5629a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5629a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5629a-125">Accept</span></span>|<span data-ttu-id="5629a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5629a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5629a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5629a-127">Request body</span></span>
<span data-ttu-id="5629a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5629a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5629a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5629a-129">Response</span></span>
<span data-ttu-id="5629a-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5629a-130">If successful, this method returns a `200 OK` response code and a collection of [importedDeviceIdentity](../resources/intune-enrollment-importeddeviceidentity.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5629a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5629a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="5629a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5629a-132">Request</span></span>
<span data-ttu-id="5629a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5629a-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/importedDeviceIdentities
```

### <a name="response"></a><span data-ttu-id="5629a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5629a-134">Response</span></span>
<span data-ttu-id="5629a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5629a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 577

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.importedDeviceIdentity",
      "id": "9f70a12f-a12f-9f70-2fa1-709f2fa1709f",
      "importedDeviceIdentifier": "Imported Device Identifier value",
      "importedDeviceIdentityType": "imei",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
      "description": "Description value",
      "enrollmentState": "enrolled",
      "platform": "ios"
    }
  ]
}
```





