# Your first "native" app with Electron

Electron allows you to write web apps, but also gives you access to native APIs that would be impossible or impractical to use in a browser.

The scope of this project was just to determine how hard it would be to write a simple shell that loads a web app. It wasn't that difficult! Electron has been around for a few years now, and major text editors such as Atom or VS Code use it.

How to get started:

1. Clone a boilerplate repo [like this one](https://github.com/szwacz/electron-boilerplate), then `yarn install`
1. Use a `<webview>` element to get an iframe that isn't subject to `X-Frame-Options` or `Content-Security-Policy` restrictions
1. Set your remote to a Github repo that is publicly accessible. Generate a personal access token from Github, set it in an environment variable, and run `npm release` to ship a build to the Releases tab in your project.
1. Implement some auto-update logic that will install the saved update at the next app startup (at the time of writing this is still in progress)

Congrats! You have shipped your first app.

Some caveats I found:

- You need to sign your app, or you'll get a scary "unsigned app" warning on both OS X and Windows
- The installer is around 30 MB, since you are shipping a build of Chromium with your app
