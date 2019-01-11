---
title: Crear mobileAppContent
description: Cree un objeto mobileAppContent.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c59d06f506dd27a8aa7b4731df94e0bed2c5480f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831202"
---
# <a name="create-mobileappcontent"></a><span data-ttu-id="6250d-103">Crear mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="6250d-103">Create mobileAppContent</span></span>

> <span data-ttu-id="6250d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6250d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6250d-105">Cree un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="6250d-105">Create a new [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6250d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6250d-106">Prerequisites</span></span>
<span data-ttu-id="6250d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6250d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6250d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6250d-109">Permission type</span></span>|<span data-ttu-id="6250d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6250d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6250d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6250d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6250d-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6250d-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="6250d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6250d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6250d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6250d-114">Not supported.</span></span>|
|<span data-ttu-id="6250d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6250d-115">Application</span></span>|<span data-ttu-id="6250d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6250d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6250d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6250d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.mobileLobApp/contentVersions
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.managedMobileLobApp/contentVersions
```

## <a name="request-headers"></a><span data-ttu-id="6250d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6250d-118">Request headers</span></span>
|<span data-ttu-id="6250d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6250d-119">Header</span></span>|<span data-ttu-id="6250d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6250d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6250d-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="6250d-121">Authorization</span></span>|<span data-ttu-id="6250d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6250d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6250d-123">Accept</span><span class="sxs-lookup"><span data-stu-id="6250d-123">Accept</span></span>|<span data-ttu-id="6250d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6250d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6250d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6250d-125">Request body</span></span>
<span data-ttu-id="6250d-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppContent.</span><span class="sxs-lookup"><span data-stu-id="6250d-126">In the request body, supply a JSON representation for the mobileAppContent object.</span></span>

<span data-ttu-id="6250d-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppContent.</span><span class="sxs-lookup"><span data-stu-id="6250d-127">The following table shows the properties that are required when you create the mobileAppContent.</span></span>

|<span data-ttu-id="6250d-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6250d-128">Property</span></span>|<span data-ttu-id="6250d-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="6250d-129">Type</span></span>|<span data-ttu-id="6250d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="6250d-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6250d-131">id</span><span class="sxs-lookup"><span data-stu-id="6250d-131">id</span></span>|<span data-ttu-id="6250d-132">String</span><span class="sxs-lookup"><span data-stu-id="6250d-132">String</span></span>|<span data-ttu-id="6250d-133">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6250d-133">The app content version.</span></span>|



## <a name="response"></a><span data-ttu-id="6250d-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6250d-134">Response</span></span>
<span data-ttu-id="6250d-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6250d-135">If successful, this method returns a `201 Created` response code and a [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6250d-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6250d-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="6250d-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6250d-137">Request</span></span>
<span data-ttu-id="6250d-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6250d-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions
Content-type: application/json
Content-length: 58

{
  "@odata.type": "#microsoft.graph.mobileAppContent"
}
```

### <a name="response"></a><span data-ttu-id="6250d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6250d-139">Response</span></span>
<span data-ttu-id="6250d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6250d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "fe0bb9a9-b9a9-fe0b-a9b9-0bfea9b90bfe"
}
```



