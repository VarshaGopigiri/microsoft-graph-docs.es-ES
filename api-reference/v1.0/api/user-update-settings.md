---
title: Configuración de actualización
description: 'Actualizar las propiedades del objeto settings. '
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: be8ed27ecff80017cab56e1d3d20755cf68351cc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980275"
---
# <a name="update-settings"></a><span data-ttu-id="c7eb0-103">Configuración de actualización</span><span class="sxs-lookup"><span data-stu-id="c7eb0-103">Update settings</span></span>

<span data-ttu-id="c7eb0-104">Actualizar las propiedades del objeto [settings](../resources/user-settings.md) .</span><span class="sxs-lookup"><span data-stu-id="c7eb0-104">Update the properties of the [settings](../resources/user-settings.md) object.</span></span> <span data-ttu-id="c7eb0-105">Los usuarios en la misma organización pueden tener diferentes configuraciones basadas en sus preferencias o en las directivas de la organización.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-105">Users in the same organization can have different settings based on their preference or on the organization policies.</span></span> <span data-ttu-id="c7eb0-106">Para obtener al usuario actual configuración, vea [Configuración del usuario actual](user-get-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c7eb0-106">To get the user current settings, see [current user settings](user-get-settings.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="c7eb0-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="c7eb0-107">Permissions</span></span>

<span data-ttu-id="c7eb0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7eb0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7eb0-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7eb0-110">Permission type</span></span>      | <span data-ttu-id="c7eb0-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7eb0-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c7eb0-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7eb0-112">Delegated (work or school account)</span></span> | <span data-ttu-id="c7eb0-113">User.ReadWrite, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7eb0-113">User.ReadWrite, User.ReadWrite.All</span></span>   |
|<span data-ttu-id="c7eb0-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7eb0-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c7eb0-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-115">Not supported.</span></span>    |
|<span data-ttu-id="c7eb0-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7eb0-116">Application</span></span> | <span data-ttu-id="c7eb0-117">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7eb0-117">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c7eb0-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7eb0-118">HTTP request</span></span>

```http
PATCH https://graph.microsoft.com/v1.0/me/settings
```

<span data-ttu-id="c7eb0-119">Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-119">Request with a 'user id' or 'userPrincipalName' is only accessible by the user or by a user with the User.ReadWrite.All permissions.</span></span> <span data-ttu-id="c7eb0-120">Para obtener más información, vea [permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7eb0-120">To learn more, see [Permissions](/graph/permissions-reference).</span></span> 

```http
PATCH https://graph.microsoft.com/v1.0/users/{id | userPrincipalName}/settings/
```

## <a name="request-headers"></a><span data-ttu-id="c7eb0-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7eb0-121">Request headers</span></span>

| <span data-ttu-id="c7eb0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7eb0-122">Header</span></span>       | <span data-ttu-id="c7eb0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c7eb0-123">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="c7eb0-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7eb0-124">Authorization</span></span>  | <span data-ttu-id="c7eb0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c7eb0-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c7eb0-127">Content-Type</span></span>  | <span data-ttu-id="c7eb0-128">application/json</span><span class="sxs-lookup"><span data-stu-id="c7eb0-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c7eb0-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7eb0-129">Request body</span></span>

<span data-ttu-id="c7eb0-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c7eb0-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c7eb0-133">Property</span></span>     | <span data-ttu-id="c7eb0-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7eb0-134">Type</span></span>   |<span data-ttu-id="c7eb0-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7eb0-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c7eb0-136">contributionToContentDiscoveryDisabled</span><span class="sxs-lookup"><span data-stu-id="c7eb0-136">contributionToContentDiscoveryDisabled</span></span>|<span data-ttu-id="c7eb0-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7eb0-137">Boolean</span></span>|<span data-ttu-id="c7eb0-138">En el valor true deshabilita el acceso de delegado a la API de [tendencias](/graph/api/resources/insights-trending?view=graph-rest-beta) y deshabilitar el acceso a los documentos de Office profundizar para el usuario.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-138">Set to true do disable delegate access to the [Trending](/graph/api/resources/insights-trending?view=graph-rest-beta) API and to disable access to documents in Office Delve for the user.</span></span> <span data-ttu-id="c7eb0-139">Configuración en true también afecta a la relevancia del contenido que se muestra en Office 365: por ejemplo, los sitios que se sugiere en la página principal de SharePoint y la vista de detección en OneDrive para la empresa muestran resultados menos relevantes.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-139">Setting to true also affects the relevance of the content displayed in Office 365 - for example, Suggested sites in SharePoint Home and the Discover view in OneDrive for Business show less relevant results.</span></span> <span data-ttu-id="c7eb0-140">Esta configuración refleja el estado de control en [Office profundizar](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span><span class="sxs-lookup"><span data-stu-id="c7eb0-140">This setting reflects the control state in [Office Delve](https://support.office.com/en-us/article/are-my-documents-safe-in-office-delve-f5f409a2-37ed-4452-8f61-681e5e1836f3?ui=en-US&rs=en-US&ad=US#bkmk_optout).</span></span>|

## <a name="example"></a><span data-ttu-id="c7eb0-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7eb0-141">Example</span></span> 

##### <a name="request"></a><span data-ttu-id="c7eb0-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7eb0-142">Request</span></span>

<span data-ttu-id="c7eb0-143">Este es un ejemplo de solicitud en cómo voluntaria de un usuario desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-143">Here is an example request on how to opt-out a user from Delve and disable his contribution on content relevancy for the whole organization.</span></span>

```http
PATCH https://graph.microsoft.com/v1.0/me/settings
Content-type: application/json
Content-length: 37

{
  "contributionToContentDiscoveryDisabled": true
}
```

##### <a name="response"></a><span data-ttu-id="c7eb0-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7eb0-144">Response</span></span>

<span data-ttu-id="c7eb0-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": true
}
```

#### <a name="batch-request"></a><span data-ttu-id="c7eb0-148">Solicitud de lote</span><span class="sxs-lookup"><span data-stu-id="c7eb0-148">Batch request</span></span>

<span data-ttu-id="c7eb0-149">También es posible voluntaria de varios usuarios desde Delve y deshabilitar su contribución en la relevancia de contenido para toda la organización a través de una solicitud por lotes.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-149">It's also possible to opt-out multiple users from Delve and disable their contribution on content relevancy for the whole organization through a batch request.</span></span>
<span data-ttu-id="c7eb0-150">Para obtener más información, vea [el procesamiento por lotes de JSON](https://developer.microsoft.com/graph/docs/concepts/json_batching).</span><span class="sxs-lookup"><span data-stu-id="c7eb0-150">To learn more, see [JSON batching](https://developer.microsoft.com/graph/docs/concepts/json_batching).</span></span>

<span data-ttu-id="c7eb0-151">**Importante**: sólo los miembros del grupo de roles de [Administración de la organización](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) pueden actualizar varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="c7eb0-151">**Important**: Only members of the [Organization Management](https://support.office.com/article/permissions-in-the-office-365-security-compliance-center-d10608af-7934-490a-818e-e68f17d0e9c1?ui=en-US&rs=en-US&ad=US) role group can update multiple users.</span></span> 



