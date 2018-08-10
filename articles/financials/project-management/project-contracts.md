---
title: Projekto sutartys
description: "Šioje temoje pateikiamos sutartys, kurias galite sukurti pagal įvairius bei lėšų skyrimo šaltinių tipus, pateikiami sutarčių pavyzdžiai ir paaiškinama, kaip galima „Microsoft Dynamics 365 for Finance and Operations“ valdyti sutartis ir klientams išrašyti sąskaitas faktūras."
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e46393b9ac8797bf12cca12099d177980b75ba38
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="project-contracts"></a>Projekto sutartys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamos sutartys, kurias galite sukurti pagal įvairius bei lėšų skyrimo šaltinių tipus, pateikiami sutarčių pavyzdžiai ir paaiškinama, kaip galima „Microsoft Dynamics 365 for Finance and Operations“ valdyti sutartis ir klientams išrašyti sąskaitas faktūras.

Jūsų sukurtas projekto sutarties tipas nustato metodą, kuris naudojamas išrašyti SF projekto klientams. Galite keisti projekto sutartį ir susijusį projektą, tačiau negalite keisti projekto tipo. 

Naudodami projekto sutartį, vienu metu galite išrašyti vieno arba kelių projektų SF. Projekto sutartis taip pat padeda užtikrinti nuoseklią SF išrašymo procedūrą kiekvienam projekto struktūros subprojektui. 

Kiekvienas projektas, kuriam bus išrašyta SF, turi būti susietas su projekto sutartimi. Projekto sutarties nuostatos taikomos visiems projektams ir subprojektams, susietiems su ta projekto sutartimi. 

Projekto sutartyje gali būti nurodytas vienas arba keli lėšų skyrimo šaltiniai. Todėl galite išskaidyti sąskaitų pateikimą keliems finansuotojams, nustatyti lėšų limitus, kad iš lėšų skyrimo šaltinių nebūtų išskaityta didesnė nei nurodyta suma, ir konfigūruoti lėšų skyrimo taisykles, taikomas išlaidų padengimui.

## <a name="funding-for-project-contracts"></a>Projektų sutarčių finansavimas
Kai kuriose projektų sutartyse nurodyta, kad projekto išlaidų finansavimo atsakomybe dalijasi kelios šalys. Štai keletas pavyzdžių:

-   Stambus klientas, turintis kelis padalinius, pageidauja, kad projekto finansavimas būtų išskaidytas pagal padalinį.
-   Jūsų įmonė stambaus projekto išlaidomis dalijasi su išorės organizacija.
-   Kelių projektą kartu finansuoja dvi savivaldybės.
-   Tilto projektą finansuoja vyriausybės subsidija ir privati korporacija.

Sprendime „Finance and Operations‟ sąskaitą už vieną operaciją ar visą projektą galite išskaidyti keliems klientams, subsidijoms ar organizacijoms. 

Projektuose, kuriuose yra keli finansuotojai, visos šalys, kurios prisideda prie išplėstinio finansavimo projekto, vadinamos finansavimo šaltiniais. Klientą, organizaciją ar subsidiją apibrėžus kaip finansavimo šaltinį, jį galima priskirti vienai ar kelioms finansavimo taisyklėms. Finansavimo taisyklėse yra kriterijai, kurie nustato, kaip išlaidos paskirstomos įvairiems projekto finansavimo šaltiniams. 

Kadangi atsargose laikomų prekių, pvz., rodomų pirkimo paraiškose ir pirkimo užsakymuose, išskaidyti negalima, platinant išlaidų sumos išskaidyti keliems finansavimo šaltiniams negalima. Todėl, kol užregistruojamas atsargų išdavimas, finansavimo šaltinio reikšmė lieka 0 (nulis). Užregistravus atsargų išdavimą, išlaidų suma paskirstoma atsižvelgiant į projekto sąskaitų paskirstymo taisykles.

Toliau nurodyti keletas veiksmų, kuriuos galite atlikti, kad būtų lengviau sąskaitas išskaidyti keliems finansavimo šaltiniams.

