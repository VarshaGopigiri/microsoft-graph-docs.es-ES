---
title: Obtener los cambios incrementales de usuarios
description: Consulta de delta permite consultar las adiciones, eliminaciones o actualizaciones a usuarios, por medio de una serie de llamadas a función delta. La consulta de delta le permite descubrir cambios en usuarios sin tener que acceder a todo el conjunto de usuarios de Microsoft Graph para comparar los cambios.
author: piotrci
localization_priority: Priority
ms.openlocfilehash: b4f79951f79393e22c40ef9a4f55e29e0145ccea
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850480"
---
# <a name="get-incremental-changes-for-users"></a><span data-ttu-id="2c0cf-104">Obtener los cambios incrementales de usuarios</span><span class="sxs-lookup"><span data-stu-id="2c0cf-104">Get incremental changes for users</span></span>

<span data-ttu-id="2c0cf-p102">[Consulta de delta](./delta-query-overview.md) permite consultar las adiciones, eliminaciones o actualizaciones a usuarios, por medio de una serie de llamadas a función [delta](/graph/api/user-delta?view=graph-rest-1.0). La consulta de delta le permite descubrir cambios en usuarios sin tener que acceder a todo el conjunto de usuarios de Microsoft Graph para comparar los cambios.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p102">[Delta query](./delta-query-overview.md) lets you query for additions, deletions, or updates to users, by way of a series of [delta](/graph/api/user-delta?view=graph-rest-1.0) function calls. Delta query enables you discover changes to users without having to fetch the entire set of users from Microsoft Graph and compare changes.</span></span>

<span data-ttu-id="2c0cf-p103">Los clientes que utilizan usuarios de sincronización con un almacén de perfil local pueden utilizar la consulta delta para su sincronización completa inicial y sus sincronizaciones incrementales futuras. Normalmente, el cliente debería realizar una sincronización completa inicial de todos los usuarios de inquilino y, después, obtener los cambios incrementales en los usuarios de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p103">Clients using synchronizing users with a local profile store can use Delta Query for both their initial full synchronization along with incremental synchronizations in the future. Typically, a client would do an initial full synchronization of all the users in a tenant, and subsequently, get incremental changes to users periodically.</span></span>

## <a name="tracking-user-changes"></a><span data-ttu-id="2c0cf-109">Seguimiento de los cambios de usuarios</span><span class="sxs-lookup"><span data-stu-id="2c0cf-109">Tracking user changes</span></span>

<span data-ttu-id="2c0cf-p104">El seguimiento de los cambios de usuarios normalmente es una ronda de una o varias solicitudes GET con la función **delta**. Realiza una solicitud GET de una forma muy similar a cómo [lista usuarios](/graph/api/user-list?view=graph-rest-1.0), excepto que incluye lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p104">Tracking user changes is a round of one or more GET requests with the **delta** function. You make a GET request much like the way you [list users](/graph/api/user-list?view=graph-rest-1.0), except that you include the following:</span></span>

- <span data-ttu-id="2c0cf-112">La función **delta**</span><span class="sxs-lookup"><span data-stu-id="2c0cf-112">The **delta** function.</span></span>
- <span data-ttu-id="2c0cf-113">Un [token de estado](./delta-query-overview.md) (_deltaToken_ o _skipToken_) de la anterior llamada a función **delta** GET.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-113">A [state token](./delta-query-overview.md) (_deltaToken_ or _skipToken_) from the previous GET **delta** function call.</span></span>

## <a name="example"></a><span data-ttu-id="2c0cf-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c0cf-114">Example</span></span>

<span data-ttu-id="2c0cf-115">El ejemplo siguiente muestra una serie de solicitudes para seguir cambios en usuarios:</span><span class="sxs-lookup"><span data-stu-id="2c0cf-115">The following example shows a series  requests to track changes to users:</span></span>

