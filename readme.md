https://code.visualstudio.com/docs/getstarted/settings

Machine A:

In the Visual Studio Code PowerShell terminal:

code --list-extensions > extensions.list

Machine B:

Copy extension.list to the machine B
WINDOWS PowerShell:
cat extensions.list |% { code --install-extension $_}
LINUX:
cat vscode-extensions.list | xargs -L 1 code --install-extension
