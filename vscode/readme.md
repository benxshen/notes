
#Installations

##Vscode and "Settings Sync"
1. Get latest version from https://code.visualstudio.com/

2. Install the plugin "Settings Sync" from https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync
![](images/install_ext.png)

3. Follow the steps of "Settings Sync" to create your own github account token and Gist.
    1. seleting Command __"Sync : Download Settings"__  and paste your own token.
    2. then paste my GIST `92a1a1154369f7b01e1fc1b7d1f6e9a1` if you would like to use my settings. (Keep empty and enter, it will create a new GIST automatically.)
    3. (if you download my GIST settings) Once all settings downloaded, restart vscode.
    4. seleting Command __"Sync : Reset Extension Settings"__ to clean up github token and Gist. And then repeat 3.1 and 3.2 again (in 3.2, leave the GIST blank to create your new gist.)
    5. selecting Command __"Sync : Update / Upload Settings"__ to upload all the latest settings to your gist.

![](images/settings_sync.png)

##Eable eslint

1. npm intall eslint -g

2. install vscode plugin with command `ext install vscode-eslint` https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint (if you downloaded my
vscode settings by above step, you have it already)

3. create a .eslintrc configuration file if your project don't have this. You can do this by either running
eslint --init in a terminal or by using the VS Code
command "Create '.eslintrc.json' file". (The below is my eslint configs)
![](images/eslintrc_and_editorconfig.png)

```json
{
    "extends": "eslint:recommended",
    "installedESLint": true,
    "env": {
        "browser": true
    },
    "plugins": [
        "json"
    ],
    "globals": {
        "angular": true,
        "$": true,
        "_": true,
        "SockJS": true,
        "Stomp": true
    },
    "rules": {
        "semi": ["error", "always"],
        "quotes": ["warn", "single"],
        "no-console": "warn",
        "no-mixed-spaces-and-tabs": "warn",
        "no-unused-vars": "warn",
        "no-invalid-this": "warn",
        "eqeqeq": "error"
    }

}
```

##Enable EditorConfig

1. Install the vscode plugin with command `ext install EditorConfig` https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig (if you downloaded my
vscode settings by above step, you have it already)

2. create a file with name '.editorconfig' under your project. Below is my settings:

```properties
# EditorConfig is awesome: http://EditorConfig.org

# top-most EditorConfig file
root = true

# Unix-style newlines with a newline ending every file
[*]
#end_of_line = lf
#insert_final_newline = true
#charset = utf-8
trim_trailing_whitespace=true
indent_style = space
indent_size = 4

# 2 space indentation
[*.{css,less,scss}]
indent_style = space
indent_size = 2

```
