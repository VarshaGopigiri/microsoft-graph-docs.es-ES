---
title: Actualizar microsoftStoreForBusinessContainedApp
description: Actualizar las propiedades de un objeto microsoftStoreForBusinessContainedApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1250e6fd95caaa4e85761ce21d8db89faa139e81
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870010"
---
# <a name="update-microsoftstoreforbusinesscontainedapp"></a><span data-ttu-id="3be57-103">Actualizar microsoftStoreForBusinessContainedApp</span><span class="sxs-lookup"><span data-stu-id="3be57-103">Update microsoftStoreForBusinessContainedApp</span></span>

> <span data-ttu-id="3be57-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3be57-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3be57-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3be57-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3be57-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3be57-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3be57-107">Actualizar las propiedades de un objeto [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) .</span><span class="sxs-lookup"><span data-stu-id="3be57-107">Update the properties of a [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3be57-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3be57-108">Prerequisites</span></span>
<span data-ttu-id="3be57-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3be57-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3be57-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3be57-111">Permission type</span></span>|<span data-ttu-id="3be57-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3be57-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3be57-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3be57-113">Delegated (work or school account)</span></span>|<span data-ttu-id="3be57-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3be57-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3be57-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3be57-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3be57-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3be57-116">Not supported.</span></span>|
|<span data-ttu-id="3be57-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3be57-117">Application</span></span>|<span data-ttu-id="3be57-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3be57-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3be57-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3be57-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps/{mobileContainedAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.microsoftStoreForBusinessApp/containedApps/{mobileContainedAppId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.windowsUniversalAppX/committedContainedApps/{mobileContainedAppId}
```

## <a name="request-headers"></a><span data-ttu-id="3be57-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3be57-120">Request headers</span></span>
|<span data-ttu-id="3be57-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3be57-121">Header</span></span>|<span data-ttu-id="3be57-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3be57-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3be57-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="3be57-123">Authorization</span></span>|<span data-ttu-id="3be57-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3be57-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3be57-125">Accept</span><span class="sxs-lookup"><span data-stu-id="3be57-125">Accept</span></span>|<span data-ttu-id="3be57-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3be57-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3be57-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3be57-127">Request body</span></span>
<span data-ttu-id="3be57-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) .</span><span class="sxs-lookup"><span data-stu-id="3be57-128">In the request body, supply a JSON representation for the [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) object.</span></span>

<span data-ttu-id="3be57-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md).</span><span class="sxs-lookup"><span data-stu-id="3be57-129">The following table shows the properties that are required when you create the [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md).</span></span>

|<span data-ttu-id="3be57-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3be57-130">Property</span></span>|<span data-ttu-id="3be57-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="3be57-131">Type</span></span>|<span data-ttu-id="3be57-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3be57-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3be57-133">id</span><span class="sxs-lookup"><span data-stu-id="3be57-133">id</span></span>|<span data-ttu-id="3be57-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="3be57-134">String</span></span>|<span data-ttu-id="3be57-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3be57-135">Key of the entity.</span></span> <span data-ttu-id="3be57-136">Se hereda de [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span><span class="sxs-lookup"><span data-stu-id="3be57-136">Inherited from [mobileContainedApp](../resources/intune-apps-mobilecontainedapp.md)</span></span>|
|<span data-ttu-id="3be57-137">appUserModelId</span><span class="sxs-lookup"><span data-stu-id="3be57-137">appUserModelId</span></span>|<span data-ttu-id="3be57-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="3be57-138">String</span></span>|<span data-ttu-id="3be57-139">El identificador del modelo de usuario de aplicación de la aplicación contenido de un MicrosoftStoreForBusinessApp.</span><span class="sxs-lookup"><span data-stu-id="3be57-139">The app user model ID of the contained app of a MicrosoftStoreForBusinessApp.</span></span>|



## <a name="response"></a><span data-ttu-id="3be57-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3be57-140">Response</span></span>
<span data-ttu-id="3be57-141">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3be57-141">If successful, this method returns a `200 OK` response code and an updated [microsoftStoreForBusinessContainedApp](../resources/intune-apps-microsoftstoreforbusinesscontainedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3be57-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3be57-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="3be57-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3be57-143">Request</span></span>
<span data-ttu-id="3be57-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3be57-144">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/contentVersions/{mobileAppContentId}/containedApps/{mobileContainedAppId}
Content-type: application/json
Content-length: 51

{
  "appUserModelId": "App User Model Id value"
}
```

### <a name="response"></a><span data-ttu-id="3be57-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3be57-145">Response</span></span>
<span data-ttu-id="3be57-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3be57-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 176

{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessContainedApp",
  "id": "bf1d79df-79df-bf1d-df79-1dbfdf791dbf",
  "appUserModelId": "App User Model Id value"
}
```





