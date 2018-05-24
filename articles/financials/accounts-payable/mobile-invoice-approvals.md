---
title: "SF patvirtinimai mobiliąja programa"
description: "Šioje temoje pateikiamas praktinis mobiliųjų įrenginių scenarijų kūrimo metodas programoje „Dynamics 365 for Finance and Operations‟, pavyzdyje naudojant tiekėjo SF tvirtinimus mobiliuosiuose įrenginiuose."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fc1483285d6ec675637c013af4949b9c7acf92b3
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="mobile-invoice-approvals"></a>SF patvirtinimai mobiliąja programa

[!include [banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Finance and Operations“ mobiliųjų įrenginių galimybės verslo vartotojui suteikia galimybę kurti mobiliąją patirtį. Sudėtingesniais scenarijais platforma taip pat suteikia galimybę kūrėjams pagal poreikį galimybes išplėsti. Efektyviausias būdas susipažinti su kai kuriomis naujomis mobiliųjų įrenginių sąvokomis yra peržiūrėti kelių scenarijų kūrimo procesą. Šioje temoje pateikiamas praktinis mobiliųjų įrenginių scenarijų kūrimo metodas, pavyzdyje naudojant tiekėjo SF tvirtinimus mobiliuosiuose įrenginiuose. Ši tema turėtų padėti sukurti kitus scenarijų variantus ir pritaikyti žinias kitiems scenarijams, kurie nėra susiję su tiekėjo SF.

<a name="prerequisites"></a>Būtinieji komponentai
-------------

| Būtinoji sąlyga                                                                                            | aprašymas                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Išankstinis mobiliųjų įrenginių vadovo perskaitymas                                                                                |[Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| „Dynamics 365 for Finance and Operations“                                                                             | Aplinka, kurioje yra „Microsoft Dynamics 365 for Operations“ 1611 versijos ir „Microsoft Dynamics for Operations“ 3 platformos naujinimas (2016 m. lapkričio mėn.)                   |
| Įdiekite karštąsias pataisas KB 3204341.                                                                              | Užduočių įrašymo priemonė gali klaidingai įrašyti dvi išplečiamųjų dialogų komandas Uždaryti; tai įtraukta į „Dynamics 365 for Operations“ 3 platformos naujinį (2016 m. lapkričio mėn. naujinys) |
| Įdiekite karštąsias pataisas KB 3207800.                                                                              | Įdiegus šias karštąsias pataisas priedus galima peržiūrėti mobiliajame kliente; tai įtraukta į „Dynamics 365 for Operations“ 3 platformos naujinį (2016 m. lapkričio mėn. naujinys).           |
| Įdiekite karštąsias pataisas KB 3208224.                                                                              | Tiekėjo SF mobiliuosiuose įrenginiuose tvirtinimo programos kodas; tai įtraukta į „Microsoft Dynamics AX“ 7.0.1 programos versiją (2016 m. gegužės mėn.).                          |
| „Android“, „iOS“ arba „Windows“ įrenginys, kuriame įdiegta „Finance and Operations“ mobilioji programa | Ieškokite programos atitinkamoje programų parduotuvėje.                                                                                                                     |

## <a name="introduction"></a>Įžanga
Norint tiekėjo SF tvirtinti mobiliuosiuose įrenginiuose, reikia įdiegti tris karštąsias pataisas, paminėtas skyriuje „Būtinosios sąlygos“. Šios karštosios pataisos nepateikia SF tvirtinimo darbo srities. Norėdami sužinoti, kas yra darbo sritis mobiliųjų įrenginių kontekste, perskaitykite mobiliųjų įrenginių vadovą, paminėtą skyriuje „Būtinosios sąlygos“. SF tvirtinimo darbo sritį reikia sukurti. 

Kiekviena organizacija skirtingai planuoja ir nustato tiekėjo SF verslo procesą. Prieš kurdami tiekėjo SF tvirtinimo mobiliuosiuose įrenginiuose patirtį, atsižvelkite į toliau nurodytus verslo proceso aspektus. Tikslas yra kiek įmanoma labiau naudoti šiuos duomenų taškus ir optimizuoti vartotojo patirtį mobiliajame įrenginyje.

-   Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?
-   Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?
-   Kiek SF yra SF eilučių? Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.
-   Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)? Jei atsakymas į šį klausimą yra teigiamas, atsižvelkite į tolesnius klausimus.
    -   Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos, skaidymai ir t. t.)? Vėl taikykite 80 / 20 taisyklę.
    -   Ar SF antraštėje taip pat yra apskaitos paskirstymų? Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?

> [!NOTE]
> Šioje temoje nepaaiškinama, kaip redaguoti apskaitos paskirstymus, nes mobiliųjų įrenginių scenarijuose ši funkcija šiuo metu nepalaikoma.

-   Ar vartotojai įrenginyje norės matyti SF priedus?

SF tvirtinimo mobiliuosiuose įrenginiuose patirties kūrimas skirsis, priklausomai nuo atsakymų į šiuos klausimus. Tikslas yra optimizuoti organizacijos verslo proceso valdymo mobiliuosiuose įrenginiuose vartotojo patirtį. Likusioje šios temos dalyje peržiūrėsime du scenarijų variantus, kurie pagrįsti skirtingais atsakymais į ankstesnius klausimus. 

Paprastai dirbant su mobiliųjų įrenginių dizaino įrankiu patariama nepamiršti publikuoti keitimų, kad neprarastumėte naujinimų.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>„Contoso“ paprasto SF tvirtinimo scenarijaus kūrimas
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
<td>Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</td>
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
<td>Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</td>
<td><ol>
<li>Įsigijimo kategorija</li>
<li>Kiekis</li>
<li>Vnt. kaina</li>
<li>Grynoji eilutės suma</li>
<li>1099 suma</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kiek SF yra SF eilučių? Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</td>
<td>Taip</td>
</tr>
<tr class="odd">
<td>Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos ir t. t.)? Vėl taikykite 80 / 20 taisyklę.</td>
<td>Išplėstinė kaina: 2 PVM: 0 Išlaidos: 0</td>
</tr>
<tr class="even">
<td>Ar SF antraštėje taip pat yra apskaitos paskirstymų? Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</td>
<td>Nenaudojama</td>
</tr>
<tr class="odd">
<td>Ar vartotojai įrenginyje norės matyti SF priedus?</td>
<td>Taip</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Darbo srities kūrimas

