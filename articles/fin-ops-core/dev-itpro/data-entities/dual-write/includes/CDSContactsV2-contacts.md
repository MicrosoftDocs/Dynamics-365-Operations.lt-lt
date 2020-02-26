## <a name="cds-contacts-v2-to-contacts"></a>CDS kontaktai V2 su kontaktais

Naudojant šį šabloną sinchronizuojami duomenys tarp „Finance and Operations“ programų ir „Common Data Service“.

Šaltinio filtras: (AssociatedContactType = 1)

Atšaukto šaltinio filtras: msdyn_contactforvendor eq true ir msdyn_sellable eq false ir msdyn_contactpersonid ne ''

„Finance and Operations“ laukas | Schemos tipas | Kitas „Dynamics 365” laukas | Numatytoji reikšmė
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | nėra | Tiekėjas
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | faksas | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | skyrius | 
NOTES | = | aprašas | 
GENDER | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
nėra | >> | msdyn_contactforvendor | Teisinga
CONTACTPERSONID | = | msdyn_contactpersonid | 
