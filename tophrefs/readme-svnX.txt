****************************************************************
THIS STRUCTURE IS BASED ON SARAH WEBSTER'S METHOD OF MANAGING 
HER BIB FILES... IF YOU ARE USING THIS AS AN EXAMPLE YOU MIGHT 
WANT TO LOOK AT HER VERY COOL STRUCTURE INSTEAD. SEE

https://svn.lcsr.jhu.edu/dscl-papers/reference/swebrefs/main/

THIS README IS BASICALLY HERS AS WELL...

toph 2012-09-20
******************************************************************

If you are reading this in a paper checked out from the
https://svn.lcsr.jhu.edu repo, the folder that contains this readme
and the *.bib files is most likely linked to a different svn repos
(a repo for my .bib files) using the svn:externals property as
described below.

This ensures that I only have one repos for the bib files and it is
always the most recent version.

This also means that you have access to the master copy of my .bib
files. Feel free to add and correct but *please* don't delete!
Remember, it's svn, I will know who you are :-)

-Topher (though mostly Sarah's original message:) 


Very Brief svn:externals description:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

I pulled the folder containing sweb.bib into an existing svn repos
using the following commands:

svn propset svn:externals 'tophrefs https://svn.lcsr.jhu.edu/dscl-papers/reference/tophrefs/main' .

svn up

svn commit

The first command creates the external link between the folder which I
am calling tophrefs (the first 'tophrefs' in the command) and the
external svn repo. (Note the ' ' around the new folder name and the
svn link. Note the . (with a space before it) at the end of the
command.)

The second command updates from said repo.

The third command commits my changes to whatever current paper repo
I'm working in.

Now everyone who checks out this repo will get a folder with the
latest version of sweb.bib from my master repo.

NOTE: You may notice that
~~~~~~~~~~~~~~~~~~~~~~~~~~
1) You will get a message about "Fetching external item..." when doing
   updates.
2) An "X" appears next to the folder swebsrefs during an 'svn status'
   command.  Any status reports for that folder are reported below the
   regular status report under the heading "Performing stats on
   external item..."