1.  Naršyklėje atidarykite „Finance and Operations“ ir prisijunkite.
2.  Prisijungę pridėkite dalį **&mode=mobile** prie URL, kaip parodyta tolesniame pavyzdyje, ir atnaujinkite puslapį: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**. Mobiliųjų programų dizaino įrankis pasirodo taip, kaip pasirodo užduočių įrašymo priemonė.
4.  Spustelėkite **Įtraukti**, kad sukurtumėte naują darbo sritį. Šiuo atveju darbo sritį pavadinkite **Mano tvirtinimai**.
5.  Įvesti aprašymą.
6.  Pasirinkti darbo srities spalvą. Darbo srities spalva bus naudojama bendram šios darbo srities mobiliosios patirties stiliui kurti.
7.  Pasirinkite darbo srities piktogramą.
8.  Spustelėkite **Atlikta**
9.  Spustelėkite **Publikuoti darbo sritį**, kad išsaugotumėte keitimus

### <a name="vendor-invoices-assigned-to-me"></a>Man priskirtos tiekėjo SF

Pirmasis mobiliųjų įrenginių puslapis, kurį turėtumėte sukurti, yra SF, kurios priskirtos vartotojui peržiūrėti, sąrašas. Norėdami kurti šį mobiliųjų įrenginių puslapį, naudokite „Finance and Operations“ puslapį **VendMobileInvoiceAssignedToMeListPage**. Prieš baigdami šią procedūrą įsitikinkite, kad bent viena tiekėjo SF yra jums priskirta peržiūrėti ir kad SF eilutėje yra du paskirstymai. Ši sąranka atitinka šio scenarijaus reikalavimus.

