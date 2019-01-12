---
title: Crear mobileAppContent
description: Cree un objeto mobileAppContent.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8904626782e6df7a0fd6f367f0e0878328a07faf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921895"
---
# <a name="create-mobileappcontent"></a><span data-ttu-id="0cc0e-103">Crear mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="0cc0e-103">Create mobileAppContent</span></span>

> <span data-ttu-id="0cc0e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0cc0e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0cc0e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0cc0e-107">Cree un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="0cc0e-107">Create a new [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0cc0e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0cc0e-108">Prerequisites</span></span>
<span data-ttu-id="0cc0e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0cc0e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0cc0e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0cc0e-111">Permission type</span></span>|<span data-ttu-id="0cc0e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0cc0e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0cc0e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0cc0e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0cc0e-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0cc0e-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0cc0e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0cc0e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0cc0e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-116">Not supported.</span></span>|
|<span data-ttu-id="0cc0e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0cc0e-117">Application</span></span>|<span data-ttu-id="0cc0e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0cc0e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0cc0e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.mobileLobApp/contentVersions
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.managedMobileLobApp/contentVersions
```

## <a name="request-headers"></a><span data-ttu-id="0cc0e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0cc0e-120">Request headers</span></span>
|<span data-ttu-id="0cc0e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cc0e-121">Header</span></span>|<span data-ttu-id="0cc0e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0cc0e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0cc0e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0cc0e-123">Authorization</span></span>|<span data-ttu-id="0cc0e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0cc0e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="0cc0e-125">Accept</span></span>|<span data-ttu-id="0cc0e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0cc0e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0cc0e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0cc0e-127">Request body</span></span>
<span data-ttu-id="0cc0e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto mobileAppContent.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-128">In the request body, supply a JSON representation for the mobileAppContent object.</span></span>

<span data-ttu-id="0cc0e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto mobileAppContent.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-129">The following table shows the properties that are required when you create the mobileAppContent.</span></span>

|<span data-ttu-id="0cc0e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0cc0e-130">Property</span></span>|<span data-ttu-id="0cc0e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0cc0e-131">Type</span></span>|<span data-ttu-id="0cc0e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cc0e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0cc0e-133">id</span><span class="sxs-lookup"><span data-stu-id="0cc0e-133">id</span></span>|<span data-ttu-id="0cc0e-134">String</span><span class="sxs-lookup"><span data-stu-id="0cc0e-134">String</span></span>|<span data-ttu-id="0cc0e-135">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-135">The app content version.</span></span>|



## <a name="response"></a><span data-ttu-id="0cc0e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cc0e-136">Response</span></span>
<span data-ttu-id="0cc0e-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [mobileAppContent](../resources/intune-apps-mobileappcontent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-137">If successful, this method returns a `201 Created` response code and a [mobileAppContent](../resources/intune-apps-mobileappcontent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0cc0e-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0cc0e-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="0cc0e-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0cc0e-139">Request</span></span>
<span data-ttu-id="0cc0e-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions
Content-type: application/json
Content-length: 58

{
  "@odata.type": "#microsoft.graph.mobileAppContent"
}
```

### <a name="response"></a><span data-ttu-id="0cc0e-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0cc0e-141">Response</span></span>
<span data-ttu-id="0cc0e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0cc0e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "fe0bb9a9-b9a9-fe0b-a9b9-0bfea9b90bfe"
}
```