1. <span data-ttu-id="2c0cf-116">[Solicitud inicial](#initial-request) y [respuesta](#initial-response)</span><span class="sxs-lookup"><span data-stu-id="2c0cf-116">[Initial request](#initial-request) and [response](#initial-response)</span></span>
2. <span data-ttu-id="2c0cf-117">[Solicitud nextLink](#nextlink-request) y [respuesta](#nextlink-response)</span><span class="sxs-lookup"><span data-stu-id="2c0cf-117">[nextLink request](#nextlink-request) and [response](#nextlink-response)</span></span>
3. <span data-ttu-id="2c0cf-118">[Solicitud nextLink final](#final-nextlink-request) y [respuesta](#final-nextlink-response)</span><span class="sxs-lookup"><span data-stu-id="2c0cf-118">[Final nextLink request](#final-nextlink-request) and [response](#final-nextlink-response)</span></span>
4. <span data-ttu-id="2c0cf-119">[Solicitud de deltaLink](#deltalink-request) y [respuesta deltaLink](#deltalink-response)</span><span class="sxs-lookup"><span data-stu-id="2c0cf-119">[deltaLink request](#deltalink-request) and [deltaLink response](#deltalink-response)</span></span>

## <a name="initial-request"></a><span data-ttu-id="2c0cf-120">Solicitud inicial</span><span class="sxs-lookup"><span data-stu-id="2c0cf-120">Initial request</span></span>

<span data-ttu-id="2c0cf-121">Para comenzar los cambios de seguimiento en el recurso usuario, debe realizar una solicitud incluyendo la función delta en el recurso usuario.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-121">To begin tracking changes in the user resource, you make a request including the delta function on the user resource.</span></span>

<span data-ttu-id="2c0cf-122">Tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2c0cf-122">Note the following:</span></span>

- <span data-ttu-id="2c0cf-123">El parámetro de consulta $select opcional se incluye en la solicitud para demostrar cómo los parámetros de consulta se incluyen automáticamente en futuras solicitudes.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-123">The optional $select query parameter is included in the request to demonstrate how query parameters are automatically included in future requests.</span></span>
- <span data-ttu-id="2c0cf-p105">La solicitud inicial no incluye un token del estado. Los tokens de estado se utilizarán en solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p105">The initial request does not include a state token. State tokens will be used in subsequent requests.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/delta?$select=displayName,givenName,surname
```

## <a name="initial-response"></a><span data-ttu-id="2c0cf-126">Respuesta inicial</span><span class="sxs-lookup"><span data-stu-id="2c0cf-126">Initial response</span></span>

<span data-ttu-id="2c0cf-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [usuario](/graph/api/resources/user?view=graph-rest-1.0) en el cuerpo de la respuesta. Suponiendo que todo el conjunto de los usuarios sea demasiado grande, la respuesta incluirá también un token de estado nextLink.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p106">If successful, this method returns `200 OK` response code and [user](/graph/api/resources/user?view=graph-rest-1.0) collection object in the response body. Assuming the entire set of users is too large, the response will also include a nextLink state token.</span></span>

<span data-ttu-id="2c0cf-p107">En este ejemplo se devuelve una dirección URL nextLink que indica la existencia de páginas de datos adicionales para recuperar en la sesión. El parámetro de consulta $select de la solicitud inicial se codifica en la dirección URL nextLink.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p107">In this example, a nextLink URL is returned indicating there are additional pages of data to be retrieved in the session. The $select query parameter from the initial request is encoded into the nextLink URL.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users(displayName,givenName,surname)",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=oEBwdSP6uehIAxQOWq_3Ksh_TLol6KIm3stvdc6hGhZRi1hQ7Spe__dpvm3U4zReE4CYXC2zOtaKdi7KHlUtC2CbRiBIUwOxPKLa",
  "value": [
    {
      "displayName":"Testuser1",
      "givenName":"John",
      "surname":"Doe",
      "id":"ffff7b1a-13b6-477b-8c0c-380905cd99f7"
    },
    {
      "displayName":"Testuser2",
      "givenName":"Jane",
      "surname":"Doe",
      "id":"605d1257-ffff-40b6-8e6f-528a53f5dc55"
    }
  ]
}
```

## <a name="nextlink-request"></a><span data-ttu-id="2c0cf-131">solicitud de nextLink</span><span class="sxs-lookup"><span data-stu-id="2c0cf-131">nextLink request</span></span>

<span data-ttu-id="2c0cf-p108">La segunda solicitud especifica el `skipToken` devuelto de la respuesta anterior. Tenga en cuenta que el parámetro `$select` no es indispensable, pues `skipToken` lo codifica y lo incluye.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p108">The second request specifies the `skipToken` returned from the previous response. Notice the `$select` parameter is not required, as the `skipToken` encodes and includes it.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/delta?$skiptoken=oEBwdSP6uehIAxQOWq_3Ksh_TLol6KIm3stvdc6hGhZRi1hQ7Spe__dpvm3U4zReE4CYXC2zOtaKdi7KHlUtC2CbRiBIUwOxPKLa
```

## <a name="nextlink-response"></a><span data-ttu-id="2c0cf-134">respuesta de nextLink</span><span class="sxs-lookup"><span data-stu-id="2c0cf-134">nextLink response</span></span>

<span data-ttu-id="2c0cf-p109">La respuesta contiene un `nextLink` y otro `skipToken`, indicando que hay más usuarios disponibles. Sigue realizando solicitudes con la dirección URL nextLink hasta obtener como respuesta una dirección URL deltaLink.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p109">The response contains a `nextLink` and another `skipToken`, indicating there are more users available. You continue making requests using the nextLink URL until a deltaLink URL is returned in the response.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.nextLink":"https://graph.microsoft.com/v1.0/users/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjtQ5LOhVoS7qQG_wdVCHHlbQpga7",
  "value": [
    {
      "displayName":"Testuser3",
      "givenName":"Pat",
      "surname":"Doe",
      "id":"d8c37826-ffff-4cae-b348-e2725b1e814b"
    },
    {
      "displayName":"Testuser4",
      "givenName":"Meghan",
      "surname":"Doe",
      "id":"8b1ee412-cd8f-4d59-ffff-24010edb9f1f"
    }
  ]
}
```

## <a name="final-nextlink-request"></a><span data-ttu-id="2c0cf-137">solicitud de nextLink final</span><span class="sxs-lookup"><span data-stu-id="2c0cf-137">Final nextLink request</span></span>

<span data-ttu-id="2c0cf-138">La tercera solicitud continúa usando el último `skipToken` devuelto desde la última solicitud de sincronización.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-138">The third request continues to use the latest `skipToken` returned from the last sync request.</span></span> 

``` http
GET https://graph.microsoft.com/v1.0/users/delta?$skiptoken=oEBwdSP6uehIAxQOWq_3Ksh_TLol6KIm3stvdc6hGhaOYDE2VPA4vxIPA90-P6OzGd6Rvku5fDgBRIGS
```

## <a name="final-nextlink-response"></a><span data-ttu-id="2c0cf-139">respuesta de nextLink final</span><span class="sxs-lookup"><span data-stu-id="2c0cf-139">Final nextLink response</span></span>

<span data-ttu-id="2c0cf-p110">Cuando se devuelve la dirección URL deltaLink, no hay más datos sobre el estado existente del recurso para devolver. Para las solicitudes futuras, la aplicación usa la dirección URL deltaLink para obtener información sobre los cambios en el recurso. Guarde `deltaToken` y utilícelo en la dirección URL de solicitud para descubrir cambios a usuarios.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-p110">When the deltaLink URL is returned, there is no more data about the existing state of the resource to be returned. For future requests, the application uses the deltaLink URL to learn about changes to the resource. Save the `deltaToken` and use it in the request URL to discover changes to users.</span></span> 

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460",
  "value": [
    {
      "displayName":"Testuser5",
      "givenName":"Al",
      "surname":"Doe",
      "id":"25dcffff-959e-4ece-9973-e5d9b800e8cc"
    },
    {
      "displayName":"Testuser6",
      "givenName":"Sam",
      "surname":"Doe",
      "id":"f6ede700-27d0-4c42-bfb9-4dffff43c74a"
    }
  ]
}
```

## <a name="deltalink-request"></a><span data-ttu-id="2c0cf-143">solicitud de deltaLink</span><span class="sxs-lookup"><span data-stu-id="2c0cf-143">deltaLink request</span></span>

<span data-ttu-id="2c0cf-144">Con el `deltaToken` de la [última respuesta](#final-nextlink-response), podrá obtener usuarios cambiados (agregados, eliminados o actualizados) desde la última solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-144">Using the `deltaToken` from the [last response](#final-nextlink-response), you will be able to get changed (by being added, deleted, or updated) users since the last request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460
```

## <a name="deltalink-response"></a><span data-ttu-id="2c0cf-145">respuesta de deltaLink</span><span class="sxs-lookup"><span data-stu-id="2c0cf-145">deltaLink response</span></span>

<span data-ttu-id="2c0cf-146">Si no ha habido cambios, se devuelve el mismo `deltaToken` sin resultados.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-146">If no changes have occurred, the same `deltaToken` is returned with no results.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460",
  "value": []
}
```

<span data-ttu-id="2c0cf-147">Si se han producido cambios, se devuelve el mismo `deltaToken` con una colección de usuarios cambiados.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-147">If changes have occurred, the same `deltaToken` is returned including a collection of changed users.</span></span>

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users",
  "@odata.deltaLink":"https://graph.microsoft.com/v1.0/users/delta?$deltatoken=oEcOySpF_hWYmTIUZBOIfPzcwisr_rPe8o9M54L45qEXQGmvQC6T2dbL-9O7nSU-njKhFiGlAZqewNAThmCVnNxqPu5gOBegrm1CaVZ-ZtFZ2tPOAO98OD9y0ao460",
  "value": [
    {
      "displayName":"Testuser7",
      "givenName":"Joe",
      "surname":"Doe",
      "id":"25dcffff-959e-4ece-9973-e5d9b800e8cc"
    },
    {
      "id":"8ffff70c-1c63-4860-b963-e34ec660931d",
      "@removed": {
         "reason": "changed"
      }
    }
  ]
}
```

<span data-ttu-id="2c0cf-148">Algunas cosas que debe tener en cuenta sobre la respuesta del ejemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="2c0cf-148">Some things to note about the example response above:</span></span>

- <span data-ttu-id="2c0cf-149">Cuando el usuario se elimina, el elemento contiene una anotación: `@removed` con el valor de `"reason": "changed"`.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-149">When the user is deleted, the item contains an annotation: `@removed` with value of `"reason": "changed"`.</span></span>

- <span data-ttu-id="2c0cf-150">Cuando el usuario se elimina permanentemente, el elemento contiene una anotación: `@removed` con el valor de `"reason": "deleted"`.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-150">When the user is permanently deleted, the item contains an annotation: `@removed` with value of `"reason": "deleted"`.</span></span>

- <span data-ttu-id="2c0cf-151">Cuando el usuario se crea o restaura, no hay ninguna anotación.</span><span class="sxs-lookup"><span data-stu-id="2c0cf-151">When the user is created, or restored, there is no annotation.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c0cf-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c0cf-152">See also</span></span>
<span data-ttu-id="2c0cf-153">Información general sobre [Consulta de delta de Microsoft Graph](delta-query-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2c0cf-153">[Microsoft Graph delta query](delta-query-overview.md) overview.</span></span>
