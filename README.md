# omnifocus-inbox

This simple program lets you quickly add tasks to your OmniFocus inbox via the command line. 

In order for it to work, you need to have set up [OmniFocus Mail Drop](https://support.omnigroup.com/omnifocus-mail-drop). This provides you with a special email address to which you can send new tasks. You can provide this address in turn to this program's configuration file (`~/.inbox`).

If you want a more complete command-line solution for OmniFocus, see [OTask](https://github.com/ttscoff/OTask). I wrote this much simpler alternative in part because I wanted something that would work specifically when the OmniFocus application is not running. (Also, I couldn't get OTask to compile, and I don't know Ruby too well. But that's not its problem.)

## Setup

To install this program's dependencies, run this command while in the same directory as this repository's `cpanfile`:

    curl -fsSL https://cpanmin.us | perl - --installdeps .
    
(If you already have _cpanm_ installed, you can just run `cpanm --installdeps .` instead.)

Then copy `.inbox` into your home directory and update it appropriately.

You can also copy the `inbox` executable into /usr/local/bin or whatever if you want.

## Usage

After running the program, type the task's name when prompted, terminating it with a newline.

Then type the task's notes when prompted, ending it with an EOT (i.e. Ctrl-D). If you don't want to include any notes, just EOT immediately.

## Sample execution

    $ inbox
    Task:
    Pay the yak-shaving bill
    
    Notes:
    The bill is on the kitchen table.
    
    Sending to OmniFocus...
    Done.

## Did it work?

If it didn't give you an error message, yeah, probably. Launch OmniFocus and re-sync; the task should show up in your inbox.

## Author

Jason McIntosh (jmac@jmac.org)
