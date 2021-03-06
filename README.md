# RLC Analyser Set Up Guide
## Product Usage
When the RLC Analyser is started the user is prompted to browse to search for a new folder or RLC to process. Alternatively, the user can also process the default folder/file displayed. Instructions are provided on the top of the window. 

## User Set Up

### 1. Download the JAR file
Navigate to the Release tab on GitHub. Download the latest release version - current version is **v1.0**. This JAR file contains the latest built version of the RLC Analyser.


### 2. Run the JAR
In order to run the JAR file, Java 8 needs to be installed. To run the JAR double click on the icon. Skip the next step if permissions are not denied.
1. On Mac - permissions may need to be changed. Open System Preferences -> Security & Privacy -> General -> Open Anyway. 

## Developer Set Up

### 1. Eclipse Development Environment Set Up
#### 1.1. Install Eclipse and Create Workspace
1. Download the latest [Eclipse Oxygen - Eclipse for RCP and RAP Developers](http://www.eclipse.org/downloads/packages/eclipse-rcp-and-rap-developers/oxygen1a)
2. Install Eclipse
3. Start Eclipse and create a workspace for the RLC Analyser Project
#### 1.2. Set Up JUnit
Settings Panel | Change
---------------|-------
Window (Menu) -> Preferences -> Java -> JUnit | Select the "add -ea to VM arguments when creating JUnit launch configuration" checkbox

Apply the changes and close.

### 2. Import Sources to Eclipse
#### 2.1. Disable "Build Automatically"
1. Uncheck the "Build Automatically" menu item in the "Project" menu.
2. Re-enable automatic building once the code has been successfully imported and the Target Platform configured and refreshed.
#### 2.2. Download the RLC Analyser Project
Either clone the project using Git or download the project into local drives. 
1. In the main page, click the "Clone or Download" button and select from one of the options given.
#### 2.3. Import RLC Analyser Project
1. Open the project import dialog: "File" menu > "Import..." menu item
2. Expand the "Maven" folder, select "Existing Maven Projects" and click the "Next > " button
3. Select the root directory as the directory of the downloaded project location
4. Click "Finish"


### 3. Compiling 
#### 3.1. Compiling the RLC Analyser
In the "Project" menu, check the "Build Automatically" menu item.


### 4. Starting RLC Analyser and Unit Tests
#### 4.1 Create a Run Configuration - Java Application
1. From the "Run" menu, click on "Run Configurations...".
2. Right click "Java Application" -> click "New".
3. Set name to "RLCAnalyserStart" or anything similar.
4. Under Project, click "Browse..." -> select the RLC Analyser project -> click "Ok".
5. Click "Search..." -> select "com.orchestral.rhapsody.rlcanalyser.RlcAnalyserConsole" -> click "Ok".
6. Click "Apply" -> click "Run".

Note: A warning should appear in the Eclipse console on first start due to the initialisation of the logger files, on the next launch these warning should disappear.

#### 4.2 Create a Run Configuration - JUnit Tests
1. From the "Run" menu, click on "Run Configurations...".
2. Right click "JUnit" -> click "New".
3. Set name to "RLCAnalyserTest" or anything similar.
4. Select "Run all tests in the selected project, package or course folder:".
5. Click "Search..." -> Select the RLCAnalyser project.
6. Ensure the "Test runner" field is set to "JUnit 4".
7. Click "Apply" -> "Run".

#### 4.3 Start Maven build
1. Right click on your project and select Run As > Maven build..
2. In the Goals text field, type 'install', apply and run.

If you get a compilation error such as: "No Compiler is provided in this environment. Perhaps you are running a JRE rather than a JDK?" after running the Maven Goal, try this:

- Run Menu > Run Configurations > Maven Build > Select an existing build or create a new one > Under the JRE tab ensure that the default Workspace JRE is checked > Uncheck and check this checkbox.
- Return to the main tab and run again with the install goal.


## Contributing to the Project
### Introducing New Features
For each feature or improvement please refer to the Projects that are currently opened under the Projects tab above. If the project is not currently opened:

1. Make a new project with a clear title and description. Set the project up so has the basic KANBAN style.
2. Add appropriate to-dos.

Use this space to populate the projects with sub tasks.

### Creating Issues
If you notice a bug or problem with the functionality of the code, create an issue and in the GitHub Issue Tracker tab in the top bar. 

### Contributing to the Code
To ensure that the code is maintained to a satisfactory standard, all changes made to the program should undergo an approval process before merging to the master branch. 

1. Fork the orionhealth/rlc-analyser repository.
2. Create a new pull request when you want to push changes. 
3. Await approval
4. The pull request must pass the build and the code review process.
