# Free Python training curriculum: 7 chapters with curated resources

This report delivers a complete, structured Python training program across 7 chapters, each with exactly **3 textual resources and 1 video resource** — all free, practical, and code-heavy. Every chapter includes suggested exercises, and the program culminates in a capstone project that ties all 7 chapters together. Resources were selected for their depth, hands-on approach, and community reputation.

---

## Chapter 1 — Python modules, imports, and packages

Understanding the import system is foundational to writing maintainable Python. These resources progress from basics (`import`, `__init__.py`, `sys.path`) through advanced topics (namespace packages, `importlib`, import hooks).

### Textual resources

**1. Real Python — "Python Modules and Packages: An Introduction"**
- **URL:** https://realpython.com/python-modules-packages/
- Covers module creation, the `import` statement, `sys.path`, `__init__.py`, subpackages, and `__all__`. Includes a **companion quiz** for self-assessment. Well-structured progression from simple modules to complex package hierarchies.

**2. Real Python — "Python import: Advanced Techniques and Tips"**
- **URL:** https://realpython.com/python-import/
- The deep-dive resource for this chapter. Covers **namespace packages, relative vs absolute imports, `importlib`, resource files, dynamic imports, and import hooks**. Includes a quiz and downloadable source code. This is the most comprehensive free article on Python's import machinery.

**3. Python Official Documentation — "6. Modules"**
- **URL:** https://docs.python.org/3/tutorial/modules.html
- The authoritative reference covering module search path, compiled files, `dir()`, intra-package references, and `__path__`. Essential as a canonical source that complements the tutorial-style articles above.

### Video resource

**4. 🎥 Corey Schafer — "Import Modules and Exploring The Standard Library"**
- **URL:** https://www.youtube.com/playlist?list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU (Video #9 in the series)
- Covers importing custom modules, standard library exploration, and `sys.path`. Code examples available on GitHub. Part of Corey's widely acclaimed beginner series (1.5M+ subscribers).

### Suggested exercises
- **Small:** Create a utility package with 3 submodules, use `__init__.py` to expose a clean public API, and experiment with relative vs absolute imports.
- **Big:** Build a plugin system using `importlib.import_module()` that dynamically discovers and loads plugins from a `plugins/` directory at runtime. Each plugin must implement a known interface.

---

## Chapter 2 — Logging and loggers

Python's `logging` module is far more powerful than `print()` debugging. These resources cover the full hierarchy: loggers, handlers, formatters, filters, and configuration approaches.

### Textual resources

**1. Real Python — "Logging in Python"**
- **URL:** https://realpython.com/python-logging/
- Comprehensive 29-minute read (updated Oct 2025) covering basics through advanced configuration. Walks through **loggers, handlers, formatters, filters, the logging hierarchy, and best practices**. Includes FAQ-style knowledge checks throughout.

