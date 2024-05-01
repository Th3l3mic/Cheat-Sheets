<h1>Linux priv escalation</h1>
-------------------------------------------------------
<p>Privilege escalation is the act of gaining higher levels of access or privileges on a system or network than were originally intended. This can be achieved through various means, such as exploiting vulnerabilities in software, gaining access to credentials or using social engineering tactics.Also a few ways to manually escalate privileges, of course, these are not all, but the ones I most commonly use.</p>

Enumeration is the key!!! Let's see what are we dealing with!

Useful commands:

<code>hostname</code> - provide host name :)

<code>uname -a</code> -kernel info, 

<code>cat /etc/issue</code> - for OS version,

<code>ps -A </code>- all running processes,

<code>ps axjf</code> - process tree,

<code>ps aux</code> - processess with users,

<code>groups</code> - list groups,

<code>cat /etc/passwd | cut -d ":" -f 1</code>- with delimiter shows only users on current machine,

<code>history</code> - maybe some sensitive info? ;)

<code>find . -name flag1.txt</code>- most popular command in CTF's ;)

<code>find / -type f -perm 0777</code> -shows files with full permissions,


Now it's time to give us full power. Privesc in Linux could be escalated in many ways, below four of them that I use  mostly in CTF's:

SUDO
<code>sudo -l</code> -shows what command could be run with sudo without password,

SUID
<code>find / -perm -u=s -type f 2>/dev/null</code> - show files that can be run with root permission/ SUID (Set Owner User ID)

Capabilities
<code>getcap -r / 2>/dev/null</code> - its very similiar to SUID; gives root privileges to a process or a binary,

When one of the above commands gives us the desired results, we go to gtfobins.com - the best place to check for privilege escalations! There we could find potentially working method to give us root!

Cron Jobs
<code>cat /etc/crontab</code> - default run scheduled process/binary with owner priv's, when we find come job that could potentially edit, that's the case!

As I stated before these are not all availible methods, but probably the easiest and I use it a lot in many CTF challenges.
<p>T.</p>
