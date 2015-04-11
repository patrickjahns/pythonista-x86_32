Pythonista - the Docker image
=============================

Pythonista is a [Docker] image for Python developers to test their applications against
common python interpreters. The image was originaly created by ikalnitsky (see [pythonista]) for 64bit containers.
Since one of my statging servers is running on 32bit, this fork was created

[pythonista]: https://github.com/ikalnitsky/pythonista
[Docker]: https://docker.com/


About Image
-----------

* **OS** - Debian Jessie (Testing)
* **CPython** - 2.6.9 / 2.7.9 / 3.2.6 / 3.3.6 / 3.4.4
* **PyPy** - PyPy 2.5.0 (based on 2.7.8) / PyPy3 2.4.0 (based on 3.2.5)
* **Env** - pip, virtualenv, tox


How To Use?
-----------

Pythonista image is available on [Docker Hub], so you can easily `pull`
it by means `docker` client:

    $ [sudo] docker pull patrickjahns/pythonista-x86_32

If you want to enter a bash session, just do it how you did it for
another containers:

    $ [sudo] docker run -t -i patrickjahns/pythonista-x86_32 bash

and enjoy `bash` session within container.

[Docker Hub]: https://hub.docker.com/


Unit Tests
----------

It's very convenient to run unit tests inside Pythonista container because
you can run it using different Python interpreters. For example, with [tox]
the command might look like:

    $ [sudo] docker run -v /path/to/src/:/src -w /src patrickjahns/pythonista-x86_32 tox

[tox]: https://tox.readthedocs.org/


Feedback
--------

It's important for me to get user's feedback, so please don't hesitate
to suggest improvements or report bugs via [GitHub Issue].

[GitHub Issue]: https://github.com/patrickjahns/pythonista-x86_32/issues

