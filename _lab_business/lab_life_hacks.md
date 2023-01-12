---
layout: index_page
title: Lab Life Hacks
toc: true
---

## Computer Hacks

### Terminal Keyboard Shortcuts

| Shortcut | Action |
|----------|-------|
| Tab | Autocomplete the path under the cursor |
| Tab Tab (double tap) | Show options for autocomplete |
| ↑ | Recall the previous command (press multiple times as needed) |
| Esc + . | Recall the last argument of the last command (press multiple times as needed) |
| Ctrl + R | Search through your command history (press multiple times as needed) |
| Ctrl + A | Move the cursor to the beginning of the line |
| Ctrl + E | Move the cursor to the end of the line |
| Ctrl + D | Delete the character under the cursor |
| Ctrl + K | Cut the line from the cursor to the end |
| Ctrl + U | Cut the line from the beginning to the cursor |
| Ctrl + Y | Paste what you previously cut |
| Ctrl + C | Kill the current running command |

### Symlinks

Use symlinks to save time typing paths to directories or files you use frequently. For example, when you `ssh` into the HPC, your working directory is initially your home directory (`/home/uniqname/`). But we keep our project files in a shared lab drive: `/nfs/turbo/schloss-lab/`. You may be actively working on a project in `/nfs/turbo/schloss-lab/uniqname/project_name/` -- that can be long and hard to remember. To save time, you can create a `symlink` to your the project in your home directory like so:

```
ln -s /nfs/turbo/schloss-lab/uniqname/project_name/ /home/uniqname/project_name/
```

Then when you log in, you can simply type `cd project_name` to get to the project directory without typing the whole path. You can use a symlink wherever you would use a normal path, such as in `ls`, `cd`, `cp`, or reading/writing files in scripts.

### Aliases

When you run the same commands repeatedly, you might like to 
create **aliases** to save yourself time typing long commands with lots of options.
Add your aliases to your `~/.bashrc` or `~/.zshrc`.

For example, typing `snakemake -c 1` every time you want to run a snakemake workflow gets tiresome.
Instead, you can define an alias to assign this command to `smk`.
In your `.zshrc` file, add this line:
```
alias smk="snakemake -c 1"
```

Then, you can run `smk` to call snakemake with 1 core. 
You can also use more cores or specify any other additonal snakemake options with `smk`:
```
smk -c 8 --configfile config/test.yml
```

Here are more aliases that we've found to be helpful:

```
# run snakemake with 1 core.
alias smk="snakemake -c 1"

# print the git commit history.
alias glo="git log --oneline --abbrev-commit --all --graph --decorate --color"

# show the jobs in the queue on GreatLakes or other HPC running SLURM.
# this modifies the default format to make it more readable.
alias sqs='squeue -u $USER -o "%.18i %50j %.2t %.6M %R"'
```

### ssh config file

If you frequently login to servers with `ssh`, you can save time by creating a `config` file.
Create a file called `~/.ssh/config` with your preferred text editor and add entries for each server like so:

```
Host host_nickname
    Hostname server.address.com
    User your_username
    Port 8674
```

Then, instead of typing `ssh -p 8674 your_username@server.address.com`, you can type `ssh host_nickname`. This also works for `scp` and `rsync`!

An entry for Great Lakes looks like this:
```
Host gl
     Hostname greatlakes.arc-ts.umich.edu
     User uniqname
```

Then to login, type `ssh gl`.


### View processes running and troubleshoot slowness

Sometimes, computers run very slow because there are processes running that take up too much CPU. This can happen on shared HPC resources (e.g. Flux, Great Lakes) when users run scripts on the login node instead of properly submitting jobs to the job scheduler. You can use a command called `top` to view what processes are running on the node you're logged into. Normally, the output of `top` will look something like this:

```
PID	USER	PR	NI	VIRT	RES	SHR	S	%CPU	%MEM	TIME+	COMMAND
----------------------------------------------------------------------------------------------------------
23047	user1	20	0	107972	680	572	S	12.1	0.0	0:09.37	wc
16222	user2	39	19	7925204	329232	6472	S	1.6	0.7	1166:53	java
23170	me	20	0	162828	3136	1600	R	1.6	0.0	0:00.89	top
1	root	20	0	193772	6108	2284	S	0.0	0.0	88:18.86	systemd
```

Each row is a process. You can see the uniqname of the person running the process in the `USER` column and how much compute resources each process is using in the `%CPU` column. In this case, all of the processes have a low `%CPU`, so everything is fine here.

When someone runs scripts that they shouldn't be running on the login node, it may look something like this:

```
PID	USER	PR	NI	VIRT	RES	SHR	S	%CPU	%MEM	TIME+	COMMAND
----------------------------------------------------------------------------------------------------------
23050	user1	20	0	107975	684	575	S	175.3	0.5	3:33.54	python
23049	user1	20	0	107974	683	574	R	174.4	0.6	3:30.18	python
23048	user1	20	0	107973	682	573	S	173.5	0.5	3:28.22	python
23047	user1	20	0	107972	681	572	S	173.2	0.5	3:32.50	python
16222	user2	39	19	7925204	329232	6472	S	1.6	0.7	1166:53	java
23170	me	20	0	162828	3136	1600	R	1.6	0.0	0:00.89	top
1	root	20	0	193772	6108	2284	S	0.0	0.0	88:18.86	systemd
```

Here, `user1` has multiple processes running that are taking up over 100% CPU. As a result, there are few resources left for other users who need to use the login node to do simple tasks like moving files, editing scripts, or checking on jobs. Since the `USER` column corresponds to the user's `uniqname`, you can send them a polite email asking them to kill their processes on the login node and submit them to the job scheduler instead.

## Bench Hacks

* Open an issue or a submit a pull request if you have ideas to add here!

## Miscellanea

### Nearby Food

Sorted from nearest to farthest from 1526 MSRB I.

#### Michigan Dining

* Break room with microwave & fridge in 1510 MSRB I
* Market on 2nd floor of MSRB II
* JavaBlu Café in the Taubman Health Sciences library
* Café in BSRB
* UH Cafeteria
* Fields Café in Palmer Commons

#### Restaurants

* Angelo's
* Jimmy John's
* Casey's Tavern
