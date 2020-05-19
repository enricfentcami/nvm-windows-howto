# How-To install and use the NVM Windows tool (Node Version Manager)

Nvm can be used to manager various node versions, very useful to develop web apps with different Angular versions:

* Step 0: Uninstall or delete existing Node.js installations in the system, e.g: "C:\Program Files\nodejs". Also remove the NPM installed in folder "C:\Users\<user>\AppData\Roaming\npm"
* Step 1: Download nvm latest release from https://github.com/coreybutler/nvm-windows/releases
* Step 2: Choose asset "nvm-setup.zip"
* Step 3: Unzip & click on installer
	* Step 3.1: Restart any opened terminal to refresh the config
* Step 4: Check if nvm properly installed, In new command prompt type "nvm"
* Step 5: Install Node.js using nvm : nvm install <version> : The version can be a Node.js version or "latest" for the latest stable version
* Step 6: check node version:
	
  > `node -v`
	
  > `npm -v`
	
  If cannot find module NPM (`npm -v` fails), check if the module exists in "C:\Users\<user>\AppData\Roaming\nvm\vX.Y.Z\node_modules\npm"
	
  If it doesn't exist, download and include the module from the Node.js release package https://nodejs.org/download/release/
	
  Steps to fix it using the 12.16.3 version:
  
	* Step 6.1: Go to https://nodejs.org/download/release/v12.16.3/
	* Step 6.2: Download file: node-v12.16.3-win-x64.zip
	* Step 6.3: Unzip the file
	* Step 6.4: Copy the folder "npm" from "node_modules" into the installed Node.js version inside the NVM folder "C:\Users\<user>\AppData\Roaming\nvm\v12.16.3\node_modules\"
   
* Step 7 (Optional): If you want to install another version of Node.js, Use STEP 5 and 6 with different version.
* Step 8: Check list Node.js version: nvm list
* Step 9: If you want to use specific node version do: nvm use <version>
* Step 10: (Re)Install any global utilities, for example Angular CLI (https://cli.angular.io/):
	
  > `nvm use 12.16.3`

  > `npm install -g @angular/cli`
	
  > `nvm use 12.0.0`
	
  > `npm install -g @angular/cli@6.1.0`


