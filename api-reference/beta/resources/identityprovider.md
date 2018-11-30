---
title: tipo de recurso identityProvider
description: Representa un proveedor de identidad de Azure Active Directory (AD Azure). El proveedor de identidad puede ser Microsoft, Google, Facebook, Amazon o LinkedIn.
ms.openlocfilehash: 672e2e6225374451a475b69e2ce4ce6adfe65ef0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085181"
---
# <a name="identityprovider-resource-type"></a><span data-ttu-id="d96b1-104">tipo de recurso identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-104">identityProvider resource type</span></span>

> <span data-ttu-id="d96b1-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d96b1-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d96b1-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d96b1-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d96b1-107">Representa un proveedor de identidad de Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="d96b1-107">Represents an Azure Active Directory (Azure AD) identity provider.</span></span> <span data-ttu-id="d96b1-108">El proveedor de identidad puede ser Microsoft, Google, Facebook, Amazon o LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="d96b1-108">The identity provider can be Microsoft, Google, Facebook, Amazon, or LinkedIn.</span></span>

<span data-ttu-id="d96b1-109">Configuración de un proveedor de identidad en el inquilino de Azure AD B2C permite:</span><span class="sxs-lookup"><span data-stu-id="d96b1-109">Configuring an identity provider in your Azure AD B2C tenant enables:</span></span>

* <span data-ttu-id="d96b1-110">A los usuarios registrarse e iniciar sesión con una cuenta de social en una aplicación de consumidor.</span><span class="sxs-lookup"><span data-stu-id="d96b1-110">Users to sign up and sign in using a social account in a consumer application.</span></span> <span data-ttu-id="d96b1-111">Por ejemplo, una aplicación puede utilizar Azure AD B2C para permitir a los usuarios para registrarse y obtener el servicio con una cuenta de Facebook.</span><span class="sxs-lookup"><span data-stu-id="d96b1-111">For example, an application can use Azure AD B2C to allow users to sign up for the service using a Facebook account.</span></span>
* <span data-ttu-id="d96b1-112">Cuenta a los usuarios vincular a un local existente a una cuenta de social en una aplicación de consumidor.</span><span class="sxs-lookup"><span data-stu-id="d96b1-112">Users to link an existing local account to a social account in a consumer application.</span></span> <span data-ttu-id="d96b1-113">Por ejemplo, un usuario ha creado un nombre de usuario y una contraseña (cuenta local) en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d96b1-113">For example, a user has created a username and password (local account) in the application.</span></span> <span data-ttu-id="d96b1-114">El usuario decide más adelante vincular la cuenta local existente a su cuenta de Facebook, por lo que puede iniciar sesión con Facebook.</span><span class="sxs-lookup"><span data-stu-id="d96b1-114">The user later decides to link the existing local account to their Facebook account so they can sign in using Facebook.</span></span>

<span data-ttu-id="d96b1-115">Configuración de un proveedor de identidad en el inquilino de Azure AD permite escenarios de invitado B2B futuros.</span><span class="sxs-lookup"><span data-stu-id="d96b1-115">Configuring an identity provider in your Azure AD tenant enables future B2B guest scenarios.</span></span> <span data-ttu-id="d96b1-116">Por ejemplo, una organización tiene recursos en Office 365 que deban ser compartidos con un usuario de Gmail.</span><span class="sxs-lookup"><span data-stu-id="d96b1-116">For example, an organization has resources in Office 365 that need to be shared with a Gmail user.</span></span> <span data-ttu-id="d96b1-117">El usuario de Gmail usará sus credenciales de cuenta de Google para autenticar y obtener acceso a los documentos.</span><span class="sxs-lookup"><span data-stu-id="d96b1-117">The Gmail user will use their Google account credentials to authenticate and access the documents.</span></span>

## <a name="methods"></a><span data-ttu-id="d96b1-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="d96b1-118">Methods</span></span>

