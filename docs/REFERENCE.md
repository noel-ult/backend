# backend source reference


Source reviewed: [`d07363beb2d7`](https://github.com/noel-ult/backend/commit/d07363beb2d7993fd23207d58feabb273b7fbe36).

This reference records the checked-in source, scripts, configuration names, and route declarations. It is a navigation aid; service availability and successful test execution require separate verification.

## Package commands

Run each command in the directory containing its package manifest. A declared script is not necessarily a passing check; guides call out placeholders and known mismatches.

### Casestudy2/package.json

| Script | Shell command |
| --- | --- |
| `start` | `node app.js` |
| `dev` | `nodemon app.js` |

Manifest: [Casestudy2/package.json](../Casestudy2/package.json).

## Configuration names

Names below are declared by source or example files. Example-only entries may be stale; consult the linked reader and project guide before relying on them. Secret values are intentionally omitted.

| Name | Declared/read in |
| --- | --- |
| `MONGO_URI` | [Casestudy2/app.js](../Casestudy2/app.js) |
| `NODE_ENV` | [Casestudy2/app.js](../Casestudy2/app.js) |
| `PORT` | [Casestudy2/app.js](../Casestudy2/app.js) |

## HTTP route declarations

Paths are **as declared in each source file**. Router/blueprint mount prefixes from the entry point must be prepended; the project guide describes the active entry point and common prefixes. Alternate entry points (such as SQLite) are listed separately by file. Authentication, request bodies, and response schemas live in the linked handlers/models.

| Source | Method | Declared path | Handler |
| --- | --- | --- | --- |
| [Casestudy2/app.js](../Casestudy2/app.js) | GET | `/api/employees` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | GET | `/api/employees/:id` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | POST | `/api/employees` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | PUT | `/api/employees/:id` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | DELETE | `/api/employees/:id` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | GET | `/api/health` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | GET | `/api/employeelist` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | GET | `/api/employeelist/:id` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | POST | `/api/employeelist` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | PUT | `/api/employeelist` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | PUT | `/api/employeelist/:id` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | DELETE | `/api/employeelist/:id` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | GET | `/debug` | `` |
| [Casestudy2/app.js](../Casestudy2/app.js) | GET | `/*` | `` |

## Source and configuration map

Generated lockfiles, binary assets, compiled output, vendored dependencies, and cached bytecode are omitted. Test files remain listed so coverage can be located.

- [Casestudy2/app.js](../Casestudy2/app.js)
- [Casestudy2/debug-update.html](../Casestudy2/debug-update.html)
- [Casestudy2/models/Employee.js](../Casestudy2/models/Employee.js)
- [Casestudy2/package.json](../Casestudy2/package.json)
- [Casestudy2/test-update.js](../Casestudy2/test-update.js)
