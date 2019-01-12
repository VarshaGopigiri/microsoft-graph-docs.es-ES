---
title: Lista iosVppAppAssignedUserLicenses
description: Propiedades de la lista y relaciones de los objetos iosVppAppAssignedUserLicense.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6147bc3e36f6bf72c365160b8afdb39cff03573e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965449"
---
# <a name="list-iosvppappassigneduserlicenses"></a><span data-ttu-id="659fc-103">Lista iosVppAppAssignedUserLicenses</span><span class="sxs-lookup"><span data-stu-id="659fc-103">List iosVppAppAssignedUserLicenses</span></span>

> <span data-ttu-id="659fc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="659fc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="659fc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="659fc-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="659fc-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="659fc-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="659fc-107">Propiedades de la lista y relaciones de los objetos [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="659fc-107">List properties and relationships of the [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="659fc-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="659fc-108">Prerequisites</span></span>
<span data-ttu-id="659fc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="659fc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="659fc-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="659fc-111">Permission type</span></span>|<span data-ttu-id="659fc-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="659fc-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="659fc-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="659fc-113">Delegated (work or school account)</span></span>|<span data-ttu-id="659fc-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="659fc-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="659fc-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="659fc-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="659fc-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="659fc-116">Not supported.</span></span>|
|<span data-ttu-id="659fc-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="659fc-117">Application</span></span>|<span data-ttu-id="659fc-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="659fc-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="659fc-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="659fc-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

## <a name="request-headers"></a><span data-ttu-id="659fc-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="659fc-120">Request headers</span></span>
|<span data-ttu-id="659fc-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="659fc-121">Header</span></span>|<span data-ttu-id="659fc-122">Valor</span><span class="sxs-lookup"><span data-stu-id="659fc-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="659fc-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="659fc-123">Authorization</span></span>|<span data-ttu-id="659fc-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="659fc-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="659fc-125">Accept</span><span class="sxs-lookup"><span data-stu-id="659fc-125">Accept</span></span>|<span data-ttu-id="659fc-126">application/json</span><span class="sxs-lookup"><span data-stu-id="659fc-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="659fc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="659fc-127">Request body</span></span>
<span data-ttu-id="659fc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="659fc-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="659fc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="659fc-129">Response</span></span>
<span data-ttu-id="659fc-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="659fc-130">If successful, this method returns a `200 OK` response code and a collection of [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="659fc-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="659fc-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="659fc-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="659fc-132">Request</span></span>
<span data-ttu-id="659fc-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="659fc-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

### <a name="response"></a><span data-ttu-id="659fc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="659fc-134">Response</span></span>
<span data-ttu-id="659fc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="659fc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 344

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosVppAppAssignedUserLicense",
      "id": "fedc747d-747d-fedc-7d74-dcfe7d74dcfe",
      "userEmailAddress": "User Email Address value",
      "userId": "User Id value",
      "userName": "User Name value",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```





