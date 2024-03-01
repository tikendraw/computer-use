# Open Interface

<picture>
	<img src="assets/icon.png" align="right" alt="Open Interface Logo" width="120" height="120">
</picture>

### Operate Your Computer Using LLMs

Open Interface can
- Figure out how to execute user requests by sending them to an LLM backend (GPT-4V) with a current screenshot.
- Simulate keyboard and mouse input to automatically execute the steps received from the LLM to operate your computer.
- Take user requests through text or voice.

[![Github All Releases](https://img.shields.io/github/downloads/AmberSahdev/Open-Interface/total.svg)]()
![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/AmberSahdev/Open-Interface)
![GitHub](https://img.shields.io/github/license/AmberSahdev/Open-Interface)
[![Code Coverage](https://img.shields.io/codecov/c/github/AmberSahdev/Open-Interface)](https://codecov.io/github/AmberSahdev/Open-Interface)

### Install
<details>
    <summary><b>MacOS</b></summary>
    <ul>
        <li>Download the MacOS binary from the latest <a href="https://github.com/AmberSahdev/Open-Interface/releases/latest">release</a>.</li>
        <li>Unzip the file and move Open Interface to the Applications Folder.<br><br> 
            <img src="assets/macos_unzip_move_to_applications.png" width="350" style="border-radius: 10px;
    border: 3px solid black;">
        </li>
        <br>
        <li>
            Launch the app from the Applications folder.<br>
            You might face the standard Mac <i>"Open Interface cannot be opened" error</i>.<br><br>
            <img src="assets/macos_unverified_developer.png" width="200" style="border-radius: 10px;
    border: 3px solid black;"><br>
            In that case, press <b><i>"Cancel"</i></b>.<br>
            Then go to <b>System Preferences -> Security and Privacy -> Open Anyway.</b><br><br>
            <img src="assets/macos_system_preferences.png" width="100" style="border-radius: 10px;
    border: 3px solid black;"> &nbsp; 
            <img src="assets/macos_security.png" width="100" style="border-radius: 10px;
    border: 3px solid black;"> &nbsp;
            <img src="assets/macos_open_anyway.png" width="400" style="border-radius: 10px;
    border: 3px solid black;"> 
        </li>
        <br>
        <li>
        Lastly, Open Interface will also need Accessibility access to use your keyboard and mouse for you, and Screen Recording access to take a screenshot to assess its progress.<br><br>
        <img src="assets/macos_accessibility.png" width="400" style="margin: 5px; border-radius: 10px;
    border: 3px solid black;"><br>
        <img src="assets/macos_screen_recording.png" width="400" style="margin: 5px; border-radius: 10px;
    border: 3px solid black;">
        </li>
        <li>Checkout the <a href="https://github.com/AmberSahdev/Open-Interface?tab=readme-ov-file#setup">Setup</a> section to connect Open Interface to LLMs (OpenAI GPT-4V)</li>
    </ul>
</details>
<details>
    <summary><b>Linux</b></summary>
    <ul>
        <li>Linux binary has been tested on Ubuntu 20.04 so far.</li>
        <li>Download the Linux binary from the latest <a href="https://github.com/AmberSahdev/Open-Interface/releases/latest">release</a>.</li>
        <li>
            Extract the executable and run it from the Terminal via <br>
            <code>./Open\ Interface</code>
        </li>
    </ul>
</details>
<details>
    <summary><b>Windows</b></summary>
    The Windows executable build is still under progress.
</details>

### Demo
![Simple Demo Placeholder](assets/Simple_Bottom_of_Wikipedia-Sped-up-2x.gif)

<hr>

### Many of the Things it's Bad at

- Accurate spatial-reasoning and hence clicking buttons.
- Keeping track of itself in tabular contexts, like Excel and Google Sheets, for similar reasons as stated above.
- Navigating complex GUI-rich applications like iMovie, Garage Band, etc.


### Future 
(*with better models trained on video walkthroughs like Youtube tutorials*)
- "Find my friends' music taste from Spotify and create a party playlist for tonight's event."
- "Create a couple of bass samples for me in Garage Band for my latest project."
- "Take the pictures from my Tahoe trip and make a White Lotus type montage in iMovie."

### Notes
- Cost: $0.05 - $0.20 per user request.<br>
(This will be much lower in the near future once GPT-4V enables assistant/stateful mode) 

### System Diagram 
```
+----------------------------------------------------+
| App                                                |
|                                                    |
|    +-------+                                       |
|    |  GUI  |                                       |
|    +-------+                                       |
|        ^                                           |
|        |                                           |
|        v                                           |
|  +-----------+  (Screenshot + Goal)  +-----------+ |
|  |           | --------------------> |           | |
|  |    Core   |                       |    LLM    | |
|  |           | <-------------------- |  (GPT-4V) | |
|  +-----------+    (Instructions)     +-----------+ |
|        |                                           |
|        v                                           |
|  +-------------+                                   |
|  | Interpreter |                                   |
|  +-------------+                                   |
|        |                                           |
|        v                                           |
|  +-------------+                                   |
|  |   Executor  |                                   |
|  +-------------+                                   |
+----------------------------------------------------+
```

### Setup
- Get OpenAI API key
- Apply in settings
