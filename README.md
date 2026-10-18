<!--
  Konnekt Lite — project README
  Visual direction: colorful, modern, developer-first.
-->

<div align="center">

# 🌐 Konnekt Lite

### One connected platform for identity, attendance, and everyday operations.

<p>
  <strong>🎓 Schools</strong> &nbsp; • &nbsp;
  <strong>🏢 Businesses</strong> &nbsp; • &nbsp;
  <strong>⚡ Developer-friendly</strong>
</p>

<p>
  <img src="https://img.shields.io/badge/STATUS-Early%20Development-8B5CF6?style=for-the-badge" alt="Status: Early Development" />
  <img src="https://img.shields.io/badge/DATABASE-Neon%20Postgres-00E599?style=for-the-badge&logo=postgresql&logoColor=111827" alt="Database: Neon Postgres" />
  <img src="https://img.shields.io/badge/BUILT%20FOR-Modularity-06B6D4?style=for-the-badge" alt="Built for modularity" />
</p>

<p>
  <em>Simple to start. Flexible enough to grow.</em>
</p>

</div>

---

## ✨ What is Konnekt Lite?

Konnekt Lite is a fresh, modular platform designed to help schools and businesses manage people, digital identity, and attendance from one connected workspace.

The goal is to make everyday workflows easier to manage while building a foundation that can grow into broader operational tools over time.

> 🚧 **Work in progress:** Konnekt Lite is in its early planning and build stage. The capabilities described here are the intended direction, not a claim that they are already implemented.

## 🧩 The building blocks

| Module | What it is intended to do |
| --- | --- |
| 🏷️ **Workspaces** | Give each school or business its own organised space and team access. |
| 🪪 **Digital IDs** | Create digital identity profiles with carefully controlled information visibility. |
| 📍 **Attendance** | Record and review attendance with workflows suited to each organisation. |
| 📊 **Reports** | Help authorised administrators understand attendance and activity. |
| 🔌 **Integrations** | Leave room for optional messaging and external-service adapters as the product evolves. |

### 🎓 For schools
A foundation for student and staff identity, class or session attendance, and records such as present, late, absent, or excused.

### 🏢 For businesses
A foundation for employee identity and shift-based attendance, including clock-in/out, lateness, and—where applicable—overtime.

## 🛠️ Technology direction

The implementation will be chosen to support maintainability, clear boundaries, and practical iteration.

- **Database:** Neon — managed PostgreSQL
- **Application direction:** TypeScript-first, modular codebase
- **Data access:** A typed ORM such as Drizzle is under consideration
- **Architecture:** One codebase for the initial school and business experiences, with distinct workflows where needed

These are current direction choices, not a promise that every framework or library has been finalised.

## 🧭 Product principles

- **🔐 Privacy by design** — expose only the information each user is allowed to see.
- **🧱 Modular, not overengineered** — build clear boundaries without adding complexity before it is needed.
- **🏫 One platform, different workflows** — share foundations while respecting the real differences between schools and businesses.
- **🔌 Integrations stay optional** — messaging and external services should not be required for core functionality.
- **🌱 Built to evolve** — make room for future use cases without letting hypothetical features dictate today's build.

## 🚀 Project status

Konnekt Lite is being built from a clean foundation. The legacy Konnekt application may serve as a reference when useful, but it does not define the new architecture.

Planned early milestones:

- [ ] Define the core user journeys and permissions.
- [ ] Establish the application structure and development conventions.
- [ ] Design the initial PostgreSQL data model.
- [ ] Build the workspace, identity, and attendance foundations.
- [ ] Add reporting and validate the school and business workflows.

## 🤝 Contributing

Contribution guidelines will be added as the project structure and development workflow are established. For now, project decisions should prioritise clear user needs, secure handling of data, and a maintainable foundation.

## 📄 License

No license has been selected yet. Until one is added, all rights are reserved by default.

---

<div align="center">

**Konnekt Lite** &nbsp; ⚡ &nbsp; *Connect people. Simplify presence. Make operations clearer.*

<sub>Built with intention by <a href="https://github.com/nekt-konnekt">Nekt-konnekt</a>.</sub>

</div>
