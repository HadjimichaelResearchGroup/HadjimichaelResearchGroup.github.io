## Instructions on contributing to the lab manual

This lab manual is built using [Jupyter Books](https://jupyterbook.org/en/stable/intro.html), a Python-based static site
generator built around Markdown and Jupyter Notebooks.

### Download up-to-date repository
- If you aren't familiar with git & GitHub, first see [this section of the lab manual](https://github.com/HadjimichaelResearchGroup/HadjimichaelResearchGroup.github.io/blob/main/docs/Training/GitAndGithub.md) for an introduction and installation instructions.
- If you don't already have the lab manual repo, clone it from [our GitHub page]. Stay on the ``main`` branch.
- If you already have the repo locally, make sure it is up to date by doing a ``git pull``.

### To create or edit a Markdown-based page
- Most of the pages in this manual (including this one) are built using Markdown (.md file endings). Markdown provides a simple and powerful way to create organized "fancy" rendered documents using only a text editor. See [this cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) and many other resources on the web.
- An example Markdown-based page for this site can be found at ``docs/Contributing/mdExample.md``.
- To edit an existing Markdown page in the lab manual, simply edit the .md file in your favorite text editor or Python IDE. If you embed any images in the .md file, add the images to the same directory.
- To create a new Markdown-based page in the lab manual, just create and fill in a new .md file. This file should be placed at the appropriate location within the nested directory structure. For example, a new page on a software called MySoft could be created as ``docs/Software/MySoft.md``.


### Committing changes to the remote repository
- Once you are satisfied with your changes locally, follow standard git protocols to ``add``, ``commit``, and ``push`` the changes to the remote repo on GitHub. 
- We use GitHub Actions to automatically rebuild the Jupyter Book and redeploy the updated website to GitHub Pages each time a new commit is pushed to the main branch of the remote GitHub repo. The GitHub Action script is found at ``.github/workflows/deploy-book.yml``, along with several other scripts it deploys in the same directory.
- **If your changes involved Jupyter Notebooks, you must include ``[ipynb]`` in the commit message**. This will trigger additional actions within the GitHub Action deployment script to install Python and R packages on the remote machine and rerun all Jupyter Notebooks. If you don't include ``[ipynb]`` in the commit message, the changes to any Jupyter Notebook-based pages will not be registered. This does not apply to Markdown-based pages, which should always be updated automatically regardless of commit message.
- After pushing your change, **verify that the [GitHub Action](https://github.com/HadjimichaelResearchGroup/HadjimichaelResearchGroup.github.io/actions) completes with no errors,** and then **verify that your changes look correct and didn't break anything else on the [lab manual website](https://HadjimichaelResearchGroup.github.io/intro.html)**. If you refresh the website and don't see your new changes, you may need to clear your browser cache.
- **If you are creating a new section in this lab manual,** you will need to complete three things. first, create a new directory to put your file in, and write your .md file there. Next, you'll need to create a **blank** file with the **same name as the new directory.** This will ensure your file generates property in the manual. Next, you'll need to edit the table of contents. This exists in the _toc.yml file. Copy the existing file structure by listing your new directory as a file name. Then your section must be named DirectoryName.md/NewFileName.md.
