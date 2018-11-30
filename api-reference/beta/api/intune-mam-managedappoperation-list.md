---
title: Enumerar managedAppOperations
description: Enumere las propiedades y las relaciones de los objetos managedAppOperation.
ms.openlocfilehash: f858a0a70b7c97321a4d6d503b238363253624f7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088340"
---
# <a name="list-managedappoperations"></a><span data-ttu-id="b33fe-103">Enumerar managedAppOperations</span><span class="sxs-lookup"><span data-stu-id="b33fe-103">List managedAppOperations</span></span>

> <span data-ttu-id="b33fe-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b33fe-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b33fe-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b33fe-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b33fe-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b33fe-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b33fe-107">Enumere las propiedades y las relaciones de los objetos [managedAppOperation](../resources/intune-mam-managedappoperation.md).</span><span class="sxs-lookup"><span data-stu-id="b33fe-107">List properties and relationships of the [managedAppOperation](../resources/intune-mam-managedappoperation.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b33fe-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b33fe-108">Prerequisites</span></span>
<span data-ttu-id="b33fe-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b33fe-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b33fe-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b33fe-111">Permission type</span></span>|<span data-ttu-id="b33fe-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b33fe-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b33fe-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b33fe-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b33fe-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="b33fe-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="b33fe-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b33fe-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b33fe-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b33fe-116">Not supported.</span></span>|
|<span data-ttu-id="b33fe-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b33fe-117">Application</span></span>|<span data-ttu-id="b33fe-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b33fe-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b33fe-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b33fe-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
```

## <a name="request-headers"></a><span data-ttu-id="b33fe-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b33fe-120">Request headers</span></span>
|<span data-ttu-id="b33fe-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b33fe-121">Header</span></span>|<span data-ttu-id="b33fe-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b33fe-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b33fe-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b33fe-123">Authorization</span></span>|<span data-ttu-id="b33fe-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b33fe-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b33fe-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b33fe-125">Accept</span></span>|<span data-ttu-id="b33fe-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b33fe-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b33fe-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b33fe-127">Request body</span></span>
<span data-ttu-id="b33fe-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b33fe-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b33fe-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b33fe-129">Response</span></span>
<span data-ttu-id="b33fe-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [managedAppOperation](../resources/intune-mam-managedappoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b33fe-130">If successful, this method returns a `200 OK` response code and a collection of [managedAppOperation](../resources/intune-mam-managedappoperation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b33fe-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b33fe-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="b33fe-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b33fe-132">Request</span></span>
<span data-ttu-id="b33fe-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b33fe-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/operations
```

### <a name="response"></a><span data-ttu-id="b33fe-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b33fe-134">Response</span></span>
<span data-ttu-id="b33fe-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b33fe-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 329

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedAppOperation",
      "displayName": "Display Name value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "state": "State value",
      "id": "f2867b06-7b06-f286-067b-86f2067b86f2",
      "version": "Version value"
    }
  ]
}
```





