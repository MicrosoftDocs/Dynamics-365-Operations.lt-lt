---
title: „Dataverse“ virtualiųjų lentelių užklausų optimizavimas
description: „Dataverse” virtualiųjų lentelių užklausų efektyvumo optimizavimas ir trikčių diagnostika
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054913"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>„Dataverse“ virtualiųjų lentelių užklausų optimizavimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Problema

### <a name="overview"></a>Apžvalga

Naudodami „Dataverse” virtualiąsias lenteles integravimų ir kitų duomenų ryšių su „Dynamics 365 Human Resources” vystymui, galite susidurti su užklausų pagal virtualiąsias lenteles efektyvumo problemomis. Lėtas užklausų vykdymas gali atsitikti įvairiems klientams arba sąsajoms. Pavyzdžiui, jums gali iškilti problemą šiomis sąlygomis:

- Pateikiant virtualiosios lentelės užklausą per „Dataverse” Žiniatinklio API
- Kuriant „Power App” pagal virtualiąją lentelę
- Kuriant „Power BI” ataskaitą virtualioje lentelėje

Yra galimybė, kad visose šiose sąsajose iškils efektyvumo problema.

Viena iš lėto Personalo valdymui skirtų „Dataverse” virtualiųjų lentelių efektyvumo priežasčių yra su lentelės [naršymo ypatybėmis](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) susijusios virtualiosios lentelės išorinio rakto stulpeliai. Kai virtualiajai lentelei sukuriamos naršymo ypatybės, išorinio rakto stulpelis automatiškai įtraukiamas į lentelę, kad būtų atspindima susijusios virtualiosios lentelės rakto stulpelio vertė. Pavyzdžiui, stulpelis **„_mshr_fk_person_id_value”** yra įtraukiamas į **„mshr_hcmworkerbaseentity”** objektą naudojant išorinio rakto ypatybę iš **„mshr_dirpersonentity”** objekto. Dėl to, kaip šių išorinio rakto stulpelių reikšmės yra tvarkomos lentelėje, reikšmių iškvietimas gali turėti neigiamos įtakos užklausos pagal virtualiąją lentelę efektyvumui.

### <a name="potential-symptoms"></a>Galimi požymiai

Pavyzdys, kur galite pastebėti šį poveikį, yra užklausos pagal Darbuotojo (**„mshr_hcmworkerentity”**) arba Pagrindinio darbuotojo (**„mshr_hcmworkerbaseentity”**) objektą. Galite pastebėti, kad efektyvumo problema pasireiškia keliais skirtingais būdais:

- **Lėtas užklausos vykdymas**: Užklausą pagal virtualiąją lentelę gali pateikti tikėtuosius rezultatus, bet užtrukti daugiau laiko nei tikėtasi užklausos vykdymui užbaigti.
- **Užklausos skirtasis laikas**: Užklausai gali baigtis skirtasis laikas ir būti grąžinama ši klaida: „Atpažinimo ženklas, skirtas iškviesti „Finance and Operations”, buvo gautas, bet „Finance and Operations” grąžino vidinę serverio klaidą („InternalServerError”).”
- **Netikėta klaida**: Užklausa gali grąžinti 400 tipo klaidą su šiuo pranešimu: „Įvyko netikėta klaida.”

  ![Klaidos tipas 400 „HcmWorkerBaseEntity” objekte](./media/HcmWorkerBaseEntityErrorType400.png)