**2. Python Official Documentation — "Logging HOWTO"**
- **URL:** https://docs.python.org/3/howto/logging.html
- Two-part official guide: a basic tutorial plus an advanced section on loggers, handlers, formatters, and filters. Links to the **Logging Cookbook** (https://docs.python.org/3/howto/logging-cookbook.html) for patterns like multi-module logging, logging from threads, and contextual information.

**3. Machine Learning Plus — "Python Logging Guide"**
- **URL:** https://machinelearningplus.com/python/python-logging-guide/
- Practical guide with full working code for every concept. **Crucially includes explicit exercises** at the end, such as: "Create a logger bearing the module's name, configure it to error level, send output to a dated log file, and log a critical message." One of the few logging tutorials with structured practice problems.

### Video resource

**4. 🎥 Corey Schafer — "Logging Advanced – Loggers, Handlers, and Formatters"**
- **URL:** https://www.youtube.com/watch?v=jxmzY9soFXg
- Covers creating custom loggers with `getLogger()`, FileHandler, StreamHandler, formatters, and multi-module logging. Companion code on GitHub. Pair with his basics video (also on his channel) for a complete two-part series.

### Suggested exercises
- **Small:** Configure a multi-module application where each module has its own named logger, with a shared file handler using `RotatingFileHandler` and a console handler at different log levels.
- **Big:** Implement a structured JSON logging system using `logging` + `python-json-logger` that includes request correlation IDs, and write a log analyzer script that parses these structured logs to produce error rate statistics.

---

## Chapter 3 — Typing and conventions

Type hints transform Python from a dynamically-typed guessing game into a statically-verifiable codebase. These resources cover annotations, `mypy`, generics, `Protocol`, `dataclasses`, and PEP 8 conventions.

### Textual resources

**1. Real Python — "Python Type Checking (Guide)"**
- **URL:** https://realpython.com/python-type-checking/
- Extremely thorough guide covering type systems (dynamic, static, duck typing), **annotations, `TypeVar`, `Protocol`, generics, `Callable`, and mypy usage**. Builds a card game project progressively throughout the tutorial. Includes a companion quiz.

**2. mypy Documentation — Type Hints Cheat Sheet**
- **URL:** https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html
- Official mypy reference showing annotations for all common Python types: variables, collections, functions, classes, decorators, generics, `TypeVar`, and `Protocol`. Pure code-example format — ideal as a day-to-day reference. The broader mypy docs at https://mypy.readthedocs.io/en/stable/ cover configuration and advanced topics.

**3. Python Type Challenges (GitHub)**
- **URL:** https://github.com/laike9m/Python-Type-Challenges
- **The entire resource is exercises.** Interactive challenges ranging from basic to advanced, each with `question.py` and `solution.py`. Requires writing correct type annotations that pass mypy validation. Can be run locally or via the web interface. Inspired by TypeScript type challenges.

### Video resource

**4. 🎥 Tech With Tim — "Python Typing – Type Hints & Annotations"**
- **URL:** https://www.youtube.com/watch?v=QORvB-_mbZ0
- 25-minute tutorial covering the `typing` module, function annotations, mypy, and types including `List`, `Dict`, `Optional`, `Any`, `Sequence`, `Callable`, and `Generic`. Timestamped for easy navigation. All code demonstrated live.

### Suggested exercises
- **Small:** Take an existing untyped Python module and add complete type annotations. Run `mypy --strict` until all errors are resolved. Use `Protocol` to define a duck-typed interface.
- **Big:** Build a fully-typed generic data validation library using `dataclasses`, `Generic[T]`, `TypeVar`, and `Protocol`. Include custom validators and ensure **100% mypy strict compliance**. Write tests that verify both runtime behavior and static type correctness.

---

## Chapter 4 — uv and virtual environments

The `uv` package manager (by Astral, makers of Ruff) has rapidly become the modern replacement for pip + venv + pyenv. These resources cover uv alongside foundational virtual environment concepts.

### Textual resources

**1. uv Official Documentation**
- **URL:** https://docs.astral.sh/uv/
- Comprehensive official docs covering installation, `uv init`, `uv add`/`uv remove`, `uv run`, `uv lock`, `uv sync`, Python version management, `pyproject.toml` configuration, and migration guides from pip/Poetry. Includes integration guides for **Docker, GitHub Actions, FastAPI, and Jupyter**.

**2. freeCodeCamp — "How to Manage Python Packages with uv"**
- **URL:** https://www.freecodecamp.org/news/how-to-manage-python-packages-with-uv/
- Beginner-friendly walkthrough covering project initialization, virtual environment creation, dependency management, `uv run`, Python version management, and the `pyproject.toml`/`uv.lock` structure. Follows a **hands-on project structure** from start to finish.

**3. SaaS Pegasus — "uv: An In-Depth Guide to Python's Fast New Package Manager"**
- **URL:** https://www.saaspegasus.com/guides/uv-deep-dive/
- Updated January 2025. Covers why uv matters, environment setup, package management, `uv lock`/`uv sync`, and **comparison with traditional pip/venv workflows**. Practical step-by-step format showing the full migration path from legacy tooling.

### Video resource

**4. 🎥 Corey Schafer — "UV – A Faster, All-in-One Package Manager to Replace Pip and Venv"**
- **URL:** https://www.youtube.com/watch?v=AMdG7IjgSPM
- 27-minute tutorial covering UV installation, project initialization, dependency management with `pyproject.toml` and lock files, automatic virtual environment handling, script execution, and global tool installation. Directly **compares UV workflow with traditional pip/venv**.

### Suggested exercises
- **Small:** Initialize a new project with `uv init`, add 5 dependencies (including dev-only ones), examine the generated `pyproject.toml` and `uv.lock`, then reproduce the environment on a fresh machine with `uv sync`.
- **Big:** Migrate an existing pip-based project (with `requirements.txt`) to uv. Create a `Dockerfile` that uses `uv sync` for deterministic builds. Document the full migration process, including dependency resolution differences and speed benchmarks.

---

## Chapter 5 — Advanced Python features

Generators, decorators, context managers, descriptors, metaclasses, and ABCs form the backbone of professional Python. These resources build mastery of Python's most powerful abstractions.

### Textual resources

**1. Real Python — "Primer on Python Decorators"**
- **URL:** https://realpython.com/primer-on-python-decorators/
- In-depth tutorial covering first-class functions, simple and nested decorators, class decorators, decorators with arguments, and real-world patterns: **timing, debugging, caching, singletons, rate-limiting, and authentication**. Includes interactive quiz, downloadable sample code, and a cheat sheet.

**2. Real Python — "Python Metaclasses"**
- **URL:** https://realpython.com/python-metaclasses/
- Thorough coverage of how classes are objects, the `type` metaclass, custom metaclasses with `__new__` and `__init__`, practical use cases, and **comparisons with simpler alternatives** (inheritance, class decorators). Includes interactive quiz and step-by-step code walkthroughs.

**3. Python for You and Me (pymbook) — "Iterators, Generators and Decorators"**
- **URL:** https://pymbook.readthedocs.io/en/latest/igd.html
- Free online book chapter covering the **iterator protocol** (`__iter__`/`__next__`), generators (`yield`, generator expressions), and decorators (closures, practical examples). Part of a full free Python book with exercises at the end of sections.

### Video resource

**4. 🎥 Tech With Tim — "10 Advanced Python Features"**
- **URL:** https://www.youtube.com/watch?v=mclftDq-jOA
- 42-minute video covering advanced unpacking, **descriptors, decorators, context managers, iterators, generators/yield, itertools**, and async programming. Progressive complexity with live code demos. Tim also has an "Expert Python Tutorials" playlist diving deeper into metaclasses and dunder methods.

### Suggested exercises
- **Small:** Implement a `@retry(max_attempts=3, delay=1.0)` decorator with exponential backoff. Create a context manager that measures execution time. Write a generator that lazily reads and processes large CSV files line-by-line.
- **Big:** Build a mini ORM (Object-Relational Mapper) using **metaclasses** for model registration, **descriptors** for field validation, **`__slots__`** for memory optimization, **ABC** for the base model interface, and **context managers** for database connection handling. Support basic CRUD operations against SQLite.

---

## Chapter 6 — Concurrency in Python

Concurrency is where Python gets complex — threading vs multiprocessing vs asyncio, the GIL, and when to use each. These resources provide both conceptual clarity and hands-on practice.

### Textual resources

**1. Real Python — "Async IO in Python: A Complete Walkthrough"**
- **URL:** https://realpython.com/async-io-python/
- Extensive hands-on walkthrough covering the **full concurrency landscape** (parallelism vs concurrency vs threading vs async I/O), coroutines, event loops, `async`/`await`, `asyncio.gather()`, async context managers, and integration with **aiohttp**. Includes quiz and practical examples including building an async web crawler.

**2. Python Official Documentation — asyncio**
- **URL:** https://docs.python.org/3/library/asyncio.html
- Authoritative reference covering high-level APIs (coroutines, tasks, streams, synchronization primitives) and low-level APIs (event loops, futures, transports). Supplemented by the conceptual overview HOWTO at https://docs.python.org/3/howto/a-conceptual-overview-of-asyncio.html.

**3. SuperFastPython — "Python Asyncio: The Complete Guide"**
- **URL:** https://superfastpython.com/python-asyncio/
- A **book-length free guide** by Jason Brownlee. Exhaustive walkthrough of asyncio: event loops, tasks, `gather()`, `wait()`, TaskGroups, timeouts, running blocking I/O in executors, async iterators/generators, and async context managers. **All code downloadable as a zip file.** The site also has equally comprehensive free guides on threading (https://superfastpython.com/threading-in-python/) and multiprocessing (https://superfastpython.com/multiprocessing-in-python/).

### Video resource

**4. 🎥 Corey Schafer — "AsyncIO – Complete Guide to Asynchronous Programming"**
- **URL:** https://www.youtube.com/watch?v=Qb9s3UiMSTA
- **~1h 43min** comprehensive tutorial with **visual animations** illustrating how coroutines, tasks, and the event loop work. Covers `async`/`await`, `create_task`, `asyncio.gather()`, TaskGroup, error handling, and refactoring synchronous code to async. Companion code at https://github.com/CoreyMSchafer/AsyncIO-Code-Examples and interactive animations at https://coreyms.com/asyncio/.

### Suggested exercises
- **Small:** Write a script that fetches 20 URLs concurrently using `asyncio.gather()` + `aiohttp`, with proper error handling and a semaphore to limit concurrency to 5 simultaneous requests.
- **Big:** Build a concurrent web scraper that uses **asyncio** for I/O-bound fetching, **multiprocessing** for CPU-bound HTML parsing, and `concurrent.futures.ProcessPoolExecutor` to bridge the two. Compare performance against a purely synchronous version.

---

## Chapter 7 — FastAPI

FastAPI is the modern standard for building Python APIs. These resources cover the framework end-to-end: Pydantic, dependency injection, middleware, background tasks, WebSockets, and testing.

### Textual resources

**1. FastAPI Official Tutorial (User Guide)**
- **URL:** https://fastapi.tiangolo.com/tutorial/
- The definitive source, written by FastAPI's creator. Covers **every key topic**: path/query parameters, Pydantic models, dependency injection, middleware, CORS, background tasks, WebSockets, security (OAuth2/JWT), SQL databases, testing, and larger application structure with APIRouter. All code blocks are tested and runnable.

**2. Real Python — "A Close Look at a FastAPI Example Application"**
- **URL:** https://realpython.com/fastapi-python-web-apis/
- Builds a complete **Randomizer API** from scratch. Covers setup, path/query parameters with type hints, Pydantic `BaseModel`, response validation, async endpoints, CORS middleware, and Swagger documentation. Includes **interactive quiz** and downloadable project code.

**3. TestDriven.io — "Developing and Testing an Asynchronous API with FastAPI and Pytest"**
- **URL:** https://testdriven.io/blog/fastapi-crud/
- Builds a **full async CRUD API** with FastAPI, PostgreSQL, pytest, and Docker using Test-Driven Development. Covers SQLAlchemy models, Pydantic schemas, async handlers, containerization, and parameterized tests. **End-of-tutorial challenges** include implementing background tasks, migrations, and auth.

### Video resource

**4. 🎥 Amigoscode — "FastAPI Tutorial – Building RESTful APIs with Python"**
- **URL:** https://www.youtube.com/watch?v=GN6ICac3OXY
- ~1 hour tutorial covering FastAPI from scratch: Uvicorn setup, HTTP methods, Pydantic models, in-memory database, Swagger UI, status codes, and exception handling. **Includes a dedicated exercise section** (timestamp 55:07) where viewers implement a PUT endpoint before seeing the solution.

### Suggested exercises
- **Small:** Build a REST API for a todo list with full CRUD, Pydantic validation, dependency injection for a database session, and automated tests using `httpx.AsyncClient`.
- **Big:** Create a real-time chat application using FastAPI WebSockets, with message persistence, user authentication via JWT, background task processing, and a full test suite.

---

## Capstone project — production-ready task queue microservice

The capstone ties all 7 chapters together into a single, substantial project: **a FastAPI-based task queue microservice** where users submit long-running tasks, monitor status via WebSockets, and retrieve results asynchronously.

### What you build

A RESTful + WebSocket API that accepts task submissions (data processing, report generation, etc.), processes them asynchronously via background workers, and provides real-time status updates. The project naturally requires every skill from the curriculum.

### How each chapter maps to the capstone

| Chapter | Application in the capstone |
|---|---|
| **1. Modules** | Multi-package structure: `app/api/`, `app/models/`, `app/services/`, `app/workers/`, `tests/`. Proper `__init__.py` files, APIRouter-based route organization, relative imports within the package. |
| **2. Logging** | Structured JSON logging via `python-json-logger`. Per-module loggers (`app.api`, `app.workers`). Request/response logging middleware with **correlation IDs** for tracing. `RotatingFileHandler` for production. |
| **3. Typing** | Full `mypy --strict` compliance. Pydantic `BaseModel` for schemas (`TaskCreate`, `TaskResponse`, `TaskStatus`). `Generic[T]` for typed task results. `Annotated` for dependency injection typing. |
| **4. UV** | `uv init` for project scaffolding, `pyproject.toml` + `uv.lock` for dependencies, `Dockerfile` using `uv sync`, documented setup with `uv run uvicorn app.main:app`. |
| **5. Advanced features** | Custom `@retry` and `@authorize` decorators. Generator-based `Depends` with `yield` for DB session management. Context managers for distributed locks. `__slots__` on high-frequency data objects. |
| **6. Concurrency** | All handlers `async def`. `asyncio.Queue` for task queuing. `asyncio.create_task()` for workers. `ProcessPoolExecutor` for CPU-bound tasks. `async for` streaming of task logs. |
| **7. FastAPI** | The framework itself. Pydantic validation, dependency injection, custom middleware, `BackgroundTasks`, WebSocket endpoint for status streaming, full `pytest` + `httpx.AsyncClient` test suite. |

### Suggested project structure

```
task-queue-service/
├── pyproject.toml              # uv dependency management
├── uv.lock
├── Dockerfile
├── app/
│   ├── __init__.py
│   ├── main.py                 # FastAPI app, middleware, lifespan events
│   ├── core/
│   │   ├── config.py           # Pydantic Settings for env vars
│   │   ├── logging.py          # Structured logging setup
│   │   └── security.py         # JWT auth decorators
│   ├── api/
│   │   ├── v1/
│   │   │   ├── tasks.py        # CRUD endpoints for tasks
│   │   │   └── ws.py           # WebSocket for real-time status
│   │   └── deps.py             # Dependencies (DB yield, auth)
│   ├── models/
│   │   ├── task.py             # SQLAlchemy/SQLModel ORM models
│   │   └── schemas.py          # Pydantic request/response schemas
│   ├── services/
│   │   ├── task_service.py     # Business logic (async)
│   │   └── worker.py           # Background task processor
│   └── utils/
│       ├── decorators.py       # @retry, @cache, @authorize
│       └── context.py          # Context managers for resource locks
└── tests/
    ├── conftest.py             # Fixtures, async test client
    ├── test_tasks.py           # API integration tests
    └── test_worker.py          # Worker unit tests
```

### Key API endpoints to implement

- `POST /api/v1/tasks` — Submit a new task (returns task ID immediately)
- `GET /api/v1/tasks` — List tasks with filtering and pagination
- `GET /api/v1/tasks/{id}` — Retrieve task status and result
- `DELETE /api/v1/tasks/{id}` — Cancel a pending task
- `WS /api/v1/tasks/{id}/stream` — WebSocket for real-time status updates

### Reference templates on GitHub

These open-source repos demonstrate similar patterns and can serve as architectural references:

- **FastAPI Full-Stack Template** (Official): https://github.com/fastapi/full-stack-fastapi-template — SQLModel, Pydantic, PostgreSQL, Docker, CI/CD. MIT licensed.
- **Building a Scalable Python Project with FastAPI and uv** (Tutorial): https://dev.to/code_2/building-a-scalable-python-project-with-fastapi-and-uv-54aa — Demonstrates uv + FastAPI + structured logging + proper folder layout.

---

## Quick-reference resource matrix

| Chapter | Textual 1 | Textual 2 | Textual 3 | Video |
|---|---|---|---|---|
| 1. Modules | [Real Python: Modules & Packages](https://realpython.com/python-modules-packages/) | [Real Python: Advanced Import](https://realpython.com/python-import/) | [Python Docs: Modules](https://docs.python.org/3/tutorial/modules.html) | [Corey Schafer: Import Modules](https://www.youtube.com/playlist?list=PL-osiE80TeTt2d9bfVyTiXJA-UTHn6WwU) |
| 2. Logging | [Real Python: Logging](https://realpython.com/python-logging/) | [Python Docs: Logging HOWTO](https://docs.python.org/3/howto/logging.html) | [ML+: Logging Guide](https://machinelearningplus.com/python/python-logging-guide/) | [Corey Schafer: Logging Advanced](https://www.youtube.com/watch?v=jxmzY9soFXg) |
| 3. Typing | [Real Python: Type Checking](https://realpython.com/python-type-checking/) | [mypy Cheat Sheet](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html) | [Python Type Challenges](https://github.com/laike9m/Python-Type-Challenges) | [Tech With Tim: Typing](https://www.youtube.com/watch?v=QORvB-_mbZ0) |
| 4. UV & Venvs | [uv Official Docs](https://docs.astral.sh/uv/) | [freeCodeCamp: uv Guide](https://www.freecodecamp.org/news/how-to-manage-python-packages-with-uv/) | [SaaS Pegasus: uv Deep Dive](https://www.saaspegasus.com/guides/uv-deep-dive/) | [Corey Schafer: UV](https://www.youtube.com/watch?v=AMdG7IjgSPM) |
| 5. Advanced | [Real Python: Decorators](https://realpython.com/primer-on-python-decorators/) | [Real Python: Metaclasses](https://realpython.com/python-metaclasses/) | [pymbook: Iterators & Generators](https://pymbook.readthedocs.io/en/latest/igd.html) | [Tech With Tim: 10 Advanced Features](https://www.youtube.com/watch?v=mclftDq-jOA) |
| 6. Concurrency | [Real Python: Async IO](https://realpython.com/async-io-python/) | [Python Docs: asyncio](https://docs.python.org/3/library/asyncio.html) | [SuperFastPython: Asyncio Guide](https://superfastpython.com/python-asyncio/) | [Corey Schafer: AsyncIO](https://www.youtube.com/watch?v=Qb9s3UiMSTA) |
| 7. FastAPI | [FastAPI Official Tutorial](https://fastapi.tiangolo.com/tutorial/) | [Real Python: FastAPI](https://realpython.com/fastapi-python-web-apis/) | [TestDriven.io: FastAPI CRUD](https://testdriven.io/blog/fastapi-crud/) | [Amigoscode: FastAPI](https://www.youtube.com/watch?v=GN6ICac3OXY) |

## Conclusion

This curriculum is deliberately sequenced. **Chapters 1–3** (modules, logging, typing) establish code quality fundamentals. **Chapter 4** (uv) provides the tooling infrastructure. **Chapters 5–6** (advanced features, concurrency) build Python mastery. **Chapter 7** (FastAPI) applies everything in a modern web framework context. The capstone then forces integration of all skills into a single production-grade codebase.

The strongest exercise-rich resources are the **Python Type Challenges repo** (Chapter 3), the **Machine Learning Plus logging guide** (Chapter 2), the **TestDriven.io FastAPI tutorial** (Chapter 7), and the **SuperFastPython asyncio guide** (Chapter 6). Prioritize these if learners want the most hands-on practice. For every chapter, the pattern of "read the Real Python article → reference the official docs → practice with the exercise-focused resource → watch the video for reinforcement" creates an effective learning loop.