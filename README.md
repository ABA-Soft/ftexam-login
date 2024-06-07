<p align="center">
    <i>🚀 <a href="https://keycloakify.dev">Keycloakify</a> v10 starter 🚀</i>
    <br/>
    <br/>
</p>

This starter is based on Vite. There is also [a Webpack based starter](https://github.com/keycloakify/keycloakify-starter-cra).

# Quick start

```bash
git clone https://github.com/keycloakify/keycloakify-starter
cd keycloakify-starter
yarn install
# Generate the dist_keycloak/.jar file that you can import in Keycloak
yarn build-keycloak-theme 
```

# Storybook

```bash
npx keycloakify add-story # Select the pages you want to add stories for
yarn storybook # Start Storybook
```

# Test in a real Keycloak environment

Test your theme in a local Keycloak docker container.

```bash
npx keycloakify start-keycloak
```

# Advanced customization

The starter only enables you to implement CSS level customization. To take full ownership
of some pages use the command:

```bash
npx keycloakify eject-page
```

# GitHub Actions

The starter comes with a generic GitHub Actions workflow that builds the theme and publishes
the jars [as GitHub releases artifacts](https://github.com/keycloakify/keycloakify-starter/releases/tag/v7.1.0).  
To release a new version **just update the `package.json` version and push**.  

To enable the workflow go to your fork of this repository on GitHub then navigate to:
`Settings` > `Actions` > `Workflow permissions`, select `Read and write permissions`.  

# Removing the account theme

If you don't need to customize [the account theme pages](https://storybook.keycloakify.dev/?path=/story/account-account--default).  
You can remove the `src/account` directory.  
This will significantly reduce the the size of the jar and the build time.  
Don't forget to update `src/main.tsx` and `src/vite-env.d.ts`.

# Email theme

Keycloakify lets you bundle an email theme however customization can't be made with React yet.  
To initialize the email theme run:  

```bash
npx keycloakify initialize-email-theme
```
