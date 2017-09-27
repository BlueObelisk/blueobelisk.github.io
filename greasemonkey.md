[TOC]

# Userscripts

**[For the impatient, this is the direct link to the download page**"&gt;**For the impatient, this is the direct link to the download page**](http://blueobelisk.svn.sf.net/svnroot/blueobelisk/userscripts/trunk/)

Using JavaScript and/or Greasemonkey, it's possible to add a lot of value to existing web pages. JavaScript is a scripting language that runs in a web browser and which can alter the html of the web page you're viewing (for example). This means that information from other web pages, or from a web service, can be added to a particular web page. Greasemonkey is a Firefox extension that can run a Javascript program automatically on pages that you visit. It also contains additional JavaScript functions for common tasks. 

**For more information see our paper:** EL Willighagen, NM O'Boyle, H Gopalakrishnan, D Jiao, R Guha, C Steinbeck, DJ Wild. [Userscripts for the Life Sciences](http://www.biomedcentral.com/1471-2105/8/487). _BMC Bioinformatics_, **2007**, _8_, 487. 

In the examples below, we show how it is possible to identify PDB codes contained in the text of normal web pages and to add a link beside each PDB code that displays the protein structure in Jmol. A more sophisticated example identifies DOIs on a page, looks them up on Chemical Blogspace, and adds a link if there are any blogs that discuss that paper. 

The first step though is to set up Greasemonkey: 

  1. Install Firefox on Windows/Linux/whatever 
  2. Install [Greasemonkey](http://www.greasespot.net)
  3. Restart Firefox. You should see a little monkey grinning in the bottom right corner. You can click on this to toggle Greasemonkey on/off. 

To give feedback on any of these scripts, you can use the Comment facility on the script download page. 

### Annotate PDB codes with links to 'FirstGlance in Jmol'

This one's by Noel, and involves simple pattern-matching of the text of the web page. 

  1. Install the PDB-Jmol Greasemonkey Script from either [Userscripts.org](http://userscripts.org/scripts/show/8033) or our [SVN Repository](http://blueobelisk.svn.sf.net/svnroot/blueobelisk/userscripts/trunk/PDBJmol.user.js). 
  2. Look at the PDB codes on [this page](http://www.ccdc.cam.ac.uk/products/life_sciences/validate/gold_validation/astex/index.php). They should all have links to Jmol beside them. 

Notes: 

  * Weird things happen when editing a wiki entry containing PDB codes as the wiki source is transformed by the Greasemonkey script also if you use Preview. The workaround is to turn Greasemonkey off if you see this happening. 

### Sechemtic: Annotate CAS number, SMILES and InChI codes with links

This script by Egon adds links to CAS numbers, SMILES strings and InChI codes. It requires web pages to use standard HTML markup to indicate that some text is a CAS number, SMILES or InChI code. You can install the script from [here](http://blueobelisk.svn.sf.net/svnroot/blueobelisk/userscripts/trunk/SechemticWeb.user.js). 

A full description plus a lot of interesting discussion can be found in two blog posts of Egon: [http://chem-bla-ics.blogspot.com/2006.../smiles-cas-and-inchi-in-blogs.html](http://chem-bla-ics.blogspot.com/2006/12/smiles-cas-and-inchi-in-blogs.html), [http://chem-bla-ics.blogspot.com/2006.../chemistry-in-html-greasemonkey-again.html](http://chem-bla-ics.blogspot.com/2006/12/chemistry-in-html-greasemonkey-again.html). 

Notes: 

  * A possible extension is a popup 2D structure of the chemical floating with the mouse when you mouseover a chemical name. This will require fetching 2D images from PubMed or [CSLS](http://cactus.nci.nih.gov/cgi-bin/lookup/search) or a web-serviced [Generated Database of Chemical Space](http://www.dcb.unibe.ch/groups/reymond/). (These links taken from [http://www.chembiogrid.org/related/re.../databases.html](http://www.chembiogrid.org/related/resources/databases.html).) It might even be possible to get 3D coordinates for things from Rajarshi's [Pub3D](http://rguha.ath.cx/~rguha/p3d/). 

### Add quotes from Postgenomic and Chemical blogspace to DOIs

This script is a major extension of the [Postgenomic.com](http://http://www.postgenomic.com/) script of Pedro Beltrão ([http://pbeltrao.blogspot.com/2006/05/postgenomics-script-for-firefox-i-am...](http://pbeltrao.blogspot.com/2006/05/postgenomics-script-for-firefox-i-am.html), [http://www.nodalpoint.org/2006/05/16/postgenomic_greasemonkey_script...](http://www.nodalpoint.org/2006/05/16/postgenomic_greasemonkey_script), [http://wiki.nodalpoint.org/projects_postgenomic...](http://wiki.nodalpoint.org/projects_postgenomic)). 

  1. Install the [PostGenomic and Chemical Blogspace Greasemonkey Script](http://userscripts.org/scripts/show/8939)
  2. Go to the [Nature Table of Contents](http://www.nature.com/nature/journal/v446/n7139/index.html#cy). You should see articles which have been commented on by Chemistry and Biology bloggers. 
  3. You can click on the 'Cb' or 'Pg' logo to bring you to the Chemical Blogspace paper for that paper, or you can wait for the popup of blog posts and click on a link to bring you directly to a particular blog post. 
  4. Under "Tools/Greasemonkey/User Script Commands" you can choose whether to include blogs from PostGenomic or Chemical Blogspace. 
  5. For more discussion on the uses/consequences of this script, see these blog posts: [1](http://baoilleach.blogspot.com/2007/04/add-quotes-from-postgenomic-and.html), [2](http://baoilleach.blogspot.com/2007/04/correctionretraction-notice.html), [3](http://baoilleach.blogspot.com/2007/05/supporting-information-available-as.html). 
[[img src=CBandPG.png]]

Notes: 

  * When first installed, the script runs only on particular journal websites. You can add more web sites (or even "*" for all URLs) in the script's settings under Tools/Greasemonkey. 
  * Neither ScienceDirect, PubMed, nor Science put the DOI on their TOC pages, so the script currently cannot be extended to these sites. 
  * All credit to [overLIB](http://www.bosrup.com/web/overlib/) for the popups. 

### Add quotes from Postgenomic and Chemical blogspace to molecules

  1. Install the [Add Quotes to Molecules Greasemonkey Script](http://userscripts.org/scripts/show/9002)
  2. See Egon's blog for a [full discussion](http://chem-bla-ics.blogspot.com/2007/05/cb-comments-for-inchis.html)

### Add to Connotea from Journal websites

  1. Install the [Add to Connotea Greasemonkey Script](http://userscripts.org/scripts/show/9526)
  2. See Noel's blog for a [full discussion](http://baoilleach.blogspot.com/search/label/Add%20to%20Connotea)

### Add 3D structures to PubChem

  1. Install the script by clicking on the following link: [3DStructureView.user.js](http://blueobelisk.svn.sf.net/svnroot/blueobelisk/userscripts/trunk/3DStructureView.user.js). Then click "Install". 
  2. Whenever you do a PubChem search for a compound, you will see a link to "View 3D" structure and also "Download" the same in SDF format. 

For more information or any queries/suggestions regarding the script please contact Harini Gopalakrishnan at Indiana University. 

### Markup chemical content using OSCAR3

This is a userscript that can help you find and highlight chemical terms in a web page in the Firefox web browser. 

In order to use this application, please follow these steps: 

  1. Install Firefox GreaseMonkey add-on as described at the top of this page. 
  2. Click on the following link to install: [ChemGM.user.js](http://blueobelisk.svn.sf.net/svnroot/blueobelisk/userscripts/trunk/ChemGM.user.js). Choose "Install". 
  3. Open any web page. At the top of the page, click on the "Highlight" button. 
  4. In a minute or so, a window will popup and tell you the number of terms found. 
  5. Click on "Ok". 
  6. Wait while terms are being highlighted. 
  7. After all terms are highlighted, you can click on the "PubChem", or "2D" link following the term to either search it in pubchem or view the 2D structure (if there is one). 

For questions, please contact David Jiao at Indiana University. 

# [Download the Latest Versions](http://blueobelisk.svn.sf.net/svnroot/blueobelisk/userscripts/trunk/)

The latest versions of these scripts are [available from the SVN repository of the Blue Obelisk project](http://blueobelisk.svn.sf.net/svnroot/blueobelisk/userscripts/trunk/). 
