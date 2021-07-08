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
{{if(isBlank(cells['name.namePart'].value), '', '<name' + if(isBlank(cells['name@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name@valueURI'].value +'"') + '><namePart>' + cells['name.namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.role.roleTerm@valueURI'].value + '">' + cells['name.role.roleTerm'].value + '</roleTerm></role></name>')}}

{{if(isBlank(cells['name.1namePart'].value), '', '<name' + if(isBlank(cells['name.1@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.1@valueURI'].value +'"') + '><namePart>' + cells['name.1namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.1.role.roleTerm@valueURI'].value + '">' + cells['name.1.role.roleTerm'].value + '</roleTerm></role></name>')}}
{{if(isBlank(cells['name.2namePart'].value), '', '<name' + if(isBlank(cells['name.2@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.2@valueURI'].value +'"') + '><namePart>' + cells['name.2namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.2.role.roleTerm@valueURI'].value + '">' + cells['name.2.role.roleTerm'].value + '</roleTerm></role></name>')}}
{{if(isBlank(cells['name.3namePart'].value), '', '<name' + if(isBlank(cells['name.3@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.3@valueURI'].value +'"') + '><namePart>' + cells['name.3namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.3.role.roleTerm@valueURI'].value + '">' + cells['name.3.role.roleTerm'].value + '</roleTerm></role></name>')}}
{{if(isBlank(cells['name.4namePart'].value), '', '<name' + if(isBlank(cells['name.4@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.4@valueURI'].value +'"') + '><namePart>' + cells['name.4namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.4.role.roleTerm@valueURI'].value + '">' + cells['name.4.role.roleTerm'].value + '</roleTerm></role></name>')}}
{{if(isBlank(cells['name.5namePart'].value), '', '<name' + if(isBlank(cells['name.5@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.5@valueURI'].value +'"') + '><namePart>' + cells['name.5namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.5.role.roleTerm@valueURI'].value + '">' + cells['name.5.role.roleTerm'].value + '</roleTerm></role></name>')}}
{{if(isBlank(cells['name.6namePart'].value), '', '<name' + if(isBlank(cells['name.6@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.6@valueURI'].value +'"') + '><namePart>' + cells['name.6namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.6.role.roleTerm@valueURI'].value + '">' + cells['name.6.role.roleTerm'].value + '</roleTerm></role></name>')}}
{{if(isBlank(cells['name.7namePart'].value), '', '<name' + if(isBlank(cells['name.7@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.7@valueURI'].value +'"') + '><namePart>' + cells['name.7namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.7.role.roleTerm@valueURI'].value + '">' + cells['name.7.role.roleTerm'].value + '</roleTerm></role></name>')}}
{{if(isBlank(cells['name.8namePart'].value), '', '<name' + if(isBlank(cells['name.8@valueURI'].value), '', ' authority="naf" valueURI="' + cells['name.8@valueURI'].value +'"') + '><namePart>' + cells['name.8namePart'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="' + cells['name.8.role.roleTerm@valueURI'].value + '">' + cells['name.8.role.roleTerm'].value + '</roleTerm></role></name>')}}
<originInfo>
{{if(isBlank(cells['dateCreated_text'].value), '', '<dateCreated' + if(isBlank(cells['dateCreated_qualifier'].value), '', ' qualifier="' + cells['dateCreated_qualifier'].value + '"') + '>' + cells['dateCreated_text'].value + '</dateCreated>')}} 
{{if(isBlank(cells['dateRange1'].value), '', '<dateCreated point="start" encoding="edtf">' + cells['dateRange1'].value + '</dateCreated><dateCreated point="end" encoding="edtf">' + cells['dateRange2'].value + '</dateCreated>')}}
{{if(isBlank(cells['dateCreated_edtf'].value), '', '<dateCreated encoding="edtf"' + if(isBlank(cells['dateCreated_qualifier'].value), '', ' qualifier="' + cells['dateCreated_qualifier'].value + '"') + '>' + cells['dateCreated_edtf'].value + '</dateCreated>')}}
</originInfo>
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form>
{{if(isBlank(cells['form_2'].value), '', '<form authority="aat" valueURI="' + cells['form_2_URI'].value + '">' + cells['form_2'].value + '</form>')}}</physicalDescription>

{{if(isBlank(cells['subject.topic'].value), '', '<subject' + if(isBlank(cells['subject.topic_URI'].value), '', ' valueURI="' + cells['subject.topic_URI'].value + '"') + '><topic>' + cells['subject.topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.1topic'].value), '', '<subject' + if(isBlank(cells['subject.1topic_URI'].value), '', ' valueURI="' + cells['subject.1topic_URI'].value + '"') + '><topic>' + cells['subject.1topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.2topic'].value), '', '<subject' + if(isBlank(cells['subject.2topic_URI'].value), '', ' valueURI="' + cells['subject.2topic_URI'].value + '"') + '><topic>' + cells['subject.2topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.3topic'].value), '', '<subject' + if(isBlank(cells['subject.3topic_URI'].value), '', ' valueURI="' + cells['subject.3topic_URI'].value + '"') + '><topic>' + cells['subject.3topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.4topic'].value), '', '<subject' + if(isBlank(cells['subject.4topic_URI'].value), '', ' valueURI="' + cells['subject.4topic_URI'].value + '"') + '><topic>' + cells['subject.4topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.5topic'].value), '', '<subject' + if(isBlank(cells['subject.5topic_URI'].value), '', ' valueURI="' + cells['subject.5topic_URI'].value + '"') + '><topic>' + cells['subject.5topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.6topic'].value), '', '<subject' + if(isBlank(cells['subject.6topic_URI'].value), '', ' valueURI="' + cells['subject.6topic_URI'].value + '"') + '><topic>' + cells['subject.6topic'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject.geographic'].value), '', '<subject' + if(isBlank(cells['subject.geographic_URI'].value), '', ' valueURI="' + cells['subject.geographic_URI'].value + '"') + '><geographic>' + cells['subject.geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.2geographic'].value), '', '<subject' + if(isBlank(cells['subject.2geographic_URI'].value), '', ' valueURI="' + cells['subject.2geographic_URI'].value + '"') + '><geographic>' + cells['subject.2geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.3geographic'].value), '', '<subject' + if(isBlank(cells['subject.3geographic_URI'].value), '', ' valueURI="' + cells['subject.3geographic_URI'].value + '"') + '><geographic>' + cells['subject.3geographic'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject.4geographic'].value), '', '<subject' + if(isBlank(cells['subject.4geographic_URI'].value), '', ' valueURI="' + cells['subject.4geographic_URI'].value + '"') + '><geographic>' + cells['subject.4geographic'].value + '</geographic></subject>')}}
<language><languageTerm authority="iso639-2b" type="text">{{cells['language'].value}}</languageTerm></language>
<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>
{{if(isBlank(cells['relatedItem.1.titleInfo.title'].value), '', '<relatedItem displayLabel="Collection" type="host"><titleInfo><title>' + cells['relatedItem.1.titleInfo.title'].value + '</title></titleInfo></relatedItem>')}}
<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['relatedItem.titleInfo.title'].value}}</title></titleInfo></relatedItem>
{{if(isBlank(cells['locationphysicalLocation'].value), '', '<location><physicalLocation' + if(isBlank(cells['locationphysicalLocation_URI'].value), '', ' authority="naf" valueURI="' + cells['locationphysicalLocation_URI'].value + '"') + '>' + cells['locationphysicalLocation'].value + '</physicalLocation></location>')}}
<recordInfo><languageOfCataloging><languageTerm authority="iso639-2b" type="text">English</languageTerm></languageOfCataloging><recordContentSource {{if(isBlank(cells['recordInfo.recordContentSource_URI'].value), '', ' authority="naf" valueURI="' + cells['recordInfo.recordContentSource_URI'].value + '"')}}>{{cells['recordInfo.recordContentSource'].value}}</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['accessCondition@xlink:href'].value}}">{{cells['accessCondition'].value}}</accessCondition>
</mods>
```

#### Suffix

```
</modsCollection>
```