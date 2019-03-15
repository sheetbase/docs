# Getting started

Using Sheetbase to build a website/app.

## Starting

You can use Sheetbase platform to build a REST API only (see below) or a fully functional app.

### The CLI

Install the [Sheetbase CLI](https://github.com/sheetbase/cli), it is the main tool for developing project. Make sure you have **Node** and **npm** installed, see Evironment setup for more.

```sh
npm install -g @sheetbase/cli@latest
```

## Setup Google account

Enable Apps Script API, go to <https://script.google.com/home/usersettings>, then enable the API.

Add manage Google Apps Script from your Google Drive:

`My Drive (click dropdown) > More > Connect more apps > (search for Google Apps Script) > Connect`

## Start an app

Run this command to create a new app, replace `project_name` with your app name (remember to double quote if the name contains space).

```sh
sheetbase start <project_name>
```

Example: `sheetbase start myapp` or `sheetbase start "My Awesome Website"`

Or manually, clone a theme from the themes list: <https://sheetbase.net/themes>

## Install dependencies

The CLI skip installing npm dependencies (`npm install`), you need to install them before start developing.

Install backend dependencies:

```sh
cd backend && npm install
```

Install frontend dependencies:

```sh
cd frontend && npm install
```

If you wish the CLI to install dependencies for you, add `-i` (--install) flag with `start` command: `sheetbase start myapp -i`.

## Workflow

The [Sheetbase CLI](https://github.com/sheetbase/cli) provides convenient commands for easily build and deploy a Sheetbase project.

### The backend (server)

For an app, backend code lives in **backend/** folder.

- Test: $ `sheetbase backend test`
- Build: $ `sheetbase backend build`
- Push code: $ `sheetbase backend push` (update code in the Apps Script server, without redeploy the webapp)
- Deploy: $ `sheetbase backend deploy` (push code, save new version and redeploy the webapp)

### The frontend (client)

For an app, frontend code lives in **frontend/** folder.

- Test: $ `sheetbase frontend test` (npm run test)
- E2E: $ `sheetbase frontend e2e` (npm run e2e)
- Build: $ `sheetbase frontend build` (npm run build)
- Prerender: $ `sheetbase frontend prerender` (prerender content, save sitemap.xml & robots.txt)
- Deploy: $ `sheetbase frontend deploy` (redeploy the a static server)

## Build a REST API server

If you only wish to build a REST API server, then clone the blank backend app from: <https://github.com/sheetbase/blank-server-app>

It just like buidling a full app, but without the frontend part.