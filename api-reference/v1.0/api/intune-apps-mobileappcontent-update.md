---
title: Actualizar mobileAppContent
description: Actualice las propiedades de un objeto mobileAppContent.
ms.openlocfilehash: f3e764866165c544fee7120978a0cef872f98d23
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029830"
---
# <a name="update-mobileappcontent"></a><span data-ttu-id="f9628-103">Actualizar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="f9628-103">Update mobileAppContent</span></span>

> <span data-ttu-id="f9628-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f9628-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f9628-105">Actualice las propiedades de un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="f9628-105">Update the properties of a [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f9628-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9628-106">Prerequisites</span></span>
<span data-ttu-id="f9628-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9628-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9628-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9628-109">Permission type</span></span>|<span data-ttu-id="f9628-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9628-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f9628-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9628-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f9628-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9628-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f9628-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9628-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f9628-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9628-114">Not supported.</span></span>|
|<span data-ttu-id="f9628-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9628-115">Application</span></span>|<span data-ttu-id="f9628-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9628-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f9628-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9628-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.mobileLobApp/contentVersions/{mobileAppContentId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.managedMobileLobApp/contentVersions/{mobileAppContentId}
```

## <a name="request-headers"></a><span data-ttu-id="f9628-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9628-118">Request headers</span></span>
|<span data-ttu-id="f9628-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9628-119">Header</span></span>|<span data-ttu-id="f9628-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f9628-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f9628-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9628-121">Authorization</span></span>|<span data-ttu-id="f9628-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f9628-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f9628-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f9628-123">Accept</span></span>|<span data-ttu-id="f9628-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f9628-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9628-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9628-125">Request body</span></span>
<span data-ttu-id="f9628-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="f9628-126">In the request body, supply a JSON representation for the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>

<span data-ttu-id="f9628-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="f9628-127">The following table shows the properties that are required when you create the [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span></span>

|<span data-ttu-id="f9628-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9628-128">Property</span></span>|<span data-ttu-id="f9628-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9628-129">Type</span></span>|<span data-ttu-id="f9628-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9628-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f9628-131">id</span><span class="sxs-lookup"><span data-stu-id="f9628-131">id</span></span>|<span data-ttu-id="f9628-132">String</span><span class="sxs-lookup"><span data-stu-id="f9628-132">String</span></span>|<span data-ttu-id="f9628-133">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9628-133">The app content version.</span></span>|



## <a name="response"></a><span data-ttu-id="f9628-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9628-134">Response</span></span>
<span data-ttu-id="f9628-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9628-135">If successful, this method returns a `200 OK` response code and an updated [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9628-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9628-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="f9628-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9628-137">Request</span></span>
<span data-ttu-id="f9628-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9628-138">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}
Content-type: application/json
Content-length: 58

{
  "@odata.type": "#microsoft.graph.mobileAppContent"
}
```

### <a name="response"></a><span data-ttu-id="f9628-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9628-139">Response</span></span>
<span data-ttu-id="f9628-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9628-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "fe0bb9a9-b9a9-fe0b-a9b9-0bfea9b90bfe"
}
```


