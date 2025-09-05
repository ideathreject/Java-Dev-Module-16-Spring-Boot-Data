# 📒 Note App – Spring Boot MVC + JPA + Flyway (CRUD)

A minimal Java app that demonstrates CRUD for a single entity **Note** using **Spring Boot MVC**, **Thymeleaf**, **Spring Data JPA**, **H2**, and **Flyway**.  


---

## Implemented Features

### ✅ Entity
**Note**
- `id` (Long, auto-generated)
- `title` (String, required)
- `content` (String, up to 2000 chars)

### ✅ Persistence (JPA + Flyway)
- `@Entity`-annotated `Note` mapped to table `note`
- `NoteRepository extends JpaRepository<Note, Long>`
- Schema managed by **Flyway** migrations (V1 creates table `note`)


### ✅ Service Layer 
CRUD operations:
- Create (`add`)
- Read (`getById`, `getAll`)
- Update (`update(Note note)`)
- Delete (`deleteById`)

### ✅ Web Layer (Spring MVC) — Routing per mentor spec
`NoteController` routes:
- `GET /note/list` — list notes
- `GET /note/create` — show create form
- `POST /note/create` — create note
- `GET /note/edit?id=123` — show edit form (**id in query**)
- `POST /note/edit` — update note (**id + fields in body**)
- `POST /note/delete` — delete note (**id in body**)

### ✅ UI (Pure HTML + Thymeleaf)
- `templates/note/list.html`
- `templates/note/create.html`
- `templates/note/edit.html`