-   Nurodykite, kad visose įvedamose projekto operacijose būtų naudojama ta pati pardavimo valiuta, kaip ir projekto sutartyje.
-   Nustatykite finansavimo limitus, kad finansavimo šaltiniui nebūtų išrašyta SF už didesnę nei nurodyta projekto sumą.
-   Sukonfigūruokite kiekvieno darbuotojo, prekės, kategorijos, kategorijų grupės ir operacijos tipo (ar visų operacijų tipų) finansavimo taisykles ir finansavimo limitus.
-   Pasirinkite pasirinktines pradžios ir pabaigos datas, kad apibrėžtumėte laikotarpį, kada galioja kiekviena finansavimo taisyklė.
-   Nurodykite procentą, už kurį atsakingas kiekvienas finansavimo šaltinis.
-   Nurodykite, kuris lėšų skyrimo šaltinis yra atsakingas už apvalinimo skirtumus, atsiradusius skaičiuojant finansavimo paskirstymą.
-   Nustatykite taisykles, nustatančias, kaip SF už projekto išlaidas išrašomos išoriniams klientams ir pateikiamos apmokėti vidinėms organizacijoms.
-   Operacijas įrašykite sulaikyto lėšų skyrimo sąskaitoje, kol bus galima gauti papildomų lėšų, arba kol nuspręsite apmokėti išlaidas viduje.

Norint nustatyti, kurią mokesčių grupę susieti su operacija, projekte ieškoma mokesčių grupės priskyrimo. Jei projekto lygiu nepriskirta jokia mokesčių grupė, ieškoma projekto sutarties.

### <a name="example-multiple-funding-sources-simple"></a>Pavyzdys: keli lėšų skyrimo šaltiniai (paprast.)

Toliau pateiktoje lentelėje pateikiami finansavimo paskirstymo keliems finansavimo šaltiniams valdymo scenarijai. Šie scenarijai paremti toliau nurodytomis prielaidomis.

-   Prieš taikant kitus lėšų skyrimo taisyklių kriterijus, paskirstant lėšas įtraukiamos prioritetų nuostatos.
-   Nenurodytas joks datų intervalas, todėl neapibrėžtas laikotarpis, kada lėšų skyrimo taisyklė galioja.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenarijus</strong></td>
<td><strong>Lėšų skyrimo šaltinis </strong></td>
<td><strong>Paskirstymo procentas </strong></td>
<td><strong>Paskirstymo prioritetas </strong></td>
</tr>
<tr class="even">
<td>Norite išlaidas paskirstyti vienam lėšų skyrimo šaltiniui, kol baigsis jo lėšos, išlaidas paskirstyti antram lėšų skyrimo šaltiniui, kol baigsi jo lėšos ir galiausiai likusias išlaidas paskirstyti trečiam lėšų skyrimo šaltiniui.</td>
<td><ul>
<li>1　finansavimo　šaltinis</li>
<li>2　finansavimo　šaltinis</li>
<li>3　finansavimo　šaltinis</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Norite 75 procentus išlaidų paskirstyti vienam lėšų skyrimo šaltiniui ir 25 procentus – antram lėšų skyrimo šaltiniui. Kai viename iš šių lėšų skyrimo šaltinių baigiasi lėšos, likusias išlaidas norite apmokėti iš trečio lėšų skyrimo šaltinio.</td>
<td><ul>
<li>1　finansavimo　šaltinis</li>
<li>2　finansavimo　šaltinis</li>
<li>3　finansavimo　šaltinis</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Norite 75 procentus išlaidų paskirstyti vienam lėšų skyrimo šaltiniui ir 25 procentus – antram lėšų skyrimo šaltiniui. Kai viename iš šių lėšų skyrimo šaltinių baigiasi lėšos, likusias išlaidas norite išskaidyti trečiam lėšų skyrimo šaltiniui ir ketvirtam lėšų skyrimo šaltiniui.</td>
<td><ul>
<li>1　finansavimo　šaltinis</li>
<li>2　finansavimo　šaltinis</li>
<li>3　finansavimo　šaltinis</li>
<li>4　finansavimo　šaltinis</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Norite pirmuosius 25 išlaidų procentus paskirstyti vienam lėšų skyrimo šaltiniui, o likusius – antram lėšų skyrimo šaltiniui.</td>
<td><ul>
<li>1　finansavimo　šaltinis</li>
<li>2　finansavimo　šaltinis</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Pavyzdys: keli lėšų skyrimo šaltiniai (sudėting.)

