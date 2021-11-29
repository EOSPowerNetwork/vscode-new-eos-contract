# Intro
Get up and running with a new EOS smart contract (with clsdk / partial gdb debugging support) in < 2 minutes.

# Prerequisites
1. VSCode installed on your development PC
2. [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) VSCode extension has been installed

# How to use
1. Clone this repo **into a new directory with the name of your project** (Directory naming restrictions: ```[a-zA-Z0-9][a-zA-Z0-9_.-]```)
2. Open in VSCode
3. Modify the .devcontainer file according to the instructions at the top of the file
4. Run the ```Remote-Containers: Rebuild and Reopen in Container``` command in VSCode

VSCode will relaunch, connecting to a new docker container with an empty eos contract ready to be compiled with clsdk (from [this](https://github.com/EOSPowerNetwork/eos-contract-template) repo).
After it launches, consider initializing it as a new git repository and pushing it to github to make sure you don't lose any work.

To collaborate with other developers, or just to work on your project from another PC, you may simply use the [VSCode Open EOS Contract](https://github.com/EOSPowerNetwork/vscode-open-eos-contract) repository.

# Misc notes
When VSCode closes, the container stops. The data within the container is not accessible, as it's stored in an unnamed volume mounted on your PC, only accessible through the docker container launched by VSCode.
All changes made within the container will persist on that PC (as long as you don't delete the docker volume), and must be pushed to a git repository if you want to work on it on another PC.
