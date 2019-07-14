# Viewing
The content can be viewed by the following means:

## Viewing in a browser
This content is not yet available to be viewed on a browser via the world wide web, so in order to view with a browser, the content must be first be copied (i.e. downloaded) onto your own computer. 

### 1) Downloading a copy of the repository
The following options are available to download the content.

#### a) Option 1 - download a 'snapshot'
To download a point-in-time snapshot: 
 1. Go back to the [home page](https://github.com/AuDigitalHealth/ci-fhir-r4) of this repository 
 2. Click on the green `Clone or download` button
 3. Click on `Download ZIP`
 4. Use the standard dialog box to save the zip file to the location of your choice
 5. Use your preferred archiving software (such as [WinZip](https://www.winzip.com/win/en/) or [7-Zip](https://www.7-zip.org/) etc) to extract the files from the zip (ie 'unzipping')
 6. The repository is then ready to be viewed (see '2. Opening the content in a browser' below)

The disadvantage with this snapshot is that the content is only up-to-date at the moment of your download action. Any later updates to the repository are therefore not seen, unless a new subsequent download is done. A more advanced option to allow updates to be seen is to "clone" the repository.

#### b) Option 2 - cloning (advanced)
This option uses the capability of the [git version control system](https://git-scm.com/) to readily obtain any updates to this repository on your computer. It does presume a basic understanding of git, which is outside the scope of this readme.  Essentially, 
1. Go back to the [home page](https://github.com/AuDigitalHealth/ci-fhir-r4) of this repository 
2. Click on the green `Clone or download` button
3. Click in the popup box containing the URL of the repository and copy it (which is https://github.com/AuDigitalHealth/ci-fhir-r4.git)
4. Use your preferred git software (such as [SourceTree](https://www.sourcetreeapp.com/), [GitKraken](https://www.gitkraken.com/git-client) or the git command line tool) to clone this repository to a location on your computer
5. The repository is then ready to be viewed (see '2. Opening the content in a browser' below)

For further information on cloning a repository, refer to [this GitHub help page](https://help.github.com/en/articles/cloning-a-repository).

### 2. Opening the content in a browser
The implementation guide pages that can be opened in a browser are all located in the repository's subfolder `output`. This `output` folder will itself have a subfolder for each available implementation guide, e.g EventSummary. Therefore, the steps to open the 'home' page of an implementation guide are:
1. Use the File Explorer application to navigate to the location of where the repository was downloaded
2. Open the folder `output` and notice the included subfolders, one for each implementation guide
3. Open the folder you are interested in to view, eg `EventSummary`
4. Scroll down to the file `index.html` and double-click on it to open it with your (default) browser.
5. The home page will then display

#### Implementation guide layout
The implementation guides all have a standard layout, organised with the blue navigation bar near the top of the page. The tabs are:
 - `Home` - this is the starting point of the implementation guide and contains introductory material intended to provide an overview of the purpose, scope, how to get started etc
 - `Guidance` - this page has information for readers unfamiliar with the FHIR standard
 - `Conformance` - this page outlines a number of requirements that should be met by implementations of the implementation guides
 - `Profiles` - this page lists all of the included profiles, organised by resource categories
 - `Extensions`- this page lists all of the included extensions
 - `Mapping from requirements` - this page outlines mapping from data items (i.e. requirements) into FHIR
 - `Downloads` - this page includes a number of artefacts that can be downloaded to enable more advanced interactions with this implementation guide
 - `Disclaimers` - this page includes the proper attribution for all included content

## Advanced content viewing
Readers wishing to view the native implementation guide content (i.e. the `xml` files), have a number of options. They are:

### 1) Viewing the raw content in GitHub
The input files in this repository can be viewed within the GitHub `code` viewing pane. Note that this does not require that any content be downloaded onto your computer.
1. Go back to the [home page](https://github.com/AuDigitalHealth/ci-fhir-r4) of this repository
2. Click on the folder `examples` to see a list of included example xml files, or the `resources` folder to see the list of included profiles
3. Click on the hyperlink of the file that interests you, noting that the purpose of any particular xml may not be clear from its name
4. The xml file will then open within the GitHub code viewing pane
5. Note that all included files may be viewed by this means

### 2) Viewing the raw content within text editor software
All downloaded content, that is text-based (e.g. xml, markdown) may also be viewed with text editor software. For optimal viewing with this approach, xml-aware software such as [Notepad++](https://notepad-plus-plus.org/) or [Oxygen](https://www.oxygenxml.com/) is recommeded. Just navigate to the directory/file that you wish to view. For example, to view the raw xml of one of the profiles, click on `resources` and then one of the listed xml files that interest you.

### 3) Opening profiles with Forge (advanced)
Profiles can be opened with the [Forge application](https://simplifier.net/forge) in order to view the technical constraints applied in the profile. This advanced option requires additional setup, which is:
1. Clone the [HL7 AU au-fhir-base repository](https://github.com/hl7au/au-fhir-base) onto your computer. This is required as our repositories are technically derived from HL7 AU `au-fhir-base` which must be present on your computer in order for Forge to collect all of the upstream constraints.
2. A symbolic link must be created between the 2 repositories, specifically from within the `ci-fhir-r4` resources folder to the resources folder of the HL7 AU `au-fhir-base` resources folder. This can be achieved with the following command (executed in an adminstrator-enabled command terminal window):
```
mklink /D C:\path\to\folder\ci-fhir-r4\resources\link_to_au-fhir-base-r4_resources C:\path\to\folder\au-fhir-base-r4\resources
```
3. Download the R4 version of [Forge](https://simplifier.net/forge) (for which you will need to first create a logon)
4. Open Forge and then open profile folder of `ci-fhir-r4\resources`, ensuring that the tickbox 'include subfolders' is ticked
5. Double click on one of the listed profiles

For further information please refer to the comprehensive [Forge documentation](http://docs.simplifier.net/forge/).