| <span data-ttu-id="d96b1-119">Método</span><span class="sxs-lookup"><span data-stu-id="d96b1-119">Method</span></span>       | <span data-ttu-id="d96b1-120">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d96b1-120">Return Type</span></span>  |<span data-ttu-id="d96b1-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d96b1-121">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d96b1-122">Obtener identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-122">Get identityProvider</span></span>](../api/identityprovider-get.md) |<span data-ttu-id="d96b1-123">identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-123">identityProvider</span></span>|<span data-ttu-id="d96b1-124">Leer las propiedades de un identityProvider existente.</span><span class="sxs-lookup"><span data-stu-id="d96b1-124">Read properties of an existing identityProvider.</span></span>|
|[<span data-ttu-id="d96b1-125">Crear identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-125">Create identityProvider</span></span>](../api/identityprovider-post-identityproviders.md)|<span data-ttu-id="d96b1-126">identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-126">identityProvider</span></span>|<span data-ttu-id="d96b1-127">Crear un nuevo identityProvider.</span><span class="sxs-lookup"><span data-stu-id="d96b1-127">Create a new identityProvider.</span></span>|
|[<span data-ttu-id="d96b1-128">Actualizar identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-128">Update identityProvider</span></span>](../api/identityprovider-update.md)|<span data-ttu-id="d96b1-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d96b1-129">None</span></span>|<span data-ttu-id="d96b1-130">Actualizar un identityProvider existente.</span><span class="sxs-lookup"><span data-stu-id="d96b1-130">Update an existing identityProvider.</span></span>|
|[<span data-ttu-id="d96b1-131">Eliminar identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-131">Delete identityProvider</span></span>](../api/identityprovider-delete.md)|<span data-ttu-id="d96b1-132">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d96b1-132">None</span></span>|<span data-ttu-id="d96b1-133">Eliminar un identityProvider existente.</span><span class="sxs-lookup"><span data-stu-id="d96b1-133">Delete an existing identityProvider.</span></span>|
|[<span data-ttu-id="d96b1-134">Lista identityProviders</span><span class="sxs-lookup"><span data-stu-id="d96b1-134">List identityProviders</span></span>](../api/identityprovider-list.md)|<span data-ttu-id="d96b1-135">colección de identityProvider</span><span class="sxs-lookup"><span data-stu-id="d96b1-135">identityProvider collection</span></span>|<span data-ttu-id="d96b1-136">Lista de todos los identityProviders configurados en un inquilino.</span><span class="sxs-lookup"><span data-stu-id="d96b1-136">List all identityProviders configured in a tenant.</span></span>|

## <a name="properties"></a><span data-ttu-id="d96b1-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d96b1-137">Properties</span></span>

|<span data-ttu-id="d96b1-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d96b1-138">Property</span></span>|<span data-ttu-id="d96b1-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="d96b1-139">Type</span></span>|<span data-ttu-id="d96b1-140">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="d96b1-140">Required</span></span>|<span data-ttu-id="d96b1-141">Nullable</span><span class="sxs-lookup"><span data-stu-id="d96b1-141">Nullable</span></span>|<span data-ttu-id="d96b1-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="d96b1-142">Description</span></span>|
|:---------------|:--------|:--------|:--------|:----------|
|<span data-ttu-id="d96b1-143">clientId</span><span class="sxs-lookup"><span data-stu-id="d96b1-143">clientId</span></span>|<span data-ttu-id="d96b1-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="d96b1-144">String</span></span>|<span data-ttu-id="d96b1-145">Sí</span><span class="sxs-lookup"><span data-stu-id="d96b1-145">Yes</span></span>|<span data-ttu-id="d96b1-146">No</span><span class="sxs-lookup"><span data-stu-id="d96b1-146">No</span></span>|<span data-ttu-id="d96b1-147">El identificador de cliente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d96b1-147">The client ID for the application.</span></span> <span data-ttu-id="d96b1-148">Este es el identificador de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="d96b1-148">This is the client ID obtained when registering the application with the identity provider.</span></span>|
|<span data-ttu-id="d96b1-149">clientSecret</span><span class="sxs-lookup"><span data-stu-id="d96b1-149">clientSecret</span></span>|<span data-ttu-id="d96b1-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="d96b1-150">String</span></span>|<span data-ttu-id="d96b1-151">Sí</span><span class="sxs-lookup"><span data-stu-id="d96b1-151">Yes</span></span>|<span data-ttu-id="d96b1-152">No</span><span class="sxs-lookup"><span data-stu-id="d96b1-152">No</span></span>|<span data-ttu-id="d96b1-153">El secreto de cliente para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d96b1-153">The client secret for the application.</span></span> <span data-ttu-id="d96b1-154">Este es el secreto de cliente que se obtuvieron cuando se registra la aplicación con el proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="d96b1-154">This is the client secret obtained when registering the application with the identity provider.</span></span> <span data-ttu-id="d96b1-155">Esto es de sólo escritura.</span><span class="sxs-lookup"><span data-stu-id="d96b1-155">This is write-only.</span></span> <span data-ttu-id="d96b1-156">Una operación de lectura devolverá "\*\*\*\*".</span><span class="sxs-lookup"><span data-stu-id="d96b1-156">A read operation will return "\*\*\*\*".</span></span>|
|<span data-ttu-id="d96b1-157">id</span><span class="sxs-lookup"><span data-stu-id="d96b1-157">id</span></span>|<span data-ttu-id="d96b1-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="d96b1-158">String</span></span>|<span data-ttu-id="d96b1-159">No</span><span class="sxs-lookup"><span data-stu-id="d96b1-159">No</span></span>|<span data-ttu-id="d96b1-160">No</span><span class="sxs-lookup"><span data-stu-id="d96b1-160">No</span></span>|<span data-ttu-id="d96b1-161">El identificador del proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="d96b1-161">The ID of the identity provider.</span></span>|
|<span data-ttu-id="d96b1-162">name</span><span class="sxs-lookup"><span data-stu-id="d96b1-162">name</span></span>|<span data-ttu-id="d96b1-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="d96b1-163">String</span></span>|<span data-ttu-id="d96b1-164">No</span><span class="sxs-lookup"><span data-stu-id="d96b1-164">No</span></span>|<span data-ttu-id="d96b1-165">No</span><span class="sxs-lookup"><span data-stu-id="d96b1-165">No</span></span>|<span data-ttu-id="d96b1-166">El nombre para mostrar del proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="d96b1-166">The display name of the identity provider.</span></span>|
|<span data-ttu-id="d96b1-167">type</span><span class="sxs-lookup"><span data-stu-id="d96b1-167">type</span></span>|<span data-ttu-id="d96b1-168">Cadena</span><span class="sxs-lookup"><span data-stu-id="d96b1-168">String</span></span>|<span data-ttu-id="d96b1-169">Sí</span><span class="sxs-lookup"><span data-stu-id="d96b1-169">Yes</span></span>|<span data-ttu-id="d96b1-170">No</span><span class="sxs-lookup"><span data-stu-id="d96b1-170">No</span></span>|<span data-ttu-id="d96b1-171">El tipo de proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="d96b1-171">The identity provider type.</span></span> <span data-ttu-id="d96b1-172">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="d96b1-172">It must be one of the following values:</span></span> <ul><li/><span data-ttu-id="d96b1-173">Microsoft</span><span class="sxs-lookup"><span data-stu-id="d96b1-173">Microsoft</span></span><li/><span data-ttu-id="d96b1-174">Google</span><span class="sxs-lookup"><span data-stu-id="d96b1-174">Google</span></span><li/><span data-ttu-id="d96b1-175">Amazon</span><span class="sxs-lookup"><span data-stu-id="d96b1-175">Amazon</span></span><li/><span data-ttu-id="d96b1-176">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="d96b1-176">LinkedIn</span></span><li/><span data-ttu-id="d96b1-177">Facebook</span><span class="sxs-lookup"><span data-stu-id="d96b1-177">Facebook</span></span></ul>|

### <a name="where-to-get-the-client-id-and-secret"></a><span data-ttu-id="d96b1-178">Dónde obtener al cliente de identificador y el secreto</span><span class="sxs-lookup"><span data-stu-id="d96b1-178">Where to get the client ID and secret</span></span>

<span data-ttu-id="d96b1-179">Cada proveedor de identidad tiene un proceso para la creación de un registro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d96b1-179">Each identity provider has a process for creating an app registration.</span></span> <span data-ttu-id="d96b1-180">Por ejemplo, los usuarios crear un registro de la aplicación con Facebook en [developers.facebook.com](https://developers.facebook.com/).</span><span class="sxs-lookup"><span data-stu-id="d96b1-180">For example, users create an app registration with Facebook at [developers.facebook.com](https://developers.facebook.com/).</span></span> <span data-ttu-id="d96b1-181">El identificador de cliente resultante y el secreto de cliente se pueden pasar al [crear identityProvider](../api/identityprovider-post-identityproviders.md).</span><span class="sxs-lookup"><span data-stu-id="d96b1-181">The resulting client ID and client secret can be passed to [create identityProvider](../api/identityprovider-post-identityproviders.md).</span></span> <span data-ttu-id="d96b1-182">A continuación, cada objeto de usuario en el directorio se puede federar en cualquiera de los proveedores de identidad del inquilino para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="d96b1-182">Then, each user object in the directory can be federated to any of the tenant's identity providers for authentication.</span></span> <span data-ttu-id="d96b1-183">Esto permite al usuario iniciar sesión escribiendo las credenciales de inicio de sesión del proveedor de identidad en la página.</span><span class="sxs-lookup"><span data-stu-id="d96b1-183">This enables the user to sign in by entering credentials on the identity provider's sign in page.</span></span> <span data-ttu-id="d96b1-184">El símbolo (token) desde el proveedor de identidad se valida por Azure AD antes de que el inquilino emite un token para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d96b1-184">The token from the identity provider is validated by Azure AD before the tenant issues a token to the application.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d96b1-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d96b1-185">JSON representation</span></span>

<span data-ttu-id="d96b1-186">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d96b1-186">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.IdentityProvider"
} -->

```json
{
    "id": "String",
    "type": "String",
    "name": "String",
    "clientId": "String",
    "clientSecret": "String"
}
```