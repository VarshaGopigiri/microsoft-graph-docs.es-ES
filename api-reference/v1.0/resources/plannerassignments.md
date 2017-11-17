<span data-ttu-id="cce79-p103">En este ejemplo se quita el usuario con el id. ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 de la lista de personas asignadas de la tarea y se cambia el orden de la persona asignada con el id. de usuario 4e98f8f1-bb03-4015-b8e0-19bb370949d8. Si la tarea todavía no está asignada al usuario con el identificador 4e98f8f1-bb03-4015-b8e0-19bb370949d8, al actualizar las asignaciones con este valor, se asignará la tarea a este usuario.</span><span class="sxs-lookup"><span data-stu-id="cce79-p103">This example removes user with ID ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 from the assignees list of the task, while changing the order of the assignee with user ID 4e98f8f1-bb03-4015-b8e0-19bb370949d8. If the task isn't already assigned to user with ID 4e98f8f1-bb03-4015-b8e0-19bb370949d8, updating the assignments with this value will assign the task to this user.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignments"
}-->

```json
{
  "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47": null,
  "4e98f8f1-bb03-4015-b8e0-19bb370949d8": { 
      "@odata.type": "microsoft.graph.plannerAssignment",
      "orderHint": "String"
    }
}
```
En este ejemplo se quita el usuario con el id. ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 de la lista de personas asignadas de la tarea y se cambia el orden de la persona asignada con el id. de usuario 4e98f8f1-bb03-4015-b8e0-19bb370949d8. Si la tarea todavía no está asignada al usuario con el identificador 4e98f8f1-bb03-4015-b8e0-19bb370949d8, al actualizar las asignaciones con este valor, se asignará la tarea a este usuario.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignments resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->