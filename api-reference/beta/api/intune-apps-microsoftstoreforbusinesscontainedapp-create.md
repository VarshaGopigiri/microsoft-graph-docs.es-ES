---
title: Crear microsoftStoreForBusinessContainedApp
description: Crear un nuevo objeto microsoftStoreForBusinessContainedApp.
ms.openlocfilehash: 131e510a1526879ffcb94c3782d9fa263dd4645c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085288"
---
# <a name="create-microsoftstoreforbusinesscontainedapp"></a><span data-ttu-id="7fd62-103">Crear microsoftStoreForBusinessContainedApp</span><span class="sxs-lookup"><span data-stu-id="7fd62-103">Create microsoftStoreForBusinessContainedApp</span></span>

> <span data-ttu-id="7fd62-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7fd62-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7fd62-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7fd62-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7fd62-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7fd62-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7fd62-107">Crear un nuevo objeto [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd62-107">Create a new [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7fd62-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7fd62-108">Prerequisites</span></span>
<span data-ttu-id="7fd62-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7fd62-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7fd62-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7fd62-111">Permission type</span></span>|<span data-ttu-id="7fd62-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7fd62-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7fd62-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7fd62-113">Delegated (work or school account)</span></span>|<span data-ttu-id="7fd62-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7fd62-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="7fd62-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7fd62-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7fd62-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7fd62-116">Not supported.</span></span>|
|<span data-ttu-id="7fd62-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7fd62-117">Application</span></span>|<span data-ttu-id="7fd62-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7fd62-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7fd62-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7fd62-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.microsoftStoreForBusinessApp/containedApps
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.windowsUniversalAppX/committedContainedApps
```

## <a name="request-headers"></a><span data-ttu-id="7fd62-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7fd62-120">Request headers</span></span>
|<span data-ttu-id="7fd62-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fd62-121">Header</span></span>|<span data-ttu-id="7fd62-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7fd62-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7fd62-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="7fd62-123">Authorization</span></span>|<span data-ttu-id="7fd62-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7fd62-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7fd62-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7fd62-125">Accept</span></span>|<span data-ttu-id="7fd62-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7fd62-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7fd62-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7fd62-127">Request body</span></span>
<span data-ttu-id="7fd62-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto microsoftStoreForBusinessContainedApp.</span><span class="sxs-lookup"><span data-stu-id="7fd62-128">In the request body, supply a JSON representation for the microsoftStoreForBusinessContainedApp object.</span></span>

<span data-ttu-id="7fd62-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el microsoftStoreForBusinessContainedApp.</span><span class="sxs-lookup"><span data-stu-id="7fd62-129">The following table shows the properties that are required when you create the microsoftStoreForBusinessContainedApp.</span></span>

|<span data-ttu-id="7fd62-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7fd62-130">Property</span></span>|<span data-ttu-id="7fd62-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="7fd62-131">Type</span></span>|<span data-ttu-id="7fd62-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fd62-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7fd62-133">id</span><span class="sxs-lookup"><span data-stu-id="7fd62-133">id</span></span>|<span data-ttu-id="7fd62-134">String</span><span class="sxs-lookup"><span data-stu-id="7fd62-134">String</span></span>|<span data-ttu-id="7fd62-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7fd62-135">Key of the entity.</span></span> <span data-ttu-id="7fd62-136">Se hereda de [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span><span class="sxs-lookup"><span data-stu-id="7fd62-136">Inherited from [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span></span>|
|<span data-ttu-id="7fd62-137">appUserModelId</span><span class="sxs-lookup"><span data-stu-id="7fd62-137">appUserModelId</span></span>|<span data-ttu-id="7fd62-138">String</span><span class="sxs-lookup"><span data-stu-id="7fd62-138">String</span></span>|<span data-ttu-id="7fd62-139">El identificador del modelo de usuario de aplicación de la aplicación contenido de un MicrosoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="7fd62-139">The app user model ID of the contained app of a MicrosoftStoreForBusinessApp.</span></span>|



## <a name="response"></a><span data-ttu-id="7fd62-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fd62-140">Response</span></span>
<span data-ttu-id="7fd62-141">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fd62-141">If successful, this method returns a `201 Created` response code and a [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7fd62-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7fd62-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="7fd62-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7fd62-143">Request</span></span>
<span data-ttu-id="7fd62-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7fd62-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps
Content-type: application/json
Content-length: 127

{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessContainedApp",
  "appUserModelId": "App User Model Id value"
}
```

### <a name="response"></a><span data-ttu-id="7fd62-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7fd62-145">Response</span></span>
<span data-ttu-id="7fd62-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7fd62-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 176

{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessContainedApp",
  "id": "bf1d79df-79df-bf1d-df79-1dbfdf791dbf",
  "appUserModelId": "App User Model Id value"
}
```




