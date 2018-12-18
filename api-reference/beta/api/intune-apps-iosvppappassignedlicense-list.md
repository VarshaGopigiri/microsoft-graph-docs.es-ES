---
title: Lista iosVppAppAssignedLicenses
description: Propiedades de la lista y relaciones de los objetos iosVppAppAssignedLicense.
author: tfitzmac
ms.openlocfilehash: ee5787593a841246165ad10673a772b6e24ddf09
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358187"
---
# <a name="list-iosvppappassignedlicenses"></a><span data-ttu-id="46790-103">Lista iosVppAppAssignedLicenses</span><span class="sxs-lookup"><span data-stu-id="46790-103">List iosVppAppAssignedLicenses</span></span>

> <span data-ttu-id="46790-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46790-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46790-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46790-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="46790-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46790-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46790-107">Propiedades de la lista y relaciones de los objetos [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="46790-107">List properties and relationships of the [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46790-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="46790-108">Prerequisites</span></span>
<span data-ttu-id="46790-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="46790-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="46790-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46790-111">Permission type</span></span>|<span data-ttu-id="46790-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46790-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46790-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46790-113">Delegated (work or school account)</span></span>|<span data-ttu-id="46790-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="46790-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="46790-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46790-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46790-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46790-116">Not supported.</span></span>|
|<span data-ttu-id="46790-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46790-117">Application</span></span>|<span data-ttu-id="46790-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46790-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46790-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46790-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

## <a name="request-headers"></a><span data-ttu-id="46790-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46790-120">Request headers</span></span>
|<span data-ttu-id="46790-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46790-121">Header</span></span>|<span data-ttu-id="46790-122">Valor</span><span class="sxs-lookup"><span data-stu-id="46790-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46790-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="46790-123">Authorization</span></span>|<span data-ttu-id="46790-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="46790-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46790-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="46790-125">Accept</span></span>|<span data-ttu-id="46790-126">application/json</span><span class="sxs-lookup"><span data-stu-id="46790-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46790-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46790-127">Request body</span></span>
<span data-ttu-id="46790-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="46790-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="46790-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46790-129">Response</span></span>
<span data-ttu-id="46790-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46790-130">If successful, this method returns a `200 OK` response code and a collection of [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46790-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46790-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="46790-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46790-132">Request</span></span>
<span data-ttu-id="46790-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46790-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

### <a name="response"></a><span data-ttu-id="46790-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46790-134">Response</span></span>
<span data-ttu-id="46790-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46790-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 340

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosVppAppAssignedLicense",
      "id": "090a8d2e-8d2e-090a-2e8d-0a092e8d0a09",
      "userEmailAddress": "User Email Address value",
      "userId": "User Id value",
      "userName": "User Name value",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```