- **Buferizavimas**: Užklausa gali pernelyg daug naudoti serverio išteklius ir todėl patirti buferizavimą. Tokiu atveju užklausa grąžina šią klaidą: „Buvo gautas atpažinimo ženklas „Finance and Operations” iškvietimui, tačiau „Finance and Operations” grąžino 429 tipo klaidą.” Daugiau informacijos apie buferizavimą Personalo valdyme rasite [Buferizavimo DUK](./hr-admin-integration-throttling-faq.md).

  ![Klaidos tipas 429 „HcmWorkerBaseEntity” objekte](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Sprendimas

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Į jūsų duomenų užklausą įtraukiamų stulpelių skaičiaus apribojimas

Naudojant virtualiąsias lenteles, vienas iš metodų, turinčių didžiausią potencialą pagerinti užklausų efektyvumą, yra riboti užklausoje pasirinktų stulpelių skaičių. Bendrosios užklausos efektyvumo optimizavimo gairės yra riboti jūsų užklausoje grąžintų stulpelių skaičių tik iki jums reikalingų ypatybių. Tai ypač pasakytina apie virtualiųjų lentelių išorinio rakto stulpelius. Jeigu jūsų integravimui ar ataskaitai nereikia išorinio rakto stulpelių reikšmių, tada sukurkite užklausą, parenkančią tik tuos stulpelius, kurių jums reikia, išskyrus išorinio rakto stulpelius.

#### <a name="selecting-columns-in-an-odata-query"></a>Stulpelių pasirinkimas „OData” užklausoje

Kai pateikiate virtualiosios lentelės užklausą per „Dataverse” Žiniatinklio API, galite apriboti į užklausą įtraukiamų stulpelių skaičių naudodami **„$select”** sistemos užklausos parinktį, ir apibrėžti stulpelius, kurių rezultatų jums turi būti grąžinami. Norėdami maksimaliai padidinti efektyvumą, neįtraukite išorinio rakto stulpelių (su **_„mshr_FK”_** priešvardžiu) į užklausą.

Pavyzdžiui, ši užklausa pagal **„mshr_hcmworkerbaseentity”** objektą įtrauks tik į **„$select”** užklausos parinkties sąlygą įtrauktus stulpelius, išskyrus išorinio rakto reikšmes. Tai labai pagerina užklausos, į kurią įtraukti visi lentelės stulpeliai, efektyvumą.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Rekomendacija apriboti pasirinktų stulpelių skaičių taip pat taikoma, kai užklausos parinktis **„$expand”** naudojama užklausai išplėsti iki susijusių virtualiųjų lentelių per naršymo ypatybes. Pavyzdžiui, šioje užklausoje yra stulpelių iš **„mshr_hcmworkerbaseentity”** objekto su išplėstiniais stulpeliais iš **„mshr_dirpersonentity”** objekto. Atkreipkite dėmesį, kad užklausos parinktis **„$select”** taip pat yra įtraukta **„$expand”** užklausos parinkties sąlygą.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Naudojant šį duomenų gavimo metodą su užklausos parinktimi **„$select”** iš užklausos parinkties **„$expand”** sąlygos, turėtumėte pastebėti geresnį efektyvumą, kai naršymo ypatybė tarp objektų yra ryšys „daugelis su vienu”. Galbūt nepamatysite tokio pat užklausos vykdymo laiko sumažėjimo, kai išplėsite ryšį „vienas su daugeliu”. Daugiau informacijos apie „Dataverse” virtualiųjų lentelių ryšio apibrėžimą ieškokite [Lentelės ryšiai](/powerapps/maker/data-platform/create-edit-entity-relationships).

Daugiau informacijos apie **„$select”** ir **„$expand”** sistemos užklausos parinktis, esančias „Dataverse” Žiniatinklio API, ieškokite [Susijusių objekto įrašų gavimas naudojant užklausą](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).

#### <a name="selecting-columns-in-power-bi"></a>Stulpelių pasirinkimas „Power BI” platformoje

Jei kurdami „Power BI” ataskaitą pagal „Dataverse” virtualiąją lentelę patiriate bet kurį iš anksčiau minėtų lėto efektyvumo požymių, galite pagerinti efektyvumą į ataskaitą neįtraukdami išorinio rakto stulpelių iš lentelėje pasirinktų stulpelių. Pavyzdžiui, jei naudojate „Power BI Desktop” ataskaitos pagal **„mshr_hcmworkerbaseentity”** objektą kūrimui, galite naudoti tolesnius veiksmus stulpeliams, kuriuos norite įtraukti į ataskaitos užklausą, pasirinkti.

1. „Power BI Desktop” pasirinkite **Daugiau...** iš **Gauti duomenis** išplečiamojo sąrašo, esančio veiksmų juostoje.
2. Lango **Gauti duomenis** ieškos lauke įveskite **„Common Data Service”**, pasirinkite **„Common Data Service”** jungtį, o tada – **Prisijungti**.
3. „Common Data Service” lango lauke **Serverio Url** įveskite organizacijos URI jūsų „Dataverse” aplinkai ir pasirinkite **Gerai**.
  
   ![Jūsų „Dataverse” aplinkos URI pavadinimas](./media/PowerBIDataverseURLSetup.png)
  
4. Naršyklės lange išplėskite **Objektų** mazgą.
5. Ieškos lauke įveskite **„mshr_hcmworkerbaseentity”** ir pasirinkite objektą.
6. Pasirinkite **Transformuoti duomenis**.
7. „Power Query“ rengyklės lange pasirinkite **Patobulinta rengyklė**.
8. Lange **Patobulinta rengyklė** atnaujinkite užklausą, kad ji atrodytų kaip žemiau, pridėdami arba pašalindami masyvo stulpelius taip, kaip jums reikia.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![Užklausos atnaujinimas Patobulintoje rengyklėje, skirtoje „Power Query“ rengyklei](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Pasirinkite **Atlikta**.

   > [!NOTE]
   > Jeigu anksčiau gavote 429 tipo užklausos klaidą, jums gali reikėti palaukti kartojimo laikotarpio prieš atnaujinant užklausą, kad ji būtų sėkmingai baigta.

10. Paspauskite **Uždaryti & Taikyti** „Power Query“ rengyklės veiksmų juostoje.

Tada galėsite pradėti kurti „Power BI” ataskaitą pagal stulpelius, pasirinktus iš virtualiosios lentelės.

#### <a name="selecting-columns-in-power-apps"></a>Stulpelių pasirinkimas „Power Apps” platformoje

Panašiai į „Dataverse” Žiniatinklio API užklausas ir „Power BI”, galite patobulinti „Power Apps” užklausų efektyvumą, pagrįstą „Dataverse” virtualiosiomis lentelėmis, neįtraukdami jūsų programos susijusių lentelių stulpelių. Jei stulpeliai iš susijusios lentelės buvo įtraukti į puslapį, tada duomenų iškvietimui sukurtuose užklausų URL bus susijusios lentelės išorinio rakto ypatybės. Tai, kaip ir aukščiau nurodyti [Stulpelių pasirinkimo „OData” užklausoje](#selecting-columns-in-power-apps) pavyzdžiai, sumažina efektyvumą dėl sukeltų papildomų duomenų peržvalgų.

Norėdami tai išspręsti, galite patikrinti, ar nei vienas duomenų laukas iš susijusių lentelių nebuvo įtrauktas į jokią jūsų „Power App” duomenų formą.

1. Medžio rodinio srityje pasirinkite duomenų formą ekranui.
2. Srityje **Ypatybės** pasirinkite **Redaguoti** ypatybei **Laukai**.
3. Srityje **Duomenys** patikrinkite, ar nei vienas iš pasirinktų laukų nėra duomenų šaltinio virtualiosios lentelės laukas.

Tarkim, jei vienas iš duomenų laukų, įtrauktų į programos puslapį, nurodo kitą lentelę, pavyzdžiui **„ThisItem.Worker.Name”**, kur **Darbuotojas** yra susijusi lentelė, tikėtina, kad duomenų efektyvumas gali sumažėti.

Galite naudoti [„Power Apps Monitor”](/powerapps/maker/monitor-overview), kad užtikrintumėte, jog tik jums reikalingi stulpeliai būtų įtraukti į užklausą, skirtą „Power App” duomenims gauti. Galite peržiūrėti „getRows” (gauti eilutes) operacijai sukurtą URL, siekiant užtikrinti, kad jūsų pasirinkti stulpeliai programai bus optimalūs duomenims nuskaityti.

![Naudokite „Power Apps Monitor” operacijai „getData” (gauti duomenis) analizuoti](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>Duomenų užklausos filtravimas

Kitas užklausų vykdymo efektyvumo metodas yra riboti užklausos rezultatuose grąžintų įrašų skaičių. Tai galite atlikti filtruodami rezultatus ir taip užtikrindami, kad gaunate tik jums reikalingus įrašus.

Skaitykite [Filtravimo rezultatai](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) norėdami gauti daugiau informacijos apie užklausų duomenų filtravimą.

### <a name="limiting-the-page-size-of-the-query"></a>Užklausos puslapio dydžio ribojimas

Jei dirbate su dideliais duomenų rinkiniais, užklausų rezultatus galite padalinti į kelis puslapius pridėdami `odata.maxpagesize` nuostatos antraštę į duomenų užklausas.

Daugiau informacijos apie puslapių kaitą rasite [Puslapyje grąžinamų objektų skaičiaus nurodymas](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).

## <a name="see-also"></a>Taip pat žiūrėkite

- [Konfigūruokite „Dataverse“ virtualias lenteles](hr-admin-integration-common-data-service-virtual-entities.md)
- [„Human Resources“ virtualiųjų lentelių DUK](hr-admin-virtual-entity-faq.md)
- [Užklausų buferizavimo DUK](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]