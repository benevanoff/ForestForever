>UNIT TESTING<

Preface: An install of the Unity Editor (VERSION 2020.3.22f1) is required to execute the unit testing for this project. However, it should be noted that all testing scripts are available in the
project folder (in \final-project-segfaultcoredumped\unity-folder\project\Assets\Scripts) and all test results are provided (in \final-project-segfaultcoredumped\unity-folder\unit-testing).

We made comprehensive unit tests for the required gameplay functions outlined in our project proposal.

Our final project implements Unity's built-in "Test Runner" to build our unit testing.
Basically, Unity utilizes two types of tests: "EditMode" and "PlayMode" testing.

EditMode - tests scripts outside of the game runtime environment
PlayMode - tests game functionality/scripts within the game runtime environment

Each individual folder contains test results generated by our unit test code which can be located
at: \final-project-segfaultcoredumped\unity-folder\project\Assets\Tests

The unit tests can be ran outside of the Unity Editor through command lines such as Command Prompt on Windows and Terminal on MacOS.

Template Command Line (Windows): [CD to where Unity.exe is located*]Unity.exe -runTests -batchmode -projectPath [Project Directory] -testResults [Save Directory] -testPlatform [EditMode/PlayMode]
Template Command Line (MacOS): /Applications/Unity/Unity.app/Contents/MacOS/Unity -runTests -batchmode -projectPath [Project Directory] -testResults [Save Directory] -testPlatform [EditMode/PlayMode]

Example Command Line Used Locally: Unity.exe -runTests -batchmode -projectPath C:\Users\safeer\cs128env\src\fp\final-project-segfaultcoredumped\unity-folder\project -testResults C:\Users\safeer\cs128env\src\fp\final-project-segfaultcoredumped\unity-folder\unit-testing\edit-mode-results\results.xml -testPlatform editmode



*(C:\Program Files\Unity\Hub\Editor\2020.3.22f1\Editor) is the default Windows save path
 (/Applications/Unity/Unity.app/Contents/MacOS/Unity) is the default MacOS save path

***The Unity.exe editor cannot be open when batchmode commandlines are called!



NOTE: Be patient as tests run. Some tests require up to 20-30 seconds minimum to execute. When using the commandline method, the only indicator that the test is done executing is 
when the results.xml file is updated to the chosen save directory.

ALTERNATIVE: Rather than running tests through batchmode command lines, tests can be directly ran within the Unity editor. Directions: Open the project in the Unity editor, click Window>General>Test Runner.