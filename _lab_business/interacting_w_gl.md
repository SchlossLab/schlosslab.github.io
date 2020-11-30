---
layout: index_page
title: Interacting with files on Great Lakes
toc: true
---

### Prerequisites

* Need a Great Lakes account
* UM VPN (for off campus connections)
* [Atom](https://atom.io)
* You can do `ssh glc` from the command line to connect to Great Lakes by editing your `~/.ssh/config` file to contain...

```
Host glc
  HostName greatlakes.arc-ts.umich.edu
  RemoteForward 52698 localhost:52698
  User pschloss

Host glx
  Hostname greatlakes-xfer.arc-ts.umich.edu
  User pschloss
    
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
```

The `glx` is useful for logging into Great Lakes if you are transferring files in and out of Great Lakes. It doesn't require Two Factor Authentication so that's a convenience.

### Two terminal windows...
   * nano/vim/emacs in one
   * R in one
   * Copy and paste back and forth to test
   * Notes:
     - Pretty tedious
     - There are R packages for vim/emacs, but then you'll have to learn them

### Connect to server through GUI
  * Connect to UM with VPN
  * Go -> Connect to server
      
      ```
      smb://schloss-lab.turbo.storage.umich.edu/schloss-lab/pschloss
      ```
      
  * Navigate to desired directory
  * Three options...
    - Use the two terminal windows approach and use this to see images
    - Open in RStudio by double clicking on RProj file
    - In Atom
      - File->Open... and navigate to project and open project
      - copy/paste or send code to R running on GL
      - R-exec atom package allows you to put cursor on line and run in terminal
  * Notes:
    - Lags and gets painful; Seems to work much better from on campus (VPN?)
    - RStudio doesn't seem happy with this

### Reverse tunnel w/ Atom (other text editors have this ability too)
  - The second line in the .ssh/config file we created allows for the reverse tunneling
  - https://atom.io/packages/remote-atom
  - remote server is Great Lakes
  * Install remote-atom package on your laptop
  * On Great Lakes, run...

    ```
    curl -o rmate https://raw.githubusercontent.com/aurora/rmate/master/rmate
    chmod +x rmate
    mv rmate ~/bin/ratom
    ```
    
  * Log out of Great Lakes
  * Turn Remote Atom package on in Atom (before you log into Great Lakes)
  * Log into Great Lakes
  * On Great Lakes, navigate to your directory. Open file using...

    ```
    ratom README.md
    ```
    
  * Should open in Atom.
  * Notes:
    - No obvious lagging
    - Can open files in separate panes of Atom, but can't open project directory
    - This is a pretty good, all around solution

### Open OnDemand
  - Good for interactive jobs and using RStudio
  - There is also a Remote Desktop app that is analogous to the Connect to Server approach above
  - Browser based interface to use Great Lakes
  * Navigate to  http://greatlakes.arc-ts.umich.edu/
  * Interactive apps -> RStudio
  * Fill in the specs for your job...
    
    ```
    account: pschloss99
    Number of Hours: (however long you want it for)
    Number of Cores: 1
    Partition: standard
    Memory per node (GB): 4
    ```
    
  * Press "Launch"
  * You will then need to wait a moment or two as it starts your instance. Then click "Launch RStudio" when presented with the button
  * RStudio will open. You can fiddle with the window layout
  * In the Files panel (lower right corner) you can click on the button with "..." to navigate to /nfs/turbo/schloss-lab/<uniquename> and from there to your project. Select the directory with your project and then do "More"->"Set As Working Directory" and you're good to go
  * When you're done, close the window and 
