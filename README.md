# 📰 RSSFeedReader

![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![Blazor](https://img.shields.io/badge/Blazor-512BD4?style=flat-square&logo=blazor&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![GitHub Copilot](https://img.shields.io/badge/GitHub_Copilot-000000?style=flat-square&logo=githubcopilot&logoColor=white)
![Spec Kit](https://img.shields.io/badge/Spec_Kit-SDD-blue?style=flat-square&logo=github&logoColor=white)

This is an **MVP** and a hands-on learning project. I built it to practice
**Spec-Driven Development (SDD)** with
[GitHub Spec Kit](https://github.com/github/spec-kit) and GitHub Copilot in VS Code.

## ✨ What it does

- Add a feed subscription by URL
- See your list of subscriptions
- Your data is saved between restarts

## 🧭 How it was built

Every step starts with a written document, and the code comes last:

`constitution` → `spec` → `plan` → `tasks` → `implement`

| Step | What it answers | Where to find it |
|---|---|---|
| Constitution | Which rules must the project follow? | `.specify/memory/` |
| Spec | **What** are we building? | `specs/` |
| Plan | **How** will we build it? | `specs/` |
| Tasks | What are the small steps? | `specs/` |

## 🛠 Tech stack

- **.NET** + **ASP.NET Core**: backend API
- **Blazor**: user interface
- **SQLite**: local storage
- **GitHub Spec Kit** + **GitHub Copilot**: AI-assisted workflow