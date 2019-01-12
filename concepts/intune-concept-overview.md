---
title: Información general sobre la API de dispositivos y aplicaciones de Intune
description: 'Microsoft Intune ayuda a las empresas a administrar dispositivos y aplicaciones de una organización. Puede usar la API de Intune en Microsoft Graph para administrar dispositivos, aplicaciones e incluso configurar Intune usando las herramientas que prefiera. '
author: tfitzmac
localization_priority: Priority
ms.prod: intune
ms.openlocfilehash: 3fc51a81bce93de3b17b8107158998a3b5764da4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913669"
---
# <a name="intune-devices-and-apps-api-overview"></a><span data-ttu-id="72855-104">Información general sobre la API de dispositivos y aplicaciones de Intune</span><span class="sxs-lookup"><span data-stu-id="72855-104">Intune devices and apps API overview</span></span>

<span data-ttu-id="72855-105">Microsoft Intune ayuda a las empresas a administrar dispositivos y aplicaciones de una organización.</span><span class="sxs-lookup"><span data-stu-id="72855-105">Microsoft Intune helps enterprises manage devices and apps within an organization.</span></span> <span data-ttu-id="72855-106">Puede usar la API de Intune en Microsoft Graph para administrar dispositivos, aplicaciones e incluso configurar Intune usando las herramientas que prefiera.</span><span class="sxs-lookup"><span data-stu-id="72855-106">You can use the Intune API in Microsoft Graph to manage devices, apps, and even configure Intune while using your preferred tools.</span></span> 

<span data-ttu-id="72855-107">Si es un ISV, también puede usar la API de Intune para administrar a los inquilinos de cliente.</span><span class="sxs-lookup"><span data-stu-id="72855-107">If you're an ISV, you can also use the Intune API to manage client tenants.</span></span>

## <a name="why-integrate-with-intune"></a><span data-ttu-id="72855-108">¿Por qué debería realizar la integración con Intune?</span><span class="sxs-lookup"><span data-stu-id="72855-108">Why integrate with Intune?</span></span>

<span data-ttu-id="72855-109">Puede usar la API de Intune en Microsoft Graph para acceder a información de dispositivos y aplicaciones de Intune, administrar dispositivos y aplicaciones, y automatizar Intune.</span><span class="sxs-lookup"><span data-stu-id="72855-109">You can use the Intune API in Microsoft Graph to access Intune device and application information, manage devices, manage apps, and automate Intune.</span></span>

### <a name="manage-devices"></a><span data-ttu-id="72855-110">Administrar dispositivos</span><span class="sxs-lookup"><span data-stu-id="72855-110">Manage devices</span></span>

<span data-ttu-id="72855-111">Puede usar la API de Intune para:</span><span class="sxs-lookup"><span data-stu-id="72855-111">You can use the Intune API to:</span></span>

- <span data-ttu-id="72855-112">Definir y aplicar directivas de [cumplimiento de dispositivo](/graph/api/resources/intune-deviceconfig-devicecomplianceactionitem?view=graph-rest-1.0), como la complejidad de la contraseña y su duración, el cifrado, los niveles de protección de amenazas y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="72855-112">Define and enforce [device compliance](/graph/api/resources/intune-deviceconfig-devicecomplianceactionitem?view=graph-rest-1.0) policies, such as password complexity and duration, encryption, threat protection levels, and so on.</span></span>  <span data-ttu-id="72855-113">(Las directivas compatibles varían según el sistema operativo y la versión).</span><span class="sxs-lookup"><span data-stu-id="72855-113">(Supported policies vary according to operating system and version).</span></span>
- <span data-ttu-id="72855-114">[Proteger los datos de la compañía](/graph/api/resources/intune-mam-windowsinformationprotectionpolicy?view=graph-rest-1.0), independientemente de si la plataforma del dispositivo es Windows, Mac, Android o iOS.</span><span class="sxs-lookup"><span data-stu-id="72855-114">[Protect company data](/graph/api/resources/intune-mam-windowsinformationprotectionpolicy?view=graph-rest-1.0), regardless of whether the device platform is Windows, Android, Mac, or iOS.</span></span>
- <span data-ttu-id="72855-115">Crear e implementar directivas de [configuración de dispositivo](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-1.0), incluyendo la plataforma del sistema operativo y el control de versiones, la pertenencia a un dominio y la administración de las opciones de configuración.</span><span class="sxs-lookup"><span data-stu-id="72855-115">Create and deploy [device configuration](/graph/api/resources/intune-deviceconfig-deviceconfiguration?view=graph-rest-1.0) policies, including operating system platform/versioning, domain membership, and configuration setting management.</span></span>
- <span data-ttu-id="72855-116">Crear e implementar directivas de [control de acceso](/graph/api/resources/intune-onboarding-onpremisesconditionalaccesssettings?view=graph-rest-1.0) a dispositivos, incluyendo descarga restringida, acceso accesorio de red y transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="72855-116">Create and deploy device [access control](/graph/api/resources/intune-onboarding-onpremisesconditionalaccesssettings?view=graph-rest-1.0) policies, including restricted download, network accessory access, and file transfer.</span></span>
- <span data-ttu-id="72855-117">Realizar [acciones remotas](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0), como buscar el dispositivo, cambiar la contraseña y borrar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72855-117">Perform [remote actions](/graph/api/resources/intune-devices-manageddevice?view=graph-rest-1.0), such as locate device, change password, and wipe device.</span></span>

