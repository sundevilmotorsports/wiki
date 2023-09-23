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

## Electrical
- KiCad: [link](https://www.kicad.org/download/)
    - We use KiCad to design schematics and printed circuit boards.
    - Tutorial should go over how to use KiCad: [link](https://docs.kicad.org/7.0/en/getting_started_in_kicad/getting_started_in_kicad.html)
    - Some overlap with the tutorial above, but goes into much more detail especially for design process and best practices: [YouTube link](https://www.youtube.com/watch?v=aVUqaB0IMh4&ab_channel=Phil%E2%80%99sLab)
- Git
## Mechanical
- SOLIDWORKS (follow instruction in Drive)
- PDM: soon :c
## Software
- Git
- VS Code: [link](https://code.visualstudio.com/download)
    - you'll also want to install Platform IO extension for Teensy development:
- Python 3
    - Windows: Search in Microsoft Store
    - Mac/Linux: likely already installed; confirm by running `python3` or `python`
- STM32CubeProg: [link](https://www.st.com/en/development-tools/stm32cubeprog.html)
    - used to download programs via the DFU bootloader
- STM32CubeIDE: [link](https://www.st.com/en/development-tools/stm32cubeide.html#get-software)
    - used to write and debug code for STM32 microcontrollers; can upload via SWD/JTAG
    - easily configure STM32 peripherals, clock settings, etc.

For STM32 software, unfortunately you will have to provide an email to download the software :(
