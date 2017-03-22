# eslint-config-edited
A shareable ESLint config for the EDITED styleguide

### Usage
- `npm install eslint-config-edited --save-dev`
- Don't forget to save the `eslint-config-edited` peerDependencies to your devDependencies!
- Change your `.eslintrc` to the following
**.eslintrc**

```json
{
  "extends": "edited",
}
```

## Import resolver settings
If you're using webpack you should

- `npm install eslint-import-resolver-webpack --save-dev`
- Add the following to your `.eslintrc`
```
settings: {
    "import/resolver": {
        webpack: {
            config: "<path-to-project-webpack-config>"
        }
    }
}
```

If you're not using webpack, but you do have .jsx files that you'd like to resolve then you can add the following settings to your `.eslintrc` file.
```
settings: {
    "import/resolver": {
        "node": {
            "extensions": [ ".js", ".jsx" ],
        }
    }
}
```

