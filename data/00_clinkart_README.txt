00_README

Distribution Version 1.1
2023-03-08

Changes wrt version 1.0
-Addition of the tokenized data 


===============
Distribution Licence
===============

All the data in this folder are available under the CC-BY-NC-4.0 licence.


=========
Training.txt
=========

The training.txt file contains the 83 documents of the training set for the Clinkart task at Evalita 2023. 
The  data are in the PubTator format, which consists of tab-delimited text file structured as follows:
<DOCID>|t|<TEXT>
<DOCID>  REL  <RML_START>-<RML_END>  <EVENT_START>-<EVENT_END>  <RML_TEXT>  <EVENT_TEXT>
<DOCID>  REL  <RML_START>-<RML_END>  <EVENT_START>-<EVENT_END>  <RML_TEXT>  <EVENT_TEXT>

<DOCID>|t|<TEXT>
<DOCID>  REL  <RML_START>-<RML_END>  <EVENT_START>-<EVENT_END>  <RML_TEXT>  <EVENT_TEXT>

Where:
Every document in the dataset is in a new line and a space line is used as a document separator.
- DOCID: document id
- t: marker to identify the lines that contain the text of the documents
- TEXT: text of the document
- Every annotated relation is in a separate line and is represented as an ordered pair of textual mentions (i.e. RML,EVENT). Each mention in the relationship is expressed by its start and end character offsets.  The text span can be set but is not mandatory.
- DOCID: document id
- REL: marker to identify the lines that contain the relations of the given  document
- RML_START:  start character offset of the RML entity mention in the document
- RML_END:  end character offset of the RML entity mention in the document
- EVENT_START:  start character offset of the EVENT entity mention in the document
- EVENT_END:  end character offset of the EVENT entity mention in the document
- RML_TEXT [optional]: text span of the RML entity mention
- EVENT_TEXT [optional]: text span of the EVENT entity mention

For example:
100509|t|Donna, 87 anni, ipertiroidismo subclinico, artrosi, osteoporosi (fratture T10-T11), ipovisus, AH in terapia steroidea cronica; ipertensione; scompenso cardiaco diastolico; un ricovero per EPA. Recente embolia polmonare, da allora in TAO. Recentemente agitazione e dolore resistente a paracetamolo. All’ECG RS 66 bpm, deviazione assiale sinistra, BBD incompleto. Chest Pain Score e Wells Score bassi. All’ecocardiogramma FE 55%. PA 160/90 mmHg. Giordano positivo, dolore paravertebrale bilateralmente. Dopo caduta accidentale vivo dolore a livello dorsale. Al quadro rx crolli vertebrali da T6 a T8 con pregresso crollo di T12. Procrastinata la chifoplastica e prescritto un busto, iniziava cauta fisioterapia. Videat oculistico e continuazione della terapia steroidea. Prescrizione di teriparatide e vitamina D.
100509     REL     309-315     306-308     66 bpm     RS
100509     REL     393-398     387-392     bassi      Score
100509     REL     393-398     373-378     bassi      Score
100509     REL     423-426     420-422     55%        FE
100509     REL     431-442     428-430     160/90 mmHg     PA
100509     REL     453-461     444-452     positivo     Giordano


===============
Training_tokenized
===============

The training_tokenized.zip file contains the tokenized version of the 83 documents of the training set for the Clinkart task. 

The annotation of pertains-to relations is strictly based on tokens (the target, in particular, must necessarily consist of one token, while the source consists of one or more token) and on sentences (source and target of a relation must belong to the same sentence).

In order to reduce the noise that might be introduced by mismatching pre-processing, participants to the Clinkart task are strongly encouraged to use the same (automatic) tokenization and sentence splitting that has been used when the data have been (manually) annotated.


