# New DAQ Team Member Computer Setup
## Git
- We use Git for version control for all of our software and electrical designs.
    - When installing, ensure you add git to `PATH`!
    - Windows: [link](https://git-scm.com/)
    - Mac/Linux: likely already installed; confirm by running `git` in a terminal.
    Otherwise follow the link above
- GitHub Desktop (optional): [link](https://desktop.github.com/)
    - GitHub Desktop client makes it very easy to use git
- Setting up git with GitHub:
    1. If you do not plan on using GH Desktop (see above), follow the instructions [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for generating a new SSH key and adding it to the ssh-agent.
    2. Then add the key to your account using [these](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) instructions.
- Intro/Overview [link](https://github.com/sundevilmotorsports/wiki/blob/main/daq/Git%20Introduction.pdf)
- Git Cheat Sheet [link](https://github.com/sundevilmotorsports/wiki/blob/main/daq/git-cheat-sheet.pdf)

## Electrical
- KiCad: [link](https://www.kicad.org/download/)
    - We use KiCad to design schematics and printed circuit boards.
    - Tutorial should go over how to use KiCad: [link](https://docs.kicad.org/7.0/en/getting_started_in_kicad/getting_started_in_kicad.html)
    - Some overlap with the tutorial above, but goes into much more detail especially for design process and best practices: [YouTube link](https://www.youtube.com/watch?v=aVUqaB0IMh4&ab_channel=Phil%E2%80%99sLab)
- RapidHarness: [link](https://rapidharness.com/)
    - we're giving this a try for wiring harness design
    - tutorial: [link](https://rapidharness.com/harness-software-tutorials)
- Git
## Mechanical
- SOLIDWORKS (follow instruction in Drive)
- PDM: soon :c
## Software
- Git
- VS Code: [link](https://code.visualstudio.com/download)
    - you'll also want to install the Platform IO extension for Teensy development
- Python 3
    - Windows: Search in Microsoft Store
    - Mac/Linux: likely already installed; confirm by running `python3` or `python`
- PyQt
    - we use PyQt for the majority of our GUI projects. [tutorial](https://build-system.fman.io/pyqt5-tutorial)
 
On the embedded side we use Teensy development boards ([Teensy 4.0](https://www.pjrc.com/store/teensy40.html), [Teensy 4.1](https://www.pjrc.com/store/teensy41.html)) and STM32 microcontrollers
- Teensy overview: [link](https://github.com/sundevilmotorsports/wiki/blob/main/daq/Teensy%20Quickstart.pdf)
  - Simple to use, can use PlatformIO and VS Code for programming
- STM32CubeProg: [link](https://www.st.com/en/development-tools/stm32cubeprog.html)
    - used to download programs via the DFU bootloader
- STM32CubeIDE: [link](https://www.st.com/en/development-tools/stm32cubeide.html#get-software)
    - used to write and debug code for STM32 microcontrollers; can upload via SWD/JTAG
    - easily configure STM32 peripherals, clock settings, etc.

For STM32 software, unfortunately you will have to provide an email to download the software :(
