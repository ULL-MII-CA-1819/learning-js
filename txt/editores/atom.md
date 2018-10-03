### Pair Programming

#### Teletype for Atom

* [teletype.atom.io](https://teletype.atom.io/)
* [Collaborate in Real Time in Atom Text Editor](https://youtu.be/C_JufDsP2Ng) YouTube Video
* [Code together in real time with Teletype for Atom](http://blog.atom.io/2017/11/15/code-together-in-real-time-with-teletype-for-atom.html)

#### AtomPair

* [AtomPair](https://atom.io/packages/atom-pair)

### Atom, Git  y Github

* [GitHub and Atom](https://youtu.be/HqrkEVWBifw) YouTube Video
* [Atom and git and GitHub](https://youtu.be/sb5o2WiNb-A) YouTube video by Mr. Kennedy
* [git-plus package](https://atom.io/packages/git-plus)
* [Version Control in Atom](https://flight-manual.atom.io/using-atom/sections/version-control-in-atom/)
    <ul>
    <li>
    <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">O</kbd> - Open file on GitHub</li>
    <li>
    <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">B</kbd> - Open Blame view of file on GitHub</li>
    <li>
    <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">H</kbd> - Open History view of file on GitHub</li>
    <li>
    <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">C</kbd> - Copy the URL of the current file on GitHub to the clipboard</li>
    <li>
    <kbd class="platform-all">Alt+G</kbd> <kbd class="platform-all">R</kbd> - Branch compare on GitHub</li>
    </ul>
* [gitHub for Atom](https://github.atom.io/) package repo and [web page](https://github.atom.io/) package
* [git diff and Atom](https://youtu.be/YJ3yfQAKSzY) YouTube Video
    - [git diff package](https://atom.io/packages/git-diff)
    - [git diff tool package](https://atom.io/packages/git-diff)

### Atom Build package

Automatically build your project inside your new favorite editor, Atom.

  * <kbd>Cmd</kbd> <kbd>Alt</kbd> <kbd>B</kbd> / <kbd>Ctrl</kbd> <kbd>Alt</kbd> <kbd>B</kbd> / <kbd>F9</kbd> builds your project.

  Create a file called `.atom-build.yml` (note the inital dot):
```yml
cmd: echo Hello world
```

Save it, and press <kbd>Cmd</kbd> <kbd>Alt</kbd> <kbd>B</kbd> (OS X) / <kbd>Ctrl</kbd> <kbd>Alt</kbd> <kbd>B</kbd> (Linux/Windows)
and you should see the output of `echo Hello world`, which should be `Hello world` if all is correct.

Pick your favorite format, save that file in your project root, and specify exactly
how your project is built (example in `yml`)

#### Specify a custom build command

```yml
cmd: "<command to execute>"
name: "<name of target>"
args:
  - <argument1>
  - <argument2>
sh: true,
cwd: <current working directory for `cmd`>
env:
  VARIABLE1: "VALUE1"
  VARIABLE2: "VALUE2"
errorMatch:
  - ^regexp1$
  - ^regexp2$
warningMatch:
  - ^regexp1$
  - ^regexp2$
keymap: <keymap string>
atomCommandName: namespace:command
targets:
  extraTargetName:
      cmd: "<command to execute>"
      args:
      # (any previous options are viable here except `targets` itself)
```

Note that if `sh` is false `cmd` must only be the executable - no arguments here.  If the
executable is not in your path, either fully qualify it or specify the path
in you environment (e.g. by setting the `PATH` var appropriately on UNIX-like
systems).

If `sh` is true, it will use a shell (e.g. `/bin/sh -c`) on unix/linux, and command (`cmd /S /C`)
on windows.

### Atom {#segundo-apartado-de-este-cap-tulo}

* [Building your first Atom plugin](https://blog.github.com/2016-08-19-building-your-first-atom-plugin/)
