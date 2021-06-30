# Open Refine Template for Tennessee Documentary History (following rights cleanup)

## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells['identifier_local'].value}}</identifier>
<identifier type="pid">{{cells['PID'].value}}</identifier>
{{if(isBlank(cells['identifier_oclc'].value), '', '<identifier type="oclc">' + cells['identifier_oclc'].value + '</identifier>')}}
<titleInfo supplied="yes"><title>{{cells["titleInfo.title"].value}}</title></titleInfo> 
{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells['author'].value), '', '<name' + if(isBlank(cells['author_URI'].value), '', ' authority="naf" valueURI="' + cells['author_URI'].value +'"') + '><namePart>' + cells['author'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['author2'].value), '', '<name' + if(isBlank(cells['author2_URI'].value), '', ' authority="naf" valueURI="' + cells['author2_URI'].value +'"') + '><namePart>' + cells['author2'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['author3'].value), '', '<name' + if(isBlank(cells['author3_URI'].value), '', ' authority="naf" valueURI="' + cells['author3_URI'].value +'"') + '><namePart>' + cells['author3'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['date_text'].value), '', '<originInfo><dateCreated>' + cells['date_text'].value + '</dateCreated><dateCreated keyDate="yes" encoding="edtf">' + cells['publication_date_edtf'].value + '</dateCreated></originInfo>')}}
{{if(isBlank(cells['date_text_2'].value), '', '<originInfo><dateCreated>' + cells['date_text_2'].value + '</dateCreated><dateCreated keyDate="yes" encoding="edtf">' + cells['publication_date_2'].value + '</dateCreated></originInfo>')}}
{{if(isBlank(cells['date_text_3'].value), '', '<originInfo><dateCreated>' + cells['date_text_3'].value + '</dateCreated><dateCreated keyDate="yes" encoding="edtf">' + cells['publication_date_3'].value + '</dateCreated></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form>
{{if(isBlank(cells['form_2'].value), '', '<form authority="aat" valueURI="' + cells['form_2_URI'].value + '">' + cells['form_2'].value + '</form>')}}</physicalDescription>
{{if(isBlank(cells['subject_lcsh'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_URI'].value + '"><topic>' + cells['subject_lcsh'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_2_URI'].value + '"><topic>' + cells['subject_lcsh_2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_3_URI'].value + '"><topic>' + cells['subject_lcsh_3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_lcsh_4'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_lcsh_4_URI'].value + '"><topic>' + cells['subject_lcsh_4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject_name'].value), '', '<subject><name authority="naf" valueURI="' + cells['subject_name_URI'].value + '"><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_naf'].value), '', '<subject><name' + if(isBlank(cells['subject_naf_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_naf_URI'].value + '"') + '><namePart>' + cells['subject_naf'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_naf_2'].value), '', '<subject><name' + if(isBlank(cells['subject_naf_2_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_naf_2_URI'].value + '"') + '><namePart>' + cells['subject_naf_2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_naf_3'].value), '', '<subject><name' + if(isBlank(cells['subject_naf_3_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_naf_3_URI'].value + '"') + '><namePart>' + cells['subject_naf_3'].value + '</namePart></name></subject>')}}
<language><languageTerm authority="iso639-2b" type="text">{{cells['language'].value}}</languageTerm></language>
<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

{{if(isBlank(cells['relatedItem.1.titleInfo.title'].value), '', '<relatedItem displayLabel="Collection" type="host"><titleInfo><title>' + cells['relatedItem.1.titleInfo.title'].value + '</title></titleInfo></relatedItem>')}}
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['relatedItem.titleInfo.title'].value}}</title></titleInfo></relatedItem>
<location><physicalLocation{{if(isBlank(cells['recordInfo.recordContentSource_URI'].value), '', ' authority="naf" valueURI="' + cells['recordInfo.recordContentSource_URI'].value + '"')}}>{{cells['recordInfo.recordContentSource'].value}}</physicalLocation></location>
<recordInfo><languageOfCataloging><languageTerm authority="iso639-2b" type="text">English</languageTerm></languageOfCataloging><recordContentSource {{if(isBlank(cells['recordInfo.recordContentSource_URI'].value), '', ' authority="naf" valueURI="' + cells['recordInfo.recordContentSource_URI'].value + '"')}}>{{cells['recordInfo.recordContentSource'].value}}</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['accessCondition@xlink:href'].value}}">{{cells['accessCondition'].value}}</accessCondition>
</mods>
```

#### Suffix

```
</modsCollection>
```