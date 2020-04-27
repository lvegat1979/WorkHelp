
# WebMap 5 for Dummy's

This a little documentation and guide to find information related to webmap 5

Download the follow repositories:

 - [WFNetDCP](https://collaboration.artinsoft.com/tfs/Product/Product/_git/WFNetDCP)
   
 - [WFNetJanus](https://collaboration.artinsoft.com/tfs/Product/Product/_git/WFNetJanus)
  
 - [WFNetConversionTool](https://collaboration.artinsoft.com/tfs/Product/Product/_git/WFNetConversionTool)

**WFNet DCP Configuration** 

Please run the follow command in any console for configuration.

> In case that you have some problems, please do a git clean up, please check that you are connected to the vpn, becasuse many of packages come from mobilize nutget repositories.

 - cmd -> .\build init 	
 - cmd -> .\RestorePackages.cmd 	
 - cmd -> .\build

## WFNetConversionTool Configuration

### Folder to download build of WebMap Conversion Tool

	\\BUILDARTIFACTORY\WebMAPWinforms\Product\Mobilize.WFNetConversionTool
	
Please run the following commands in any console. In case that you want to run locally the migration tool.

    Please open Powershell as adminstrator

 - cmd -> .\build.cmd init 	
 - cmd -> .\RestorePackages.cmd 	
 - cmd -> .\build.cmd
 - cmd -> cd .  "return folder"
 - cmd -> .\deploy.bat 

> Note: In case of any problems with running **build.cmd init** build.core issue, please open the folder ***\\ais-build-w7\BuildScriptUpdate*** and save login the credentials, cause some people is not inside the **mobilize network** just connected with the vpn, we need to store our credentials inside credetials manager.  Buiild core is store in this folder. Please run again the command.


## Running Migration Tool

	cmd=> CmdRunner\release\net461\wfnetct.exe -i  "..\UICheckBox\UICheckBox.sln" -o "..\Example\UICheckBoxOut3" -l "..\Example\InternalWebMap.lic" -c "..\LGC\Example\webmap.config"
	
	-i = Solution to migrate
	-o = Output folder
	-l = License
	-c = WebMap Config file


## Introduction Videos Backend and  Frontend

[Backend Part 1](https://1drv.ms/v/s!AjbyneS6s2dlgaV_l8gG1n0tOw8Lzg?e=Sy8PXY) This video talk about WebMap 5 and some generals things.

[Backend Part 2](https://1drv.ms/v/s!AjbyneS6s2dlgaYAGq77sq5dbRLdNg?e=cJHVf1) In this video, we are talking about DTO, Data Transfer Object, also Models and Mapers the mains important objects in the server side.

[Frontend](https://github.com/lvegat1979/WorkHelp/blob/master/WorkHelp.md) This video talk about Frontend.

## Checking Builds
	In order to check if the build was successfulll, please go here and  look up for you  build.

[Builds](https://collaboration.artinsoft.com/tfs/Product/Product/_build?definitionId=1199) All builds of all components are created for alphas and stantards builds.

> Note: If you need a alpha, your branch need to be created like with inside feature/**BranchName**. 

![Feature](https://github.com/lvegat1979/WorkHelp/blob/master/Feature.PNG)

## FrontEnd Tips.

Global commands, you can run it in any folder (just one time, not anymore)

- cmd -> npm install @angular/cli -g 
- cmd -> npm install yarn  -g
- cmd -> npm install gulp -g



### Janus Component.

If you are on Janus Component. Please go to Angular Folder run the following commands where the json file are.

 
 - cmd -> .\yarn.cmd install
 - cmd -> .\gulp

> Note: In case that you need  install yarn please run.  npm install yarn -g and  npm install gulp -g

### Any Migrated App (FrontEnd)

	If you are on Janus Component. Please go to Angular Folder run the following commands where the json file are.

	
	 - cmd -> .\yarn.cmd install
	 - cmd -> ng build
	 - cmd -> ng serve -o

> Tip: There are a nice command to remove files easy and faster in order to delete node_modules and yarn lock is a rimraf. To install it please execute the next following npm rimraf install -g

	 - cmd -> rimraf.cmd .\node_modules\
	 - cmd -> rimraf.cmd .\yarn.lock
	 
### Make a component template (FrontEnd)

	In order to create a component please run the following command. In the path where the components are. **frontend\JanusComponents\projects\janus\src\lib\components**
	
> cmd -> ng g c ui-radio-button

![Create a Componet](https://github.com/lvegat1979/WorkHelp/blob/master/createcomponent.PNG)

### How to packages a nutget in the client side.

In order to test Janus component changes, please packing Janus Component, paste it to migrated the app.

Please open a command line and go to follow folder WFNetJanus\frontend\JanusComponents

> cmd : cd WFNetJanus\frontend\JanusComponents>
 cmd: npm pack

A tgz file should be created.

![Feature](https://github.com/lvegat1979/WorkHelp/blob/master/tz.PNG)

After that please unzip and copy it in your migrated app nutget folder, then content should be copied in jns-winforms-commponents. Please keep node_modules folder.

![Feature](https://github.com/lvegat1979/WorkHelp/blob/master/mobilizenutget.PNG)


### How to get a Model in running

	ng.probe($0).componentInstance.model


## References Documentation
[WebMap Documentation](https://artinsoft.sharepoint.com/sites/LGC-Dev/Documentos%20compartidos/General/Phase%201%20-%20Compilation%20Delivery/LGC-NextGen-Accounting-Compilation-ReleaseNote-20200117.pdf?CT=1587158918683&OR=ItemsView) This is a documentation releated to the some tips, some commands, nutgets. Was created by Esteban.

[Angular for heroes](
https://angular.io/tutorial) This manual is basic information how angular works.
