# Open Refine Template for C. E. Brehm collection


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="filename">{{cells["identifier"].value}}</identifier>
<titleInfo supplied="yes"><title>{{cells['title'].value}}</title></titleInfo>
<abstract>{{cells['abstract'].value}}</abstract>
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form>
{{if(isBlank(cells['form2'].value), '', '<form authority="aat" valueURI="' + cells['form2_URI'].value + '">' + cells['form2'].value + '</form>')}}
</physicalDescription>
<originInfo><dateCreated>{{cells['date_text'].value}}</dateCreated><dateCreated encoding="edtf" keyDate="yes">{{cells['date'].value}}</dateCreated></originInfo>
{{if(isBlank(cells['author'].value), '', '<name' + if(isBlank(cells['author_URI'].value), '', ' authority="naf" valueURI="' + cells['author_URI'].value + '"') + '><namePart>' + cells['author'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/aut">Author</roleTerm></role></name>')}}
{{if(isBlank(cells['correspondent'].value), '', '<name' + if(isBlank(cells['correspondent_URI'].value), '', ' authority="naf" valueURI="' + cells['correspondent_URI'].value + '"') + '><namePart>' + cells['correspondent'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/crp">Correspondent</roleTerm></role></name>')}}
{{if(isBlank(cells['addressee'].value), '', '<name' + if(isBlank(cells['addressee_URI'].value), '', ' authority="naf" valueURI="' + cells['addressee_URI'].value + '"') + '><namePart>' + cells['addressee'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/rcp">Addressee</roleTerm></role></name>')}}
{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
{{if(isBlank(cells['subject'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_URI'].value + '"><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name_2'].value), '', '<subject authority="naf" valueURI="' + cells['subject_name_2URI'].value + '"><name><namePart>' + cells['subject_name_2'].value + '</namePart></name></subject>')}}
<typeOfResource>text</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>C. E. Brehm, University of Tennessee Office of the President Records, 1948-1959</title></titleInfo></relatedItem>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>University of Tennessee Office of the President Records 1948-1959</title></titleInfo><identifier>AR.0006</identifier><location><url>https://n2t.net/ark:/87290/v8416v6b</url></location></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<language><languageTerm type="text" authority="iso639-2b">English</languageTerm></language>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource><languageOfCataloging><languageTerm type="text" authority="iso639-2b">English</languageTerm></languageOfCataloging><recordOrigin>
Created and edited in general conformance to MODS Guidelines (Version 3.5).
</recordOrigin></recordInfo>
<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```