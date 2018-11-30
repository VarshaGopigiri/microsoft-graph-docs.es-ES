---
title: Usar la API de Microsoft Graph para trabajar con Project Roma
description: Roma de proyecto es una iniciativa de Microsoft para crear un dispositivo entre experiencias de plataforma. Proyecto Roma permite a una aplicación en un cliente local o el servicio para interactuar con las aplicaciones y servicios en un host remoto cuando el usuario inicia sesión con la misma cuenta de Microsoft que se utilizan para iniciar sesión en el dispositivo de cliente. Esto le permite a las experiencias de entre el dispositivo y multiplataforma de programa que se centran en las tareas de usuario en lugar de dispositivos.
ms.openlocfilehash: ab703ff76d3da4ec1c6a8cd1189f3d85e57bac65
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030696"
---
# <a name="use-the-microsoft-graph-api-to-work-with-project-rome"></a>Usar la API de Microsoft Graph para trabajar con Project Roma

[Roma de proyecto](https://developer.microsoft.com/en-us/windows/project-rome) es una iniciativa de Microsoft para crear un dispositivo entre experiencias de plataforma. Proyecto Roma permite a una aplicación en un cliente local o el servicio para interactuar con las aplicaciones y servicios en un host remoto cuando el usuario inicia sesión con la misma cuenta de Microsoft que se utilizan para iniciar sesión en el dispositivo de cliente. Esto le permite a las experiencias de entre el dispositivo y multiplataforma de programa que se centran en las tareas de usuario en lugar de dispositivos.

Un componente clave se expone a través de Microsoft Graph para habilitar estas evaluaciones: actividades.

## <a name="activities"></a>Actividades

Actividades en Microsoft Graph habilitar compromiso de usuario de unidad con sus aplicaciones en dispositivos y plataformas. Una actividad es la unidad de contratación de usuario y se compone de tres componentes:

- Un vínculo profundo
- Una representación visual
- Los metadatos de contenido que describe la actividad, con el [https://schema.org/](https://schema.org/) shared vocabulario

Cuando se crea una sesión de una aplicación, se agrega un elemento de historial a la actividad para reflejar el período de contratación de usuario. Cada vez que un usuario reengages con una actividad, se agrega un nuevo elemento de historial a la actividad para acumular compromiso de usuario.

Cuando una aplicación publica los objetos de actividad de usuario, el objeto se mostrará en algunas de las nuevas superficies de la interfaz de usuario de Windows; Por ejemplo, las notificaciones de Cortana y escala de tiempo. Puede especificar metadatos enriquecidos (para permitir actividades se presenten en el contexto de derecho) y elementos visuales enriquecidos (con el marcado de la [Tarjeta de adaptable](https://adaptivecards.io/) ) en los objetos de actividad.

Puede usar las siguientes API de gráfico de Microsoft para crear y recuperar las actividades del usuario:

- [Crear o reemplazar la actividad](../api/projectrome-put-activity.md)
- [Obtener las actividades](../api/projectrome-get-activities.md)
- [Obtener actividades recientes](../api/projectrome-get-recent-activities.md)
- [Eliminar una actividad](../api/projectrome-delete-activity.md)
- [Crear o reemplazar un elemento de historial](../api/projectrome-put-historyitem.md)
- [Eliminar un elemento de historial](../api/projectrome-delete-historyitem.md)

