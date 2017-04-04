---
title: "Mobiliojo ryšio sąskaitos faktūros patvirtinimai"
description: "Mobiliuosiuose įrenginiuose galimybės Microsoft Dynamics 365 operacijoms tegul dizaino mobili patirtimi verslo vartotojas. Sudėtingesnius, platforma taip pat leidžia kūrėjams išplėsti galimybes kaip jie nori. Efektyviausias būdas išmokti kai kurių naujų koncepcijų, mobiliesiems turi eiti per procesą, projektuojant keli scenarijai. Šioje temoje siekiama užtikrinti praktinį požiūrį kurti mobiliojo ryšio scenarijų atsižvelgiant tiekėjo SF patvirtinimo mobile, naudojimo atveju. Šios temos turėtų padėti jums sukurti kitų variantų scenarijų ir taip pat gali būti taikomas kitų scenarijų, kurie nėra susiję su tiekėjo SF."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Mobiliojo ryšio sąskaitos faktūros patvirtinimai

Mobiliuosiuose įrenginiuose galimybės Microsoft Dynamics 365 operacijoms tegul dizaino mobili patirtimi verslo vartotojas. Sudėtingesnius, platforma taip pat leidžia kūrėjams išplėsti galimybes kaip jie nori. Efektyviausias būdas išmokti kai kurių naujų koncepcijų, mobiliesiems turi eiti per procesą, projektuojant keli scenarijai. Šioje temoje siekiama užtikrinti praktinį požiūrį kurti mobiliojo ryšio scenarijų atsižvelgiant tiekėjo SF patvirtinimo mobile, naudojimo atveju. Šios temos turėtų padėti jums sukurti kitų variantų scenarijų ir taip pat gali būti taikomas kitų scenarijų, kurie nėra susiję su tiekėjo SF.

<a name="prerequisites"></a>Būtinieji komponentai
-------------

| Būtinoji sąlyga                                                                                            | aprašymas                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Iš anksto perskaitykite mobiliojo ryšio vadovas                                                                                |(/ dynamics365/operacijos/dev-itpro/Mobilieji-programos / mobile-platform.md)                                                                                                  |
| Dinamika 365 operacijoms                                                                             | Aplinkoje, kurioje yra Microsoft Dynamics 365 operacijų versija 1611 ir "Microsoft Dynamics" operacijų platformos naujinimas 3 (2016 m lapkričio mėn.)                   |
| Įdiegti karštąją pataisą KB 3204341.                                                                              | Užduočių rašytuvas klaidingai įrašyti du glaudžiai komandas išplečiamajame sąraše dialogai, tai yra įtraukti į Dynamics 365 operacijos platformos naujinimas 3 (2016 m. lapkričio naujinimas) |
| Įdiegti karštąją pataisą KB 3207800.                                                                              | Šios karštosios pataisos leidžia priedus norite peržiūrėti mobiliojo ryšio kliento, tai yra įtraukti į Dynamics 365 operacijos platformos naujinimas 3 (2016 m. lapkričio naujinimas).           |
| Įdiegti karštąją pataisą KB 3208224.                                                                              | Paraiškos kodas mobiliojo ryšio tiekėjo SF patvirtinimo taikymo tai yra įtrauktas į Microsoft Dynamics AX programos, 7.0.1 (2016 m. gegužės).                          |
| "Android" arba "iOS" arba "Windows" įrenginį, kuriame yra įdiegta Dynamics "365" dėl veiklos mobiliojo ryšio programa | Viešbučių paieška: atitinkamų app Store app.                                                                                                                     |

## <a name="introduction"></a>Įžanga
Mobiliojo ryšio tiekėjo SF patvirtinimo reikia trijų karštosios pataisos, kurios yra nurodytos "Būtinosios sąlygos" skyriuje. Šias karštąsias pataisas nereikia numatyti SF patvirtinimo darbo sritis. Norėdami sužinoti, kokie darbo sritis yra dėl mobiliojo ryšio, skaityti mobiliojo ryšio vadovas, paminėtam skyriuje "Būtinosios sąlygos". Turi būti suprojektuota SF patvirtinimo darbo sritį. 

Kiekviena organizacija užprogramuoja ir skirtingai apibrėžia savo verslo procesų tiekėjo SF. Prieš kurdami mobiliuoju patirtis tiekėjo SF liudijimui gauti, jūs turėtumėte apsvarstyti verslo proceso aspektai. Idėja yra naudoti šiuos duomenų taškų, kiek įmanoma optimizuoti vartotojų patirtį prietaiso.

