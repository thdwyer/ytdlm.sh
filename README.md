This is best viewed using the [Raw] button near the top of this panel.
It allows the original formatting to be preserved.

This was written for Linux Mint 21.x and 22  It should work in most distros
as long as you can install yt-dlp.

This is a wrapper for yt-dlp ehich should be available via software manager
(in Mint at least)

Keep in mind that youtube is constantly coming up with ways to disable any
utility that is capable of downloading from a url pointing to one of it's
files.

The author of yt-dlp is pretty much on top of Youtube's attempts to prevent
downloadin anything it considers an asset.  yt-dlp is updated often enough
that if you use this script or run 'sudo yt-dlp -U' it can be updated at will.

I have it installed in the Cinnamon->Internet menu as an application.
I'll explain how to do this, but first install the script.
Extract it from the .tar.gz file and copy it to your ~/home/bin directory.
  (that is /home/[user]/bin/)
If you don't have a bin directory, In a terminal, type 'cd' (no parameters)
and that will take you to your home directory. type 'ls -d ./bin'. If you
see 'ls: cannot access 'bin': No such file or directory', you definitely
don't have it.  To make the directory, type 'md ./bin' and the directory
will be created. Now type 'cd bin'.  In order to have the bin directory
in your PATH environment variable, it will happen if you log out or restart
until then you will need to address the script directly from within the bin
directory by typing './ytdlm.sh' which tells the terminal to run that script
that is in the current './' directly

In your filebrowser [nemo, thunar etc..] copy the extracted ytdlm.sh script
to your bin directory.  To make it executable go back to the terminal and
type 'chmod +x ytdlm.sh', and it's ready to run.

NOTE: I cannot explain how to do any of the following for other than
the Mint Cinnamon environment.  If you use Mate or XFCE you'll need
to use the following instructions as a guide only.
If anyone who uses either of the other Mint releases wants to, give me
a documeted means of inserting a new menu item and I'll include it with the
other files.
Inserting a command into the Cinnamon menu is trivial and if you've done it
before you can skip over this section.  For anyone who is not familiar with
inserting/creating a menu item follow along
Open the menu by using a <Right click> on the Cinnamon menu Icon,
the leftmost Icon on the panel.  A selection box will pop up.  select the
top option <Edit Menu>. In the middle pane where the two columns are
[Show  Item] select the menu section you'd prefer to have the script entry
placed in.  I chose [Internet].
On the right pane, select the second from top item [New Item].

A new dialog box will pop up. this is where you enter the details of
your menu entry.

The top line labelled [Name:] is what you will call your program
  I used 'Youtube Downloader' (without the quotes)
The second line labelled [Command:] is the full path to the program
  I used '/home/[user]/bin/ytdlm.sh' replace [user] with your login name
The third line labelled [Comment:] is a brief description of what the
  program does
  I used 'Download from Youtube URLs'
To enable it to run it has to be called from a shell (terminal)
  enable this by ticking the checkbox labelled [Launch inTerminal?]

Click [OK] on the dialog box
Click [Close] on the [MainMenu] window

Open the cinnamon menu with a <Left click>
Browse to the [Internet] menu (or whichever you chose)
Move the cursor to the right pane where the applications are located
Open the [Youtube Downloader] application with a <Left click>

If it opens all you have to do is install yt-dlp if you haven't already,
and you're finished.

If you don't alread have a directory nsmrd 'YouTube' in your home directory
The script will create it for you.  This is where all downloaded files will 
be put.
Ther is another function tha ytdlm.sh can perform, and that is a list of
URLs, single files or playlists you supply can be downloaded all at once.
Create a file in the YouTube directory named 'urls.txt'  Paste each URL 
into the file on sucessive lines and once you use Option 9 in the menu
downloding will start.

This application does not rely on any window components so you can run it
from a remote terminal ssh'ed to the host where it's installed
