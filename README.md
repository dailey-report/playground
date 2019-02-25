Playground Repository
=====================

Change for testing `git revert`.

Testing and experimentation with source control using git and github.

## Overview

If this was a project of significant size, a longer description of the
purpose and details of the project would be here.

This line added during rebase experimentation.

### Sub-Topic

This is a sub-topic section.

### Additional Sub-Topic

This is an additional sub-topic section.  Everything from here down is
just example markdown for reference.

### IPC

All IPC is implemented to conform with the
[Inter-Process Communications Specification](https://docs.google.com/document/d/blah-blah-blah)

### Threads

All IPC services, queue controllers and the USB service run in isolated
threads.  Some of these services require other services or queue controllers
to be running, before they can be started.  This requires control over the
order of startup and confirmation that a started thread is actually ready to
start processing events / requests.  This requirement is fulfilled by using a
synchronized thread starting function....
[synced_thread_start()](https://github.com/dailey-report/playground/blob/master/src/some_source_file.c#L39)
to start each thread only after the previously started thread has reported it
is ready.

#### Sub-sub Topic with Bullets
* gnu build system (gcc, pkg-config, etc)
* cunit -- for unit testing
* all libraries referenced by .h headers in project source
  * glib 2.54.3
  * czmq 4.1.1

#### Documentation
* doxygen -- for documentation generation (documentation may be generated
without all of the following installed.  see http://www.doxygen.org/index.html
for more information)
  * cmake
  * Qt GUI toolkit
  * a LaTeX distribution such as TeX Live (example packages for ubuntu:)
    * texlive-base
    * texlive-font-utils
    * texlive-recommended
    * texlive-latex-extra
  * FLEX
  * bison
  * graphviz
  * ghostscript

## Additional Information

### Style

Coding style in this project conforms to the
[GLib C Coding Style](https://developer.gnome.org/programming-guidelines/stable/c-coding-style.html.en).
Where GLib's style guide offers no preference between GNU and Linux kernel
style, Linux kernel style is preferred.  Most importantly, when contributing
to this project, please remember the golden rule of code style: **"check the
surrounding code and try to imitate it"**.

### Important Libraries

This project makes extensive use of GLib and ØMQ.  It may prove useful to be familiar
with the following:

* https://developer.gnome.org/glib/2.54/
* https://developer.gnome.org/glib/stable/glib-Strings.html
* https://developer.gnome.org/glib/stable/glib-Arrays.html
* https://developer.gnome.org/programming-guidelines/stable/logging.html.en
* http://zeromq.org/

### Important Concepts

[Sequential Consistency](http://preshing.com/20120612/an-introduction-to-lock-free-programming/index.html#sequential-consistency "Sequential Consistency Intro")

[GLib Main Event Loop](https://developer.gnome.org/glib/stable/glib-The-Main-Event-Loop.html "GLib: The Main Event Loop")

[Multithreading with ØMQ](http://zguide.zeromq.org/page:all#Multithreading-with-ZeroMQ "Multithreading with ØMQ")

