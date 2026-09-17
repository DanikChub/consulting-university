# Consulting University

Corporate learning management system developed for ООО «Консалтинг-Волга».

The platform covers the full learning lifecycle: creating programs, publishing materials, enrolling users, completing tests and practical assignments, tracking progress and issuing certificates. The first production version is already used by approximately **40 users**.

## Main features

- personal accounts for learners and administrators;
- three access levels: administrator, learner and read-only administrator;
- hierarchical course builder: programs, topics and learning units;
- autosaving editor for complex learning programs;
- tests, attempts, answers and grade book;
- practical assignments and review workflow;
- individual learning progress and statistics;
- certificates and diplomas;
- email notifications;
- real-time chat;
- administrative user and content management.

## Content pipeline

The platform works with DOCX, PDF, presentations, images, audio and video.

DOCX files can be converted to HTML for browser viewing. File uploads, Vimeo integration and independent processing of different content types are handled as separate operations so that long-running uploads do not corrupt the rest of the editor state.

## Architecture

```text
React + TypeScript
        │ REST / Socket.IO
Node.js + Express
        │
PostgreSQL + Sequelize
        │
Files / Vimeo / Email
```

The frontend and backend are stored in one repository. Backend modules cover authorization, programs, enrollments, tests, progress, certificates, statistics, chat and file access.

## Tech stack

**Frontend:** React, TypeScript, MobX, Axios, Tailwind CSS  
**Backend:** Node.js, Express, JavaScript, REST API, Socket.IO  
**Data:** PostgreSQL, Sequelize, migrations  
**Integrations:** Vimeo API, Nodemailer, Mammoth DOCX-to-HTML  
**Infrastructure:** Docker, Nginx, Linux

## Engineering highlights

- complete product development from initial idea to production;
- role-based access control and protected file access;
- relational model for programs, enrollment, progress and testing;
- autosave with debounce for content editing;
- separation of text, files, images and video into independent save operations;
- support for large ZIP-based program imports;
- database migrations for evolving production data.

## Current status

The LMS is deployed and used in production. The repository represents an actively developed commercial product.

## Author

Designed and implemented by [Daniil Chabanov](https://github.com/DanikChub): product flows, UI, frontend, backend, database model, server setup and deployment.
