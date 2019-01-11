---
title: Obtener la configuración
description: Leer el objeto de configuración de usuario y de organización.
author: dkershaw10
localization_priority: Priority
ms.openlocfilehash: ace7c43b27860832968572628838484bc8c91c84
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815494"
---
# <a name="get-settings"></a><span data-ttu-id="c96cc-103">Obtener la configuración</span><span class="sxs-lookup"><span data-stu-id="c96cc-103">Get settings</span></span>

<span data-ttu-id="c96cc-104">Leer el objeto de [configuración de](../resources/user-settings.md) usuario y de organización.</span><span class="sxs-lookup"><span data-stu-id="c96cc-104">Read the user and organization [settings](../resources/user-settings.md) object.</span></span>
<span data-ttu-id="c96cc-105">Para obtener más información acerca de cómo actualizar las propiedades del objeto de [configuración](../resources/user-settings.md) , consulte [actualización de la configuración de usuario](user-update-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c96cc-105">To learn how to update the properties of the [settings](../resources/user-settings.md) object, see [update user settings](user-update-settings.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c96cc-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c96cc-106">Permissions</span></span>

<span data-ttu-id="c96cc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c96cc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c96cc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c96cc-109">Permission type</span></span>      | <span data-ttu-id="c96cc-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c96cc-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c96cc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c96cc-111">Delegated (work or school account)</span></span> | <span data-ttu-id="c96cc-112">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c96cc-112">User.Read.All, User.ReadWrite.All</span></span>    |
|<span data-ttu-id="c96cc-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c96cc-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c96cc-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c96cc-114">Not supported.</span></span>    |
|<span data-ttu-id="c96cc-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c96cc-115">Application</span></span> | <span data-ttu-id="c96cc-116">User.Read.All,User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c96cc-116">User.Read.All,User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c96cc-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c96cc-117">HTTP request</span></span>

```http
GET /me/settings/
```

<span data-ttu-id="c96cc-118">Solicitar a un 'id' o 'userPrincipalName' sólo es accesible por el usuario o por un usuario con los permisos de User.ReadWrite.All.</span><span class="sxs-lookup"><span data-stu-id="c96cc-118">Request with a 'user id' or 'userPrincipalName' is only accessible by the user or by a user with the User.ReadWrite.All permissions.</span></span> <span data-ttu-id="c96cc-119">Para obtener más información, vea [permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c96cc-119">To learn more, see [Permissions](/graph/permissions-reference).</span></span>

```http
GET /users/{id | userPrincipalName}/settings/
```

## <a name="request-body"></a><span data-ttu-id="c96cc-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c96cc-120">Request body</span></span>

<span data-ttu-id="c96cc-121">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c96cc-121">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c96cc-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c96cc-122">Response</span></span>

<span data-ttu-id="c96cc-123">Si tiene éxito, este método devuelve una `200 OK` objeto de [configuración de usuario](../resources/user-settings.md) y el código de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c96cc-123">If successful, this method returns a `200 OK` response code and [user settings](../resources/user-settings.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c96cc-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c96cc-124">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c96cc-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c96cc-125">Request</span></span>

```http
GET https://graph.microsoft.com/v1.0/me/settings
```

##### <a name="response"></a><span data-ttu-id="c96cc-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c96cc-126">Response</span></span>

<span data-ttu-id="c96cc-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c96cc-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 72

{
  "contributionToContentDiscoveryAsOrganizationDisabled": false,
  "contributionToContentDiscoveryDisabled": false
}
```

