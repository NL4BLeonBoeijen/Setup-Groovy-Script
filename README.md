# Setup IntelliJ IDEA for Groovy Script

## Download IntelliJ IDEA and Groovy Script

* Download Latest versions via links below, or check the [files](./files) folder
* Download [Visual C++ 2013 Runtime](https://help.sap.com/docs/link-disclaimer?site=https%3A%2F%2Fwww.microsoft.com%2Fde-de%2Fdownload%2Fdetails.aspx%3Fid%3D40784)
* Download [SAP JVM](https://tools.hana.ondemand.com/#cloud)
* Download [Groovy Script](https://groovy.apache.org/download.html)
* Download [IntelliJ IDEA Community Edition](https://www.jetbrains.com/idea/download/?section=windows)
* Download [Script API](https://tools.hana.ondemand.com/#cloudintegration)


* Install/Update Visual C++ 2013 Runtime
* Unzip SAP JVM, and copy sapjvm_8 folder to C:/Program Files
* Install Groovy Script, run groovy-xxx.msi
* Install IntelliJ IDEA
 
## Setup IntelliJ IDEA for Creating Groovy Script projects

* Start IDEA and create a new Project
  * Location: d:\GroovyScripts
  * Language: Groovy
  * Build system: IntelliJ
  * JDK: sap-1.8, Point to c:\program files\sapjvm_8 folder
  * Groovy SDK: 2.4.21

* Create new project **sap-press-cpi-groovy**
* Modify the project structure: choose: **File - Project Structure**
* Goto **Project Settings - Modules**
* Remove the *Sources* tab from the **src** folder
* Create a new **main** folder in the **src** folder and then a new **groovy** folder in the **main** folder
* Add the *Sources* tab to the **groovy** folder.

* Create a **lib** folder in the d:\GroovyScripts folder
* Copy the *Script API* to this **lib** folder
* Add the library to the project
  * Choose: **File - Project Structure**
  * Goto: **Platform Settings - Global Libraries**
  * Add, (+) Sign, a New Global Library of type **JAVA**
  * Select the *cloud.integration.script.apis-2.7.1.jar* from the **lib** folder

* Create a **CPI Groovy Project Template**
  * In the menu bar, choose **File - New Projects Setup - Save Project as Template** with name **Groovy for CPI**

* Create a **Groovy Script for CPI** Code Template
  * In the menu bar, choose **File - Settings**
  * Then under **Editor - File and Code Templates** use the (+) Sign and add the script: **Groovy Script for CPI**
  
``` groovy
import com.sap.gateway.ip.core.customdev.util.Message;

def Message processData(Message message){

    return message
    
}
```