### <a name="manage-apps"></a><span data-ttu-id="72855-118">Administrar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="72855-118">Manage apps</span></span> 

<span data-ttu-id="72855-119">Puede usar la API de Intune para realizar las siguientes tareas de administración de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="72855-119">You can use the Intune API to perform the following app management tasks:</span></span>

- <span data-ttu-id="72855-120">Implementar [aplicaciones en dispositivos](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-1.0) o impedir que se implementen aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="72855-120">Deploy [apps to devices](/graph/api/resources/intune-apps-mobileapp?view=graph-rest-1.0) or prevent apps from being deployed.</span></span>
- <span data-ttu-id="72855-121">Administrar el acceso a [libros electrónicos](/graph/api/resources/intune-books-ebookinstallsummary?view=graph-rest-1.0) y otros servicios relacionados.</span><span class="sxs-lookup"><span data-stu-id="72855-121">Manage access to [ebooks](/graph/api/resources/intune-books-ebookinstallsummary?view=graph-rest-1.0) and related services.</span></span>
- <span data-ttu-id="72855-122">Definir e implementar opciones de configuración, opciones de protección y directivas de uso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="72855-122">Define and deploy app configuration settings, app protection settings, and app usage policies.</span></span>

### <a name="automate-intune"></a><span data-ttu-id="72855-123">Automatizar Intune</span><span class="sxs-lookup"><span data-stu-id="72855-123">Automate Intune</span></span>

<span data-ttu-id="72855-124">Automatice Intune mediante la API de Intune para:</span><span class="sxs-lookup"><span data-stu-id="72855-124">Automate Intune by using the Intune API to:</span></span>

- <span data-ttu-id="72855-125">Definir y asignar controles de acceso [basados en roles](/graph/api/resources/intune-rbac-conceptual?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="72855-125">Define and assign [role based](/graph/api/resources/intune-rbac-conceptual?view=graph-rest-1.0) access controls.</span></span>
- <span data-ttu-id="72855-126">Auditar y crear informes de cumplimiento, uso y acceso.</span><span class="sxs-lookup"><span data-stu-id="72855-126">Audit and report compliance, usage, and access.</span></span>
- <span data-ttu-id="72855-127">Administrar [gastos de telecomunicaciones](/graph/api/resources/intune-tem-conceptual?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="72855-127">Manage [telecom expenses](/graph/api/resources/intune-tem-conceptual?view=graph-rest-1.0).</span></span>

## <a name="api-reference"></a><span data-ttu-id="72855-128">Referencia de la API</span><span class="sxs-lookup"><span data-stu-id="72855-128">API reference</span></span>
<span data-ttu-id="72855-129">¿Busca la referencia de la API para este servicio?</span><span class="sxs-lookup"><span data-stu-id="72855-129">Looking for the API reference for this service?</span></span>

- [<span data-ttu-id="72855-130">API de Intune en Microsoft Graph v1.0</span><span class="sxs-lookup"><span data-stu-id="72855-130">Intune API in Microsoft Graph v1.0</span></span>](/graph/api/resources/intune-graph-overview?view=graph-rest-1.0)
- [<span data-ttu-id="72855-131">API de Intune en Microsoft Graph beta</span><span class="sxs-lookup"><span data-stu-id="72855-131">Intune API in Microsoft Graph beta</span></span>](/graph/api/resources/intune-graph-overview?view=graph-rest-beta)

## <a name="next-steps"></a><span data-ttu-id="72855-132">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="72855-132">Next steps</span></span>

- <span data-ttu-id="72855-133">[Usar Azure AD para obtener acceso a la API de Intune](https://docs.microsoft.com/intune/intune-graph-apis).</span><span class="sxs-lookup"><span data-stu-id="72855-133">[Use Azure AD to access the Intune API](https://docs.microsoft.com/intune/intune-graph-apis).</span></span>
- <span data-ttu-id="72855-134">Obtenga información sobre cómo realizar tareas comunes con los [ejemplos de Intune de PowerShell](https://github.com/microsoftgraph/powershell-intune-samples).</span><span class="sxs-lookup"><span data-stu-id="72855-134">See how to perform common tasks by using the [PowerShell Intune samples](https://github.com/microsoftgraph/powershell-intune-samples).</span></span>
- <span data-ttu-id="72855-135">Descubra cómo [Usar la API de REST de Intune](/graph/api/resources/intune-graph-overview?view=graph-rest-1.0).</span><span class="sxs-lookup"><span data-stu-id="72855-135">Find out how to [use the Intune REST API](/graph/api/resources/intune-graph-overview?view=graph-rest-1.0).</span></span>
- <span data-ttu-id="72855-136">Consulte el [registro de cambios](changelog.md) para obtener información sobre las novedades de la API de Intune.</span><span class="sxs-lookup"><span data-stu-id="72855-136">See the [Changelog](changelog.md) for information about what's new in the Intune API.</span></span>
- <span data-ttu-id="72855-137">Explore los [ejemplos](https://developer.microsoft.com/graph/graph/examples) para obtener más ideas sobre cómo usar Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="72855-137">Explore [examples](https://developer.microsoft.com/graph/graph/examples) for more ideas about how to use Microsoft Graph.</span></span>