Turite tris lėšų skyrimo šaltinius, kuriuos norite naudoti toliau nurodyta tvarka.

1.  2 lėšų skyrimo šaltinį ir 3 lėšų skyrimo šaltinį naudoti po lygiai, kol 2 lėšų skyrimo šaltinyje baigsis lėšos.
2.  Toliau naudoti 3 lėšų skyrimo šaltinį, kol jame baigsis lėšos.
3.  Kai 3 lėšų skyrimo šaltinyje baigiasi lėšos, naudoti 1 lėšų skyrimo šaltinį.

Norėdami pasiekti šį tikslą, turite atlikti toliau nurodytus veiksmus.

-   Atitinkamoms sumoms nustatykite 2 lėšų skyrimo šaltinio ir 3 lėšų skyrimo šaltinio lėšų limitus.
-   Sukurkite toliau nurodytas lėšų skyrimo taisykles.
    -   1 taisyklė (1 prioritetas): 50 procentų operacijų paskirstyti 2 lėšų skyrimo šaltiniui ir 50 procentų – 3 lėšų skyrimo šaltiniui.
    -   2 taisyklė (2 prioritetas): 100 procentų operacijų paskirstyti 3 lėšų skyrimo šaltiniui.
    -   3 taisyklė (3 prioritetas): 100 procentų operacijų paskirstyti 1 lėšų skyrimo šaltiniui.

Ši sąranka veikia, nes operacijos tikrinamos pagal taisykles ir limitus, siekiant nustatyti, ar bet kuri (-is) iš jų taikoma (-as) operacijai. Jei operacijai netaikomos jokios konkrečios taisyklės ar limitai, taikoma Visų operacijų taisyklė. Visų operacijų taisyklė atitinka visas operacijas. 

Jei randama operaciją atitinkanti taisyklė, pirmiausia taikoma procentinė dalis, paskirstyta toje taisyklėje, bet tik atitikmenis patikrinus pagal visus nustatytus limitus. Jei limitui atitikta, ir baigėsi lėšų skyrimo šaltinio lėšos, lėšų skyrimo taisyklės, susietos su lėšų limitu, nepaisoma, ir programa iėško kitos taikytinos taisyklės. 

Kai kuriais atvejais pagal taisyklę gali būti paskirstyta tik operacijos dalis. Taip gali nutikti, nes, paskirstant operaciją, pasiekiamas limitas. Šiuo atveju pagal tą taisyklę paskirstoma tik tam tikra suma, pvz., 50 procentų kiekvienam lėšų skyrimo šaltiniui. Taip taikoma 1 taisyklė, kuri aprašyta pirmiau šiame skyriuje. Likutis yra paskirstomas pagal kitą sekos taisyklę. 

