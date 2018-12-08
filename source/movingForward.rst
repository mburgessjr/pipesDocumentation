Moving Forward
===============================

How the Documentation Reached Here
-------------------------------

The pipes documentation was written through a simple program called Sphinx. 
This program can be used to automatically create documentation via the docstrings of program files.
However, it can also be used to easily convert reStructuredText (.rst) files into webpages.
In the case of pipes, the latter technique was employed.
The webpage seen here is comprised of a handful of .rst files designated in an index file.
All of these files can be seen on the `GitHub page`_ (more so, they are individually described in a README on the frontpage of the repository).
The webpage itself was conceived by tying these files to ReadTheDocs, as you can see.
Thus, this page can be easily edited via the `GitHub page`_

.. _Github page: https://github.com/mburgessjr/pipesDocumentation


Best Ways to Edit the Documentation
-------------------------------

If one wants to edit the documentation of pipes, they can easily do so via its `GitHub page`_.
The process really only takes a few steps.

1. Identify Edit
	- Before changes can be made, the editor should figure out what exactly they want to edit in the documentation
	- This could mean adding a whole class, rearranging the site's index, or fixing a typo
	
2. Go to GitHub:
	- After deciding what to fix, the editor should head to the `GitHub page`
	- Here, the editor can commit changes to .rst files accordingly (assuming the editor is a collaborator)
	- All significant webpage text files are in the folder::
	
		./source
	
3. How to Edit .RST:
	- The text files that comprise this webpage are all reStructuredText files
	- These sorts of files can be very confusing to someone who has never used them before
	- However, they are very helpful in applications such as this
	- Quite simple, main headers can be made using an underline of equal signs::
	
		===============
		
	- Section headers can be maded with an underline of dashes::
	
		---------------
	
	- These headers will appear a large and bold on the actual webpage
	- A line break can be inserted with the symbol::
	
		|
	
	- To add internal links, a reference point must be placed above the target header as such::
	
		.. _linkToHeader:
		
		Header
		-----------------
		
	- Then, the Header can be referenced elsewhere like so::
	
		The reader can now visit this :ref:`section <linkToHeader>`.
		
	- Here, only the word "section" will show, not the name "linkToHeader".
	- Clicking on the word "section" sends the user to "Header" because of the "linkToHeader"
	- It should be noted that links are not case sensitive, meaning that the links "a" and "A" will be viewed as the same and confuse the program
	- To fix this, it is suggested to change the "A" link to "aa"
	- To add external links, the link must be defined under the section of text it appears like this::
	
		The reader can click here to visit `this site`_.
		
		.. _this link: https://domain.invalid/
		
	- For more methods of changing the text, see the `Sphinx documentation`_

4. Apply Edits to Webpage:
	- From here, all there is to do is tie the fresh GitHub repository to `ReadTheDocs`_
	- To do so, first head to `ReadTheDocs`_ and log in
	- Hopefully, your account is already connected to your GitHub account
	- If not, you must sign into `ReadTheDocs`_ with GitHub which can be done `here`_ by clicking::
	
		Sign In With GitHub
	
	- Now, all there is to do is `import the documentation`_
	- You should be able to simply click on the pipesDocumentation repository and create the site
	- If not, head back to the `GitHub page`_ and fork the repository
	- After importing, just follow the steps and build the website version
	- It should be noted that if the editor is not listed as a maintainer on ReadTheDocs, they will likely have to send the documentation to a new domain but the content will remain
	
- If any of the above is confusing, the last 5 minutes of this `video`_ or this `page`_ should be much more helpful in walking you through the process

	
.. _video: https://www.youtube.com/watch?v=oJsUvBQyHBs&feature=youtu.be

.. _page: https://docs.readthedocs.io/en/latest/intro/import-guide.html
	
.. _import the documentation: https://readthedocs.org/dashboard/import/
	
.. _here: https://readthedocs.org/accounts/signup/	
	
.. _ReadTheDocs: https://readthedocs.org/
	
.. _Sphinx documentation: http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html#external-links

.. _Github page: https://github.com/mburgessjr/pipesDocumentation



What Else Requires Explanation
-------------------------------
The reason the above instructions are provided is because the documentation on this site is most certainly not complete.
The pipes module is long and complex, thus not nearly everything has been outlined.
However, there are certain things that are known to require more attention.
Most simply, if an editor would like to upgrade the documentation, he or she should scroll through the files and find things that neither them or the documentation understands, then resolve and document this.
This is of course difficult.
Personally, I would start with the file::
	:ref:`setupandrun.cpp`.
Once all files are understood, a complex map can be made that depicts the interconnections of all of them and the Object Map can be updated

All of the below files require attention:
	- :ref:`driver.cpp`
	- :ref:`f_blas_lapack.h`
	- :ref:`justrunit.cpp`
	- :ref:`libcla.c`
	- :ref:`mp_mat.h`
	- :ref:`mp_mat.cpp`
	- :ref:`mp_mat_aux.cpp`
	- :ref:`mp_mat_double.cpp`
	- :ref:`newton.cpp`
	- :ref:`optimizeit.cpp`
	- :ref:`real_def.h`
	- :ref:`ridders.h`
	- :ref:`setup.py`
	- :ref:`setupandrun.cpp`
	- :ref:`smarterputittogether.py`
	- :ref:`steady_states.py`
	- :ref:`str_double.h`
	- :ref:`str_double.cpp`
	- :ref:`top.h`
	- :ref:`writeit.py`
	- :ref:`levmar.cpp`









