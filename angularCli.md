The Angular CLI is the official tool to create, build, and serve Angular apps.
The CLI (Command Line Interface) creates projects, runs a dev server, and provides helpful commands.

# Install the Angular CLI globally:

npm install -g @angular/cli

Installing it globally makes the ng command available everywhere.
You can also use npx without a global install.
If you hit permission errors, use npx or run your terminal with elevated rights.

# Verify Angular CLI

Verify the installation to ensure ng is on your PATH and versions are compatible.

ng version

PATH is the list of folders your system searches for commands like ng.

# Recommended choices when prompted:

Stylesheet format: CSS (you can change later)
Server-side rendering (SSR): No for now (you can add later with ng add @angular/ssr)
Zoneless application: No for now (you can change later with ng add @angular/zoneless)
Other prompts: keep the defaults

# If you don't want to install the CLI globally, you can use npx:

npx @angular/cli@latest new my-angular-app

# Run the Angular Application

cd my-angular-app
ng serve
cd enters your new project folder.

ng serve starts a local dev server and watches for changes.

The first build can take a minute.

✔ Compiled successfully. ✔ Browser application bundle generation complete.
You can add the --open flag to automatically open the app in your default browser:

ng serve --open
By default the dev server runs on http://localhost:4200.
