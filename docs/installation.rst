Installation
============

To install or upgrade to the latest version::

    pip install -U intspan

On some systems, you may need to use ``pip2`` to install under Python 2, or
``pip3`` to install under Python 3. You may also need to prefix these commands
with ``sudo`` to authorize installation. In environments without super-user
privileges, you may want to use ``pip``'s ``--user`` option, to install only
for a single user, rather than system-wide. Finally, in cases where ``pip`` is
not well-configured to match a specific Python interpreter you want to use, a
useful fallback::

    python3.6 -m pip install -U intspan


Testing
-------

``intspan`` is tested twice before each release--once on the developer's workstation,
and once by the Travis CI continuous integration service. If you'd like
to also run the module tests locally, you'll need to install
``pytest`` and ``tox``.  For full testing, you will also need ``pytest-cov``
and ``coverage``. Then run one of these commands::

    tox                # normal test run, across all currently-supported versions
    tox -e py27        # run for a environment only (e.g. py27)
    tox -c toxcov.ini  # run full coverage tests
