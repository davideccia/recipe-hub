# Goal
This repository contains an identical REST API and/or frontend application implemented across multiple framework stacks.
Each implementation maintains functional parity to enable direct architectural comparison.

## Specification
Each implementation provides:
- Identical REST endpoints (according to conventions)
- Same data models (according to conventions)
- Equivalent frontend UI/UX

# The App
RecipeHub, an application for recipe management.

## Data Models
| Entity                  | Column                     | Type/Constraints                                   |
|-------------------------|----------------------------|----------------------------------------------------|
| **Users**               |                            |                                                    |
| **Ingredients**         |                            |                                                    |
|                         | user reference             | nullable (null = admin-managed common ingredients) |
|                         | name                       |                                                    |
|                         | allergens                  | JSON                                               |
| **Measurement Units**   |                            | admin-managed                                      |
|                         | name                       |                                                    |
|                         | label                      | e.g. "kg"                                          |
| **Recipes**             |                            |                                                    |
|                         | user reference             |                                                    |
|                         | title                      |                                                    |
|                         | description                | nullable                                           |
|                         | public                     | default: false                                     |
|                         | difficulty                 | max: 10                                            |
|                         | rating                     | calculated on review create/update                 |
| **Ingredient - Recipe** |                            |                                                    |
|                         | ingredient reference       |                                                    |
|                         | recipe reference           |                                                    |
|                         | measurement unit reference |                                                    |
|                         | quantity                   |                                                    |
|                         | notes                      | nullable                                           |
| **Reviews**             |                            |                                                    |
|                         | user reference             |                                                    |
|                         | recipe reference           |                                                    |
|                         | value                      | max: 10                                            |
|                         | title                      |                                                    |
|                         | description                | nullable                                           |

# Tree

<table style="width: 100%; border-collapse: collapse; text-align: center; table-layout: fixed;">
  <thead>
    <tr>
      <th>FW</th>
      <th>Repo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        API List
      </td>
      <td>
        <a target="_blank" href="https://github.com/davideccia/recipe-hub-api-list.git">Click here</a>
      </td>
    </tr>
    <tr>
      <td>
        <img style="width: 100%; max-width: 100%; height: auto; display: block;" src="https://raw.githubusercontent.com/laravel/art/refs/heads/master/logo-lockup/5%20SVG/3%20rgb/1%20Full%20Color/laravel-logolockup-rgb-red.svg" alt="Descrizione immagine" />
      </td>
      <td>
        <a target="_blank" href="https://github.com/davideccia/recipe-hub-laravel/tree/fc73b7a75f5294cbeae35035918992c07ee995d8">Click here</a>
      </td>
    </tr>
  </tbody>
</table>
