---
title: Actualizar mobileAppContent
description: Actualice las propiedades de un objeto mobileAppContent.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: fa5f9295d70124633728e5816c2d506d6f5aeff0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831181"
---
# <a name="update-mobileappcontent"></a><span data-ttu-id="98a34-103">Actualizar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="98a34-103">Update mobileAppContent</span></span>

> <span data-ttu-id="98a34-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="98a34-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="98a34-105">Actualice las propiedades de un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="98a34-105">Update the properties of a [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="98a34-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="98a34-106">Prerequisites</span></span>
<span data-ttu-id="98a34-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="98a34-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="98a34-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98a34-109">Permission type</span></span>|<span data-ttu-id="98a34-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98a34-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="98a34-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98a34-111">Delegated (work or school account)</span></span>|<span data-ttu-id="98a34-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="98a34-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="98a34-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98a34-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="98a34-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98a34-114">Not supported.</span></span>|
|<span data-ttu-id="98a34-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98a34-115">Application</span></span>|<span data-ttu-id="98a34-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98a34-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="98a34-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98a34-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.mobileLobApp/contentVersions/{mobileAppContentId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.managedMobileLobApp/contentVersions/{mobileAppContentId}
```

## <a name="request-headers"></a><span data-ttu-id="98a34-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98a34-118">Request headers</span></span>
|<span data-ttu-id="98a34-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98a34-119">Header</span></span>|<span data-ttu-id="98a34-120">Valor</span><span class="sxs-lookup"><span data-stu-id="98a34-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="98a34-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="98a34-121">Authorization</span></span>|<span data-ttu-id="98a34-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="98a34-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="98a34-123">Accept</span><span class="sxs-lookup"><span data-stu-id="98a34-123">Accept</span></span>|<span data-ttu-id="98a34-124">application/json</span><span class="sxs-lookup"><span data-stu-id="98a34-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="98a34-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98a34-125">Request body</span></span>
<span data-ttu-id="98a34-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="98a34-126">In the request body, supply a JSON representation for the [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>

<span data-ttu-id="98a34-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="98a34-127">The following table shows the properties that are required when you create the [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span></span>

|<span data-ttu-id="98a34-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98a34-128">Property</span></span>|<span data-ttu-id="98a34-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="98a34-129">Type</span></span>|<span data-ttu-id="98a34-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="98a34-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="98a34-131">id</span><span class="sxs-lookup"><span data-stu-id="98a34-131">id</span></span>|<span data-ttu-id="98a34-132">String</span><span class="sxs-lookup"><span data-stu-id="98a34-132">String</span></span>|<span data-ttu-id="98a34-133">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98a34-133">The app content version.</span></span>|



## <a name="response"></a><span data-ttu-id="98a34-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98a34-134">Response</span></span>
<span data-ttu-id="98a34-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98a34-135">If successful, this method returns a `200 OK` response code and an updated [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98a34-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98a34-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="98a34-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98a34-137">Request</span></span>
<span data-ttu-id="98a34-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98a34-138">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}
Content-type: application/json
Content-length: 58

{
  "@odata.type": "#microsoft.graph.mobileAppContent"
}
```

### <a name="response"></a><span data-ttu-id="98a34-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98a34-139">Response</span></span>
<span data-ttu-id="98a34-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98a34-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "fe0bb9a9-b9a9-fe0b-a9b9-0bfea9b90bfe"
}
```



