# ClimateStudioDocs
Read the docs documentation repository for ClimateStudio

Requirements
To edit you first need to install the SPHINX package for Python (https://www.sphinx-doc.org/en/master/).
Install python - make sure to check the path installation. pip installs from command line, not python interpreter.

pip install -U -- sphinx

pip install recommonmark

pip install ipython

pip install matplotlib

pip install sphinx_rtd_theme

To update text or image:

(1) Get the latest version of the CS_Docs from Github

(2) Go to the folder "docs" and edit the RST file  with the same root name as the html file that you want to change.

(3) When you are done editing go to the root folder ClimateStudioDocs\ and type "make html" This process will start building the html pages which 
will be stored under ClimateStudioDocs\_build\html.

(4) Copy the resulting html pages to the ClimateStudioDocs web site under https://www.climatestudiodocs.com
