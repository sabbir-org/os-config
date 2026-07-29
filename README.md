### Driver Install
watch the following tutorials before installing gpu drivers

[video 1 : optimize driver guide](https://www.youtube.com/watch?v=B4baN3b8oOE&t=0s)\
[video 2 : proper install guide](https://www.youtube.com/watch?v=98DAgw1KcmI)

### Drivers links as follows
- [nvidia](https://www.nvidia.com/en-us/geforce/drivers/)
- [amd](https://www.amd.com/en/support)
- for **realtek** audio visit motherboard manufacturer website
  - [asus](https://www.asus.com/support/download-center/)
  - [asrock](https://www.asrock.com/support/index.asp?cat=Drivers)
  - msi - individual motherboard
  - gigabyte - individual motherboard

### Other Apps

- [afterburner](https://www.msi.com/Landing/afterburner/graphics-cards)
- [obs](https://cdn-fastly.obsproject.com/downloads/OBS-Studio-29.0.2-Full-Installer-x64.exe)
- [steam](https://cdn.akamai.steamstatic.com/client/installer/SteamSetup.exe)
- [epic](https://launcher-public-service-prod06.ol.epicgames.com/launcher/api/installer/download/EpicGamesLauncherInstaller.msi)
- [.net sdk lts](https://dotnet.microsoft.com/en-us/download/visual-studio-sdks)
- [python](https://www.python.org/)
- [c++](https://code.visualstudio.com/docs/cpp/config-mingw)
- [java](https://aws.amazon.com/corretto/)
- [avro](https://www.omicronlab.com/avro-keyboard-download.html)
- [power toys](https://learn.microsoft.com/en-us/windows/powertoys/)
- [razer software](https://www.razer.com/synapse-4)
- [postman](https://dl.pstmn.io/download/latest/win64)
- [warp](https://one.one.one.one/)
- [twinkle tray](https://twinkletray.com/)
- [flaw launcher](https://www.flowlauncher.com/)

### Browser Extension
- darkreader
- tempmail
- ublock origin
- fdm
- youtube enhance

### Install NodeJs

[node download](https://nodejs.org/en/download)

## INSTALL MONGODB(NoSql)

[mongodb download link](https://www.mongodb.com/try/download/community)

```bash
click install, just agree and choose complete installation
```

- it will automatically download and install monogo compass(data base ui) which will take few extra minutes.

[mongodb shell download](https://downloads.mongodb.com/compass/mongodb-mongosh_1.6.1_amd64.deb?_ga=2.66967086.1814885739.1671987424-986248264.1671987424)

- unzip the downloaded file and rename it something like `mongosh`
- move the `mongosh` folder to `C:\Program Files`
- start button and type **environment variables**. open it.
- go to advance tab. click **enviroment variables** at the bottom.
- in **system variables** select **path** and click **edit**
- create a new variable with the following url
  > `C:\Program Files\mongosh\bin`
- click ok and exit.
- start a terminal or cmd. type **mongosh** and press enter
- you should see mongosh log id, connection and other information

---
### Git configuration

**INSTALL GIT BASH**

download gitbash from [official website](https://github.com/git-for-windows/git/releases/download/v2.38.1.windows.1/Git-2.38.1-64-bit.exe)

- install git bash keeping all the settings to default
- click next ... next ...

**INSTALL WINDOWS TERMINAL**

1. download windows terminal from <a href="https://www.microsoft.com/store/apps/9n0dx20hk701" target="_blank">MS store</a> on windows 10 (windows 11 have this terminal by default)
2. to setup git bash in windows terminal follow the steps below :
   - open windows terminal and go to settings
   - click add new profile
   - click new empty profile
   - change the name to **gitbash** or **bash** upon ur like
   - replace the command line url with gitbash url
     > `C:\Program Files\Git\bin\bash.exe`
   - choose custom icon of your choice or use default gitbsh icon from the location below
     > `C:\Program Files\Git\mingw64\share\git\git-for-windows.ico`
   - go startup tab and choose gitbash as default profile

**Connect github with your pc using SSH key**
- open terminal
- paste the following command
```
ssh-keygen -t ed25519-sk -C YOUR_EMAIL
```
> if your system shows error on above command, use below command instead
```
ssh-keygen -t rsa -b 4096 -C YOUR_EMAIL
```

- go to `C:\Users\[username]\.ssh`
- open editor inside current directory
- open `id_ed25519.pub` and copy the full ssh key
- go to this [link](https://github.com/settings/keys)
- click on `new ssh key`.
- give a title and paste the copied key at key field.\

now github should recognize your device.

**User login**\
open terminal and follow the command below
```
git config --global user.email YOUR_EMAIL
```
```
git config --global user.name YOUR_USERNAME
```

try to clone any of your private repository. you will get a warning and given option like
```
yes/no/[fingerprint]
```
- type `yes` and hit enter
- a file named `known_host` is being created at .ssh (`C:\Users\[username]\.ssh`) folder.\
_Done!_

**Git Basic Commands**

<details>
<summary>click to see basic commands</summary>


### Simple commands
git clone url\
git remote set-url origin url\
git remote -v\
git status\
git add .\
git commit -m 'cloned commit'\
git push -u origin main

### Clone repo with commits
git clone --bare <original-url>\
git push --mirror <new-url>\
git remote -v\
get remote set-url origin <new-url>

### Clone remote branch
git clone <your-repo-url>\
cd my-cloned-project-folder\
git branch -a\
git checkout <branch-name>

### Set remote to, already created remote repo with readme file
git branch -M main\
git remote add <origin-url>\
git pull origin main\
add .\
commit -m ‘first commit’\
git push -u origin main

### fix (another branch is pushing conflict) (tags-fast forward, git pull)
git checkout master\
git pull origin

### Delete git local branch
git branch -a\
git branch -d test\
git branch -D test (This will delete the branch regardless of its merge status)

### Delete git remote branch
git push origin --delete <branch-name>

### Clone branch from remote repo
git clone --single-branch -b <branchname-url >

</details>

---
### vscode configuration
[vscode download link](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user)\
**list of extension**\
✅ auto rename tag\
✅ color highlight\
✅ es7+ react/redux\
✅ fluent icons\
✅ hide files\
✅ live server\
✅ material icon theme\
✅ prettier code formatter\
✅ tailwindcss intellisense\
✅ c/c++ 76m\
✅ code runner

### VS code settings

**Snippets setting**

setting snippets as global across the editor. Open vscode code editor. Press `ctrl+shift+p`. Type `snippets`. click `snippets: configre user snippets`. and choose `new global snippets file`. Name it and paste the following code.

<details>
<summary>click to see the snippets</summary>

<pre>
{
"console output": {
	"prefix": "clog",
	"body": "console.log($0)",
	"description": ""
	},
	
	
	"regular function": {
		"prefix": "fun",
		"body": "function ${1:name}(${2:arg}) {$0}",
		"description": ""
	},
	
	"regular async function": {
		"prefix": "funf",
		"body": "async function ${1:name}(${2:arg}) {$0}",
		"description": ""
	},
	
	"arrow function": {
		"prefix": "af",
		"body": "const ${1:name} = (${2:arg}) => {$0}",
		"description": ""
	},
	
	"arrow async function": {
		"prefix": "aff",
		"body": "const ${1:name} = async (${2:arg}) => {$0}",
		"description": ""
	},
	
	"anonymous arrow function": {
		"prefix": "aaf",
		"body": "(${1}) => $0",
		"description": ""
	},
	

	"html tag": {
		"prefix": "tag",
		"body": "<$1 className={`$2`}>$0</$1>",
		"description": ""
	},
	
	"document id": {
		"prefix": "docid",
		"body": "document.getElementById('$0')"
	},
	
	"query selector id": {
		"prefix": "qs",
		"body": "document.querySelector('#$0')"
	},
	
	"query selector class": {
		"prefix": "cqs",
		"body": "document.querySelector('.$0')"
	},
	
	"query selector class all": {
		"prefix": "cqsa",
		"body": "document.querySelectorAll('.$0')"
	},
	
	
	"use state": {
		"prefix": "cstate",
		"body": [
			"const [${1:name}, set${1/(.*)/${1:/capitalize}/}] = useState$0($2)"
		]
	},
	
	"use effect": {
		"prefix": "signal",
		"body": ["useEffect$0 (() => {\t\n},[${1:dependency}])"]
	},
	
	"pass props": {
		"prefix": "pass",
		"body": ["${1:propname}={${0:prop}}"]
	},
	
	"class name": {
		"prefix": "cn",
		"body": ["className={`${0}`}"]
	},
	
		"React Functional Component with Props": {
			"prefix": "rfc-props",
			"body": [
				"type ${1:ComponentName}Props = {",
				"  children: React.ReactNode;",
				"};",
				"",
				"const ${1:ComponentName} = ({ children }: ${1:ComponentName}Props) => {",
				"  return (",
				"    ${2:<div>}{children}</div>",
				"  );",
				"};",
				"",
				"export default ${1:ComponentName};"
			],
			"description": "Creates a React functional component with TypeScript props."
		}
	
	
}

</pre>
</details>

---


**Editor interface and ueses setting**
- copy full json code from the link above
- open vscode
- press ctrl + shift + p
- search for `open user settings (json)`
- paste the copied code here and save

<details >
<summary>click to see the settings.json</summary>
<pre>
{
  "breadcrumbs.enabled": false,
  "editor.fontFamily": "monaspace neon var",
  "editor.fontSize": 14,
  "editor.fontLigatures": "'calt','cv01', 'cv02', 'cv06','cv13', 'cv14', 'cv18', 'cv27', 'cv31','ss01','ss02', 'ss03','ss04','ss05','ss08'",
  "editor.fontWeight": "400",
  "editor.cursorSmoothCaretAnimation": "off",
  "editor.cursorSurroundingLines": 8,
  "editor.smoothScrolling": true,
  "editor.mouseWheelScrollSensitivity": 2,
  "editor.minimap.enabled": false,
  "editor.wordWrap": "on",
  "editor.tabCompletion": "on",
  "editor.formatOnSave": true,
  "editor.acceptSuggestionOnEnter": "off",
  "editor.acceptSuggestionOnCommitCharacter": false,
  "editor.tabSize": 2, //extension
  "editor.parameterHints.enabled": false,
  "editor.hover.above": false,
  "editor.guides.bracketPairs": "active",
  "editor.lineNumbers": "on",
  "editor.glyphMargin": false,
  "editor.stickyScroll.enabled": false,
  "editor.lightbulb.enabled": "off",
  // "editor.folding": false,
  // "editor.renderWhitespace": "boundary",
  "editor.tokenColorCustomizations": {
    
  },
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  },
  //** <-- terminal -->
  "terminal.integrated.tabs.location": "left",
  "terminal.integrated.fontSize": 16,
  "terminal.integrated.fontFamily": "cascadia code, jetbrains mono, monospace",
  "terminal.integrated.cursorStyle": "line",
  "terminal.integrated.cursorWidth": 2,
  "terminal.integrated.cursorBlinking": true,
  "debug.console.fontFamily": "consolas",
  "debug.console.fontSize": 16,
  //** inegretd terminal switch to terminal from powershell -->
  "terminal.integrated.defaultProfile.windows": "Git Bash",
  "terminal.integrated.profiles.windows": {
    "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe (migrated)": {
      "path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
      "args": []
    }
  },
  //** <-- other -->
  "files.defaultLanguage": "typescript",
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1050,
  "zenMode.fullScreen": false,
  "tailwindCSS.emmetCompletions": true,
  "breadcrumbs.symbolPath": "off",
  "explorer.compactFolders": false, // expands folder structre even for the single file
  "workbench.startupEditor": "none",
  "workbench.editor.showTabs": "multiple",
  "workbench.iconTheme": "material-icon-theme",
  "workbench.productIconTheme": "fluent-icons",
  "workbench.colorCustomizations": {
    "tab.inactiveForeground": "#e9e9e9",
    "tab.activeForeground": "#ffffff",
    "editorIndentGuide.activeBackground1": "#2bff00"
    /*    
      "statusBar.background": "#222225",
      "statusBar.noFolderBackground": "#222225",
      "statusBar.debuggingBackground": "#511f1f"
      "editorWhitespace.foreground": "#606b8d"
      */
  },
  "notebook.lineNumbers": "on",
  "notebook.markup.fontSize": 17,
  "[python]": {
    "editor.formatOnType": true
  },
  "javascript.updateImportsOnFileMove.enabled": "always",
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "liveServer.settings.donotVerifyTags": true,
  "explorer.confirmDelete": false,
  "reactSnippets.settings.importReactOnTop": false,
  "liveServer.settings.donotShowInfoMsg": true,
  "window.menuBarVisibility": "compact",
  "window.commandCenter": false,
  "workbench.colorTheme": "Anysphere dark"
}
</pre>
</details>

---
<details >
<summary>click to see the .prettierrc</summary>
<pre>
{
  "jsxBracketSameLine": true,
  "plugins": ["prettier-plugin-tailwindcss"],
  "tailwindAttributes": ["css"]
}
</pre>
</details>

---