Toliau pateikiamoje lentelėje šis scenarijus nagrinėjamas išsamiau.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Dėmesio centras </strong></td>
<td><strong>Informacija</strong></td>
</tr>
<tr class="even">
<td>Lėšų skyrimo taisyklės</td>
<td><ul>
<li>1 taisyklė (1 prioritetas): Visos operacijos. 2 lėšų skyrimo šaltiniui paskirkite 50 proc. ir 3 lėšų skyrimo šaltiniui – 50 proc.</li>
<li>2 taisyklė (2 prioritetas): Visos operacijos. 3 lėšų skyrimo šaltiniui paskirkite 100 proc.</li>
<li>3 taisyklė (2 prioritetas): Visos operacijos. 1 lėšų skyrimo šaltiniui paskirkite 100 proc.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lėšų limitai</td>
<td><ul>
<li>1 lėšų skyrimo šaltinio limitas = 10 000,00</li>
<li>2 lėšų skyrimo šaltinio limitas = 500,00</li>
<li>3 lėšų skyrimo šaltinio limitas = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>1 operacija</td>
<td><strong>Operacijos suma:</strong> 100,00<strong>Finansavimas:</strong> operacija apmokama tik pagal 1 taisyklę, nes, pritaikius 1 taisyklę, operacija yra visiškai apmokėta. Operaciją po lygiai finansuoja 2 lėšų skyrimo šaltinis ir 3 lėšų skyrimo šaltinis.
<ul>
<li>2 lėšų skyrimo šaltinis: 50,00</li>
<li>3 lėšų skyrimo šaltinis: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>2 operacija</td>
<td><strong>Operacijos suma:</strong> 5 000,00<strong>Finansavimas:</strong> operacija apmokama pagal visas tris taisykles. <strong>1 taisyklė</strong>
<ul>
<li>2 lėšų skyrimo šaltinis: 450,00</li>
<li>3 lėšų skyrimo šaltinis: 450,00</li>
</ul>
<strong>2 taisyklė</strong>
<ul>
<li>3 lėšų skyrimo šaltinis: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>3 taisyklė</strong>
<ul>
<li>1 lėšų skyrimo šaltinis: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Visos lėšos, paskirstomos kiekvienam lėšų skyrimo šaltiniui</td>
<td><ul>
<li>1 lėšų skyrimo šaltinis: 3 850,00</li>
<li>2 lėšų skyrimo šaltinis: 500,00</li>
<li>3 lėšų skyrimo šaltinis: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Atsiskaitymo taisyklės
Kai su klientu deratės dėl projekto sutarties, apibrėžiate, kaip ir kada galite išrašyti klientui SF už projekto darbą. Kai nustatote projekto sutartį ir projektą, galite nustatyti to projekto atsiskaitymo taisykles. Atsiskaitymo taisyklės yra pagrįstos projekto sąlygomis, kurios nurodytos projekto sutartyje. Atsiskaitymo taisyklės, kurias galite sukurti, priklauso nuo projekto sutarties sąlygų ir projekto tipo, pavyzdžiui, laikas ir medžiaga arba fiksuota kaina, kurį susiejate su atsiskaitymo taisykle. Galite sukurti daugiau nei vieną atsiskaitymo taisyklę projekto sutarčiai. Be to, atsiskaitymo taisyklę galite priskirti keliems projektams, susietiems su ta pačia projekto sutartimi ir kurių atsiskaitymo sąlygos yra panašios. 

Galite nustatyti šiuos atsiskaitymo taisyklių tipus:

-   **Pristatymo vienetas** – klientui SF išrašyti baigus darbą su pristatymo vienetu. Pristatymo vienetai apibrėžiami sutartyje.
-   **Eiga** – klientui SF išrašyti įvykdžius nurodytą projekto procentinę dalį. Galite nustatyti atsiskaitymo taisyklę, kad automatiškai apskaičiuotų atlikto darbo procentinę dalį arba galite neautomatiškai apskaičiuoti atlikto darbo procentą ir klientui išrašytinos SF sumą.
-   **Etapas** – SF klientui išrašyti už visą projekto etapo sumą, kai etapas pasiekiamas.
-   **Mokestis** – klientui SF išrašyti už paslaugas ir įtraukti valdymo mokestį, kuris paprastai yra paslaugų savikainos procentas.
-   **Laikas ir medžiagos** – klientui SF išrašyti už projekto laiką ir sunaudotas medžiagas.

Visų tipų atsiskaitymo taisyklėse galite nurodyti užlaikymo procentinį dydį, kuris atskaitomas iš kliento SF, kol projektas pasiekia sutartą etapą. Mokėjimo užlaikymo procentas nurodomas projekto sutartyje. Suma apskaičiuojama pagal bendrąją kliento SF eilučių vertę, ir iš jos atimama. 

**Laiko ir medžiagų** bei **Eigos** atsiskaitymo taisykėms galite priskirti apmokestinimo kategorijas. Apmokestinimo kategorijos rodo operacijas, kurios turėtų būti įtrauktos į kliento SF. 

