---
title: tipo de recurso educationSynchronizationConnectionSettings
description: 'Representa la configuración de conexión del proveedor. Esto permite que el sistema saber cómo conectarse al proveedor de API. '
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 17fedb5094016bd3df3bd8262390eaa7eeb37537
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27841772"
---
# <a name="educationsynchronizationconnectionsettings-resource-type"></a><span data-ttu-id="304c3-104">tipo de recurso educationSynchronizationConnectionSettings</span><span class="sxs-lookup"><span data-stu-id="304c3-104">educationSynchronizationConnectionSettings resource type</span></span>

> <span data-ttu-id="304c3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="304c3-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="304c3-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="304c3-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="304c3-107">Representa la configuración de conexión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="304c3-107">Represents the provider connection settings.</span></span> <span data-ttu-id="304c3-108">Esto permite que el sistema saber cómo conectarse al proveedor de API.</span><span class="sxs-lookup"><span data-stu-id="304c3-108">This allows the system to know how to connect to the provider APIs.</span></span> 

> <span data-ttu-id="304c3-109">**Nota:** Este tipo complejo es abstracta.</span><span class="sxs-lookup"><span data-stu-id="304c3-109">**Note:** This complex type is abstract.</span></span> <span data-ttu-id="304c3-110">Hacer referencia a los tipos específicos de la configuración de conexión que aparecen.</span><span class="sxs-lookup"><span data-stu-id="304c3-110">Refer to the specific types of connection settings listed.</span></span>

## <a name="derived-types"></a><span data-ttu-id="304c3-111">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="304c3-111">Derived types</span></span>
| <span data-ttu-id="304c3-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="304c3-112">Type</span></span> | <span data-ttu-id="304c3-113">Description</span><span class="sxs-lookup"><span data-stu-id="304c3-113">Description</span></span> | 
|:-|:-|
| [<span data-ttu-id="304c3-114">**educationSynchronizationOAuth1ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="304c3-114">**educationSynchronizationOAuth1ConnectionSettings**</span></span>](educationsynchronizationoauth1connectionsettings.md) | <span data-ttu-id="304c3-115">Use este tipo para proporcionar la configuración de conexión de OAuth1.</span><span class="sxs-lookup"><span data-stu-id="304c3-115">Use this type to provide OAuth1 connection settings.</span></span> |
| [<span data-ttu-id="304c3-116">**educationSynchronizationOAuth2ClientCredentialsConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="304c3-116">**educationSynchronizationOAuth2ClientCredentialsConnectionSettings**</span></span>](educationsynchronizationoauth2clientcredentialsconnectionsettings.md) | <span data-ttu-id="304c3-117">Use este tipo para proporcionar la configuración de conexión de concesión de las credenciales de cliente de OAuth2.</span><span class="sxs-lookup"><span data-stu-id="304c3-117">Use this type to provide OAuth2 Client Credentials Grant connection settings.</span></span> |

## <a name="properties"></a><span data-ttu-id="304c3-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="304c3-118">Properties</span></span>

| <span data-ttu-id="304c3-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="304c3-119">Property</span></span> | <span data-ttu-id="304c3-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="304c3-120">Type</span></span> | <span data-ttu-id="304c3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="304c3-121">Description</span></span> |
|:-|:-|:-|
| <span data-ttu-id="304c3-122">**clientId**</span><span class="sxs-lookup"><span data-stu-id="304c3-122">**clientId**</span></span> | <span data-ttu-id="304c3-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="304c3-123">String</span></span> |  <span data-ttu-id="304c3-124">Identificador de cliente que se usa para conectarse al proveedor de.</span><span class="sxs-lookup"><span data-stu-id="304c3-124">Client ID used to connect to the provider.</span></span> |
| <span data-ttu-id="304c3-125">**clientSecret**</span><span class="sxs-lookup"><span data-stu-id="304c3-125">**clientSecret**</span></span> | <span data-ttu-id="304c3-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="304c3-126">String</span></span> |  <span data-ttu-id="304c3-127">Secreto de cliente para autenticar la conexión con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="304c3-127">Client secret to authenticate the connection to the provider.</span></span> |
