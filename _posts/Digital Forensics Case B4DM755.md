In this room, we will simulate an actual crime scenario whereby a court of law has authorised us to conduct a search on a specific person and analyse obtained artefacts and evidence.

## Case B4DM755: Details of the Crime
```ruby
As a Forensics Lab Analyst, you analyse the artefacts from crime scenes. Occasionally, the law enforcement agency you work for receives "intelligence reports" about different cases, and today is one such day. A trusted informant, who has connections to an international crime syndicate, contacted your supervisor about William S. McClean from Case #B4DM755.

The informant provided information about the suspect's whereabouts in Metro Manila, Philippines, which is currently at large, and a transaction that will happen today with a local gang member. They also knew the exact location of the meetup and that the suspect would have incriminating materials at the time.

The law enforcement agency prepared for the operation by obtaining proper search authority and assigning a DFIR (Digital Forensics & Incident Response) First Responder (i.e., you) to ensure the appropriate acquisition of digital artefacts and evidence for examination at the Forensics Lab, and eventually for use in litigation. The court issued a **search warrant on the same day, allowing law enforcement officers to investigate the suspect and his place of residence based on the informant's tip.
```

#### What is your official role?
Forensics Lab Analyst

#### What role was assigned to you for this specific scenario?
DFIR First Responder

#### What do you have to gather?
Digital artefacts and evidence

#### What document is needed before performing any legal search?
Search warrant

---

## Practical Application of the Digital Forensics Process

#### Before imaging drives, what must we check them for?
Drive encryption

#### What should be done to ensure and maintain the integrity of original files in the Chain of Custody?
Hash and copy

#### What must be done before sending obtained artefacts to the Forensics Laboratory?
Bag, Seal, and Tag the obtained artefacts

---

## Case B4DM755: At the Scene of Crime

#### What is the only possible artefact found in the suspect's residence?
Flash drive

#### Based on the scenario and the previous task, what should be done with that acquired suspect artefact?
Taking an image

#### What is the crucial aspect of the Chain of Custody that ensures individual accountability and guarantees a transparent and untainted transfer of artefacts and evidence?
Ensure proper documentation

---

## Introduction to FTK Imager

#### What device will prevent tampering when acquiring a forensic disk image?
Write-blocking device

#### What is the UI element of FTK Imager which displays a hierarchical view of the added evidence sources?
Evidence Tree Pane

#### Is the attached flash drive encrypted? (Y/N)
For checking this, simply mount the flash drive and in the menu bar select File >  **Detect EFS encryption**

#### What is the UI element of FTK Imager which displays a list of files and folders?
File List Pane

---

## Using FTK Imager to Acquire Digital Artefacts and Evidence.

#### What is the UI element of FTK Imager which displays the content of selected files?
Viewer Pane

#### What is the SHA1 hash of the physical drive and forensic image?
After creating the disk image, select **Verify images after they are created**. The SHA1 hash will be displayed.

#### Including hidden files, how many files are currently stored on the flash drive?
Adding the image file as evidence, will provide us with the information about exporting the files. We can see the number of files on the flash drive.(eight)

#### How many files were deleted in total?
Checking the number of files in the drive and in FTK will provide us with the results.(six)

#### How many recovered files are corrupted (e.g., 0 file size)?
In the destination folder where we have exported the files, we can see the files with 0 kb size.(three)


---

## Case B4DM755: At the Forensics Laboratory

#### Aside from FTK Imager, what is the directory name of the other tool located in the tools directory under Desktop?
exiftool-12.47

#### What is the visible extension of the "hideout" file?
Checking the properties of the file will give the extension as .pdf

#### View the metadata of the "hideout" file. What is its actual extension?
Using exiftool, we can get the metadata where the actual extension is displayed.(image file)

#### A phone was used to photograph the "warehouse". What is the phone's model?
The results of the metadata will have the model of the phone.(Oneplus...) 

#### Are there any indications that the suspect is involved in other illegal activity? (Y/N)
Again checking the metadata with the help of exiftool will provide with the model of the phone(Mi...)

#### Are there any indications that the suspect is involved in other illegal activity? (Y/N)
There is an excel document related to some operations, it does seem suspicious. It shows some error while trying to open i.e. it does not have the correct extension. Checking the same in FTK gives us a hint that the extension could be .zip and thus changing the same, we get a zip folder where our further answers will be present.

#### Who was the point of contact of Mr William S. McClean in 2022?
In the operation folder, there is a text file which contains the answer. (Karl...) 

#### A meetup occurred in 2022. What are the GPS coordinates during that time?
In the same text file, coordinates are also given. (14°26'25.7"N....)

#### What is the password to extract the contents of pandorasbox.zip?
The password is given at the end of the same file. (DarkVault....)

#### From which company did the source code in the pandorasbox directory originate?
Extracting the zip folder with the acquired password will have a folder named **HFT_Algorithm**. A python script is present inside of it. Executing it, will us the name of the company. (Swift...)

#### In one of the documents that the suspect has yet to sign, who was listed as the beneficiary?
The second folder named **MUST_CLEAN** and it contains few word documents. In one of them (Capitalisation...), the name of the beneficiary is listed. (Mr. Giovanni.....)

#### What is the hidden flag?
In the last file **DONOTOPEN** the flag is given. (THM{...})


---

## Post-Analysis of Evidence to Court Proceedings

#### In which phase is a warrant obtained for search, seizure, and examination of the suspect's computer data due to violations of domestic and international laws?
Pre-search

#### In which phase is a forensic analysis performed on the acquired digital evidence requested from various sources?
Post-search

#### Which phase involves presenting forensic artefacts and evidence with proper documentation in a court of law?
Trial



