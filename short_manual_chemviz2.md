# ChemViz2 user manual
This short manual describes a way of how a network can be made using text files and visualize the structures of compounds.

## Add ChemViz2 extension

### Download & install Cytoscape
1. Download and start Cytoscape, look at install instructions on https://cytoscape.org

### Download & install ChemViz2
2. Download ChemViz2 via https://apps.cytoscape.org/apps/chemViz2 or create a jar file by following the steps below.
3. Go to https://github.com/RBVI/chemViz2. Click on 'Code' and then Click on 'Download Zip'. After downloading, unzip the file, if necessary.
4. Go to the folder ChemViz2 and run in the terminal 'mvn clean install'.
5. A jar file wil become visible in the 'target' folder within the ChemViz2 folder. The chemViz2-2.0.3.jar file is the App for Cytoscape.
6. In Cytoscape go to the 'top' menu and click on ‘Apps’ and select ‘Install App from File’ in the 'App Store'.

### Visualize structures
7. To be able to view the structure of a compound, its SMILES of InChI needs to be present in the dataset. The SMILES and InChI information of a compound can be retrieved from, for example, the PubChem website.
In the steps that follow, a method based on two txt files is given. Here a 'network' file and a 'node table' file are used. Both files can be in txt format but more options are possible, see the manual on the cytoscape website.
8. The 'node_table.txt' file contains SMILES and/or InChI information. A 'node table' can be as simple as a text file (tab separated) with three columns with headers like for example 'PubChem CID', 'Compound name', 'SMILES' or 'INCHI'. SMILES or INCHI are essential for a structure visualization.
9. The 'network.txt' file needs to contain unique references to the compound in the node_table, the 'PubChem CID' can be used. To make a network two headers in this file are necessary called 'source' and 'target'. However, more columns can be add. Every line in the network file represents a interaction between compounds. Interaction are identified based on the unique references. In the example here 'PubChem CID' is used.
10. Load the 'node_table.txt' by clicking on 'File' and 'Network from File' in 'Import'. Select your file and click 'Open'. A new window will appear with import options, click on 'Ok'.
11. Load the 'network.txt' file by clicking on 'File' and 'Table from File' in 'Import'. Select your file and click 'Open'. A new window will appear with import options, click on 'Ok'.
12. Now, in the 'top' menu of Cytoscape go to 'Apps', 'Cheminformatics Tools' and click on settings. In the 'Attribute Settings' select the column where the SMILES are located or the InChI or both. After selecting, they will appear blue. Close the window by clicking 'ok'.
13. After selecting, the appropriate columns the 'actions' in the 'Cheminformatics Tools' options to show structures and more will now appear in white instead of grey and can be used.


