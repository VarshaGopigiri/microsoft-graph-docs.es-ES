---
title: Crear iosVppAppAssignedUserLicense
description: Crear un nuevo objeto iosVppAppAssignedUserLicense.
ms.openlocfilehash: 0a4bdad168dcb3baa633cf918ac12b6730e7f61b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089091"
---
# <a name="create-iosvppappassigneduserlicense"></a><span data-ttu-id="75347-103">Crear iosVppAppAssignedUserLicense</span><span class="sxs-lookup"><span data-stu-id="75347-103">Create iosVppAppAssignedUserLicense</span></span>

> <span data-ttu-id="75347-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75347-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75347-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75347-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="75347-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="75347-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="75347-107">Crear un nuevo objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="75347-107">Create a new [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="75347-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="75347-108">Prerequisites</span></span>
<span data-ttu-id="75347-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75347-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="75347-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="75347-111">Permission type</span></span>|<span data-ttu-id="75347-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="75347-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="75347-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="75347-113">Delegated (work or school account)</span></span>|<span data-ttu-id="75347-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="75347-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="75347-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="75347-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="75347-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75347-116">Not supported.</span></span>|
|<span data-ttu-id="75347-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="75347-117">Application</span></span>|<span data-ttu-id="75347-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75347-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="75347-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="75347-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/microsoft.graph.iosVppApp/assignedLicenses
```

## <a name="request-headers"></a><span data-ttu-id="75347-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="75347-120">Request headers</span></span>
|<span data-ttu-id="75347-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75347-121">Header</span></span>|<span data-ttu-id="75347-122">Valor</span><span class="sxs-lookup"><span data-stu-id="75347-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="75347-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="75347-123">Authorization</span></span>|<span data-ttu-id="75347-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="75347-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="75347-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="75347-125">Accept</span></span>|<span data-ttu-id="75347-126">application/json</span><span class="sxs-lookup"><span data-stu-id="75347-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="75347-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="75347-127">Request body</span></span>
<span data-ttu-id="75347-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosVppAppAssignedUserLicense.</span><span class="sxs-lookup"><span data-stu-id="75347-128">In the request body, supply a JSON representation for the iosVppAppAssignedUserLicense object.</span></span>

<span data-ttu-id="75347-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosVppAppAssignedUserLicense.</span><span class="sxs-lookup"><span data-stu-id="75347-129">The following table shows the properties that are required when you create the iosVppAppAssignedUserLicense.</span></span>

|<span data-ttu-id="75347-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75347-130">Property</span></span>|<span data-ttu-id="75347-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="75347-131">Type</span></span>|<span data-ttu-id="75347-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="75347-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75347-133">id</span><span class="sxs-lookup"><span data-stu-id="75347-133">id</span></span>|<span data-ttu-id="75347-134">String</span><span class="sxs-lookup"><span data-stu-id="75347-134">String</span></span>|<span data-ttu-id="75347-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="75347-135">Key of the entity.</span></span> <span data-ttu-id="75347-136">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="75347-136">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="75347-137">userEmailAddress</span><span class="sxs-lookup"><span data-stu-id="75347-137">userEmailAddress</span></span>|<span data-ttu-id="75347-138">String</span><span class="sxs-lookup"><span data-stu-id="75347-138">String</span></span>|<span data-ttu-id="75347-139">La dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="75347-139">The user email address.</span></span> <span data-ttu-id="75347-140">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="75347-140">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="75347-141">userId</span><span class="sxs-lookup"><span data-stu-id="75347-141">userId</span></span>|<span data-ttu-id="75347-142">String</span><span class="sxs-lookup"><span data-stu-id="75347-142">String</span></span>|<span data-ttu-id="75347-143">El identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="75347-143">The user ID.</span></span> <span data-ttu-id="75347-144">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="75347-144">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="75347-145">userName</span><span class="sxs-lookup"><span data-stu-id="75347-145">userName</span></span>|<span data-ttu-id="75347-146">String</span><span class="sxs-lookup"><span data-stu-id="75347-146">String</span></span>|<span data-ttu-id="75347-147">El nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="75347-147">The user name.</span></span> <span data-ttu-id="75347-148">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="75347-148">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|
|<span data-ttu-id="75347-149">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="75347-149">userPrincipalName</span></span>|<span data-ttu-id="75347-150">String</span><span class="sxs-lookup"><span data-stu-id="75347-150">String</span></span>|<span data-ttu-id="75347-151">El nombre principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="75347-151">The user principal name.</span></span> <span data-ttu-id="75347-152">Se hereda de [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span><span class="sxs-lookup"><span data-stu-id="75347-152">Inherited from [iosVppAppAssignedLicense](../resources/intune-apps-iosvppappassignedlicense.md)</span></span>|



## <a name="response"></a><span data-ttu-id="75347-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75347-153">Response</span></span>
<span data-ttu-id="75347-154">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75347-154">If successful, this method returns a `201 Created` response code and a [iosVppAppAssignedUserLicense](../resources/intune-apps-iosvppappassigneduserlicense.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75347-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="75347-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="75347-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="75347-156">Request</span></span>
<span data-ttu-id="75347-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="75347-157">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="75347-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75347-158">Response</span></span>
<span data-ttu-id="75347-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="75347-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





