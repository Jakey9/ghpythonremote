*********
Changelog
*********

1.2.1 (2019-07-24)
------------------

Fix
^^^
- Cleanup examples directory, and fix missing file at installation (#26).
- Update logger names in .ghuser file

1.2.0 (2019-07-08)
------------------

New
^^^
- Now fully compatible with Rhino 6.

Changes
^^^^^^^
- Revert using a special RPyC distribution, now explicitly using upstream.
- Upgrade to RPyC 4.1.0.
- Hide rpyc behind a special ghpythonremote import. ``rpyc.utils`` functions ``deliver`` and ``obtain`` are available as ``ghpythonremote.deliver`` and ``ghpythonremote.obtain``; ``rpyc`` should be imported with ``from ghpythonremote import rpyc`` if ever needed.
- Expand the environment path in CPython subprocess, trying to match what conda would do, helping Numpy finds its DLLs.

Fix
^^^
- Repair pip install command on recent pip with pip.main deprecated.
- Repair incompatibilities with IronPython 2.7.0.
- Repair incompatibilities with RPyC 4.1.0, using monkey-patched compatibilty fixes for IronPython.
- Remove unnecessary pip install parameters.

1.1.4 (2018-02-28)
------------------

Fix
^^^
- Stop using the `exposed` prefix to remote attributes, per rpyc v4.

1.1.3 (2018-02-27)
------------------

Fix
^^^
- Rename ``async`` import from rpyc to ``async_``.
- Bump rpyc version to pilcru/rpyc@3.4.6 to fix IronPython 2.7.0 dump bytes issues.

1.1.2 (2018-02-23)
------------------

Fix
^^^
- Use https file location for the dependencies, to remove the need for git when installing.

1.1.0 (2018-02-14)
------------------

New
^^^
- Documented ``obtain`` and ``deliver`` features of rpyc to speedup remote array-like objects creation and retrieval.

Changes
^^^^^^^
- Use the v4.0.0 pre-release of rpyc to fix IronPython <-> CPython ``str`` unpickling issues.
- Improve error messages when connection is lost.

Fix
^^^
- Repair the GH to python example, where argument passing (for the port configuration) was broken.

1.0.4 (2017-10-06)
------------------

Fix
^^^
- Fix quote escaping issue in pip install command for IronPython.

1.0.3 (2017-10-02)
------------------

First public release.
