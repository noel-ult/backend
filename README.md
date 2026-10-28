# Employee management backend

An Express/Mongoose employee API that also serves a prebuilt Angular frontend. The application lives in `Casestudy2/`; the Angular source project is not included.

## Setup

Start a development MongoDB instance. Create an untracked `Casestudy2/.env` containing:

```dotenv
MONGO_URI=mongodb://127.0.0.1:27017/employee_demo
PORT=5000
NODE_ENV=development
```

Then run:

```sh
cd Casestudy2
npm ci
npm start
```

Visit http://localhost:5000 and http://localhost:5000/api/health. `npm run dev` uses nodemon.

## API and model

The `/api/employees` collection supports GET and POST; `/api/employees/:id` supports GET, PUT, and DELETE. Compatibility routes under `/api/employeelist` return raw records/arrays rather than the primary API's response envelope. `PUT /api/employeelist` accepts `_id` or `id` in the body; the ID-suffixed update form also exists.

`models/Employee.js` requires name, position, location, and a nonnegative salary. `dateOfJoining` defaults to now; Mongoose adds creation/update timestamps. Invalid IDs and validation failures are handled by individual routes. Read the route-specific handler before assuming identical error responses across the two route families.

## Frontend, verification, and operation

`dist/Frontend/` contains built Angular assets served by `app.js`; non-API URLs fall back to its index page. `/debug` serves the update-debugging page. `test-update.js` is an API exercise, so use a disposable database and inspect its mutations before running it. There is no declared npm test script.

Check health, create a test employee, retrieve it, update it, and delete it. API access has no authentication middleware, and debug logging includes request bodies. Deploy only with an appropriate access boundary until authentication and logging policy are implemented. The prebuilt frontend's API assumptions must be checked when changing the host or port.

## More documentation

- [Source, command, and configuration reference](docs/REFERENCE.md)
- [Contributing](CONTRIBUTING.md)

<!-- developer-handbook-20261028 -->
[Source reference](docs/REFERENCE.md) · [Verification and operations](docs/OPERATIONS.md)
<!-- /developer-handbook-20261028 -->
