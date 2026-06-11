

# Angular13 Project

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.3.11. It includes a configured mock backend using `json-server` to simulate REST API calls during development.

##  Getting Started

To get the project up and running locally, follow these steps:

### 1. Install Dependencies

Ensure you have Node.js and npm installed. Clone the repository, navigate to the project directory, and run:

```bash
npm install

```

*(This will install both the Angular frontend dependencies and the `json-server` development tools.)*

### 2. Start the Development Environment

This project is configured to run both the Angular development server and the JSON mock database simultaneously.

Run the following command:

```bash
npm start

```

* **Frontend:** The Angular application will be available at `http://localhost:4200/`. The app will automatically reload if you change any of the source files.
* **Backend:** The mock API will be running on `http://localhost:3000/`.

---

## Mock Backend Configuration (`json-server`)

This project uses `json-server` to mock backend API responses.

### Database (`db.json`)

The mock database is located in the root directory in the `db.json` file. Any changes made to the data through the UI (POST, PUT, DELETE) will automatically be saved to this file.

### API Proxy (`proxy.conf.json`)

To avoid CORS issues, an Angular proxy is configured in `src/proxy.conf.json`.
All frontend requests made to `/api/*` are automatically redirected to the JSON server at `http://localhost:3000/*`.

*Example: An Angular HTTP request to `/api/posts` resolves to `http://localhost:3000/posts`.*

---

## Standard Angular CLI Commands

### Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

### Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.