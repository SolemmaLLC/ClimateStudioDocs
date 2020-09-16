# ClimateStudioDocs
Read the docs documentation repository for ClimateStudio

To edit you first need to install the SPHINX package for Python (https://www.sphinx-doc.org/en/master/).

To update text or image:

(1) Get the latest version of the CS_Docs from Github

(2) Go to the folder "docs" and edit the RST file  with the same root name as the htiml file that you want to change.

(3) When you are done editing go to the root folder ClimateStudioDocs\ and type "make html" This process will start building the html pages which 
will be stored under ClimateStudioDocs\_build\html.

(4) Copy the resulting html pages to the Solemma web site under https://solemma.com/Docs/ClimateStudio/
