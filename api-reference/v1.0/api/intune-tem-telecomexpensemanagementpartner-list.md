---
title: Enumerar telecomExpenseManagementPartners
description: Enumere las propiedades y las relaciones de los objetos telecomExpenseManagementPartner.
ms.openlocfilehash: e71be2fb4975407fc0e1ad272899d2d73f39d861
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028561"
---
# <a name="list-telecomexpensemanagementpartners"></a><span data-ttu-id="8ea6c-103">Enumerar telecomExpenseManagementPartners</span><span class="sxs-lookup"><span data-stu-id="8ea6c-103">List telecomExpenseManagementPartners</span></span>

> <span data-ttu-id="8ea6c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ea6c-105">Enumere las propiedades y las relaciones de los objetos [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md).</span><span class="sxs-lookup"><span data-stu-id="8ea6c-105">List properties and relationships of the [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8ea6c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8ea6c-106">Prerequisites</span></span>
<span data-ttu-id="8ea6c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8ea6c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8ea6c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ea6c-109">Permission type</span></span>|<span data-ttu-id="8ea6c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ea6c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8ea6c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ea6c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8ea6c-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="8ea6c-112">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="8ea6c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ea6c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8ea6c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-114">Not supported.</span></span>|
|<span data-ttu-id="8ea6c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ea6c-115">Application</span></span>|<span data-ttu-id="8ea6c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8ea6c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ea6c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/telecomExpenseManagementPartners
```

## <a name="request-headers"></a><span data-ttu-id="8ea6c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ea6c-118">Request headers</span></span>
|<span data-ttu-id="8ea6c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ea6c-119">Header</span></span>|<span data-ttu-id="8ea6c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8ea6c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8ea6c-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8ea6c-121">Authorization</span></span>|<span data-ttu-id="8ea6c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8ea6c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8ea6c-123">Accept</span></span>|<span data-ttu-id="8ea6c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8ea6c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8ea6c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ea6c-125">Request body</span></span>
<span data-ttu-id="8ea6c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8ea6c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ea6c-127">Response</span></span>
<span data-ttu-id="8ea6c-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-128">If successful, this method returns a `200 OK` response code and a collection of [telecomExpenseManagementPartner](../resources/intune-tem-telecomexpensemanagementpartner.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8ea6c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ea6c-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="8ea6c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ea6c-130">Request</span></span>
<span data-ttu-id="8ea6c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/telecomExpenseManagementPartners
```

### <a name="response"></a><span data-ttu-id="8ea6c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ea6c-132">Response</span></span>
<span data-ttu-id="8ea6c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ea6c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 358

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
      "id": "47a3b399-b399-47a3-99b3-a34799b3a347",
      "displayName": "Display Name value",
      "url": "Url value",
      "appAuthorized": true,
      "enabled": true,
      "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
    }
  ]
}
```



