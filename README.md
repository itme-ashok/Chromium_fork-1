# Chromium
---

### Building Chromium for iOS
Chromium is an open-source browser project that aims to build a safer, faster, and more stable way for all Internet users to experience the web. 
In this tutorial, I'm going to tell how to do checking out and building Chromium for iOS. It's quite bit complicated 😟 when you see in the official site. I made it simple to play around.💪

### Reference : https://chromium.googlesource.com/chromium/src/+/master/docs/ios/build_instructions.md#System-requirements

### Prerequisites
You should have atleast 80 to 90 gb free space in your mac before getting into it.
Fastest network connection
You must have patience to complete this task 😜

### Step1 :
### Clone depot toot
Open terminal → Folder → Paste this command
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
Its take few seconds to complete and after that you will have depot_tools folder in your directory.

### Step2:
### Setting up path
In the terminal,
vim .zshrc
Add depot_tools absolute path to .zshrc file and save it
export PATH="$PATH:/your path/depot_tools"
then again come to terminal and execute the command
source .zshrc

### Step3 :
### Create chromium directory
Open terminal → Folder → Paste this command
mkdir chromium && cd chromium
Now you are in the chromium folder. Following commands should be executed in this folder

### Step4 :
### Fetching iOS code
Execute the following commands
1. pwd
2. ../depot_tools/fetch iOS

### Step5 :
### Running iOS
Short commercial break ☕️
It takes minimum 1hr for fast network and X hrs for slow network to complete. Let's meet after that! 😅


---

### Step6 :
### Syncing projects
It takes minimum 3 hrs! Please have patience. 😜
Once syncing done, you have chromium folder finally.

### Step7 :
### Setting up the build
In the src folder, execute the following command. It takes  a couple of minutes to generate out/build/all.xcodeproj.
ios/build/tools/setup-gn.py

### Step8 :
### Debugging
Once you get the all.xcodeproj, you need to generate debug folder. To achieve this, run the below command from src folder
autoninja -C out/Debug-iphonesimulator gn_all
It will take 7 to 9 hrs to complete

### Step9 :
### Open Xcode and Play around 🙌


---
