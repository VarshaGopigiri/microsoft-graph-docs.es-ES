---
title: tipo de enumeración firewallCertificateRevocationListCheckMethodType
description: Valores posibles para firewallCertificateRevocationListCheckMethod
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e479b10339ab515a17f67d85de0c8d43c1507825
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940060"
---
# <a name="firewallcertificaterevocationlistcheckmethodtype-enum-type"></a><span data-ttu-id="00e54-103">tipo de enumeración firewallCertificateRevocationListCheckMethodType</span><span class="sxs-lookup"><span data-stu-id="00e54-103">firewallCertificateRevocationListCheckMethodType enum type</span></span>

> <span data-ttu-id="00e54-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="00e54-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="00e54-105">Valores posibles para firewallCertificateRevocationListCheckMethod</span><span class="sxs-lookup"><span data-stu-id="00e54-105">Possible values for firewallCertificateRevocationListCheckMethod</span></span>
## <a name="members"></a><span data-ttu-id="00e54-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="00e54-106">Members</span></span>
|<span data-ttu-id="00e54-107">Miembro	</span><span class="sxs-lookup"><span data-stu-id="00e54-107">Member</span></span>|<span data-ttu-id="00e54-108">Valor</span><span class="sxs-lookup"><span data-stu-id="00e54-108">Value</span></span>|<span data-ttu-id="00e54-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="00e54-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="00e54-110">deviceDefault</span><span class="sxs-lookup"><span data-stu-id="00e54-110">deviceDefault</span></span>|<span data-ttu-id="00e54-111">0</span><span class="sxs-lookup"><span data-stu-id="00e54-111">0</span></span>|<span data-ttu-id="00e54-112">No hay un valor configurado mediante Intune, invalidar el valor predeterminado de dispositivo configurado por el usuario</span><span class="sxs-lookup"><span data-stu-id="00e54-112">No value configured by Intune, do not override the user-configured device default value</span></span>|
|<span data-ttu-id="00e54-113">none</span><span class="sxs-lookup"><span data-stu-id="00e54-113">none</span></span>|<span data-ttu-id="00e54-114">1</span><span class="sxs-lookup"><span data-stu-id="00e54-114">1</span></span>|<span data-ttu-id="00e54-115">No comprobar la lista de revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="00e54-115">Do not check certificate revocation list</span></span>|
|<span data-ttu-id="00e54-116">intento de</span><span class="sxs-lookup"><span data-stu-id="00e54-116">attempt</span></span>|<span data-ttu-id="00e54-117">2</span><span class="sxs-lookup"><span data-stu-id="00e54-117">2</span></span>|<span data-ttu-id="00e54-118">Intente la comprobación de CRL y permitir que un certificado sólo si el certificado está confirmado por la comprobación de</span><span class="sxs-lookup"><span data-stu-id="00e54-118">Attempt CRL check and allow a certificate only if the certificate is confirmed by the check</span></span>|
|<span data-ttu-id="00e54-119">requerir</span><span class="sxs-lookup"><span data-stu-id="00e54-119">require</span></span>|<span data-ttu-id="00e54-120">3</span><span class="sxs-lookup"><span data-stu-id="00e54-120">3</span></span>|<span data-ttu-id="00e54-121">Requerir una comprobación CRL correcta antes de permitir que un certificado</span><span class="sxs-lookup"><span data-stu-id="00e54-121">Require a successful CRL check before allowing a certificate</span></span>|



