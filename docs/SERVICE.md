## Crunch Image(s) macOS Right Click Menu Service

### Install Crunch

In order to use the macOS service, you must install the Crunch GUI tool.  The macOS service depends upon the embedded versions of the PNG image optimization applications that are used by Crunch to modify your image files.

See the install instructions on the README page.  You may use either the Homebrew or .dmg installer approach.  When the Crunch install is complete, continue with the instructions below. Please do not modify the default Crunch.app install location if you intend to use the macOS service.

### Install the Crunch Image(s) service

First, [download the latest release version of the Crunch repository source](https://github.com/chrissimpkins/Crunch/releases/latest).  You can use either the .zip or .tar.gz download link.

Next, unpack the Crunch repository source archive in a directory on your system.

Then, use either of the following approaches to install the macOS service on your system.

#### 1) Install with Finder

- Open the Crunch source repository in the Finder. Open the `service` directory that is located in the root of the repository directory. The `Crunch Image(s).workflow` directory will be contained in the `services` directory.  This is the workflow that you will install.
- Open a new tab in the Finder with `CMD-T` and select Go > Go to Folder in the Finder menu (or type `SHIFT-CMD-G`)
- In the open "Go to the folder:" free text prompt, enter the following:  `~/Library/Services`
- Switch back to the first tab that is located inside the Crunch source repository and drag the `Crunch Image(s).workflow` directory to the second tab so that it is installed on the path `~/Library/Services/Crunch Image(s).worflow`.
- Close the Finder
- You may now delete the Crunch source repository.  These files are no longer necessary.

#### 2) Install with make

If `make` is installed on your macOS system, you can use the Crunch Makefile to install the macOS service.

- Open a terminal in the root of the Crunch source repository
- Enter the following command to install the macOS service in the directory `~/Library/Services`:

```
$ make install-macos-service
```

`sudo` is necessary in order to complete the copy of the macOS service to this directory on your system.  You will be prompted for your password after you enter the above command.  Enter it and you will receive confirmation that the install completed.

### Usage