1.  „Finance Operations“ URL pakeiskite meniu elemento pavadinimą į **VendMobileInvoiceAssignedToMeListPage**, kad atidarytumėte sąrašo puslapio **Man priskirtos laukiančios tiekėjo SF** mobiliąją versiją modulyje **Mokėtinos sumos**. Atsižvelgiant į SF, kurios jūsų sistemoje jums priskirtos, skaičių, šiame puslapyje bus rodomos tos SF. Norėdami rasi konkrečią SF, galite naudoti dešinėje pusėje pateiktą filtrą. Tačiau šiame pavyzdyje konkreti SF nėra reikalinga. Tereikia, kad jums būtų priskirta kokia nors SF, jog galėtumėte kurti mobiliųjų įrenginių puslapį. Nauji puslapiai, kuriuos galima naudoti, buvo specialiai sukurti tiekėjo SF mobiliųjų įrenginių scenarijams kurti. Todėl turite šiuos puslapius naudoti. URL turėtų būti toks, kaip toliau toliau, ir įvedus URL turi būti rodomas puslapis su iliustracija: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Puslapis Man priskirtos laukiančios tiekėjo SF](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**
3.  Pasirinkite savo darbo sritį ir spustelėkite **Redaguoti**.
4.  Spustelėkite **Įtraukti puslapį**, kad sukurtumėte pirmą mobiliųjų įrenginių puslapį.
5.  Įveskite pavadinimą, pvz., **Mano tiekėjo SF**, ir aprašą, pvz., **Man peržiūrėti priskirtos tiekėjo SF**.
6.  Spustelėkite **Atlikta**.
7.  Mobiliųjų įrenginių dizaino įrankio skirtuke **Laukai** spustelėkite **Pasirinkti laukus**. Šio sąrašo puslapio stulpeliuose turi būti tolesnėje iliustracijoje nurodyta informacija. [![Stulpeliai puslapyje Man priskirtos laukiančios tiekėjo SF](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  Iš sąrašo puslapio įtraukite reikiamus stulpelius, kurie vartotojams turi būti rodomi mobiliųjų įrenginių puslapyje. Galutiniam vartotojui laukai bus rodomi ta tvarka, kuria juos įtrauksite. Laukų tvarką galima pakeisti tik iš naujo pažymint visus laukus. Pagal šio scenarijaus reikalavimus reikalingi aštuoni toliau nurodyti laukai. Tačiau kai kuriems vartotojams aštuoni laukai gali pasirodyti per didelis informacijos kiekis mobiliajame įrenginyje. Todėl mobiliųjų įrenginių sąrašo rodinyje bus rodomi tik patys svarbiausi laukai. Likę laukai bus rodomi informacijos rodinyje, kurį sukursime vėliau. Dabar įtrauksime toliau nurodytus laukus. Spustelėkite šių stulpelių pliuso ženklą (**+**), kad įtrauktumėte į mobiliųjų įrenginių puslapį.
    - Tiekėjo vardas
    - Bendroji SF suma
    - Mokėtojo kodas
    - SF numeris
    - Data

    Įvedus laukus mobiliųjų įrenginių puslapyje turi būti rodoma tolesnėje iliustracijoje nurodyta informacija. 
    [![Puslapio rodinys įtraukus laukus](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  Taip pat dabar turite įtraukti tolesnius stulpelius, kad vėliau galėtumėte įjungti darbo eigos veiksmus.
    - Rodyti baigti užduotį
    - Rodyti perduoti užduotį
    - Rodyti atšaukti užduotį
    - Rodyti atmesti užduotį
    - Rodyti prašyti užpildymo užduoties
    - Rodyti iš naujo pateikti užduotį

10. Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.
11. Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.
12. Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą.
13. Mokėtinų sumų parametrų formoje, prie dalies **SF** įjunkite parinktį **Laukiančių tiekėjo SF sąraše rodyti bendrą SF sumą**. Atminkite, kad tik įjungus šį parametrą SF sumos bus apskaičiuotos ir rodomos laukiančių tiekėjo SF sąrašo puslapyje. Ši nauja galimybė yra būtinų karštųjų pataisų 3208224 dalis.

### <a name="vendor-invoice-details"></a>Tiekėjo SF informacija

Norėdami kurti sąskaitų faktūrų informacijos mobiliųjų įrenginių puslapį, naudokite „Finance and Operations“ puslapį **VendMobileInvoiceHeaderDetails**. Atminkite, kad, atsižvelgiant į SF, kurios sistemoje jums priskirtos, skaičių, šiame puslapyje rodoma seniausia SF (SF, kuri buvo sukurta pirmoji). Norėdami rasi konkrečią SF, galite naudoti dešinėje pusėje pateiktą filtrą. Tačiau šiame pavyzdyje konkreti SF nėra reikalinga. Tereikia kokių nors SF duomenų, kad galėtumėte kurti mobiliųjų įrenginių puslapį. [![Darbo eigos puslapis](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. „Finance and Operations“ URL pakeiskite meniu elemento pavadinimą įrašydami **VendMobileInvoiceHeaderDetails**, kad atidarytumėte formą
2. Atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.
3. Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.
4. Pasirinkite puslapį **Mano tiekėjo SF**, kurį sukūrėte anksčiau, tada spustelėkite **Redaguoti**.
5. Skirtuke **Laukai** spustelėkite stulpelio antraštę **Tinklelis**.
6. Spustelėkite **Ypatybės &gt; Įtraukti puslapį**. **Pastaba.** Kai spustelėjate antraštę **Tinklelis** ir įtraukiate puslapį, ryšys su informacijos puslapiu nustatomas automatiškai.
7. Įveskite puslapio pavadinimą, pvz., **SF informacija SF**, ir aprašą, pvz., **SF antraštės ir eilutės informacijos peržiūra**.
8. Spustelėkite **Pasirinkti laukus**. Atminkite, kad galutiniam vartotojui laukai bus rodomi ta tvarka, kuria juos įtrauksite. Laukų tvarką galima pakeisti tik iš naujo pažymint visus laukus. 
9. Iš antraštės įtraukite toliau nurodytus laukus, atsižvelgdami į šio scenarijaus reikalavimus.
   - Tiekėjo vardas
   - Bendroji SF suma
   - Mokėtojo kodas
   - SF numeris
   - Data
   - SF aprašas
   - Terminas
   - SF valiuta

10. Iš puslapio eilučių tinklelio įtraukite toliau nurodytus laukus.
    - Įsigijimo kategorija
    - Kiekis
    - Vnt. kaina
    - Grynoji eilutės suma
    - 1099 suma

11. Kai visi ankstesniuose dviejuose veiksmuose nurodyti laukai įtraukti, spustelėkite **Atlikta**. Puslapyje turi būti tolesnėje iliustracijoje nurodyta informacija.
    [![Puslapio rodinys įtraukus laukus](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.
13. Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.
14. Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą

### <a name="workflow-actions"></a>Darbo eigos veiksmai

Norėdami įtraukti darbo eigos veiksmų, naudokite „Finance and Operations“ puslapį **VendMobileInvoiceHeaderDetails**. Norėdami atidaryti šį puslapį, URL pakeiskite meniu elemento pavadinimą, kaip tai padarėte anksčiau. Tada atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**. Norėdami į informacijos puslapį įtraukti darbo eigos veiksmų, atlikite nurodytus veiksmus. Jums turi būti priskirta tam tikrą būseną turinčių sąskaitų faktūrų, jog kurdami galėtumėte naudoti darbo eigos veiksmus.

#### <a name="record-workflow-actions"></a>Darbo eigos veiksmų įrašymas
1.  Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.
2.  Pasirinkite puslapį **SF informacija**, kurį sukūrėte anksčiau, o tada spustelėkite **Redaguoti**.
3.  Skirtuke **Veiksmai** spustelėkite **Įtraukti veiksmą**.
4.  Įveskite veiksmo pavadinimą, pvz., **Tvirtinti**, tada įveskite aprašymą, pvz., **Tvirtinti SF**. Atkreipkite dėmesį, kad čia įvestas veiksmo pavadinimas tampa mobiliojoje programoje vartotojui rodomo veiksmo pavadinimu.
5.  Spustelėkite **Atlikta**.
6.  Spustelėkite **Pasirinkti laukus**.
7.  Atidarykite darbo eigos procesą puslapyje **VendMobileInvoiceHeaderDetails** ir užbaikite veiksmą, kurį norėjote įrašyti. Įsitikinkite, kad šio proceso metu įvedėte darbo eigos komentarus, kad į mobiliąją patirtį taip pat būtų įtrauktas komentarų laukas.
8.  Paleidę darbo eigos veiksmą, spustelėkite **Atlikta**, kad baigtumėte užduoti Pasirinkti laukus.
9.  Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.
10. Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.
11. Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą
12. Pakartodami ankstesnius veiksmus įrašykite visus reikiamus darbo eigos veiksmus. 

#### <a name="create-a-js-file"></a>.js failo kūrimas
1. Atidarykite „Notepad“ arba „Microsoft Visual Studio“ ir įklijuokite tolesnį kodą. Įrašykite failą kaip .js failą. Šis kodas atlieka šiuos veiksmus:
    - Jis paslepia papildomus su darbo eiga susijusius stulpelius, kuriuos į mobiliųjų įrenginių sąrašo puslapį mes įtraukėme anksčiau. Šiuos stulpelius mes įtraukėme, kad programai pateiktume informacijos kontekstą ir ji galėtų atlikti kitą veiksmą.
    - Atsižvelgiant į aktyvų darbo eigos veiksmą, jis pritaiko logiką, kad būtų rodomi tik tie veiksmai.

> [!NOTE]
> Kode nurodyti puslapių ir kitų valdiklių pavadinimai turi sutapti su pavadinimais darbo srityje.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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

2.  Įkelkite kodo failą į darbo sritį pasirinkdami skirtuką **Logika**
3.  Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.
4.  Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.
5.  Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą

### <a name="vendor-invoice-attachments"></a>Tiekėjo SF priedai

1. Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**
2. Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.
3. Pasirinkite puslapį <strong>SF informacija **, kurį sukūrėte anksčiau, o tada spustelėkite** Redaguoti</strong>.
4. Nustatykite parinkties **Dokumentų valdymas** reikšmę **Taip**, kaip parodyta toliau. **Pastaba.** Jei mobiliajame įrenginyje priedų rodyti nereikia, galite palikti nustatytą šios parinkties reikšmę **Ne**, kuri yra numatytasis nustatymas.
   ![Dokumentų tvarkymas](./media/docmanagement-216x300.png)
5. Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.
6. Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.
7. Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą

### <a name="vendor-invoice-line-distributions"></a>Tiekėjo SF eilutės paskirstymai

Šio scenarijaus reikalavimai patvirtina, kad bus vykdomi tik eilutės lygio paskirstymai ir kad SF visada turės tik vieną eilutę. Kadangi šis scenarijus yra paprastas, vartotojo patirtis mobiliajame įrenginyje taip pat turi būti pakankamai paprasta, kad paskirstymus norinčiam peržiūrėti vartotojui nereikėtų duomenų detalizuoti keliais lygiais. „Finance and Operations“ tiekėjo SF apima galimybę rodyti visus sąskaitos faktūros antraštės paskirstymus. Ši patirtis yra tai, ko mums reikia mobiliajame scenarijuje. Todėl norėdami kurti šią mobiliojo scenarijaus dalį naudosime puslapį **VendMobileInvoiceAllDistributionTree**. 

> [!NOTE] 
> Žinant reikalavimus galima lengviau nuspręsti, kurį konkretų puslapį naudoti ir kaip kuriant šį scenarijų optimizuoti vartotojo mobiliąją patirtį. Antruoju scenarijumi paskirstymams rodyti naudosime kitą puslapį, nes to scenarijaus reikalavimai skiriasi.

1.  URL pakeiskite meniu elemento pavadinimą, kaip tai padarėte anksčiau. Pasirodžiusiame puslapyje turi būti tolesnėje iliustracijoje nurodyta informacija.
[![Puslapis Visi paskirstymai](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.
3.  Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą. **Pastaba.** Pastebėsite, kad automatiškai sukurti du nauji puslapiai. Sistema šiuos puslapius kuria, ankstesniame skyriuje įjungėte dokumentų valdymo funkciją. Šiuos naujus puslapius galite ignoruoti.
4.  Spustelėkite **Įtraukti puslapį**.
5.  Įveskite puslapio pavadinimą, pvz., **Apskaitos peržiūra**, ir aprašą, pvz., **SF apskaitos peržiūra**.
6.  Spustelėkite **Atlikta**.
7.  Skirtuke **Laukai** spustelėkite **Pasirinkti laukus**, pasirinkite tolesnius laukus iš paskirstymų puslapio ir tada spustelėkite **Atlikta**.
    1.  Suma
    2.  Valiuta
    3.  DK sąskaita

    > [!NOTE] 
    > Paskirstymų tinklelio stulpelio **Aprašas** nepasirinkome, nes šio scenarijaus reikalavimai patvirtino, kad išplėstinė kaina yra vienintelė suma, kuri bus paskirstyta. Todėl paskirstymo sumos tipą norinčiam nustatyti vartotojui kito lauko nereikės. Tačiau kitame scenarijuje mes **naudosime** šią informaciją, nes to scenarijaus reikalavimai nurodo, kad yra nustatytų kitų tipų sumų paskirstymų (pvz., PVM).
8.  Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.
9.  Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.
10. Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą

> [!NOTE] 
> Mobiliųjų įrenginių puslapis **Apskaitos peržiūra** nėra susietas su jokiais iki šiol sukurtais mobiliųjų įrenginių puslapiais. Kadangi vartotojas privalo gebėti mobiliajame įrenginyje naršydamas iš puslapio **SF informacija** atidaryti puslapį **Apskaitos peržiūra**, turime pateikti nurodyti naršymą iš puslapio **SF informacija** į puslapį **Apskaitos peržiūra**. Šį naršymą nustatome naudodami papildomą logiką ir „JavaScript“.

1.  Atidarykite anksčiau sukurtą .js failą ir įtraukite toliau nurodytu kodu pažymėtas eilutes. Šio kodo paskirtys yra dvi.
    1.  Taip užtikrinama, kad naršydami puslapį **Apskaitos peržiūra** vartotojai negalės atidaryti darbo srities.
    2.  Sukuriamas naršymo iš puslapio **SF informacija** į puslapį **Apskaitos peržiūra** valdiklis.

> [!NOTE] 
> Kode nurodyti puslapių ir kitų valdiklių pavadinimai turi sutapti su pavadinimais darbo srityje.

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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

2.  Įkelkite kodo failą į darbo sritį pasirinkdami skirtuką **Logika**, kad perrašytumėte ankstesnį kodą
3.  Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.
4.  Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.
5.  Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą

### <a name="validation"></a>Tikrinimas

Iš mobiliojo įrenginio atidarykite programą ir prijunkite ją prie savo „Finance and operations“ egzemplioriaus. Įsitikinkite, kad prisijungėte prie įmonės, kurioje tiekėjo SF yra jums priskirtos peržiūrėti. Turėtumėte galėti atlikti tolesnius veiksmus.

-   Peržiūrėti darbo sritį **Mano tvirtinimai**.
-   Detalizuoti darbo sritį **Mano tvirtinimai** ir peržiūrėti puslapį **Mano tiekėjo SF**.
-   Detalizuoti puslapį **Mano tiekėjo SF** ir peržiūrėti jums priskirtų SF sąrašą.
-   Detalizuoti vieną iš SF ir peržiūrėti SF antraštės ir eilutės informaciją.
-   Informacijos puslapyje matyti saitą į priedus ir jį panaudojus atidaryti bei peržiūrėti priedų sąrašą.
-   Informacijos puslapyje matyti saitą į puslapį **Apskaitos peržiūra** ir jį panaudojus atidaryti bei peržiūrėti paskirstymų puslapį.
-   Informacijos puslapio apačioje spustelėti meniu **Veiksmai** ir atlikti darbo eigos veiksmus, kurie taikomi darbo eigos veiksmui.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Fabrikam sudėtingo SF tvirtinimo scenarijaus kūrimas
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
<td>Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</td>
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
<td>Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</td>
<td><ol>
<li>Įsigijimo kategorija</li>
<li>Kiekis</li>
<li>Vnt. kaina</li>
<li>Grynoji eilutės suma</li>
<li>1099 suma</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kiek SF yra SF eilučių? Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</td>
<td>Taip</td>
</tr>
<tr class="odd">
<td>Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos ir t. t.)? Vėl taikykite 80 / 20 taisyklę.</td>
<td>Išplėstinė kaina: 2 PVM: 2 Išlaidos: 2</td>
</tr>
<tr class="even">
<td>Ar SF antraštėje taip pat yra apskaitos paskirstymų? Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</td>
<td>Nenaudojama</td>
</tr>
<tr class="odd">
<td>Ar vartotojai įrenginyje norės matyti SF priedus?</td>
<td>Taip</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Kiti veiksmai

Galima vykdyti tolesnius 1 scenarijaus variantus, atsižvelgiant į 2 scenarijaus reikalavimus. Šį skyrių galite naudoti norėdami patobulinti mobiliosios programos patirtį.

1.  Kadangi 2 scenarijuje galima tikėtis daugiau SF eilučių, toliau nurodyti dizaino keitimai padės optimizuoti vartotojo patirtį mobiliajame įrenginyje.
    1.  Vartotojai gali pasirinkti peržiūrėti SF eilutes atskirame mobiliųjų įrenginių puslapyje, o ne informacijos puslapyje (1 scenarijaus atveju).
    2.  Kadangi šiame scenarijuje galima tikėtis daugiau SF eilučių, jei puslapis **VendMobileInvoiceAllDistributionTree** naudojamas mobiliųjų įrenginių paskirstymų puslapiui kurti (1 scenarijaus atveju), vartotojas gali nesuprasti, kaip eilutes susieti su paskirstymais. Todėl paskirstymų puslapiui kurti naudokite puslapį **VendMobileInvoiceLineDistributionTree**.
    3.  Geriausia šiame scenarijuje būtų paskirstymus rodyti SF eilutės kontekste. Todėl įsitikinkite, kad vartotojas gali detalizuoti eilutę ir peržiūrėti paskirstymų puslapį. Naudokite puslapio saito galimybę, kad nustatytumėte detalizavimo funkciją (kaip tai atlikote 1 scenarijuje nustatydami antraštės ir informacijos puslapių detalizavimo funkciją).

2.  Kadangi 2 scenarijuje tikimasi daugiau nei vieno tipo sumos paskirstymų (PVM, išlaidos ir t. t.), būtų naudinga parodyti sumos tipo aprašą. (1 scenarijuje šia informaciją praleidome.)





