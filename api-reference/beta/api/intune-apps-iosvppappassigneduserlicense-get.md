---
title: Obtener iosVppAppAssignedUserLicense
description: Leer las propiedades y las relaciones del objeto iosVppAppAssignedUserLicense.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ae27bb491717bf3f9516d863d2f3526cd30467be
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934474"
---
# <a name="get-iosvppappassigneduserlicense"></a><span data-ttu-id="01977-103">Obtener iosVppAppAssignedUserLicense</span><span class="sxs-lookup"><span data-stu-id="01977-103">Get iosVppAppAssignedUserLicense</span></span>

> <span data-ttu-id="01977-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01977-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01977-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01977-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="01977-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01977-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01977-107">Leer las propiedades y las relaciones del objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="01977-107">Read properties and relationships of the [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="01977-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01977-108">Prerequisites</span></span>
<span data-ttu-id="01977-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01977-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01977-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01977-111">Permission type</span></span>|<span data-ttu-id="01977-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01977-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="01977-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01977-113">Delegated (work or school account)</span></span>|<span data-ttu-id="01977-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="01977-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="01977-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01977-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="01977-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01977-116">Not supported.</span></span>|
|<span data-ttu-id="01977-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01977-117">Application</span></span>|<span data-ttu-id="01977-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01977-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="01977-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01977-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="01977-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="01977-120">Optional query parameters</span></span>
<span data-ttu-id="01977-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01977-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="01977-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01977-122">Request headers</span></span>
|<span data-ttu-id="01977-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01977-123">Header</span></span>|<span data-ttu-id="01977-124">Valor</span><span class="sxs-lookup"><span data-stu-id="01977-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="01977-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="01977-125">Authorization</span></span>|<span data-ttu-id="01977-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="01977-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="01977-127">Accept</span><span class="sxs-lookup"><span data-stu-id="01977-127">Accept</span></span>|<span data-ttu-id="01977-128">application/json</span><span class="sxs-lookup"><span data-stu-id="01977-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="01977-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01977-129">Request body</span></span>
<span data-ttu-id="01977-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="01977-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="01977-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01977-131">Response</span></span>
<span data-ttu-id="01977-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01977-132">If successful, this method returns a `200 OK` response code and [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01977-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01977-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="01977-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01977-134">Request</span></span>
<span data-ttu-id="01977-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01977-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses/{iosVppAppAssignedLicenseId}
```

### <a name="response"></a><span data-ttu-id="01977-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01977-136">Response</span></span>
<span data-ttu-id="01977-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="01977-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 318

{
  "value": {
    "@odata.type": "#microsoft.graph.iosVppAppAssignedUserLicense",
    "id": "fedc747d-747d-fedc-7d74-dcfe7d74dcfe",
    "userEmailAddress": "User Email Address value",
    "userId": "User Id value",
    "userName": "User Name value",
    "userPrincipalName": "User Principal Name value"
  }
}
```





