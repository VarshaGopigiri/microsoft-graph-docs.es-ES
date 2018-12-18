---
title: Agregar datos personalizados a usuarios mediante extensiones abiertas
description: 'Vamos a guiarle a través de un ejemplo para demostrarle cómo usar las *extensiones abiertas*. '
author: dkershaw10
ms.openlocfilehash: 37df1bd03e68b00be41496ee9f66a076d8758149
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337173"
---
# <a name="add-custom-data-to-users-using-open-extensions"></a><span data-ttu-id="34efe-103">Agregar datos personalizados a usuarios mediante extensiones abiertas</span><span class="sxs-lookup"><span data-stu-id="34efe-103">Add custom data to users using open extensions</span></span>
<span data-ttu-id="34efe-104">Vamos a guiarle a través de un ejemplo para demostrarle cómo usar las *extensiones abiertas*.</span><span class="sxs-lookup"><span data-stu-id="34efe-104">We're going to walk you through an example to demonstrate how to use *open extensions*.</span></span> 

<span data-ttu-id="34efe-p101">Imagine que está creando una aplicación que está disponible en muchas plataformas cliente distintas, como equipos de sobremesa y móviles.  Quiere que los usuarios puedan configurar su experiencia de interfaz para que sea coherente sin importar en qué dispositivo inicien sesión en su aplicación. Se trata de un requisito común para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="34efe-p101">Imagine you're building an application that is available on lots of different client platforms, such as desktop and mobile.  You want to let users configure their UI experience so it’s consistent no matter which device they use to sign in to your app. This is a common requirement for most apps.</span></span> 

<span data-ttu-id="34efe-108">En este escenario, vamos a mostrarle cómo:</span><span class="sxs-lookup"><span data-stu-id="34efe-108">For this scenario, we're going to show you how to:</span></span>

1. <span data-ttu-id="34efe-109">Agregar una extensión abierta que represente cierta información móvil acerca del usuario.</span><span class="sxs-lookup"><span data-stu-id="34efe-109">Add an open extension representing some roaming profile information about the user.</span></span>
2. <span data-ttu-id="34efe-110">Realizar una consulta al usuario y devolver el perfil móvil.</span><span class="sxs-lookup"><span data-stu-id="34efe-110">Query the user and return the roaming profile.</span></span>
3. <span data-ttu-id="34efe-111">Cambiar la información del perfil móvil del usuario (el valor de extensión abierta).</span><span class="sxs-lookup"><span data-stu-id="34efe-111">Change the user's roaming profile information (the open extension value).</span></span>
4. <span data-ttu-id="34efe-112">Eliminar la información de perfil móvil del usuario.</span><span class="sxs-lookup"><span data-stu-id="34efe-112">Delete the user's roaming profile information.</span></span>

><span data-ttu-id="34efe-p102">**Nota:** Este tema muestra cómo agregar, leer, actualizar y eliminar extensiones abiertas en un recurso *usuario*.  Estos métodos también se admiten para los tipos de recurso *administrativeUnit*, *póngase en contacto con*, *dispositivo*, *evento*, *grupo*, *evento de grupo*, *publicación de grupo* y *organización*.</span><span class="sxs-lookup"><span data-stu-id="34efe-p102">**Note:** This topic shows you how to add, read, update and delete open extensions on a *user* resource.  These methods are also supported for the *administrativeUnit*, *contact*, *device*, *event*, *group*, *group event*, *group post* and *organizaton* resource types.</span></span>  
<span data-ttu-id="34efe-p103">Solo tiene que actualizar las solicitudes de ejemplo mostradas a continuación usando cualquiera de estos tipos de recurso. Las respuestas mostradas en los ejemplos siguientes pueden aparecer truncadas para abreviar.</span><span class="sxs-lookup"><span data-stu-id="34efe-p103">Simply update the example requests below using any of those resource types. The responses shown in the examples below may be truncated for brevity.</span></span> 

## <a name="1-add-roaming-profile-information"></a><span data-ttu-id="34efe-117">1. Agregar información de perfil móvil</span><span class="sxs-lookup"><span data-stu-id="34efe-117">1. Add roaming profile information</span></span>
<span data-ttu-id="34efe-p104">El usuario inicia sesión en la aplicación y configura su apariencia.  La configuración de la aplicación debe ser móvil para que el usuario reciba la misma experiencia en cualquier dispositivo desde el que inicie sesión en la aplicación.  Aquí veremos cómo agregar la información del perfil móvil a un recurso de usuario.</span><span class="sxs-lookup"><span data-stu-id="34efe-p104">The user signs in to the app and configures the look and feel of the app.  These app settings should roam so that the user gets the same experience on whatever device they sign in to the app from.  Here we'll see how to add the roaming profile information to a user resource.</span></span>

##### <a name="request"></a><span data-ttu-id="34efe-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34efe-121">Request</span></span>
```http
POST https://graph.microsoft.com/v1.0/me/extensions
Content-type: application/json
{
    "@odata.type":"microsoft.graph.openTypeExtension",
    "extensionName":"com.contoso.roamingSettings",
    "theme":"dark",
    "color":"purple",
    "lang":"Japanese"
}
```
##### <a name="response"></a><span data-ttu-id="34efe-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34efe-122">Response</span></span>
```http
HTTP/1.1 201 Created
Content-Type: application/json
Content-length: 420

{
    "@odata.type": "#microsoft.graph.openTypeExtension",
    "extensionName": "com.contoso.roamingSettings",
    "id": "com.contoso.roamingSettings",
    "theme": "dark",
    "color": "purple",
    "lang": "Japanese"
}
```

