# git-learn

One n00b coder's journey from the land of Doy to 1337-land.

2018-04-13T17:20:50-0700
Unexpectedly, I could not read in a shell command.  The following failed:

    :r !date --iso-8601=seconds

I don't know yet why it failed; but I soon shall.

Let me try again (so I can crib the errmsg).  Here's the error message:

    ~/Documents/GitHub/git-learn/README.md[+] [unix] (17:14 13/04/2018)
        1 [main] vim 7148 child_info_fork::abort:
	C:\Users\UserName\AppData\Local\GitHub\PortableGit_[long-hexadecimal-hash]\usr\bin\msys-ssp-0.dll:
	Loaded to different address: parent(0x1E0000) != child(0xD0000)
        
	Cannot fork
        
	E485: Can't read file /tmp/v4D588c/2

So basically, even though I think I'm in the ~/Documents/GitHub/git-learn dir, 
for some reason either git-bash or its instance of Vim believes that I'm in
~/AppData/Local/blah-blah-blah.  Ok, it doesn't necessarily think that's where 
we are; but that's where the shell is trying to send the result of the date cmd?

Okay, that's something to read about on Stack Exchange later.  For now, I'm 
learning how local Git repos work with remote repos on GitHub.com.

2018-04-13T17:40:01-0700
I wrote this file locally; so it's "modified".  Next, it needs to be "staged"
so it can then be "committed".
(As per https://git-scm.com/book/en/v2/Getting-Started-Git-Basics )

I was expecting there to be some way on the web client to pull in the modified
file, but I didn't see one.  Maybe after it's been locally staged?  Hmm, I
probably have some fundamental misunderstanding.  Let's see, I get this error
when, on the web client, I click the "Open in local" link:

	This address wasn't understood.  The following
	protocol (x-github-client) isn't associated with
	any program or is not allowed in this context.

So, I can make that association in the "helper programs" section; but I guess
that's something else I'll defer until later.  Meanwhile, it looks like I can
use the GUI client to "publish" repos and commits to my GitHub.com profile; 
but there might not be a way, from the www client, to suck in changes that
are on my laptop.  (Thinking about it, that avoids a security risk, right?)

Side note:  Git-bash, y u no tmux?
Also:  How do I get rid of the .swp file in the repo?

2018-11-08
Argh.  Starting from scratch, essentially.
