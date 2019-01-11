---
title: Crear iosVppAppAssignedUserLicense
description: Crear un nuevo objeto iosVppAppAssignedUserLicense.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2e6178570da6e89ef50c933d027daa2a9d7e1adf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27864655"
---
# <a name="create-iosvppappassigneduserlicense"></a><span data-ttu-id="d30e7-103">Crear iosVppAppAssignedUserLicense</span><span class="sxs-lookup"><span data-stu-id="d30e7-103">Create iosVppAppAssignedUserLicense</span></span>

> <span data-ttu-id="d30e7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d30e7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d30e7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d30e7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d30e7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d30e7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d30e7-107">Crear un nuevo objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="d30e7-107">Create a new [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d30e7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d30e7-108">Prerequisites</span></span>
<span data-ttu-id="d30e7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d30e7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d30e7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d30e7-111">Permission type</span></span>|<span data-ttu-id="d30e7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d30e7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d30e7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d30e7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d30e7-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d30e7-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d30e7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d30e7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d30e7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d30e7-116">Not supported.</span></span>|
|<span data-ttu-id="d30e7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d30e7-117">Application</span></span>|<span data-ttu-id="d30e7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d30e7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d30e7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d30e7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

## <a name="request-headers"></a><span data-ttu-id="d30e7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d30e7-120">Request headers</span></span>
|<span data-ttu-id="d30e7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d30e7-121">Header</span></span>|<span data-ttu-id="d30e7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d30e7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d30e7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d30e7-123">Authorization</span></span>|<span data-ttu-id="d30e7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d30e7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d30e7-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d30e7-125">Accept</span></span>|<span data-ttu-id="d30e7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d30e7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d30e7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d30e7-127">Request body</span></span>
<span data-ttu-id="d30e7-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosVppAppAssignedUserLicense.</span><span class="sxs-lookup"><span data-stu-id="d30e7-128">In the request body, supply a JSON representation for the iosVppAppAssignedUserLicense object.</span></span>

<span data-ttu-id="d30e7-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosVppAppAssignedUserLicense.</span><span class="sxs-lookup"><span data-stu-id="d30e7-129">The following table shows the properties that are required when you create the iosVppAppAssignedUserLicense.</span></span>

|<span data-ttu-id="d30e7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d30e7-130">Property</span></span>|<span data-ttu-id="d30e7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d30e7-131">Type</span></span>|<span data-ttu-id="d30e7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d30e7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d30e7-133">id</span><span class="sxs-lookup"><span data-stu-id="d30e7-133">id</span></span>|<span data-ttu-id="d30e7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d30e7-134">String</span></span>|<span data-ttu-id="d30e7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d30e7-135">Key of the entity.</span></span> <span data-ttu-id="d30e7-136">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="d30e7-136">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="d30e7-137">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d30e7-137">userEmailAddress</span></span>|<span data-ttu-id="d30e7-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="d30e7-138">String</span></span>|<span data-ttu-id="d30e7-139">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="d30e7-139">The user email address.</span></span> <span data-ttu-id="d30e7-140">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="d30e7-140">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="d30e7-141">userId</span><span class="sxs-lookup"><span data-stu-id="d30e7-141">userId</span></span>|<span data-ttu-id="d30e7-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="d30e7-142">String</span></span>|<span data-ttu-id="d30e7-143">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="d30e7-143">The user ID.</span></span> <span data-ttu-id="d30e7-144">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="d30e7-144">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="d30e7-145">userName</span><span class="sxs-lookup"><span data-stu-id="d30e7-145">userName</span></span>|<span data-ttu-id="d30e7-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="d30e7-146">String</span></span>|<span data-ttu-id="d30e7-147">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="d30e7-147">The user name.</span></span> <span data-ttu-id="d30e7-148">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="d30e7-148">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="d30e7-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d30e7-149">userPrincipalName</span></span>|<span data-ttu-id="d30e7-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="d30e7-150">String</span></span>|<span data-ttu-id="d30e7-151">El nombre principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="d30e7-151">The user principal name.</span></span> <span data-ttu-id="d30e7-152">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="d30e7-152">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|



## <a name="response"></a><span data-ttu-id="d30e7-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d30e7-153">Response</span></span>
<span data-ttu-id="d30e7-154">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d30e7-154">If successful, this method returns a `201 Created` response code and a [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d30e7-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d30e7-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="d30e7-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d30e7-156">Request</span></span>
<span data-ttu-id="d30e7-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d30e7-157">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
Content-type: application/json
Content-length: 238

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedUserLicense",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="d30e7-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d30e7-158">Response</span></span>
<span data-ttu-id="d30e7-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d30e7-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 287

{
  "@odata.type": "#microsoft.graph.iosVppAppAssignedUserLicense",
  "id": "fedc747d-747d-fedc-7d74-dcfe7d74dcfe",
  "userEmailAddress": "User Email Address value",
  "userId": "User Id value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value"
}
```





