# VSTS Custom Build Task Sample

This repository is intended to provide a sample template to build a VSTS custom build task extension.


# Prerequisites

- [NodeJS](http://nodejs.org)
- [TFX Cli](https://github.com/Microsoft/tfs-cli)

# Download the CLI

Execute the following command from your favorite shell/command prompt 
```sh
npm install -g tfx-cli
```

# Getting Started

The following is a brief jump start to building your first VSTS custom build task

## Files and Directories

| Files              | Description | 
| ------------------ | ------------- | 
| README.md          | Details about project and files | 
| icon.png           | Icon for extension      |   
| vss-extension.json | Extension manifest      |    
| task.json          | Task manifest      | 
| powershell.psh     | PowerShell script to perform build task      | 

Directory structure
```
project
│   README.md
│   icon.png    
│   vss-extension.json    
│
└───buildtask
│   │   task.json
│   │   powershell.ps1
```

# Package the Build Task

Package the extension using the follwing

```sh
tfx extension create --manifest-globs vss-extension.json
```

# Publish the Build Task

Use the following to publish your build task

```sh
tfx extension publish --manifest-globs vss-extension.json --share-with youraccount
```

## Links

https://www.andrewhoefling.com/devops/2017/10/02/Dev-Ops-VSTS-Custom-Build-Task-Extension.html

https://docs.microsoft.com/en-us/vsts/extend/develop/add-build-task?view=vsts