# 📒 Note App – Spring Boot MVC CRUD Example

A minimal Java app that demonstrates basic CRUD using **Spring Boot MVC**, **Thymeleaf**, and Java Collections.  
The app manages a single entity: `Note`, with a **pure HTML UI** (no frameworks) and in-memory storage via `HashMap`.

---

## Implemented Features

### ✅ Entity
**Note**
- `id` (Long, auto-generated)
- `title` (String)
- `content` (String)

### ✅ Service Layer
Encapsulates business logic in a Spring `@Service`.  
Provides full CRUD operations:
- Create (`add`)
- Read (`getById`, `getAll`)
- Update (`update(Note note)`) — updates title/content by id
- Delete (`deleteById`)

Uses a `HashMap<Long, Note>` to simulate DB behavior and `AtomicLong` for unique id generation.

### ✅ Web Layer (Spring MVC)
`NoteController` with routes:
- `GET /note/list` — list notes
- `GET /note/create` — show create form
- `POST /note/create` — create note
- `GET /note/edit?id=123` — show edit form (id as query parameter)
- `POST /note/edit` — update note (id and fields in request body)
- `POST /note/delete` — delete note (id in request body)

### ✅ UI (Pure HTML + Thymeleaf)
Simple templates
- `templates/note/list.html`
- `templates/note/create.html`
- `templates/note/edit.html`
# Java-Dev-Module-16-Spring-Boot-Data
# Java-Dev-Module-16-Spring-Boot-Data