## <a name="2-retrieve-roaming-profile-information"></a><span data-ttu-id="34efe-123">2. Recuperar información de perfil móvil</span><span class="sxs-lookup"><span data-stu-id="34efe-123">2. Retrieve roaming profile information</span></span>
<span data-ttu-id="34efe-p105">Cuando el usuario inicia sesión en la aplicación desde otro dispositivo, esta puede recuperar los detalles del perfil de usuario, además de su configuración móvil. Esto puede hacerse obteniendo el recurso de usuario y expandiendo la propiedad de navegación de extensión.</span><span class="sxs-lookup"><span data-stu-id="34efe-p105">When the user signs in to the app from another device, the app can retrieve the user's profile details as well as their roaming settings. This can be done by getting the user's resource and expanding the extension navigation property.</span></span>

##### <a name="request"></a><span data-ttu-id="34efe-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34efe-126">Request</span></span>
```http
GET https://graph.microsoft.com/v1.0/me?$select=id,displayName,mail,mobilePhone&$expand=extensions
```
##### <a name="response"></a><span data-ttu-id="34efe-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34efe-127">Response</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-length: 420

{
    "id": "84b80893-8749-40a3-97b7-68513b600544",
    "displayName": "John Smith",
    "mail": "john@contoso.com",
    "mobilePhone": "1-555-6589",
    "extensions": [
        {
            "@odata.type": "#microsoft.graph.openTypeExtension",
            "extensionName": "com.contoso.roamingSettings",
            "id": "com.contoso.roamingSettings",
            "theme": "dark",
            "color": "purple",
            "lang": "Japanese"
        }
    ]
}
```
><span data-ttu-id="34efe-128">**Nota:** Si tiene varias extensiones, puede filtrar por la *id* para obtener aquella que le interese.</span><span class="sxs-lookup"><span data-stu-id="34efe-128">**Note:** If you have multiple extensions, you can filter on the *id* to get the extension that you are interested in.</span></span>

## <a name="3-change-roaming-profile-information"></a><span data-ttu-id="34efe-129">3. Cambiar información de perfil móvil</span><span class="sxs-lookup"><span data-stu-id="34efe-129">3. Change roaming profile information</span></span>
<span data-ttu-id="34efe-p106">El usuario puede cambiar la información de su perfil móvil.  Esta actualización puede realizarse con un ```PATCH``` en el valor de extensión abierta.</span><span class="sxs-lookup"><span data-stu-id="34efe-p106">The user may choose to change their roaming profile information.  This update can be done with a ```PATCH``` on the open extension value.</span></span> 

##### <a name="request"></a><span data-ttu-id="34efe-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34efe-132">Request</span></span>
```http
PATCH https://graph.microsoft.com/v1.0/me/extensions/com.contoso.roamingSettings
Content-type: application/json
{
    "theme":"light",
    "color":"yellow",
    "lang":"Swahili"
}
```

##### <a name="response"></a><span data-ttu-id="34efe-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34efe-133">Response</span></span>
```
HTTP/1.1 204 No content
```

## <a name="4-delete-a-users-roaming-profile"></a><span data-ttu-id="34efe-134">4. Eliminar un perfil de usuario móvil</span><span class="sxs-lookup"><span data-stu-id="34efe-134">4. Delete a user's roaming profile</span></span>
<span data-ttu-id="34efe-p107">El usuario decide que ya no desea tener un perfil móvil y lo elimina. Esto puede realizarse con una solicitud ```DELETE``` en el valor de extensión abierta.</span><span class="sxs-lookup"><span data-stu-id="34efe-p107">The user decides that they don't want a roaming profile anymore, so they delete it. This can be done with a ```DELETE``` request on the open extension value.</span></span>

##### <a name="request"></a><span data-ttu-id="34efe-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34efe-137">Request</span></span>
```http
DELETE https://graph.microsoft.com/v1.0/me/extensions/com.contoso.roamingSettings
```

##### <a name="response"></a><span data-ttu-id="34efe-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34efe-138">Response</span></span>
```
HTTP/1.1 204 No content
```

## <a name="see-also"></a><span data-ttu-id="34efe-139">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="34efe-139">See also</span></span>

- [<span data-ttu-id="34efe-140">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="34efe-140">Add custom data to resources using extensions</span></span>](extensibility-overview.md)
- [<span data-ttu-id="34efe-141">Agregar datos personalizados a los grupos mediante extensiones de esquema</span><span class="sxs-lookup"><span data-stu-id="34efe-141">Add custom data to groups using schema extensions</span></span>](extensibility-schema-groups.md)
- [<span data-ttu-id="34efe-142">Tipo de recurso openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="34efe-142">openTypeExtension resource type</span></span>](/graph/api/resources/opentypeextension?view=graph-rest-1.0)
- [<span data-ttu-id="34efe-143">Crear extensión abierta</span><span class="sxs-lookup"><span data-stu-id="34efe-143">Create open extension</span></span>](/graph/api/opentypeextension-post-opentypeextension?view=graph-rest-1.0)
- [<span data-ttu-id="34efe-144">Obtener extensión abierta</span><span class="sxs-lookup"><span data-stu-id="34efe-144">Get open extension</span></span>](/graph/api/opentypeextension-get?view=graph-rest-1.0)
- [<span data-ttu-id="34efe-145">Actualizar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="34efe-145">Update open extension</span></span>](/graph/api/opentypeextension-update?view=graph-rest-1.0)
- [<span data-ttu-id="34efe-146">Eliminar extensión abierta</span><span class="sxs-lookup"><span data-stu-id="34efe-146">Delete open extension</span></span>](/graph/api/opentypeextension-delete?view=graph-rest-1.0)