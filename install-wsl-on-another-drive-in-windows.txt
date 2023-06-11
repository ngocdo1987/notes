Installing WSL on another drive in Windows

1.Check WSL 2 installations that are already installed in your computer.

wsl --list -v

If the installation you want to move to another drive is still running we have to stop it with following command. In my case, I want to move Ubuntu, so I am terminating Ubuntu.

wsl -t Ubuntu

2.Export to a folder. (Here exporting Ubuntu as ubuntu-ex.tar to D:\wsl\wsl_export)

wsl --export Ubuntu "D:\wsl_export\ubuntu-ex.tar"

3.Unregister previous WSL installation. When you unregister it will remove Ubuntu from the wsl2 list that we saw earlier.

wsl --unregister Ubuntu

4.import your WSL installation to a folder. This step also re-registers the ubuntu.
wsl --import Ubuntu "D:\wsl_import\ubuntu" "D:\wsl_export\ubuntu-ex.tar"