Kai esate pasiruošę klientui išrašyti SF, projekto SF suma apskaičiuojama pagal atsiskaitymo taisykles ir sugeneruojamas projekto SF pasiūlymas. 

Tolesniuose skyriuose pateiktuose pavyzdžiuose parodyta, kaip nustatyti ir valdyti projekto atsiskaitymo taisykles.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Pavyzdys: atsiskaitymo taisyklės kūrimas atsižvelgiant į pristatytų vienetų skaičių

Jūsų organizacija sutaria kliento darbuotojams suteikti iš viso penkias mokymo sesijas, kurių vienos kaina – 10 000. SF klientui išrašote po kiekvienos mokymo sesijos. 

Nustatydami sutarties atsiskaitymo taisykles, naudojate toliau nurodytas reikšmes.

-   Pristatymo vienetas yra viena mokymo sesija.
-   Vieneto kaina yra 10 000 už mokymo sesiją.
-   Bendras vienetų skaičius yra penkios mokymo sesijos.

Baigę vieną mokymo sesiją galite sukurti SF su 10 000 suma už pirmą pristatytą vienetą ir tą SF nusiųsti klientui.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis nurodyta įvykdyta projekto procentine dalimi (apskaičiuota rankiniu būdu)

Jūsų organizacija, programinės įrangos konsultavimo įmonė, sudaro sutartį su klientu, kad sukurtų dalį kliento kuriamo produkto. Jūsų organizacija sutinka per šešis mėnesius pateikti programinės įrangos kodą. Klientas sutinka sumokėti jūsų organizacijai už darbą iš viso 100 000. Galite sukurti atsiskaitymo taisyklę norėdami išrašyti klientui SF pagal projekto atlikto darbo procentinę dalį, kaip nurodyta sutartyje.

-   Pirmo mėnesio pabaigoje susitiksite su klientu norėdami nustatyti atlikto darbo procentinę dalį. Jums ir klientui peržiūrėjus projektą, nusprendžiate, kad projekto įvykdyta 15 procentų.
-   Sukuriate SF 15 000 sumai (15 100 000 procentų) ir nusiunčiate ją klientui.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis nurodyta įvykdyta projekto procentine dalimi (apskaičiuota automatiškai)

Jūsų organizacija, programinės įrangos kūrimo įmonė, sutinka klientui už 30 000 sukurti atlyginimų apskaitos paketą. Klientas sutinka mokėti jūsų organizacijai už atlikto darbo procentinę dalį. Įvertinate, kad projekto išlaidos yra 20 000. Projekto sutartyje nurodomos darbo kategorijos, naudotinos atsiskaitymo procese. Galite nustatyti atsiskaitymo taisykles, kad SF sumos būtų automatiškai apskaičiuojamos pagal tai, kiek atlikta kiekvienos kategorijos darbų. Nustatykite kiekvienos kategorijos biudžetą:

-   **Programavimas** – išlaidos – 15 000, įplaukos – 20 000
-   **Diegimas** – išlaidos – 5 000, įplaukos – 10 000

Pirmą kartą kuriant kliento SF, SF suma automatiškai apskaičiuojama remiantis tokia informacija:

-   Po mėnesio projekto darbuotojas pateikia projekto tabelį. Darbuotojo darbo valandų išlaidos yra 5 000 už programavimą ir 1 000 už diegimą. Atlikta 33 procentai programavimo darbo (5 000 faktinių išlaidų / 15 000 biudžeto išlaidų) ir 20 procentų diegimo darbo (1 000 faktinių išlaidų / 5 000 biudžeto išlaidų).
-   Automatiškai apskaičiuota SF suma: 8 667 (33 procentai nuo 20 000 + 20 procentų nuo 10 000).
-   Sukuriate SF 8 667 sumai ir nusiunčiate ją klientui.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis sutartais etapais

Jūsų organizacija, valdymo konsultavimo įmonė, sutinka atlikti ketinamo parduoti kliento produkto rinkos tyrimą. Klientas sutinka tris mėnesius, pradedant nuo kovo mėnesio, naudotis jūsų paslaugomis ir sutinka jūsų organizacijai sumokėti 50 000. Projektą sudaro trys etapai.

