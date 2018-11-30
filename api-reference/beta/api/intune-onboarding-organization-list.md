---
title: Enumerar organizaciones
description: Lea las propiedades y las relaciones de los objetos organization.
ms.openlocfilehash: 9b4b211b71ad619d50b3813022bcc03bf24a87c4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087888"
---
# <a name="list-organizations"></a><span data-ttu-id="6fbca-103">Enumerar organizaciones</span><span class="sxs-lookup"><span data-stu-id="6fbca-103">List organizations</span></span>

> <span data-ttu-id="6fbca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6fbca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6fbca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6fbca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6fbca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6fbca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6fbca-107">Lea las propiedades y las relaciones de los objetos [organization](../resources/intune-onboarding-organization.md).</span><span class="sxs-lookup"><span data-stu-id="6fbca-107">List properties and relationships of the [organization](../resources/intune-onboarding-organization.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6fbca-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6fbca-108">Prerequisites</span></span>
<span data-ttu-id="6fbca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6fbca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6fbca-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6fbca-111">Permission type</span></span>|<span data-ttu-id="6fbca-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6fbca-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6fbca-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6fbca-113">Delegated (work or school account)</span></span>|<span data-ttu-id="6fbca-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="6fbca-114">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="6fbca-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6fbca-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6fbca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6fbca-116">Not supported.</span></span>|
|<span data-ttu-id="6fbca-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6fbca-117">Application</span></span>|<span data-ttu-id="6fbca-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6fbca-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6fbca-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6fbca-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /organization
```

## <a name="request-headers"></a><span data-ttu-id="6fbca-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6fbca-120">Request headers</span></span>
|<span data-ttu-id="6fbca-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fbca-121">Header</span></span>|<span data-ttu-id="6fbca-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6fbca-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6fbca-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6fbca-123">Authorization</span></span>|<span data-ttu-id="6fbca-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6fbca-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6fbca-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6fbca-125">Accept</span></span>|<span data-ttu-id="6fbca-126">application/json</span><span class="sxs-lookup"><span data-stu-id="6fbca-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6fbca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6fbca-127">Request body</span></span>
<span data-ttu-id="6fbca-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6fbca-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6fbca-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6fbca-129">Response</span></span>
<span data-ttu-id="6fbca-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [organization](../resources/intune-onboarding-organization.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fbca-130">If successful, this method returns a `200 OK` response code and a collection of [organization](../resources/intune-onboarding-organization.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6fbca-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fbca-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="6fbca-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6fbca-132">Request</span></span>
<span data-ttu-id="6fbca-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fbca-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/organization
```

### <a name="response"></a><span data-ttu-id="6fbca-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6fbca-134">Response</span></span>
<span data-ttu-id="6fbca-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6fbca-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 622

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.organization",
      "id": "9efe224a-224a-9efe-4a22-fe9e4a22fe9e",
      "mobileDeviceManagementAuthority": "intune",
      "certificateConnectorSetting": {
        "@odata.type": "microsoft.graph.certificateConnectorSetting",
        "status": 6,
        "certExpiryTime": "2017-01-01T00:00:03.9979674-08:00",
        "enrollmentError": "Enrollment Error value",
        "lastConnectorConnectionTime": "2017-01-01T00:02:50.2393584-08:00",
        "connectorVersion": "Connector Version value",
        "lastUploadVersion": 1
      }
    }
  ]
}
```




