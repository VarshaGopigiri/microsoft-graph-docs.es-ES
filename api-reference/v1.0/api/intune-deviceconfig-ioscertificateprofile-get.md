---
title: Obtener iosCertificateProfile
description: Lea las propiedades y las relaciones del objeto iosCertificateProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b4a3d7f4e6fc2a38964d740fe94a4ad4a71c6374
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983530"
---
# <a name="get-ioscertificateprofile"></a><span data-ttu-id="6b8cb-103">Obtener iosCertificateProfile</span><span class="sxs-lookup"><span data-stu-id="6b8cb-103">Get iosCertificateProfile</span></span>

> <span data-ttu-id="6b8cb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6b8cb-105">Lea las propiedades y las relaciones del objeto [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md).</span><span class="sxs-lookup"><span data-stu-id="6b8cb-105">Read properties and relationships of the [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6b8cb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6b8cb-106">Prerequisites</span></span>
<span data-ttu-id="6b8cb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6b8cb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6b8cb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6b8cb-109">Permission type</span></span>|<span data-ttu-id="6b8cb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6b8cb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6b8cb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6b8cb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6b8cb-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="6b8cb-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="6b8cb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6b8cb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6b8cb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-114">Not supported.</span></span>|
|<span data-ttu-id="6b8cb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6b8cb-115">Application</span></span>|<span data-ttu-id="6b8cb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6b8cb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6b8cb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6b8cb-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6b8cb-118">Optional query parameters</span></span>
<span data-ttu-id="6b8cb-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6b8cb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6b8cb-120">Request headers</span></span>
|<span data-ttu-id="6b8cb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b8cb-121">Header</span></span>|<span data-ttu-id="6b8cb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6b8cb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6b8cb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="6b8cb-123">Authorization</span></span>|<span data-ttu-id="6b8cb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6b8cb-125">Accept</span><span class="sxs-lookup"><span data-stu-id="6b8cb-125">Accept</span></span>|<span data-ttu-id="6b8cb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6b8cb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6b8cb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6b8cb-127">Request body</span></span>
<span data-ttu-id="6b8cb-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6b8cb-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b8cb-129">Response</span></span>
<span data-ttu-id="6b8cb-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-130">If successful, this method returns a `200 OK` response code and [iosCertificateProfile](../resources/intune-deviceconfig-ioscertificateprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6b8cb-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6b8cb-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="6b8cb-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6b8cb-132">Request</span></span>
<span data-ttu-id="6b8cb-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="6b8cb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6b8cb-134">Response</span></span>
<span data-ttu-id="6b8cb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6b8cb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 364

{
  "value": {
    "@odata.type": "#microsoft.graph.iosCertificateProfile",
    "id": "0ea4f39a-f39a-0ea4-9af3-a40e9af3a40e",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7
  }
}
```



