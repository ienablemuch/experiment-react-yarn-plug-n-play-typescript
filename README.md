Create React App, TypeScript, Yarn Plug'n'Play, VS Code

```
$ npx create-react-app your-project-name-here --use-pnp
```

```
$ yarn add typescript
```

To enable running NPM Scripts directly in VS Code, this should be in settings.json (in .vscode directory):

```
{
    "npm.packageManager": "yarn"
}
```

If .vscode directory and settings.json file does not exist, create a .vscode directory and create settings.json file in it.

Though running the start script from the VS Code's NPM Scripts panel is possible, VS Code will still complain that it cannot find React.

To fix that, add pnpify:

````
$ yarn add --dev @berry/pnpify
```

Then run this:
```
$ yarn pnpify --sdk
```

Then change the TypeScript version by pressing Command+Shift+P (from menu: View > Command Palette). Note, the active file must be a .tsx file before pressing Command+Shift+P. Select **TypesScript: Select TypeScript version**, select **Use Workspace Version**


Solution found here: https://stackoverflow.com/questions/54954337/is-it-possible-to-use-yarn-pnp-with-typescript-vscode
````
