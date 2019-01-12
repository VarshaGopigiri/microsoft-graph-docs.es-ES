---
title: tipo de enumeración firewallCertificateRevocationListCheckMethodType
description: Valores posibles para firewallCertificateRevocationListCheckMethod
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 915fab77e7a2c28ab9d6902f3e1cb7d2d05cb2b0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27958414"
---
# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a><span data-ttu-id="4be4e-103">tipo de enumeración firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="4be4e-103">firewallCertificateRevocationListCheckMethodType enum type</span></span>

> <span data-ttu-id="4be4e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4be4e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4be4e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4be4e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4be4e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4be4e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4be4e-107">Valores posibles para firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="4be4e-107">Possible values for firewallCertificateRevocationListCheckMethod</span></span>
## <a name="members"></a><span data-ttu-id="4be4e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4be4e-108">Members</span></span>
|<span data-ttu-id="4be4e-109">Miembro	</span><span class="sxs-lookup"><span data-stu-id="4be4e-109">Member</span></span>|<span data-ttu-id="4be4e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="4be4e-110">Value</span></span>|<span data-ttu-id="4be4e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4be4e-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4be4e-112">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="4be4e-112">deviceDefault</span></span>|<span data-ttu-id="4be4e-113">0</span><span class="sxs-lookup"><span data-stu-id="4be4e-113">0</span></span>|<span data-ttu-id="4be4e-114">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="4be4e-114">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="4be4e-115">none</span><span class="sxs-lookup"><span data-stu-id="4be4e-115">none</span></span>|<span data-ttu-id="4be4e-116">1</span><span class="sxs-lookup"><span data-stu-id="4be4e-116">1</span></span>|<span data-ttu-id="4be4e-117">No comprobar la lista de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="4be4e-117">Do not check certificate revocation list</span></span>|
|<span data-ttu-id="4be4e-118">intento de</span><span class="sxs-lookup"><span data-stu-id="4be4e-118">attempt</span></span>|<span data-ttu-id="4be4e-119">2</span><span class="sxs-lookup"><span data-stu-id="4be4e-119">2</span></span>|<span data-ttu-id="4be4e-120">Intente la comprobación de CRL y permitir que un certificado sólo si el certificado está confirmado por la comprobación de</span><span class="sxs-lookup"><span data-stu-id="4be4e-120">Attempt CRL check and allow a certificate only if the certificate is confirmed by the check</span></span>|
|<span data-ttu-id="4be4e-121">requerir</span><span class="sxs-lookup"><span data-stu-id="4be4e-121">require</span></span>|<span data-ttu-id="4be4e-122">3</span><span class="sxs-lookup"><span data-stu-id="4be4e-122">3</span></span>|<span data-ttu-id="4be4e-123">Requerir una comprobación CRL correcta antes de permitir que un certificado</span><span class="sxs-lookup"><span data-stu-id="4be4e-123">Require a successful CRL check before allowing a certificate</span></span>|





