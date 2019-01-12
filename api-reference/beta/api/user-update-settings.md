---
title: Configuración de actualización
description: 'Actualizar las propiedades del objeto settings. '
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 8f538d298f71ad7ef537988a29bae812015566ec
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913229"
---
# <a name="update-settings"></a><span data-ttu-id="ba6b2-103">Configuración de actualización</span><span class="sxs-lookup"><span data-stu-id="ba6b2-103">Update settings</span></span>

> <span data-ttu-id="ba6b2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ba6b2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ba6b2-106">Actualizar las propiedades del objeto [settings](../resources/user-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="ba6b2-106">Update the properties of the [settings](../resources/user-settings.md) object.</span></span> <span data-ttu-id="ba6b2-107">Los usuarios en la misma organización pueden tener diferentes configuraciones basadas en sus preferencias o en las directivas de la organización.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-107">Users in the same organization can have different settings based on their preference or on the organization policies.</span></span> <span data-ttu-id="ba6b2-108">Para obtener al usuario actual configuración, vea [Configuración del usuario actual](user-get-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ba6b2-108">To get the user current settings, see [current user settings](user-get-settings.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="ba6b2-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="ba6b2-109">Permissions</span></span>

<span data-ttu-id="ba6b2-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba6b2-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba6b2-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba6b2-112">Permission type</span></span>      | <span data-ttu-id="ba6b2-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba6b2-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ba6b2-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba6b2-114">Delegated (work or school account)</span></span> | <span data-ttu-id="ba6b2-115">User.ReadWrite, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba6b2-115">User.ReadWrite, User.ReadWrite.All</span></span>   |
|<span data-ttu-id="ba6b2-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba6b2-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ba6b2-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-117">Not supported.</span></span>    |
|<span data-ttu-id="ba6b2-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba6b2-118">Application</span></span> | <span data-ttu-id="ba6b2-119">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ba6b2-119">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ba6b2-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba6b2-120">HTTP request</span></span>

```http
PATCH https://graph.microsoft.com/beta/me/settings
```

<span data-ttu-id="ba6b2-121">Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-121">Request with a 'user id' or 'userPrincipalName' is only accessible by the user or by a user with the User.ReadWrite.All permissions.</span></span> <span data-ttu-id="ba6b2-122">Para obtener más información, vea [permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba6b2-122">To learn more, see [Permissions](/graph/permissions-reference).</span></span> 

```http
PATCH https://graph.microsoft.com/beta/users/{id | userPrincipalName}/settings/
```

## <a name="request-headers"></a><span data-ttu-id="ba6b2-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba6b2-123">Request headers</span></span>

| <span data-ttu-id="ba6b2-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba6b2-124">Header</span></span>       | <span data-ttu-id="ba6b2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ba6b2-125">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="ba6b2-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="ba6b2-126">Authorization</span></span>  | <span data-ttu-id="ba6b2-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ba6b2-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ba6b2-129">Content-Type</span></span>  | <span data-ttu-id="ba6b2-130">application/json</span><span class="sxs-lookup"><span data-stu-id="ba6b2-130">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ba6b2-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba6b2-131">Request body</span></span>

<span data-ttu-id="ba6b2-p106">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-p106">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="ba6b2-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ba6b2-135">Property</span></span>     | <span data-ttu-id="ba6b2-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba6b2-136">Type</span></span>   |<span data-ttu-id="ba6b2-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba6b2-137">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ba6b2-138">contributionToContentDiscoveryDisabled</span><span class="sxs-lookup"><span data-stu-id="ba6b2-138">contributionToContentDiscoveryDisabled</span></span>|<span data-ttu-id="ba6b2-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="ba6b2-139">Boolean</span></span>|<span data-ttu-id="ba6b2-140">En el valor true deshabilita el acceso de delegado a la API de [tendencias](../resources/insights-trending.md) y deshabilitar el acceso a los documentos de Office profundizar para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-140">Set to true do disable delegate access to the [Trending](../resources/insights-trending.md) API and to disable access to documents in Office Delve for the user.</span></span> <span data-ttu-id="ba6b2-141">Configuración en true también afecta a la relevancia del contenido que se muestra en Office 365: por ejemplo, los sitios que se sugiere en la página principal de SharePoint y la vista de detección en OneDrive para la empresa muestran resultados menos relevantes.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-141">Setting to true also affects the relevance of the content displayed in Office 365 - for example, Suggested sites in SharePoint Home and the Discover view in OneDrive for Business show less relevant results.</span></span> <span data-ttu-id="ba6b2-142">Esta configuración refleja el estado de control en [Office profundizar](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span><span class="sxs-lookup"><span data-stu-id="ba6b2-142">This setting reflects the control state in [Office Delve](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span></span>|

## <a name="example"></a><span data-ttu-id="ba6b2-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba6b2-143">Example</span></span> 

##### <a name="request"></a><span data-ttu-id="ba6b2-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba6b2-144">Request</span></span>

<span data-ttu-id="ba6b2-145">Este es un ejemplo de solicitud en cómo voluntaria de un usuario desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-145">Here is an example request on how to opt-out a user from Delve and disable his contribution on content relevancy for the whole organization.</span></span>

```http
PATCH https://graph.microsoft.com/beta/me/settings
Content-type: application/json
Content-length: 37

{
  "contributionToContentDiscoveryDisabled": true
}
```

##### <a name="response"></a><span data-ttu-id="ba6b2-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba6b2-146">Response</span></span>

<span data-ttu-id="ba6b2-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": true
}
```

#### <a name="batch-request"></a><span data-ttu-id="ba6b2-150">Solicitud de lote</span><span class="sxs-lookup"><span data-stu-id="ba6b2-150">Batch request</span></span>

<span data-ttu-id="ba6b2-151">También es posible voluntaria de varios usuarios desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización a través de una solicitud por lotes.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-151">It's also possible to opt-out multiple users from Delve and disable their contribution on content relevancy for the whole organization through a batch request.</span></span>
<span data-ttu-id="ba6b2-152">Para obtener más información, vea [el procesamiento por lotes de JSON](/graph/json-batching).</span><span class="sxs-lookup"><span data-stu-id="ba6b2-152">To learn more, see [JSON batching](/graph/json-batching).</span></span>

<span data-ttu-id="ba6b2-153">**Importante**: sólo los miembros del grupo de roles de [Administración de la organización](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) pueden actualizar varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="ba6b2-153">**Important**: Only members of the [Organization Management](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) role group can update multiple users.</span></span> 