-   1 etapas: vartotojų duomenų rinkimas – kovo 31 d.
-   2 etapas: vartotojų duomenų analizė – balandžio 30 d.
-   3 etapas: produkto panaudojimo pasiūlymo pateikimas – gegužės 31 d.

Klientas sutinka sumokėti jūsų organizacijai 10 000 už pirmąjį etapą, 20 000 už antrąjį etapą ir 20 000 už trečiąjį etapą. 

Kai sudarote projekto sutartį, sutinkate išrašyti klientui sąskaitą atsižvelgdami į atliktą etapą. Atsiskaitymo taisyklės nustatyme yra šie veiksmai:

-   Apibrėžkite projekto etapus.
-   Apibrėžkite sumą, kurią klientas turės sumokėti užbaigus kiekvieną etapą.

Kai pirmasis etapas baigiamas kovo 31 d., jį pažymite kaip atliktą ir sukuriate SF su 10 000 suma bei ją nusiunčiate klientui. Negalima sukurti etapo SF, kol etapas nepažymėtas kaip baigtas.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Pavyzdys: atsiskaitymo taisyklės kūrimas remiantis paslaugų ir valdymo mokesčiu

Jūsų organizacija, valdymo konsultavimo įmonė, sutinka vykdyti rinkos tyrimą ir įvertinti produkto, kurį klientas, mažmeninės prekybos įmonė, kuria, gyvybingumą. Sutarties sąlygose nurodyta, kad suteiksite savo trijų pagrindinių vadybos konsultantų paslaugas; jie atliks tyrimą atsižvelgdami į laiką ir medžiagas. Klientas sutinka už projekto konsultavimo valandą mokėti 100 ir 10 procentų valdymo mokestį. 

Kai sudarote projekto sutartį, sukurkite atsiskaitymo taisyklę norėdami 10 procentų valdymo mokestį pridėti prie apmokamų projekto konsultavimo valandų. 

Kuriant kliento SF, įtraukiamas 10 procentų valdymo mokestis ir konsultavimo valandų išlaidos. Pavyzdžiui, jei trys konsultantai iš viso projektui skyrė 200 valandų, pagal toliau nurodytą skaičiavimą sukuriama SF su 22 000 suma.

-   200 valandų, 100 už valandą = 20 000
-   10 procentų valdymo mokestis = 2 000
-   Bendroji SF suma = 22 000

Jei mokesčius moka klientas ir projekto sutartyje pasirenkate PVM grupę, PVM grupė automatiškai įvedama į mokesčių atsiskaitymo taisyklę.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Pavyzdys: atsiskaitymo taisyklės kūrimas atsižvelgiant į laiko ir medžiagų vertę

Jūsų organizacija, programinės įrangos konsultavimo įmonė, sutinka pateikti penkis techninius konsultantus dirbti programinės įrangos kūrimo projekte klientui per ateinančius šešis mėnesius. Klientas sutinka mokėti 150 už kiekvieną konsultavimo valandą ir padengti biuro reikmenų išlaidas. Jūsų organizacija siųs klientui SF kiekvieno mėnesio pabaigoje. 

Kai sudarote projekto sutartį, sutinkate kas mėnesį išrašyti klientui sąskaitą atsižvelgdami projekto į laiką ir medžiagas. Sukurkite atsiskaitymo taisyklę su šia informacija:

-   Sutarties laikotarpis yra šeši mėnesiai.
-   Konsultavimo laikas apskaičiuojamas už valandą taikant 150 tarifą.
-   Biuro reikmenims SF išrašoma su tam tikra suma, o visos projekto išlaidos neturi viršyti 10 000.
-   Vykdydami projektą sukurkite kliento SF kiekvieno kalendorinio mėnesio pabaigoje.

Pirmąjį mėnesį projekto konsultantai iš viso įrašė 800 valandų. Projekto biuro reikmenų išlaidos yra 2 000. Todėl mėnesio pabaigoje sukurkite SF su 122 000 suma: 800 valandų po 150 už valandą ir 2 000 už biuro reikmenis.