-   Kokius laukus iš SF antraštėje vartotojas norės pamatyti mobiliojo patirtį ir kokia tvarka?
-   Kokius laukus iš SF eilutes vartotojas norės pamatyti mobiliojo patirtį ir kokia tvarka?
-   Kiek SF eilutes ar sąskaitą faktūrą? Taikyti 80-20 taisyklė čia, ir optimizuoti 80 procentų.
-   Vartotojai norite matyti apskaitos paskirstymo (SF kodavimo) mobiliajame įrenginyje per atsiliepimai? Jei atsakymas į šį klausimą yra "taip", Apsvarstykite šiuos klausimus:
    -   Kiek apskaitos paskirstymo (išplėstas kaina, PVM, mokesčiai, įskilimų ir t.t.) yra SF eilutei? Vėlgi, taikoma 80-20 taisyklė.
    -   Ar sąskaitos faktūros taip pat turi apskaitos paskirstymo SF antraštės? Jei taip, šios apskaitos distribucijos reikėtų pateikti prietaisą?

> [!NOTE]
> Šioje temoje nepaaiškina kaip redaguoti apskaitos paskirstymo, kadangi šiuo metu šios funkcijos nepalaiko mobiliojo ryšio scenarijų.

-   Vartotojai norite pamatyti priedus SF įrenginyje?

Mobiliojo ryšio sąskaitos faktūros patvirtinimų patirtį dizaino skirsis pagal atsakymus į šiuos klausimus. Tikslas – optimizuoti vartotojo patirtį verslo procesų mobiliesiems organizacijoje. Kitose šią temą, mes pažvelgti į du scenarijaus variantus, pagal skirtingus atsakymus į pirmiau pateiktus klausimus. 

Kaip bendrąsias gaires, dirbant su Mobilus dizaineris, įsitikinkite, kad "publikuoti" pakeitimus, norint neprarasti naujinimus.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Projektuojant paprastas SF patvirtinimo scenarijų Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarijaus atributas</th>
<th>Atsakymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kokius laukus iš SF antraštėje vartotojas norės pamatyti mobiliojo patirtį ir kokia tvarka?</td>
<td><ol>
<li>Tiekėjo vardas</li>
<li>Bendroji SF suma</li>
<li>Mokėtojo kodas</li>
<li>SF numeris</li>
<li>Data</li>
<li>SF aprašas</li>
<li>Terminas</li>
<li>SF valiuta</li>
</ol></td>
</tr>
<tr class="even">
<td>Kokius laukus iš SF eilutes vartotojas norės pamatyti mobiliojo patirtį ir kokia tvarka?</td>
<td><ol>
<li>Įsigijimo kategorija</li>
<li>Kiekis</li>
<li>Vnt. kaina</li>
<li>Grynoji eilutės suma</li>
<li>1099 suma</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kiek SF eilutes ar sąskaitą faktūrą? Taikyti 80-20 taisyklė čia, ir optimizuoti 80 procentų.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Vartotojai norite matyti apskaitos paskirstymo (SF kodavimo) mobiliajame įrenginyje per atsiliepimai?</td>
<td>Taip</td>
</tr>
<tr class="odd">
<td>Kiek apskaitos paskirstymo (išplėstas kaina, PVM, mokesčiai ir t.t.) yra SF eilutei? Vėlgi, taikoma 80-20 taisyklė.</td>
<td>Išplėstinė kainos: 2 PVM: 0 mokesčiai: 0</td>
</tr>
<tr class="even">
<td>Ar sąskaitos faktūros taip pat turi apskaitos paskirstymo SF antraštės? Jei taip, šios apskaitos distribucijos reikėtų pateikti prietaisą?</td>
<td>Nenaudojama</td>
</tr>
<tr class="odd">
<td>Vartotojai norite pamatyti priedus SF įrenginyje?</td>
<td>Taip</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Sukurti darbo sritį

1.  Naršyklėje atidarykite Dynamics 365 operacijoms ir prisijunkite.
2.  Po to, kai prisijungsite, pridėti **& režimas = mobiliojo** kaip parodyta toliau pavyzdys, ir atnaujinti puslapio URL: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& režimas = mobiliojo**
3.  Spustelėkite į **parametrai** (pavarų) mygtuką viršutiniame dešiniajame puslapio, ir tada spustelėkite **mobiliesiems**. Mobilioji programėlė dizaineris turi rodomi kaip Diktofonas pasirodo užduočių.
4.  Spustelėkite **pridėti** sukurti naują darbo sritį. Pavyzdžiui, pavadinimas darbo srities **mano patvirtinimų**.
5.  Įvesti aprašymą.
6.  Pasirinkite darbo srities spalvą. Darbo srityje spalva bus naudojamas bendras stilius mobiliojo patirtį šioje darbo srityje.
7.  Pasirinkite darbo srities piktogramą.
8.  Spustelėkite **padaryta**
9.  Spustelėkite **skelbti darbo srities** Išsaugoti pakeitimus

