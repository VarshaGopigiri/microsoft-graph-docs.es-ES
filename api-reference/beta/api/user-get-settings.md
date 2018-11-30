---
title: Obtener la configuración
description: Leer el objeto de configuración de usuario y de organización.
ms.openlocfilehash: dc0f5e23f1c00291af90a1e2f685d947046b925f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088486"
---
# <a name="get-settings"></a><span data-ttu-id="75545-103">Obtener la configuración</span><span class="sxs-lookup"><span data-stu-id="75545-103">Get settings</span></span>

> <span data-ttu-id="75545-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75545-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75545-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75545-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="75545-106">Leer el objeto de [configuración de](../resources/user-settings.md) usuario y de organización.</span><span class="sxs-lookup"><span data-stu-id="75545-106">Read the user and organization [settings](../resources/user-settings.md) object.</span></span>
<span data-ttu-id="75545-107">Para obtener más información acerca de cómo actualizar las propiedades del objeto de [configuración](../resources/user-settings.md) , consulte [actualización de la configuración de usuario](user-update-settings.md).</span><span class="sxs-lookup"><span data-stu-id="75545-107">To learn how to update the properties of the [settings](../resources/user-settings.md) object, see [update user settings](user-update-settings.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="75545-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="75545-108">Permissions</span></span>

<span data-ttu-id="75545-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75545-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="75545-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="75545-111">Permission type</span></span>      | <span data-ttu-id="75545-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="75545-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="75545-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="75545-113">Delegated (work or school account)</span></span> | <span data-ttu-id="75545-114">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="75545-114">User.Read.All, User.ReadWrite.All</span></span>    |
|<span data-ttu-id="75545-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="75545-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="75545-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75545-116">Not supported.</span></span>    |
|<span data-ttu-id="75545-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="75545-117">Application</span></span> | <span data-ttu-id="75545-118">User.Read.All,User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="75545-118">User.Read.All,User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="75545-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="75545-119">HTTP request</span></span>

```http
GET /me/settings/
```

<span data-ttu-id="75545-120">Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="75545-120">Request with a 'user id' or 'userPrincipalName' is only accessible by the user or by a user with the User.ReadWrite.All permissions.</span></span> <span data-ttu-id="75545-121">Para obtener más información, vea [permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75545-121">To learn more, see [Permissions](/graph/permissions-reference).</span></span>

```http
GET /users/{id | userPrincipalName}/settings/
```

## <a name="request-body"></a><span data-ttu-id="75545-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="75545-122">Request body</span></span>

<span data-ttu-id="75545-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="75545-123">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="75545-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75545-124">Response</span></span>

<span data-ttu-id="75545-125">Si tiene éxito, este método devuelve una `200 OK` objeto de [configuración de usuario](../resources/user-settings.md) y el código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75545-125">If successful, this method returns a `200 OK` response code and [user settings](../resources/user-settings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75545-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="75545-126">Example</span></span>

##### <a name="request"></a><span data-ttu-id="75545-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="75545-127">Request</span></span>

```http
GET https://graph.microsoft.com/beta/me/settings
```

##### <a name="response"></a><span data-ttu-id="75545-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75545-128">Response</span></span>

<span data-ttu-id="75545-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="75545-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": false
}
```
