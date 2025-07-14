
# 🐹 Go + Gin Progressive Assignment Series
**Goal:** Walk a novice through building a feature‑complete REST backend for the Garage Management System, step by step, so every core concept (routing, validation, DB, relationships, auth, testing, deployment) is learned in logical progression.

---

## Assignment 1 (Day 1‑3) – Basic Server & Health Check
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 1.1 | Create project skeleton `garage-backend` with **standard Go layout** (`cmd/`, `internal/`, `pkg/`) | Go modules, folder conventions |
| 1.2 | Write `cmd/garage-api/main.go` using **Gin**. Add `/healthz` GET returning `{ "status": "ok" }` | Gin basics, JSON response |
| 1.3 | Enable **hot‑reload** with `air` or `fresh` (optional) | Faster dev loop |
| 1.4 | Learn to render Html and Css and images and static files via gin and go  | Faster dev loop |

---

## Assignment 2 (Day 4‑6) – Vehicles CRUD (No DB yet)
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 2.1 | Add `/api/v1/vehicles` routes: GET (list), POST (create), PUT, DELETE. Store data **in‑memory slice** | Routing groups, HTTP verbs |
| 2.2 | Validate JSON with Gin `binding` tags (e.g., `required`) | Payload validation |
| 2.3 | Return proper HTTP status codes & error objects | API design principles |

---

## Assignment 3 (Day 7‑9) – PostgreSQL & GORM Integration
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 3.1 | Spin up **Postgres** via Docker Compose. Create DB `garage_db` | DB setup |
| 3.2 | Add GORM connection in `internal/db/postgres.go`; read creds from `.env` | Env config, connection pooling |
| 3.3 | Replace in‑memory slice with **GORM model `Vehicle`**; auto‑migrate | ORM modeling |
| 3.4 | Refactor handlers to use `repository` layer for DB CRUD | Layered architecture |

---

## Assignment 4 (Day 10‑12) – Dropdown‑Style Data & Relationships
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 4.1 | Create table/model `VehicleType` (id, name) and seed 3 types | Reference data |
| 4.2 | Add FK `vehicle_type_id` to `Vehicle`; preload type on GET | GORM relations, preloading |
| 4.3 | Endpoint `GET /api/v1/vehicle-types` to feed frontend dropdown | REST for reference tables |

---

## Assignment 5 (Day 13‑15) – Edit & Cascading Updates
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 5.1 | Implement **PUT /vehicles/:id** to update vehicle & its type | Complex updates |
| 5.2 | Add transaction wrapper to guarantee atomic update | GORM transactions |
| 5.3 | Write **unit test** for update service using `sqlmock` | Testing with mocks |

---

## Assignment 6 (Day 16‑17) – Validation & Custom Errors
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 6.1 | Add struct‑level validation: reg_no must be unique regex `[A-Z]{2}\d{2}...` | Advanced validation |
| 6.2 | Create centralized `ErrorResponse{code,message}`; Gin middleware to format all errors | Consistent error API |

---

## Assignment 7 (Day 18‑20) – User Auth with JWT
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 7.1 | Create `User` model (id, email, password_hash, role) | Auth groundwork |
| 7.2 | Build `/register` & `/login` (hash with bcrypt, issue JWT) | Security best practices |
| 7.3 | Protect all `/vehicles` mutating routes with **JWT middleware** | Middleware chaining |

---

## Assignment 8 (Day 21‑23) – Garage ↔ Vehicle Relationship
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 8.1 | Make `Garage` model (name, location) & FK in Vehicle | One‑to‑many |
| 8.2 | Endpoint sequence:<br>• POST `/garages`<br>• GET `/garages/:id/vehicles` | Nested routing |
| 8.3 | Add cascading delete (garage deletes its vehicles) & test | ON DELETE CASCADE, integration tests |

---

## Assignment 9 (Day 24‑26) – Pagination, Filtering, Sorting
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 9.1 | Add query params `page`, `size`, `sort` to `/vehicles` | Query building |
| 9.2 | Implement reusable `PaginatedResponse` struct | API usability |
| 9.3 | Index on `reg_no` & `vehicle_type_id` for performance | Postgres indices |

---

## Assignment 10 (Day 27‑29) – Logging & Observability
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 10.1 | Integrate **Zap** logger; add requestID middleware | Structured logs |
| 10.2 | Expose `/metrics` (Prometheus via `gin-prometheus`) | Basic metrics |
| 10.3 | Log SQL execution time via GORM callback | Performance tracing |

---

## Assignment 11 (Day 30‑32) – Docker & CI/CD
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 11.1 | Create multi‑stage **Dockerfile** for API | Containerization |
| 11.2 | Expand `docker-compose.yml` to include Postgres + API | Local orchestration |
| 11.3 | Add GitHub Actions: lint → test → build → docker push | Continuous delivery |

---

## Assignment 12 (Day 33‑35) – Graceful Shutdown & Deployment
| Task | Details | Learning Outcome |
|------|---------|------------------|
| 12.1 | Add context‑aware shutdown (`http.Server.Shutdown`) | Production readiness |
| 12.2 | Deploy to Render/Fly.io (or VPS) using Docker image | Cloud deployment |
| 12.3 | Document all env variables and setup in `README` | Ops documentation |

---

> **By the end** the learner will have built a fully‑featured, production‑ready REST API with authentication, relational data, validations, paging, logging, and CI/CD—all using idiomatic Go, Gin, GORM, and PostgreSQL.