### <a name="vendor-invoices-assigned-to-me"></a>Man priskirtos tiekėjo SF

Pirmąjį mobilųjį puslapį, kuriame turite sukurti yra SF, kurios yra priskirtas vartotojo peržiūros sąrašas. Maketuoti šį mobilųjį puslapį, naudokite su **VendMobileInvoiceAssignedToMeListPage** Dynamics 365 operacijų puslapį. Prieš užbaigdami šią procedūrą, įsitikinkite, kad bent vieną tiekėjo SF yra priskirtas jūsų peržiūrai, ir kad SF eilutė turi du paskirstymo. Šis nustatymas atitinka šį scenarijų.

1.  Dynamics "365" dėl operacijų URL, pakeisti pavadinimą, meniu elementas su **VendMobileInvoiceAssignedToMeListPage** atidaryti mobili versija su **tol, kol bus paskirtas man tiekėjo SF** sąrašo puslapį ir **mokėtinos sumos** modulis. Priklausomai nuo jūsų sistemoje priskirtas jūsų sąskaitų-faktūrų, šiame puslapyje bus parodyti šios sąskaitos faktūros. Norėdami rasti konkrečią SF, galite naudoti filtrą į kairę. Tačiau, mums nereikia į konkrečią SF šiame pavyzdyje. Mes tiesiog reikia kai jums priskirti SF, kuri leidžia jums sukurti puslapio mobiliems įrenginiams. Naujus puslapius, kurie yra prieinami jau buvo sukurta specialiai sukurti mobiliojo ryšio tiekėjo SF scenarijai. Todėl, turite naudoti šiuose puslapiuose. URL turi būti panaši į šią nuorodą ir įvedę jį, puslapio, kuriame yra pavaizduota paveiksle, turi būti: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& režimas = mobiliojo [![tol, kol bus paskirtas man tiekėjo SF psl.](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Spustelėkite į **parametrai** (pavarų) mygtuką viršutiniame dešiniajame puslapio, ir tada spustelėkite **mobiliąją programėlę**
3.  Pasirinkite savo darbo sritį ir spustelėkite **redaguoti**
4.  Spustelėkite **pridėti puslapį** sukurti pirmąjį mobilųjį puslapį.
5.  Įveskite pavadinimą, pvz., **mano tiekėjo SF**, ir aprašymas, pvz., **paskirtas man peržiūrėti tiekėjo SF**.
6.  Spustelėkite **atlikti**.
7.  Mobilus dizaineris, apie į **laukus** skirtuką, spustelėkite **pasirinkite laukus,**. Stulpelius puslapyje sąrašas turi panašios į šį paveikslėlį. [![Laukianti SF stulpelių paskirtas man puslapis](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Pridėti reikiami stulpeliai iš sąrašo puslapio, kuriame turi būti pranešta vartotojams mobiliųjų puslapyje. Kai pridedate tvarka yra tvarka, kuris bus rodomas laukų galutiniam vartotojui. Vienintelis būdas pakeisti užsakymo laukai bus iš naujo pasirinkite Visi laukai. Pagal šį scenarijų reikalavimus, šių aštuonių laukai yra privalomi. Tačiau, kai kurie vartotojai gali apsvarstyti aštuoni laukai per daug informacijos, kad mobiliajame įrenginyje. Todėl mes parodysime tik patys svarbiausi laukai mobiliojo sąrašo rodinyje. Likusieji laukai bus rodomi išsamios informacijos rodinį, kad mes bus sukurti vėliau. Dabar, mes pridėti šiuos laukus. Spustelėkite pliuso ženklą (**+**), šių stulpelių pridėti prie puslapio mobiliems įrenginiams.
    1.  Tiekėjo vardas
    2.  Bendroji SF suma
    3.  Mokėtojo kodas
    4.  SF numeris
    5.  Data

    Pridėjus laukus, puslapio mobiliems įrenginiams turi panašios į šį paveikslėlį. [![Puslapis po laukai pridedami](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Turite taip pat įtraukti šiuos stulpelius dabar, taip, kad vėliau galėtume leisti darbo eigos veiksmai.
    1.  Rodyti visas užduotis
    2.  Rodyti deleguoti užduotį
    3.  Rodyti atšaukti užduotį
    4.  Rodyti atmesti užduotis
    5.  Rodyti prašymą užbaigti užduotį
    6.  Rodyti iš naujo pateikti užduotį

10. Spustelėkite **padaryti** į išeikite iš redagavimo režimo.
11. Spustelėkite **atgal** ir tada **padaryti** išeiti iš darbo
12. Spustelėkite **skelbti darbo srities** įrašyti savo darbą.
13. Įgalinti **ekranas SF sumuoti laukdama tiekėjo SF, sąrašas** sąskaitų formos mokėtinų sumų parametrai pagal **SF**. Atkreipkite dėmesį, kad tik suteikiant šį parametrą SF sumos apskaičiuojamas bus rodomas puslapyje laukianti SF sąrašas. Tai naujų pajėgumų kaip išankstinė sąlyga karštoji pataisa 3208224.

### <a name="vendor-invoice-details"></a>Tiekėjo SF duomenys

Išskirtinio dizaino Mobilus sąskaitos faktūros informacijos puslapį, naudokite su **VendMobileInvoiceHeaderDetails** Dynamics 365 operacijų puslapį. Atkreipkite dėmesį, kad, atsižvelgiant į sąskaitas, kad jūs turite savo sistemą, skaičių, šiame puslapyje bus nurodyti seniausia sąskaitą faktūrą (sąskaitą faktūrą, kuri buvo sukurta pirmiausia). Norėdami rasti konkrečią SF, galite naudoti filtrą į kairę. Tačiau, mums nereikia į konkrečią SF šiame pavyzdyje. Tik reikalaujame tam tikri SF duomenys, kad galime suprojektuoti puslapio mobiliems įrenginiams. [![Darbo eigos puslapyje](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Dynamics "365" dėl operacijų URL, pakeisti pavadinimą, meniu elementas su **VendMobileInvoiceHeaderDetails** Norėdami atidaryti formą
2.  Atidaryti Mobilus dizaineris iš to **parametrai** (pavarų) mygtuką.
3.  Spustelėkite į **redaguoti** mygtuką, Norėdami pradėti redagavimo režimą darbo srityje.
4.  Pasirinkite į ** mano tiekėjo SF ** puslapio, kurį sukūrėte anksčiau, ir tada spustelėkite **redaguoti**.
5.  Dėl į **laukus** skirtuko lape spustelėkite, **tinklelį** stulpelio antraštę.
6.  Spustelėkite **ypatybės**&gt;**pridėti puslapį**. **Pastaba:** jums spustelėjus, **tinklelį** pozicijoje ir pridėti puslapį, santykiai su informacijos puslapis sukuriamas automatiškai.
7.  Įveskite puslapio pavadinimas, pvz., **SF duomenys**, ir aprašymas, pvz., **peržiūrėti SF antraštėje ir eilutės informaciją**.
8.  Spustelėkite **pasirinkite laukus,**. Atkreipkite dėmesį, kad, siekiant įtraukti užsakymo, kuris bus rodomas laukų galutiniam vartotojui. Vienintelis būdas pakeisti užsakymo laukai bus iš naujo pasirinkite Visi laukai.
9.  Pridėti šiuos laukus iš antraštės, reikalavimai pagal šį scenarijų:
    1.  Tiekėjo vardas
    2.  Bendroji SF suma
    3.  Mokėtojo kodas
    4.  SF numeris
    5.  Data
    6.  SF aprašas
    7.  Terminas
    8.  SF valiuta

10. Pridėti šiuos laukus iš linijų tinklelis puslapyje:
    1.  Įsigijimo kategorija
    2.  Kiekis
    3.  Vnt. kaina
    4.  Grynoji eilutės suma
    5.  1099 suma

11. Pridėjus visus ankstesnius veiksmus laukai, spustelėkite **atlikti**. Puslapio turi panašios į šį paveikslėlį. [![Puslapis po laukai pridedami](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Spustelėkite **padaryti** į išeikite iš redagavimo režimo.
13. Spustelėkite **atgal** ir tada **padaryti** išeiti iš darbo
14. Spustelėkite **skelbti darbo srities** įrašyti savo darbą

### <a name="workflow-actions"></a>Darbo eigos veiksmai

Pridėti darbo eigos veiksmai, naudokite su **VendMobileInvoiceHeaderDetails** Dynamics 365 operacijų puslapį. Atidarykite šį puslapį, pakeisti pavadinimą meniu elemento URL, kaip jūs veikėte anksčiau. Tada atidarykite Mobilus dizaineris iš to **parametrai** (pavarų) mygtuką. Atlikite šiuos veiksmus ir pridėkite darbo eigos veiksmai išsamios informacijos puslapyje.

1.  Spustelėkite į **redaguoti** mygtuką, Norėdami pradėti redagavimo režimą darbo srityje.
2.  Pasirinkite į **SF duomenys** puslapyje, kurį sukūrėte anksčiau, ir tada spustelėkite **redaguoti**.
3.  Dėl į **veiksmai** skirtuką, spustelėkite **aukti veiksmą**.
4.  Įvesti veiklos pavadinimą, pvz., **tvirtinti**, ir aprašymas, pvz., **tvirtinti SF**. Atkreipkite dėmesį, kad veiksmo pavadinimas, kurią čia įvesite tampa pavadinimą, veiksmo, kuris yra rodomas naudotojui mobiliąja programa.
5.  Spustelėkite **atlikti**.
6.  Spustelėkite **pasirinkite laukus,**.
7.  Eiti per darbo eigos procesas ir **VendMobileInvoiceHeaderDetails** puslapyje, ir jūsų norimą įrašyti veiksmui atlikti. Įsitikinkite, kad įvedėte darbo eigos komentarai šio proceso metu, kad komentarų laukelyje taip pat įtraukta į mobiliojo patirtį.
8.  Paleidus darbo eigos veiksmai, spustelėkite **padaryti** pasirinkite laukų užduotį.
9.  Spustelėkite **padaryti** į išeikite iš redagavimo režimo.
10. Spustelėkite **atgal** ir tada **padaryti** išeiti iš darbo
11. Spustelėkite **skelbti darbo srities** įrašyti savo darbą
12. Pakartokite veiksmus nuo 3 iki 11 įrašyti visas reikalingas darbo eigos veiksmai. Atkreipkite dėmesį, kad, tai yra reikalavimas turėti sąskaitas-faktūras jums priskirti, jiems to padaryti darbo eigos veiksmai jums, kad jūs ketinate kurti.
13. Atidarykite užrašinę arba Microsoft Visual Studio ir įklijuokite šį kodą. Įrašykite failą kaip .js rinkmenas. Šį kodą daro du dalykus:
    1.  Ji slepia papildomų darbo eigos susijusių stulpelius, kuriuos mes pridėjome anksčiau mobiliojo sąrašo puslapyje. Mes pridėjome šių stulpelių, kad programa turi tą informaciją kontekste ir galite atlikti kitą žingsnį.
    2.  Atsižvelgiant į darbo eigos žingsnis, kuris yra aktyvus, jis taikomas logika rodo tik tuos veiksmus.

Atkreipkite dėmesį, kad, pavadinimą, puslapių ir kitų valdiklių JS kodas turi būti tas pats iš darbo srities.

1.  (metadataService, DataServic, cacheService, $q) pagrindinė funkcija {grįžti {appInit: funkcija (appMetadata) {/ / slėpti valdiklius, kurie turi būti pateikti, bet nesimato metadataService.configureControl ("mano-tiekėjo-SF, 'ShowAccept', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowApprove', {paslėpti: tiesa}); metadataService.configureControl ("mano-tiekėjo-SF, 'ShowReject', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowDelegate', {paslėpti: tiesa}); metadataService.configureControl ("mano-tiekėjo-SF, 'ShowRequestChange', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowRecall', {paslėpti: tiesa}); metadataService.configureControl ("mano-tiekėjo-SF, 'ShowComplete', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowResubmit', { paslėpti: tiesa}); }, pageInit: funkcija (pageMetadata, params) {jei (pageMetadata.Name == "SF duomenys") {/ / Rodyti/slėpti darbo eigos veiksmai, atsižvelgiant į darbo eigos žingsnis metadataService.configureAction ("Priimti", {matomas: tiesa}); metadataService.configureAction ("Patvirtinti", {matomas: tiesa}); metadataService.configureAction ("Atmesti", {matomas: tiesa}); metadataService.configureAction ('Atstovas', {matomas: tiesa}); metadataService.configureAction ("prašymą pakeisti", {matomas: tiesa}); metadataService.configureAction ("Atšaukti", {matomas: tiesa}); metadataService.configureAction ("Pilnas", {matomas: tiesa}); metadataService.configureAction ("pateikti", iš naujo {matomas: tiesa});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  Įkelti failą kodą į darbinę sritį pasirinkę ir **logika** skirtukas
3.  Spustelėkite **padaryti** į išeikite iš redagavimo režimo.
4.  Spustelėkite **atgal** ir tada **padaryti** išeiti iš darbo
5.  Spustelėkite **skelbti darbo srities** įrašyti savo darbą

### <a name="vendor-invoice-attachments"></a>Tiekėjo sąskaitos-faktūros priedai

1.  Spustelėkite į **parametrai** (pavarų) mygtuką viršutiniame dešiniajame puslapio, ir tada spustelėkite **mobiliąją programėlę**
2.  Spustelėkite į **redaguoti** mygtuką, Norėdami pradėti redagavimo režimą darbo srityje.
3.  Pasirinkite į ** SF duomenys ** puslapio, kurį sukūrėte anksčiau, ir tada spustelėkite **redaguoti**.
4.  Nustatyti, **dokumentų ruošimas** į **taip** kaip parodyta žemiau. **Pastaba:** jei nėra jokių reikalavimų parodyti priedai mobiliajame įrenginyje, galite palikti šią parinktį nustatyti **Nr**, kuris yra numatytasis parametras.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Spustelėkite **padaryti** į išeikite iš redagavimo režimo.
7.  Spustelėkite **atgal** ir tada **padaryti** išeiti iš darbo
8.  Spustelėkite **skelbti darbo srities** įrašyti savo darbą

### <a name="vendor-invoice-line-distributions"></a>Tiekėjo sąskaitos-faktūros eilutėje distribucijos

Šiuo atveju reikalavimai patvirtinti, kad bus tik eilutės lygio paskirstymo, ir kad sąskaita faktūra visada turi tik vieną eilutę. Todėl, kad šis scenarijus yra paprasta, vartotojo patirtis mobiliajame įrenginyje turi būti gana paprasta, kad vartotojas neturi detalizuoti keliais lygmenimis Peržiūrėkite paskirstymo. Tiekėjo SF Dynamics 365 operacijoms, numatyta galimybė, kad rodo visos distribucijos iš SF antraštės. Ši patirtis yra tai, ko mums reikia už mobiliojo ryšio scenarijų. Todėl, mes naudosime ir **VendMobileInvoiceAllDistributionTree** puslapio dizainas šiuo mobilųjį scenarijaus dalis. 

> [!NOTE] 
> Žinant reikalavimai padeda mums nuspręsti, kurį konkretų puslapį naudoti ir kaip tiksliai optimizuoti mobiliojo ryšio vartotojo patirtį, kai mes projektuojame pagal scenarijų. Pagal antrąjį scenarijų, mes naudojame kitą puslapį parodyti distribucijos, nes to scenarijaus reikalavimai skiriasi.

1.  URL, pakeisti pavadinimą, meniu elementą, kaip jūs veikėte anksčiau. Rodomame puslapyje turėtų panašios į šį paveikslėlį. [![Visi paskirstymo puslapis](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Atidaryti Mobilus dizaineris iš to **parametrai** (pavarų) mygtuką.
3.  Spustelėkite į **redaguoti** mygtuką, Norėdami pradėti redagavimo režimą darbo srityje. **Pastaba:** jūs pamatysite, kad du nauji puslapiai buvo sukurta automatiškai. Sistema sukuria šiuose puslapiuose, nes įjungtas dokumentų valdymas ankstesniame skyriuje. Jūs galite ignoruoti šiuos naujus puslapius.
4.  Spustelėkite **pridėti puslapį**.
5.  Įveskite puslapio pavadinimas, pvz., **Rodyti apskaitos**, ir aprašymas, pvz., **View apskaitos SF**.
6.  Spustelėkite **atlikti**.
7.  Dėl į **laukus** skirtuką, spustelėkite **pasirinkite laukus**, pasirinkite šiuos laukus iš distribucijos puslapio, ir tada spustelėkite **padaryti**:
    1.  Suma
    2.  Valiuta
    3.  DK sąskaita

> [!NOTE] 
> Mes ne pasirinkti, **Aprašymas** stulpelį iš paskirstymo tinklelį, nes tokiu reikalavimus patvirtino, kad išplėstas kaina yra tik suma, kuri bus paskirstymo. Todėl vartotojas nereikalaus kitam laukui nustatyti sumos tipas, skirtas platinti. Tačiau pagal kitą scenarijų, mes **bus** naudoti šią informaciją, nes šį scenarijų reikalavimai nurodyti, kad kitokio dydžio turėti distribucijos (pvz., PVM).
8.  Spustelėkite **padaryti** į išeikite iš redagavimo režimo.
9.  Spustelėkite **atgal** ir tada **padaryti** išeiti iš darbo
10. Spustelėkite **skelbti darbo srities** įrašyti savo darbą

**Pastaba:** ir **View apskaitos** mobiliojo puslapis šiuo metu nėra susijęs nė su viena mobiliųjų puslapių, kuriuose mes sukūrėme iki šiol. Nes vartotojas turėtų galėti naudotis į **Rodyti apskaitos** puslapis iš į **SF duomenys** puslapis mobiliajame įrenginyje, mes teikiame navigacijos į **SF duomenys** pereiti į **Rodyti apskaitos** puslapis. Mes nustatyti šią navigaciją naudojant papildomą logika per JavaScript.

1.  .Js failą, kurį sukūrėte anksčiau, ir pridėti eilutes, kurios yra paryškinti šį kodą. Šį kodą daro du dalykus:
    1.  Tai padeda užtikrinti, kad vartotojai negali vykti tiesiai iš darbo sritį, kad į **View apskaitos** puslapis.
    2.  Ji nustato navigacijos sistema iš į **SF duomenys** pereiti į **Rodyti apskaitos** puslapis.

> [!NOTE] 
> Puslapių ir kitų valdiklių JS kodas pavadinimas turi būti tas pats iš darbo srities.

1.  (metadataService, DataServic, cacheService, $q) pagrindinė funkcija {grįžti {appInit: funkcija (appMetadata) {/ / slėpti valdiklius, kurie turi būti pateikti, bet nesimato metadataService.configureControl ("mano-tiekėjo-SF, 'ShowAccept', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowApprove', {paslėpti: tiesa}); metadataService.configureControl ("mano-tiekėjo-SF, 'ShowReject', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowDelegate', {paslėpti: tiesa}); metadataService.configureControl ("mano-tiekėjo-SF, 'ShowRequestChange', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowRecall', {paslėpti: tiesa}); metadataService.configureControl ("mano-tiekėjo-SF, 'ShowComplete', {paslėpti: tiesa}); metadataService.configureControl (" mano-tiekėjo-SF, 'ShowResubmit', { paslėpti: tiesa}); Slėpti puslapių netaikoma šakninio navigacijos metadataService.hideNavigation('View-accounting'); Saitą Norėdami peržiūrėti apskaitos metadataService.addLink ("SF-duomenys" Rodyti apskaitos "," View-apskaitos-nav-kontrolės ', "Rodyti apskaitos", tiesa); }, pageInit: funkcija (pageMetadata, params) {jei (pageMetadata.Name == "SF duomenys") {/ / Rodyti/slėpti darbo eigos veiksmai, atsižvelgiant į darbo eigos žingsnis metadataService.configureAction ("Priimti", {matomas: tiesa}); metadataService.configureAction ("Patvirtinti", {matomas: tiesa}); metadataService.configureAction ("Atmesti", {matomas: tiesa}); metadataService.configureAction ('Atstovas', {matomas: tiesa}); metadataService.configureAction ("prašymą pakeisti", {matomas: tiesa}); metadataService.configureAction ("Atšaukti", {matomas: tiesa}); metadataService.configureAction ("Pilnas", {matomas: tiesa}); metadataService.configureAction ("pateikti", iš naujo {matomas: tiesa});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  Įkelti failą kodą į darbinę sritį pasirinkę ir **logika** tab, jei norite perrašyti ankstesnį kodą
3.  Spustelėkite **padaryti** į išeikite iš redagavimo režimo.
4.  Spustelėkite **atgal** ir tada **padaryti** išeiti iš darbo
5.  Spustelėkite **skelbti darbo srities** įrašyti savo darbą

### <a name="validation"></a>Tikrinimas

Mobiliajame įrenginyje atidarykite programą ir prisijungti prie jūsų Dynamics 365 operacijų atveju. Įsitikinkite, kad jums prisijungti prie įmonės tais atvejais, kai tiekėjo SF priskiriami jums peržiūrai. Jūs galėsite atlikti šiuos veiksmus:

-   Matyti, **mano patvirtinimų** darbo srities.
-   Gręžti į **mano patvirtinimų** darbo srities ir pamatyti, kad **mano tiekėjo SF** puslapis.
-   Gręžti į **mano tiekėjo SF** puslapyje ir peržiūrėkite sąskaitas faktūras, kurie yra jums priskirti sąraše.
-   Gręžti į vieną iš sąskaitų faktūrų, ir peržiūrėti SF antraštės informaciją ir eilutės informaciją.
-   Išsamios informacijos puslapyje pateiktas saitas su priedais, ir naudokite šią nuorodą į priedų sąrašą naršyti ir Peržiūrėti priedus.
-   Išsamios informacijos puslapyje pateiktas saitas su į **Rodyti apskaitos** puslapyje, ir naudoti šią nuorodą, pereikite į paskirstymo puslapį ir peržiūrėti paskirstymo.
-   Išsamios informacijos puslapyje spustelėkite į **veiklos** meniu apačioje, ir atlikti darbo eigos veiksmai, kurie yra taikomi darbo eigos žingsnio.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Projektuojant sudėtingą SF patvirtinimo scenarijų fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarijaus atributas</th>
<th>Atsakymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kokius laukus iš SF antraštėje vartotojas norės pamatyti mobiliojo patirtį ir kokia tvarka?</td>
<td><ol>
<li>Tiekėjo vardas</li>
<li>Iš viso su PVM</li>
<li>Mokėtojo kodas</li>
<li>SF numeris</li>
<li>Data</li>
<li>SF aprašas</li>
<li>Terminas</li>
<li>SF valiuta</li>
</ol></td>
</tr>
<tr class="even">
<td>Kokius laukus iš SF eilutes vartotojas norės pamatyti mobiliojo patirtį ir kokia tvarka?</td>
<td><ol>
<li>Įsigijimo kategorija</li>
<li>Kiekis</li>
<li>Vnt. kaina</li>
<li>Grynoji eilutės suma</li>
<li>1099 suma</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kiek SF eilutes ar sąskaitą faktūrą? Taikyti 80-20 taisyklė čia, ir optimizuoti 80 procentų.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Vartotojai norite matyti apskaitos paskirstymo (SF kodavimo) mobiliajame įrenginyje per atsiliepimai?</td>
<td>Taip</td>
</tr>
<tr class="odd">
<td>Kiek apskaitos paskirstymo (išplėstas kaina, PVM, mokesčiai ir t.t.) yra SF eilutei? Vėlgi, taikoma 80-20 taisyklė.</td>
<td>Išplėstinė kainos: 2 PVM: 2 kainos: 2</td>
</tr>
<tr class="even">
<td>Ar sąskaitos faktūros taip pat turi apskaitos paskirstymo SF antraštės? Jei taip, šios apskaitos distribucijos reikėtų pateikti prietaisą?</td>
<td>Nenaudojama</td>
</tr>
<tr class="odd">
<td>Vartotojai norite pamatyti priedus SF įrenginyje?</td>
<td>Taip</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Pratimai

Šie sąlygų keitimai gali būti padaryta dėl scenarijaus autorius 1, reikalavimai pagal 2 scenarijų. Naudokite šią sekciją kaip pratybų, kad galėsite atlikti mokymosi tikslais.

1.  Nes daugiau SF eilutes, turėtų būti pateikti 2 scenarijus, šios konstrukcijos pakeitimai padės optimizuoti vartotojų patirtį mobiliajame įrenginyje:
    1.  O ne per˛iūri SF eilutės informacijos puslapyje (kaip 1 atvejis), vartotojai gali pasirinkti Rodyti eilutes atskirame mobiliojo puslapyje.
    2.  Nes daugiau nei vieną SF eilutės tikimasi tokiu atveju, jei į **VendMobileInvoiceAllDistributionTree** puslapyje yra naudojami kurti paskirstymo puslapio Mobile (kaip 1 atvejis), tai gali būti painu, kad vartotojas galėtų susieti pelno eilutėse. Todėl naudoti su **VendMobileInvoiceLineDistributionTree** puslapį ir distribucijos puslapio dizainas.
    3.  Idealiu atveju, paskirstymo turi būti rodoma sąskaitos-faktūros eilutę tokiu kontekste. Todėl įsitikinkite, kad vartotojas gali gręžti linijos iki paskirstymo psl. Naudoti puslapis nuorodą gebėjimą nustatyti gręžimo-per, kaip jūs antraštės ir informacijos puslapiai 1 scenarijus.

2.  Nes daugiau nei vieną sumą tikimasi distribucijos 2 scenarijaus atveju (PVM, mokesčiai ir t.t.), tai bus naudinga parodyti suma tipo aprašymas. (Mes praleisti šią informaciją pagal scenarijų 1.)

## <a name="conclusion"></a>Išvada
Mobiliųjų platformų ir taikymo galimybės leidžia sukurti mobiliojo ryšio scenarijų, kurie yra optimizuoti vartotojų bazę organizacijoje. Remiantis pavyzdžiais, kurie yra pateikti šioje temoje, galite išbandyti kitus variantus ir sukurti įvairių patirtimi, kad reikia.


