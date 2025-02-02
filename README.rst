Code-Sharing-Python
===================

A repository for storing Python scripts and tools that may be useful for others.


Adding scripts and tools
------------------------

If you have a script or a tool (e.g. function) that you think may be useful
for others, you can add it to this repository. To do this, you should follow
the below steps. There will also be an accompanying video describing the
process.


#. Fork this repository.
#. Clone your forked repository.
#. On the cloned repo (locally) create and checkout a new git branch
   e.g. newbranch.

#. Choose where to put your script/tool in the folder directory.
    - If it is a script, place the script in the relevant folder in
      ``./scripts``.
    - If it is a tool such as a function or class, place it in the
      relevant folder in ``./tools``.
    - For example, if you have a script that is RTDC-related, put it
      in ``./scripts/rtdc_scripts``
#. Give your script/tool a short but desciptive name.

#. Create a ``requirements.txt`` file and place it in the same folder
   as your new script/tool. Use ``./Examples/requirements.txt`` as
   a template.

#. Make sure the script/tool runs by testing it within a venv (virtual environment).
    - ``cd`` to the folder containing your new script/tool.
    - Run ``python -m venv .venv``
    - On windows run ``.venv\Scripts\activate``. On mac run
      ``source .venv/bin/activate``
    - Install the script's requirements by running
      ``pip install -r requirements.txt``
    - Run your script with ``python script_name.py``
    - If the script executes as expected, run ``pip freeze``. This will
      print out all the current packages in your venv. Use the relevant
      package version numbers as minimal versions for your
      ``requirements.txt`` file. See the ``./Examples/requirements.txt``
      file as an example.

#. ``cd`` back to the source folder (Code-Sharing-Python).
#. Check the code syntax with flake8.
    - Run ``flake8 .``
    - Fix any syntax errors that are output. If this command returns nothing,
      then there are no mistakes.
#. Host an example dataset somewhere remotely (not in the repo!)
    - For RTDC files, DCOR is a great option for remote hosting of data.

#. Now you have to upload the file to the repository using git
    - Run the following:
        - ``git add -A``
        - ``git commit short-description-of-addition``
        - ``git push -u origin newbranch``

#. Create a pull request on the `Code-Sharing-Python <https://github.com/GuckLab/Code-Sharing-Python/pulls>`_ repo
    - The maintainers will discuss the code and see if anything can be improved.
    - When the code is ready, the newbranch will be merged into the main branch
      and now is useable by anyone.
