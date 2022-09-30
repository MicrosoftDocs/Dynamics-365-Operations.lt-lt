---
title: Kas nauja ar pasikeitė programoje „Dynamics AX 7.0“ (2016 m. vasario mėn.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos „Microsoft Dynamics AX 7.0“ funkcijos. Šioje versijoje pateikiamos platformos ir programos funkcijos, ir ji išleista 2016 m. vasario mėn.
author: sericks007
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 4cd59d5ea2ef8d280a927fd9e9fe3b9af7974d7c
ms.sourcegitcommit: 0a5885dc792fc608ae59d0ef9b36fb61790b24de
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2022
ms.locfileid: "9593993"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Kas nauja ar pasikeitė programoje „Dynamics AX 7.0“ (2016 m. vasario mėn.)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos naujos ir pakeistos „Microsoft Dynamics AX 7.0“ funkcijos. Šioje versijoje pateikiamos platformos ir programos funkcijos, ir ji išleista 2016 m. vasario mėn.

## <a name="cost-management"></a>Kaštų valdymas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Greitai apžvelkite atsargų balansą, nebaigtos gamybos (NG) atsargų balansą ir pasirinktų ataskaitinių metų atsargų vidinį bei išorinį srautą.</td>
<td>Netaikoma</td>
<td>Darbo srityje <strong>Išlaidų administravimas</strong> yra dalis, kurioje pateikiamas pasirinkto ataskaitinio laikotarpio atsargų išrašas arba NG atsargų išrašas. Išrašas paremtas duomenų rinkinio talpykla, kuri pagal numatytąsias nuostatas atnaujinama kas 24 valandas. Duomenų rinkinio talpyklą galima sukonfigūruoti taip, kad vartotojai galėtų rankiniu būdu ją atnaujinti ir būtų galima ataskaitas teikti realiu laiku. Dalyje <strong>Duomenų atnaujinimo būsenos kortelė</strong>, kuri yra darbo srityje <strong>Išlaidų administravimas</strong>, rodoma, kada talpykla buvo paskutinį kartą atnaujinta.</td>
<td>Išlaidų kontrolieriai nori žinoti, ar per tam tikrą laiką atsargos arba NG atsargų išrašo balansas didėja, ar mažėja. Veiklos įvykius klasifikuodamas išraše, išlaidų kontrolierius gali apžvelgti atsargų srautą. Jei atsargos arba NG atsargos įkainojamos pagal standartines išlaidas, taip pat galima matyti bendrą užregistruotą nuokrypį.</td>
</tr>
<tr>
<td>Naudokite modulį <strong>Išlaidų valdymas</strong>.</td>
<td>Netaikoma</td>
<td>Išlaidų valdymas pristatomas kaip domeno sritis. Su išlaidomis susijusi konfigūracija ir įžvalga buvo išsklaidytos Atsargų valdymo, Gamybos kontrolės ir Mokėtinų sumų srityse.</td>
<td>Kadangi visos užduotys, susijusios su išlaidų valdymu, yra centralizuotos viename modulyje, išlaidų kontrolieriams bus lengviau palaikyti sistemą.</td>
</tr>
<tr>
<td>Atnaujinti registravimo tipai, susiję su atsargų apskaita ir gamybos apskaita.</td>
<td>Etiketės formose <strong>InventPosting</strong>, <strong>Išteklius</strong>, <strong>ResourceGroup</strong> ir <strong>ProductionGroup</strong> ne visada suderintos su faktiškai naudojamomis <strong>LedgerPostingType</strong> etiketėmis. Nelengva suprasti terminologiją, naudojamą etiketėse.</td>
<td>Etiketės atnaujintos, kad etiketės puslapiuose <strong>AtsargRegistrav</strong>, <strong>Išteklius</strong>, <strong>IštekliųGrupė</strong> ir <strong>GamybosGrupė</strong> atitiktų faktines <strong>DKRegistravTipo</strong> etiketes. Visos etiketės taip pat pervardytos, kad atitiktų veiklos įvykius. Atkreipkite dėmesį, kad faktinė registravimo logika nepakeista.</td>
<td>Lengviau konfigūruoti sistemą, nes naujos etiketės yra susijusios su veiklos įvykiais, kurie naudoja šį registravimo tipą.</td>
</tr>
<tr>
<td>Importuokite / eksportuokite pirkimo kainą, išlaidas ar pardavimo kainą iš „Microsoft Excel“ į įkainojimo versiją arba iš jos.</td>
<td>Tinkamai importuoti kainų ar išlaidų į įkainojimo versiją negalite, nes duomenų modelis reikalauja AtsargųDim ID.</td>
<td>Naudojant duomenų objektus, galima įdiegti importavimo / eksportavimo funkciją. Ši funkcija leidžia naudotojams kainas ar išlaidas importuoti / eksportuoti į įkainojimo versiją.
<ul>
<li>Importuoti visą kitų metų pirkimo kainų sąrašą, gautą iš Pirkimo skyriaus.</li>
<li>Atlikdami vieną operaciją, išlaidas ir standartines pardavimo kainas iš būstinės perkelkite į vieną ar kelias pardavimo įmones.</li>
</ul></td>
<td>Taip išlaidų kontrolieriams galima sutaupyti daug laiko, kai jie atlieka sistemos priežiūros darbus, ypač kai reikia išlaikyti iš anksto nustatytas ateinančių ataskaitinių metų išlaidas.</td>
</tr>
<tr>
<td>Greitai apžvelkite atsargų balansą ir vidutinę išlaidų objekto vieneto savikainą.</td>
<td>Naudotojas turi atidaryti turimą formą ir pasirinkti atsargų dimensijas, kurios atspindi išlaidų objektą. Todėl naudotojas turi žinoti, kurios konkretaus produkto finansinių atsargų dimensijos buvo pažymėtos.</td>
<td>Įdiegiamas naujas <strong>Išlaidų objekto</strong> puslapis. Pagal numatytąsias nuostatas šiame puslapyje rodomi visi išlaidų objektai, susiję su produktu. Šiame puslapyje rodomas dabartinis atsargų kiekis, vertė ir vidutinė vieno išlaidų objekto savikaina.</td>
<td>Šiek tiek sumažinamas sudėtingumas ir lengviau būti išlaidų kontrolieriumi.</td>
</tr>
<tr>
<td>Valdydami atsargas naudokite naują puslapį <strong>Išlaidų įrašai</strong>.</td>
<td>Gali būti sudėtinga atlikti registruotų atsargų operacijų ir susijusių sudengimų kontrolę, kadangi tos pačios operacijos gali būti faktinės arba finansinės.</td>
<td><strong>Išlaidų įrašų</strong> puslapis suteikia naują būdą peržiūrėti atsargų operacijoms.
<ul>
<li>Operacijos rodomos chronologine tvarka.</li>
<li>Įtraukiamos tik tos operacijos, kurios turi įtakos išlaidoms.</li>
<li>Nėra faktinių išlaidų ir finansinių išlaidų sąvokų.</li>
<li>Nėra faktinio kiekio ir finansinio kiekio sąvokų.</li>
<li>Išlaidos pridedamos palaipsniui.</li>
</ul></td>
<td>Kai išlaidų kontrolieriams reikia operacijos lygiu atlikti atsargų kontrolę, taip jiems galima sutaupyti daug laiko.</td>
</tr>
<tr>
<td>Naudokite naują dialogo langą <strong>Gamybos NG išrašas</strong>, norėdami peržiūrėti apibendrintą sukauptų konkretaus produkto išlaidų vaizdą.</td>
<td>Netaikoma</td>
<td>NG išraše rodomas apibendrintas konkretaus gamybos užsakymo NG balansas, sugrupuotas į atitinkamas išlaidų klasifikacijas. Diagramoje chronologine tvarka rodoma, kaip veiklos registravimai paveikė NG balansą.</td>
<td>Kai išlaidų kontrolieriai turi žinoti, koks yra dabartinis konkretaus gamybos užsakymo NG balansas arba kiek sunaudota užsakymo medžiagos; tokiu būdu jie gali sutaupyti daug laiko.</td>
</tr>
<tr>
<td>Naudokite įdiegtą gamybos užsakymų funkciją Peržiūrėti savikainos palyginimą. Šia funkcija lengviau lyginti savikainas, susijusias su gamybos užsakymu.</td>
<td>Naudotojas lyginti gali tik įvertintas savikainas ir realizuotas savikainas. Lyginti galima žemiausiu lygiu.</td>
<td>Savikainos palyginimo funkcija išlaidų kontrolieriams leidžia palyginti toliau nurodytus duomenis.
<ul>
<li>Aktyvią savikainą su įvertinta savikaina = planavimo nuokrypis.</li>
<li>Įvertinta savikaina su realizuota savikaina = gamybos nuokrypis.</li>
<li>Planavimo nuokrypis + gamybos nuokrypis = bendrasis nuokrypis.</li>
</ul>
Ši funkcija veikia nepriklausomai nuo įkainojimo metodų, priskirtų pagamintai prekei. Pagal numatytąsias nuostatas diagramoje savikainos palyginimas rodomas pagal savikainos grupės tipą. Diagrama naudotojams leidžia peržiūrėti išsamesnius lygius.</td>
<td>Ji išlaidų kontrolieriams ar gamybos vadovams leidžia analizuoti, iš kur atsiranda gamybos nuokrypiai ir kas juos sukelia.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Kūrėjas

| Ką galite daryti? | Dynamics AX 2012 | Dynamics AX 7.0 | Kodėl tai svarbu? |
|------------------|------------------|-----------------|------------------------|
| Kurkite žiniatinklio sprendimus debesyje, kuriuos būtų galima pasiekti daugelyje įrenginių. | Neprieinama | Dabartinė „Dynamics AX“ versija paremta nauju žiniatinklio klientu ir kliento sistema. | Savo galutiniams naudotojams galite teikti naujos kartos sprendimus. |
| Kurti sprendimams naudokite „Microsoft Visual Studio“. | Pagrindinė programavimo aplinka yra „Microsoft MorphX“, tačiau šiek tiek programuojama ir programoje „Visual Studio“. | „Visual Studio“ yra vienintelė programavimo aplinka. | Joje išlaikomos žinomos „Dynamics AX 2012“ sąvokos, kurios sklandžiai pritaikomos „Visual Studio“ sistemai ir paradigmoms. Taip įgalinama standartinė sąveika su kitomis .NET kalbomis ir projektais. |
| Kompiliuokite visų funkcijų bendrąją tarpinę kalbą (CIL). | X++ sukompiliuota pseudokodu. | Visiškai naujas X++ kompiliatorius generuoja visų funkcijų CIL. CIL yra ta pati tarpinė kalba, kurią naudoja kitos .NET paremtos kalbos. | CIL yra greitesnė, gali efektyviai nurodyti klases valdomose dinaminių saitų bibliotekose (DLL) ir gali veikti didelėje .NET priemonių įrankių bazėje. |
| Įdėkite verslo įžalgų (BI) ataskaitas ir vizualizacijas „Microsoft Dynamics AX“ kliente. | Neprieinama | Kurkite itin intuityvias ir sklandžias vizualizacijas. | Pateikiamos sprendimų priėmimo įžvalgos, paremtos BI. |
| Integruokite su „Microsoft Office“. | Neprieinama | Naujos galimybės – tai „Excel‟ duomenų jungties programa, puslapis **Darbaknygės dizaino įrankis**, Eksportavimo API ir dokumentų valdymo priemonė. | Savo galutiniams naudotojams galite kurti produktyvumo sprendimus. |
| Automatizuokite kūrimą, tikrinimą ir diegimą. | Iš dalies neužimtas | Naudodami Kūrėjo ir Kūrimo VM, diekite kūrėjo topologiją. Automatiškai konfigūruokite Kūrimo VM, kad rastumėte, kurtumėte modulius iš „Visual Studio Online“ (VSO) ir vykdytumėte testus. Palaikomas C\# ir X++ modulių kompiliavimas bei nuorodos. | Ddidinamas kūrėjų produktyvumas mažinant bandymų ir tikrinimų savikainą bei reikalingas pastangas. |
| Tinkinkite perdengdami ir naudodami plėtinius. | Plėtiniai negalimi. | Dabartinė „Dynamics AX“ versija turi naują tinkinimo modelį. | Galite tinkinti modelio elementų, kuriuos siunčia „Microsoft‟ ar trečiosios šalies „Microsoft‟ partneriai, šaltinio kodą ir metaduomenis. |
| Naudodami X++ ir modernią žiniatinklio sistemą, kurkite naujus valdiklius ir UI elementus. | Pasirinktiniai valdikliai pasikliauja išorės sistemomis, pvz., „Microsoft ActiveX‟ ir „Windows‟ grafikos pateikimo platforma (WPF). | Kurti valdiklius lengviau dabartinėje versijoje. X++ sistema gali būti naudojama programos veikimo ir verslo logikai, o HTML / „JavaScript‟ paremtas klientas leidžia naudoti modernias vizualizacijas. | Jūsų valdiklius galima suprojektuoti taip, kad jie atrodytų ir veiktų tiksliai kaip „Dynamics AX“ parengti naudoti (OOB) valdikliai. |
| Naudodami naujus įrankius, vertinkite ir derinkite našumą. | „PerfSDK‟, duomenų išplėtimo įrankių rinkinys, sekimo analizatoriaus žiniatinklio programa ir „PerfTimer‟ negalimi. | „PerfSDK‟, duomenų išplėtimo įrankių rinkinys, sekimo analizatoriaus žiniatinklio programa ir „PerfTimer‟ yra nauji. | Programinės įrangos kūrimo rinkinys (SDK) leidžia bandyti ir tikrinti visus svarbius vieno naudotojo ir, jei taikoma, kelių naudotojų testų vykdymo našumo verslo procesus. Duomenų išplėtimo įrankių rinkinys leidžia teisingai išplėsti visus našumo testus, kuriems reikia teisingai išplėsti bendruosius duomenis ir operacijų duomenis. Sekimo analizatorius leidžia patikrinti vieno naudotojo našumo testą arba vykdomą kelių naudotojų testą. „PerfTimer‟ leidžia matyti, ar dėl kokios nors užklausos ar kokio konkretaus metodo iškvietimo kyla našumo problema. Todėl nereikia visko išsamiai sekti ir analizuoti. |
| Naudodami „OData‟, rodykite atnaujintiną rodinį. | Neprieinama | Dabartinėje „Dynamics AX“ versijoje įdiegtas viešasis „OData“ tarnybos galinis punktas, kuris nuosekliai, įvairiuose klientuose įgalina prieigą prie „Dynamics AX“ duomenų. | Jūsų sprendimai gali sąveikauti su „RESTful‟ tarnybomis, aptinkamu būdu bendrinti duomenis ir, naudodami HTTP rietuvės protokolą, įgalinti platų integravimą. |
| Pasinaudodami „Business Connector‟, autorizuokite verslo logiką ir palaikykite integravimo scenarijus. | Naudojant „Business Connector‟ galima iš valdomojo kodo kreiptis į X++ kodą. Rekomenduojame naudoti „Business Connector‟ tik autorizuojant verslo logiką su C\# kodais ir nenaudoti su integravimo scenarijais. | „Business Connector‟ nebepalaikomas. Autorizuoti reikia todėl, kad X++ sukompiliuotas į valdomą kodą. Todėl sąveika yra lengvesnė. Integravimo scenarijai patenkinami naudojant „OData‟. | Nuo šiol „Business Connector‟ naudoti negalite. |
| Pasirinkite realių duomenų bazės laukų ir išplėstinių duomenų tipų (EDT) skalę (t. y., skaitmenų po kablelio skaičių). | 16 skalė yra numatytoji, ir jos keisti kūrėjas negali. | EDT ir laukuose dabar yra skalės ypatybė, kuri gali būti taikoma atskiram laukui ir EDT. Nustatyta numatytoji yra 6, o ne 16. | Kai naudojama mažesnė skalė, NCCI lentelių našumas (atminties palaikymo SQL) yra keleriopai didesnis. Skalę keiskite pagal tai, kokios reikia naudojant atskirus laukus. |

## <a name="financial-management"></a>Finansų valdymas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Eksportuokite sąskaitų struktūras į „Microsoft Excel“.</td>
<td>Neprieinama</td>
<td>Dabar galite pasirinkti sąskaitos struktūrą ir ją eksportuoti į „Excel‟.</td>
<td>Daug klientų pageidavo galimybės eksportuoti sąskaitų struktūras į „Excel‟, kad būtų lengviau filtruoti.</td>
</tr>
<tr>
<td>Viename puslapyje peržiūrėkite DK ir išplėstinių taisyklių struktūras, susietas su sąskaitos struktūra.</td>
<td> Norėdamas matyti naudojamas DK ir sąskaitos struktūrą, vartotojas turi pereiti į kelias formas.</td>
<td>Į sąskaitos struktūros puslapį pridėtos „FactBox‟.</td>
<td>Kai sąskaitų struktūros yra apibrėžtos ir redaguotos, lengviau pasiekti svarbią informaciją.</td>
</tr>
<tr>
<td>Viename puslapyje peržiūrėkite DK, susietas su sąskaitų planu.</td>
<td>Norėdamas matyti sąskaitų planą, priskirtą DK, naudotojas turi pereiti prie kiekvienos įmonės ir atidaryti DK formą.</td>
<td>Į <strong>Sąskaitų plano</strong> puslapį pridėtos „FactBox‟.</td>
<td> Kai sąskaitų planas yra apibrėžtas ir priskirtas, lengviau pasiekti svarbią informaciją.</td>
</tr>
<tr>
<td><strong>Bandomojo balanso</strong> sąrašo puslapyje, atskiruose stulpeliuose peržiūrėkite uždarymo žiniaraščio koregavimus ir uždarymo operacijas.</td>
<td>Viename stulpelyje naudotojas mato abu operacijų tipus.</td>
<td>Į <strong>Bandomojo balanso</strong> sąrašo puslapį pridėtas papildomas parametras.</td>
<td>Jis leidžia glausčiau analizuoti duomenis ir jo taip pat reikia kai kurių šalių / regionų teisės aktų nustatytoms ataskaitoms.</td>
</tr>
<tr>
<td>Naudokite naują puslapį <strong>Visuotinis bendrasis žurnalas</strong>.</td>
<td>Nepasiekiama</td>
<td>Naujas puslapis <strong>Visuotinis bendrasis žurnalas</strong>, skirtas bendriesiems žurnalams atidaryti. Šio puslapio prieigos teisės įtrauktos į vaidmenį <strong>Buhalteris</strong>.</td>
<td>Bendrai naudojamos tarnybos buhalteris, neuždarydamas formos ir neperjungdamas įmonės konteksto, galės atidaryti visų įmonių bendruosius žurnalus.</td>
</tr> 
<tr>
<td>Naudokite naują puslapį <strong>Apskaitos šaltinių naršyklė</strong>.</td>
<td>Galima naudoti „Dynamics AX 2012 R3 CU10“.</td>
<td>Naujas puslapis <strong>Apskaitos šaltinių naršyklės</strong> ir veiksmai, skirti jį atidaryti iš sąrašo puslapio <strong>Bandomasis balansas</strong> ir puslapio <strong>Kvitų operacijos</strong>.</td>
<td>Suteikia galimybę peržiūrėti išsamiausią informaciją apie DK bandomojo balanso ar apskaitos įrašo arba ad hoc analizės šaltinį.</td>
</tr>
<tr>
<td>Įtraukite papildomų registravimo sluoksnių.</td>
<td>Įtraukti papildomų registravimo sluoksnių galėjo tik kūrėjai.</td>
<td>Dabar galima naudoti dešimt registravimo sluoksnių.</td>
<td>Dauguma klientų įtraukia papildomų registravimo sluoksnių.</td>
</tr>
<tr>
<td>Naudokite parinktį Susijęs kvitas.</td>
<td>Nepasiekiama</td>
<td>Vartotojai gali naudoti parinktį Susijęs kvitas, norėdami peržiūrėti korespondentinės įmonės kvitą, kai registruoja vidinės įmonės operacijas. Susijusių kvitų rodinyje vartotojai gali spustelėti išsamią informaciją ir greitai atidaryti korespondentinės įmonės kvitą.</td>
<td>Registruodami vidinės įmonės operacijas, vartotojai negali matyti arba sekti kvito, kuris buvo užregistruotas korespondentinėje įmonėje.</td>
</tr>
<tr>
<td>Masinis finansinio laikotarpio uždarymas</td>
<td>Nepasiekiama</td>
<td>Vartotojai vienu metu gali naujinti kelių įmonių modulio prieigą ir keisti laikotarpio būseną.</td>
<td>Kol šios funkcijos nebuvo, vartotojai turėjo prisijungti prie kitos įmonės, atidaryti DK kalendoriaus formą ir neautomatiškai naujinti modulio prieigą bei laikotarpio būseną.</td>
</tr>
<tr>
<td>Importuokite „Oanda“ valiutų kursus.</td>
<td>Konfigūruoti valiutų kursų tiekimo įrankio valiutų kursų importavimo iš „Oanda“ funkciją galėjo tik kūrėjai.</td>
<td>Jei vartotojai turi „Oanda“ raktą, jie gali jį įvesti konfigūruodami valiutos kursų tiekimo įrankį.</td>
<td>Vartotojai gali pasinaudoti parengta naudoti funkcija, kuri suteikia galimybę „Oanda“ valiutų kursus importuoti pagal grafiką.</td>
</tr>
<tr>
<td>Filtruokite finansines ataskaitas („Management Reporter“) pagal dimensijas, atributus, datas ir scenarijus.</td>
<td> Visas „Management Reporter‟ ataskaitų filtravimas tvarkomas naudojant ataskaitos dizainą. Pavyzdžiui, jei vartotojas, turintis peržiūros teises, nori peržiūrėti kitos datos ataskaitą, ataskaitų dizaino įrankis turi atlikti keitimą.</td>
<td>Įtraukta ataskaitų parinkčių, tad vartotojui peržiūrint ataskaitą galima taikyti skirtingus filtrus. Tada pagal šiuos filtrus generuojama nauja ataskaita.</td>
<td>Finansinių ataskaitų naudotojai gali taikyti skirtingus dimensijų, datų, atributų ir scenarijų filtrus, ir nereikia naujinti ataskaitų dizainų.</td>
</tr>
<tr>
<td>Peržiūrėkite finansines ataskaitas („Management Reporter“) „Microsoft Dynamics AX“ kliente.</td>
<td>Peržiūrėti „Management Reporter‟ ataskaitoms buvo naudojamas atskiras žiniatinklio klientas.</td>
<td>Visas finansines ataskaitas galima pasiekti „Dynamics AX“ kliente. Naudotojas pasirenka norimą peržiūrėti ataskaitą, ir ji rodoma kliente.</td>
<td>Dabar peržiūrėti finansines ataskaitas galima nenaudojant kito kliento / programos.</td>
</tr>
<tr>
<td>Spausdinkite finansines ataskaitas („Management Reporter“) iš „Microsoft Dynamics AX“ kliento.</td>
<td>Spausdinant ataskaitą naudojamos naršyklės spausdinimo parinktys ir spausdinamas tik tas turinys, kurį vartotojas mato ekrane.</td>
<td>Vartotojas gali pasirinkti ataskaitos išsamumo lygį ir puslapio sąranką, naudodamas „Dynamics AX“ kliento finansinės ataskaitos parinktį Spausdinti.</td>
<td>Ataskaitos spausdinamos, kaip nori vartotojai, o ne tinklalapio formatu.</td>
</tr><tr>
<td>Analizuokite finansinius duomenis naudodami „Power BI“ turinį „Stebėti finansinį našumą“.</td>
<td>Neprieinama</td>
<td>PowerBI.com pasirinkite <strong>Gauti duomenis</strong> ir tada pasirinkite turinio paketą <strong>„Dynamics AX“ – finansinis našumas</strong>. Įveskite savo „Dynamics AX“ galinio punkto URL, kad jūsų duomenys atsispindėtų ataskaitų srityje.</td>
<td>Trimis–keturiais spustelėjimais organizacijos gali „Power BI“ ataskaitų sritį su svarbiais finansiniais duomenimis. Organizacija turinį gali prisitaikyti.</td>
</tr>
<tr>
<td>Sekite finansinio laikotarpio uždarymo procesus.</td>
<td>Nepasiekiama</td>
<td>Uždarymo šablonus ir grafikus galima kurti naudojant Finansinio laikotarpio uždarymo konfigūraciją. Naudokite <strong>Finansinio laikotarpio uždarymo</strong> darbo sritį, kad sektumėte grafikų keliose įmonėse uždarymo eigą.</td>
<td>Ši darbo sritis pašalina rankines sistemas, kad apibrėžtų, planuotų ir komunikuotų uždarymo veiklas. Todėl sumažinamas uždaryti skirtas dienų skaičius.</td>
</tr>
<tr>
<td>Naudodami darbo sritį <strong>DK biudžetai ir prognozės</strong> ir papildomas užklausų formas, stebėkite biudžetą ir faktines sumas bei kurkite DK prognozes.</td>
<td>Neprieinama</td>
<td> Darbo sritį galima pasiekti per „Dynamics AX“ ataskaitų sritį. Joje yra saitai į kelis naujus užklausos puslapius: <strong>Faktinių sumų ir biudžeto suvestinė</strong>, <strong>Biudžeto kontrolės statistikos suvestinė</strong>, <strong>Biudžeto registro įrašai</strong> ir <strong>Biudžeto planai</strong>.</td>
<td>Naujuose užklausų puslapiuose galima lengvai pasiekti biudžeto informaciją. Darbo srityje visos biudžeto priežiūros ir stebėsenos užduotys pateikiamos vienoje vietoje, kurią gali lengvai naudoti biudžeto vadovai ar apskaitos vadovai.</td>
</tr>
<tr>
<td>Kurkite biudžeto planų ir prognozių maketus.</td>
<td><strong>Biudžeto plano</strong> dokumentas peržiūrimas kaip eilučių, kuriose yra finansinių dimensijų derinių įsigaliojimo datos ir sumos, sąrašas. Norėdamas biudžeto plano duomenis peržiūrėti „PivotTable‟, naudotojas turi sukurti ir naudoti „Excel‟ šablonus.</td>
<td>Biudžeto planų ir prognozių maketų skaičius gali būti neribotas. Makete galite jungti pasirinktas finansines dimensijas, naudotojo apibrėžtus stulpelius ir kitus eilučių atributus (pvz., komentarus, projektus ir turtą). Naudotojai gali iš karto perjungti biudžeto plano dokumento maketą ir redaguoti duomenis naudodami bet kurį pasirinktą maketą. Biudžeto planavimo konfigūracija supaprastinama pašalinant scenarijų apribojimus ir naudojant maketus, siekiant apibrėžti, kokius duomenis galima peržiūrėti ir redaguoti kiekviename biudžeto plano dokumento etape.</td>
<td>Suteikiamas lankstumas kurti ir redaguoti biudžeto planus naudojant „Excel“ ir „Dynamics AX“ klientą. „Excel‟ darbaknygių šablonus galima generuoti naudojant Biudžeto plano maketo sąranką.</td>
</tr>
<tr>
<td>Spausdinkite <strong>Tiekėjo SF operacijų</strong> ataskaitą naudodami informaciją iš <strong>Išsamaus termino dienų sąrašo</strong> ataskaitos, kurioje nurodytos po nustatyto termino praėjusios dienos.</td>
<td>Turite spausdinti dvi skirtingas ataskaitas: <strong>Išsamus termino dienų sąrašas</strong> ir <strong>Tiekėjo SF operacijos</strong>.</td>
<td>Šių dviejų ataskaitų Informacija konsoliduota <strong>Tiekėjo SF operacijų</strong> ataskaitoje. <strong>Išsamaus terminų dienų sąrašo</strong> ataskaita nebenaudojama.</td>
<td>Nebereikia spausdinti dviejų atskirų, tačiau susijusių ataskaitų.</td>
</tr>
<tr>
<td>Generuokite teisės aktų numatytas ataskaitas tiesiogiai PDF formatu.</td>
<td>Pirmiausia teisės aktų numatytą ataskaitą turite generuoti vienu formatu, o tada ją eksportuoti į PDF formatą.</td>
<td>PDF formatas yra numatytasis teisės aktų numatytų ataskaitų formatas.</td>
<td>Jį naudojant, tiek kompiuterio monitoriuje, tiek atspausdintoje popierinėje kopijoje matomas vienodas vaizdas.</td>
</tr>
<tr>
<td>PVM sudengimo procesą vykdykite kaip paketinį procesą.</td>
<td>Nepasiekiama</td>
<td><strong>PVM sudengimo laikotarpio</strong> puslapyje galite nurodyti, kad sudengimo procesas turėtų būti vykdomas paketiniu režimu.</td>
<td>Laikotarpių, kuriuose yra daug mokesčių operacijų, sudengimo procesas gali ilgai užtrukti, ir gali būti geriau procesą vykdyti fone kaip paketinį procesą.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Platforma

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Klientą pasiekite bet kuriuo metu, iš bet kur.</td>
<td>„AX 2012“ darbalaukio klientas pateikia visą formų rinkinį, bet jį galima paleisti tik tuose kompiuteriuose, kuriuose veikia „Microsoft Windows“, ir jį reikia įdiegti. Su darbalaukio klientu dažnai naudojamas terminalo serveris, kad būtų įgalinta teritorinio tinklo (WAN) prieiga. Įmonės portalo žiniatinklio kliente pateikiamas sumažintas formų rinkinys.</td>
<td>Šiuos du „AX 2012“ klientus pakeitė vienas standartais paremtas žiniatinklio klientas, kuris pateikia visą darbalaukio kliento funkcijų rinkinį ir įmonės portalo kliento aprėptį.</td>
<td>Jis neleidžia kūrimo veiklai išsiskaidyti tarp dviejų UI platformų. Naudodamas standartines žiniatinklio sąsajas, jis pašalina terminalo serverio poreikį.</td>
</tr>
<tr>
<td>Būkite produktyvūs naudodami naująjį užduočių įrašytuvą.</td>
<td>„AX 2012“ užduočių įrašytuvui reikia tiesioginės prieigos prie programos objektų serverio (AOS) kompiuterio ir didesnių teisių, ir jis nesuteikia jokių redagavimo galimybių.</td>
<td>Naująjį Užduočių įrašytuvą galima naudoti tiesiai iš žiniatinklio kliento. Norint pasiekti Užduočių įrašytuvą, administratoriaus teisių nereikia. Įrašytus veiksmus galima peržiūrėti tiesiogiai juos įrašant, įdiegtos naujos redagavimo galimybės ir Užduočių įrašytuvas be Verslo proceso modeliavimo įrankio (BPM) scenarijų palaiko daugiau scenarijų.</td>
<td>Naujasis Užduočių įrašytuvas suteikia supaprastintą naudojimo patirtį ir įgalina naujus „Dynamics AX“ pajėgumus. Kai kuriuos iš šių pajėgumų galima naudoti dabar, o ateityje jų atsiras daugiau.</td>
</tr>
<tr>
<td>Padėkite vartotojams geriau suprasti savo būsimą darbą naudodami darbo sritis.</td>
<td>Vaidmenų centruose pateikiama informacijos, susijusios su vartotojo verslo ar įmonės užduoties funkcija, apžvalga.</td>
<td>Darbo sritis yra nauja „Dynamics AX“ sąvoka, kuri vaidmenų centrus pakeis kaip pagrindinis būdas naršyti užduotis ir konkrečius puslapius. Jose pateikiama vieno puslapio verslo veiklos apžvalga, jas naudodami vartotojai gali lengviau suprasti dabartinę proceso arba vartotojo būseną, darbo krūvį ir našumą. Darbo sritys yra išsamesnės nei „AX 2012“ vaidmenų centrai; taip pat vartotojas gali turėti prieigą prie kelių darbo sričių.</td>
<td>Darbo sritys skirtos vartotojų darbo našumui didinti. Kūrėjai turės sukurti kiekvienos svarbios produkto palaikomos „veiklos“ darbo sritį. Senesnį „AX 2012“ vaidmenų centrą dabartinėje „Dynamics AX“ versijoje paprastai pakeis kelios darbo sritys.</td>
</tr>
<tr>
<td>Formų matmenis nustatykite pagal naršyklės peržiūros sritį arba įrenginio dydį.</td>
<td>„AX 2012“ formos turinys buvo griežtai išdėstomas stulpeliais, o bendras formos aukštis / plotis buvo nustatomas daugiausia pagal formos valdiklius.</td>
<td>Naujausioje „Dynamics AX“ versijoje pradėjus naudoti žiniatinklį, formos matmenys dabar nustatomi pagal naršyklės peržiūros sritį arba įrenginį. Buvo pakeisti arba įtraukti valdikliai ir maketo parametrai, kad formos matmenys geriau atitiktų peržiūros srities dydžio keitimus.</td>
<td>Formos turinys rodinys turi būti lengviau modifikuojamas, siekiant optimaliai panaudoti esamą naršyklės arba įrenginio aukštį / plotį. Siekiant užtikrinti, formos turinio rodinį galima lengvai modifikuoti, gali reikėti keisti formos modeliavimo būdą.</td>
</tr>
<tr>
<td>Naudodami modelius sumaniau kurkite formas.</td>
<td>„AX 2012“ formų šablonus buvo galima naudoti formų kūrimo darbo pradžioje, atsižvelgiant į formos stilių. Formos stiliaus tikrintuvas, pasirinktinis papildinys, suteikė informacijos apie tai, kuo forma skiriasi nuo jos atitinkamo šablono.</td>
<td>Dabartinėje „Dynamics AX“ naudojami formų modeliai. Formos modeliai yra formų šablonų ir formos stiliaus tikrintuvo derinys, glaudžiai integruotas į kūrimo patirtį. Modeliai apibrėžti formos lygyje (pvz., „AX 2012“), o papildomus antrinius modelius galima apibrėžti grupės ir skirtuko puslapio lygyje.</td>
<td>Formos, kurioms galima taikyti modelius, turi daug privalumų, įskaitant nuoseklesnę vartotojo sąsają, paprastesnę kūrimo patirtį, lengvesnį formos naujinimo kelią ir didesnes galimybes modifikuoti formos turinio rodinį.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Žinynas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pasiekite valdomąjį procedūrinį žinyną (užduočių vedlius) ir abstrakčias temas spustelėdami <strong>Žinynas</strong>.</td>
<td>„AX 2012“ žinyno sistema nurodo į HTML temas, kurios saugomos vietos žiniatinklio serveryje. Klientai ir partneriai gali kurti savo Žinyną.</td>
<td>Dabartinės „Dynamics AX“ versijos Žinyno sistemoje rodomi užduočių vadovai, saugomi „Microsoft Dynamics Lifecycle Services“ (LCS) BPM. Žinyno sistema taip pat rodo temas Microsoft Learn. Daugiau informacijos žr. <a href="help-overview.md" data-raw-source="[Help system](help-overview.md)">Žinyno sistema</a> ir <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides (February 2016)](new-task-guides-available-february-2016.md)">Nauji užduočių vedliai (2016 m. vasaris)</a>.</td>
<td>Užduočių vadovai suteikia valdomą, interaktyvią patirtį, kuri jums padeda atlikti užduoties ar verslo proceso veiksmus. Galite atsisiųsti ir tinkinti užduočių vedlius, kuriuos teikia „Microsoft“. Straipsnyje pateikiamas greitesnis ir lankstesnis produkto dokumentacijos kūrimo, pristatymo ir atnaujinimo būdas. Todėl jis padeda užtikrinti, kad turite prieigą prie vėliausios techninės informacijos.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Žmogiškojo kapitalo valdymas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Po kursų baigimo dalyviams perduokite įgūdžius ir sertifikatus.</td>
<td>Tai yra rankinis procesas.</td>
<td>Baigus kursą, atsiranda nauja galimybė dalyvio įrašus atnaujinti naujaisiais įgūdžiais ir sertifikatais.</td>
<td>Pateikiamas naujas ir efektyvus būdas atnaujinti darbuotojo įrašus.</td>
</tr>
<tr>
<td>Sparčiai tikrinkite įdarbinimą.</td>
<td>Tai yra rankinis procesas.</td>
<td>Jūsų personalo padalinys, naudodamas darbo sritį arba darbuotojų puslapį, gali sparčiai patikrinti įdarbinimą.</td>
<td>Kad patikrintų pradžios datą, vadovą, mėnesių pareigose skaičių ir kompensavimo duomenis, personalo padalinys nebeturi eiti į kelis puslapius.</td>
</tr>
<tr>
<td>Leiskite darbuotojams peržiūrėti, atnaujinti ir panaikinti sistemos informaciją.</td>
<td>Galima naudoti, bet su ribotais naujinimo pajėgumais ir rodiniu.</td>
<td>Ši funkcija yra įgalinta, ir leidžia darbuotojams bei rangovams peržiūrėti įvairius asmeninius duomenis. Neprivaloma: kuriant, naujinant ar naikinant informaciją, galima naudoti darbo eigą.</td>
<td>Ji darbuotojams leidžia perimti savo informacijos kontrolę – atnaujinti adreso ar kontaktinę informaciją, kreiptis dėl darbo, atsakyti į klausimyną ar atnaujinti savo nuotrauką. Įgalinus darbo eigą, informaciją gali peržiūrėti tvirtintojas arba ją galima automatiškai patvirtinti, atsižvelgiant į jūsų verslo procesus.</td>
</tr>
<tr>
<td>Leiskite vadovams peržiūrėti ar redaguoti darbuotojų informaciją.</td>
<td>Galima naudoti, bet su ribotais naujinimo pajėgumais ir rodiniu.</td>
<td>Atsižvelgiant į konfigūracijos nuostatas ir saugą, vadovai gali peržiūrėti ar redaguoti darbuotojų informaciją.</td>
<td>Vadovams leidžiama pasiekti svarbius darbuotojų duomenis, kad jie galėtų priimti geresnius sprendimus dėl išteklių, našumo ir darbuotojų lavinimo.</td>
</tr>
<tr>
<td>Pasinaudokite vadovo savitarnos funkcija.</td>
<td>Nepasiekiama</td>
<td>Vadovai dabar gali teikti prašymus dėl naujų darbuotojų ir rangovų, pervedimų ir atleidimo (įdarbinimo nutraukimo). Vadovai taip pat gali teikti užklausą dėl naujų pareigų, pareigų trukmės išplėtimo arba pareigų keitimo.</td>
<td>Šiuos scenarijus ankščiau galėjo naudoti tik personalas. Naudodami šiuos scenarijus organizacijos vadovai gauna efektyvių įrankių. Galima suaktyvinti pasirinktines darbo eigas, kad būtų galima pateikti reikiamo lygio peržiūrą ir tvirtinimus.</td>
</tr>
<tr>
<td>Pasiekite kompensavimo apdorojimo rezultatus.</td>
<td>Rezultatus galima pasiekti tik apdorojimo metu.</td>
<td>Kompensavimo apdorojimo rezultatus dabar galima pasiekti bet kada įvykdžius procesą.</td>
<td>Taip pateikiamas puikus to proceso ir jo rezultato auditas. Taip pat pateikiamas išsamus duomenų vaizdas prieš atnaujinant darbuotojų įrašus.</td>
</tr>
<tr>
<td>Pasiekite išmokų apdorojimo rezultatus.</td>
<td>Rezultatus galima pasiekti tik apdorojimo metu.</td>
<td>Išmokų apdorojimo rezultatus dabar galima pasiekti bet kada įvykdžius procesą.</td>
<td>Taip pateikiamas išsamus duomenų vaizdas, atnaujinamas po registracijos išmokoms gauti ir pasikeitus savikainai.</td>
</tr>
<tr>
<td>Peržiūrėkite laiko juostos „Įsigaliojimo data“ pokyčius.</td>
<td>Neprieinama</td>
<td>Šį lyginimo įrankį galima naudoti darbuotojams, pareigoms ir darbams. Jis pateikia išsamų pokyčių tarp vienos įrašo versijos ir kitos vaizdą.</td>
<td>Jums peržiūrint per tam tikrą laiką įvykusius darbuotojų, pareigų ir darbo įrašų pokyčius, taupomas laikas. Jis leidžia sparčiai palyginti per tam tikrą laiką atsiradusias dvi įrašo ar visų įrašų versijas.</td>
</tr>
<tr>
<td>Darbuotojus peržiūrėkite pagal įmonę.</td>
<td>Tai rankinis procesas, atliekamas naudojant filtravimą.</td>
<td>Darbuotojų ir rangovų sąrašai automatiškai filtruojami pagal įmonę, prie kurios esate prisijungę.</td>
<td>Pateikiamas filtruotas darbuotojų, kurie dirba prijungtoje įmonėje, rodinys. Nefiltruotame visų darbuotojų ir rangovų rodinyje vis dar galima peržiūrėti darbuotojų sąrašą. Dabartinėje „Dynamics AX“ versijoje sistema pagal tai, koks darbuotojas pasirinktas sąraše, įmonės nekeičia.</td>
</tr>
<tr>
<td>Naujinkite kurso dalyvių sąrašą.</td>
<td>Nepasiekiama</td>
<td>Kurso dalyvius galima šalinti iš dalyvių sąrašo.</td>
<td>Suteikiamas lengvas būdas atnaujinti kurso dalyvius, užsiregistravusius per klaidą.</td>
</tr>
<tr>
<td>Tvarkykite kompensacijų įvykius grupėje.</td>
<td>Nepasiekiama</td>
<td>Ši funkcija supaprastina darbuotojų kompensacijų pokyčių apdorojimą.</td>
<td>Pateikiamas paprastas, supaprastintas procesas, skirtas atnaujinti darbuotojų įrašams naudojant kompensacijų darbo sritį ir susijusius puslapius.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Atsargų valdymas

Nepridėta jokių naujų funkcijų.

## <a name="localization"></a>Lokalizavimas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Konfigūruokite ir generuokite elektroninius dokumentus, kad būtų atitikta įvairių šalių / regionų teisiniams reikalavimams.</td>
<td>Elektroniniai dokumentai užprogramuoti X++ arba kaip išplėstinės stiliaus aprašų kalbos transformacijos (XSLT). Bet kokie formatų koregavimai reikalauja kūrėjų darbo. Prieiga prie duomenų ir formatavimo nėra izoliuota. Norint diegti pakoreguotą formatą, reikia naujo „Microsoft Dynamics AX“ karštųjų pataisų paketo, perrašančio esamą formatą. Pasirinktines kiekvieno formato modifikacijas reikia rankiniu būdu perkelti į naujo „Microsoft Dynamics AX“ karštųjų pataisų paketo šaltinio kodą.</td>
<td>Elektroninės ataskaitos (ER) yra naujas įrankis, kuriuo galima konfigūruoti ir generuoti elektroninius dokumentus, skirtus ne programuotojui, o verslo vartotojui. ER suteikia galimybę nustatyti duomenų modelius, kurie yra konkretaus domeno ir kaip dokumentų formatų duomenų šaltiniai yra nepriklausomi nuo „Microsoft Dynamics AX“ duomenų bazės. Pagal šiuos konkretaus domeno duomenų modelius (pvz., mokėjimų, „Intrastat‟ ataskaitų ar mokesčių ataskaitų), šiuos formatus gali konfigūruoti verslo naudotojas. Naudotojas formatus konfigūruoja naudodamas paprastus vaizdo įrankius, panašius į „Excel‟. ER šiuo metu palaiko elektroninių dokumentų generavimą teksto, XML ir „Excel‟ formatais. Šiuos dokumentus galima generuoti vienu metu ir supakuoti į „zip‟ failus. Duomenų modeliai ir formatai palaiko įvairias versijas. Formatų versijos gali turėti galiojimo laikotarpius. Kiekvienas duomenų modelis ar formato versija yra saugomi atskiroje konfigūracijoje ir partneriams bei klientams platinami per LCS. Partneriai ir klientai gali tinkinti „Microsoft‟ duomenų modelius bei formatus arba kurti savus. ER partnerių ir klientų konfigūracijų pakeitimus kaip pokyčius įrašo į „Microsoft‟ konfigūraciją, o tai supaprastina naujinimą į naujas „Microsoft‟ konfigūracijų versijas. Naudodami LCS, partneriai savo duomenų modeliais ir formatų konfigūracijomis taip pat gali dalytis su kitais partneriais ir klientais, kurie jas gali tinkinti ir bendrinti. Pokyčių tinkinimas ir lengvas naujinimas palaikomi visoje tinkinimo grandinėje.</td>
<td>ER supaprastina elektroninių dokumentų formatų kūrimą, priežiūrą ir naujinimą, kad būtų laikomasi teisinių įvairių šalių / regionų reikalavimų. ER pagreitina ir palengvina elektroninių dokumentų formatų kūrimo ar keitimo procesą. Šiuos pakeitimus vietoj programuotojų gali atlikti verslo naudotojai. Naudodami ER, partneriai ir klientai gali greičiau ir lengviau savo formatų tinkinimus atnaujinti naujomis formatų versijomis, kurias išleidžia „Microsoft‟ ar kiti partneriai. ER suteikia vieną bendrą būdą (per LCS), kuriuo „Microsoft‟ ir partneriai gali platinti elektroninių dokumentų konfigūracijas kitiems partneriams ir klientams. Naudodami ER, partneriai ir klientai taip pat gali lengviau pagal savo konkrečius verslo poreikius tinkinti, naujinti ir platinti elektroninių dokumentų formatus.</td>
</tr>
<tr>
<td>(MEX) Generuokite Meksikos pridėtinės vertės mokesčio (PVM) teisės aktų numatytas ataskaitas.</td>
<td><strong>Pardavimo ir pirkimo PVM</strong> ataskaitas turite generuoti naudodami nesumokėto PVM funkcijas, kad naudotojai galėtų pagal būseną identifikuoti operacijas, priklausančias sumokėto ir nesumokėto PVM dalims.</td>
<td><strong>Pardavimo ir pirkimo PVM</strong> ataskaitos buvo modifikuotos ir dabar į sąlyginių mokesčių funkciją atsižvelgiama tik naudojant konkrečius sudengimo laikotarpius, skirtus apibrėžti sumokėto ir nesumokėto PVM kodams.</td>
<td>Reikia keisti PVM kodų konfigūraciją, nes kitaip naudotojai negalės teisingai generuoti šių ataskaitų. Reikalinga sąlyginio PVM funkcija, ir naudotojas turi sukonfigūruoti atskirus sudengimo laikotarpius – įvykdytus ir neįvykdytus – kad būtų galima identifikuoti operacijas susijusiose dalyse.</td>
</tr>
<tr>
<td>(JPN) Tvarkykite Japonijos ilgalaikio turto pagreitinto nusidėvėjimo deklaracijos dokumentą.</td>
<td>Nepasiekiama</td>
<td>Siekiant geresnės priežiūros, svarbi deklaravimo informacija yra centralizuotai saugoma viename dokumente.</td>
<td>Dokumentų atitiktis ir tvarkymo lengvumas padeda sumažinti problemų skaičių atliekant auditą ir kitas peržiūras.</td>
</tr>
<tr>
<td>(JPN) Patikrinkite banko sąskaitos JBA simbolius.</td>
<td>Nepasiekiama</td>
<td>Galite patikrinti, ar kana pavadinimų laukuose yra tik tie simboliai, kuriuos leidžia JBA banko formatas.</td>
<td>Sumažinama pertraukų, atsirandančių dėl netinkamų simbolių, kai naudotojai generuoja mokėjimo failą.</td>
</tr>
<tr>
<td>(JPN) Atgaline data įvertinkite Japonijos ilgalaikio turto skirtumą centais ataskaitinių metų pabaigoje.</td>
<td>Nepasiekiama</td>
<td><strong>Ilgalaikio turto parametrų</strong> puslapyje galite pasirinkti, ar atgaline data vertinti ataskaitinio laikotarpio, ar finansinių metų pabaigoje.</td>
<td>Suteikiama daugiau lankstumo, kad būtų galima atitikti vietos praktiką.</td>
</tr>
<tr>
<td>(JPN) Generuokite Japonijos pelno mokesčių deklaravimo lentelių su priedais 16 seriją su bendra suma pagal ilgalaikio turto pagrindinį tipą.</td>
<td>Nepasiekiama</td>
<td>Ilgalaikio turto vertinimo modeliuose galite pasirinkti sumuoti pagal pagrindinį tipą. Pagal numatytąsias nuostatas ši funkcija naudojama su naujai sukurtu ilgalaikiu turtu.</td>
<td>Stambioms korporacijoms, turinčioms tūkstančius ilgalaikio turto objektų, suvestinės ataskaitos itin sumažina generuojamos ataskaitos dydį.</td>
</tr>
<tr>
<td>(JPN) Japonijos ilgalaikiam turtui pradėkite skirstyti kitų ataskaitinių metų specialiojo nusidėvėjimo rezervą.</td>
<td>Nepasiekiama</td>
<td>Ilgalaikio turto, turinčio tinkamą visiško nusidėvėjimo profilį, vertinimo modeliuose galite pasirinkti pradėti skirstymą nuo kito ataskaitinio laikotarpio arba kitų ataskaitinių metų.</td>
<td>Suteikiama daugiau lankstumo, kad būtų galima atitikti vietos praktiką.</td>
</tr>
<tr>
<td>(JPN) Generuokite Japonijos vartojimo mokesčių ataskaitą, į kurią įeitų patikslinti mokesčių tarifai.</td>
<td>Galima kurti 5 procentų mokesčio tarifo vartojimo mokesčio ataskaitą.</td>
<td>Vartojimo mokesčių ataskaitoje yra dalis, skirta patikslintam mokesčio tarifui (pavyzdžiui, 8 procentų).</td>
<td>Naująjį maketą paskelbė vyriausybė.</td>
</tr>
<tr>
<td>(ES) Konfigūruokite ES pardavimų sąrašo apvalinimo parametrus.</td>
<td>Įvairių šalių / regionų ES pardavimo sąrašo ataskaitų apvalinimo parametrai užprogramuoti naudojant X++ arba išplėstinės stiliaus aprašų kalbos transformaciją (XSLT).</td>
<td>Apvalinimo parametrai įtraukti į užsienio prekybos parametrus. Galite konfigūruoti apvalinimo tikslumą, apvalinimo metodą, išeigos tikslumą ir elgseną, kai sumos yra mažesnės už apvalinimo tikslumą.</td>
<td>Tokiu būdu suvienodinama ir supaprastinama ES pardavimo sąrašo ataskaitų konfigūracija. Koreguojant apvalinimo parametrus nebereikia kūrėjų darbo.</td>
</tr>
<tr>
<td>(ES) Konfigūruokite atvirkštinio mokesčio taikymo taisykles.</td>
<td>Vidaus atvirkštinio mokesčio scenarijui užprogramuotos atvirkštinio mokesčio taikymo taisyklės. Taikymo ribas galima nustatyti kiekvienai prekių grupei. Šią funkcija galima naudoti tik Didžiojoje Britanijoje.</td>
<td>Atvirkštinio mokesčio taikymo taisykles galite konfigūruoti kiekvienam dokumento tipui (pirkimo / pardavimo užsakymui, pirkimo užsakymo SF, laisvos formos SF ir kt.) ir atvirkštinio mokesčio grupei, kurioje sujungiamos prekės, prekių grupės ir pirkimo / pardavimo kategorijos. Taikymo taisyklės turi galiojimo datą. Taip pat atskirus PVM grupių PVM kodus galite pažymėti kaip taikomus atvirkštiniam mokesčiui. Pardavimo SF ataskaita pakoreguota, kad joje būtų rodoma informacija apie taikomą atvirkštinį mokestį. Šią funkciją galima naudoti visose Europos šalyse / regionuose.</td>
<td>Šis pakeitimas suvienodina atvirkštinio mokesčio taikymo taisyklių konfigūraciją ir suteikia galimybę Europos šalyse / regionuose taikyti vidaus atvirkštinio mokesčio taisykles.</td>
</tr>
<tr>
<td>(DE) Generuokite Vokietijos audito failą – GDPdUGoBD</td>
<td>Vartotojai gali nustatyti lentelių, kuriose yra finansiniai duomenys, aprašą eksportuoti Vokietijos auditorių ir institucijų patvirtintu formatu.</td>
<td>Ši funkcija buvo įvykdyta elektroninių ataskaitų konfigūravimo principu. Funkciją galima naudoti Vokietijoje ir Austrijoje.</td>
<td>Šis pakeitimas suteikia vartotojui daug daugiau galimybių duomenis formatuoti, keisti, taip pat suteikia visus elektroninių ataskaitų konfigūracijos gyvavimo ciklo valdymo privalumus, pvz., lengvą konfigūracijų keitimą, versijų kūrimą ir t. t.</td>
</tr>
<tr>
<td>(FR) Balanso sąrašas su bendrųjų grupės sąskaitų ataskaita.</td>
<td>Balanso sąrašas su bendrųjų grupės sąskaitų ataskaita yra realizuojamas kaip SSRS ataskaita (LedgerAccountSum_FR).</td>
<td>Balanso sąrašas su bendrųjų grupės sąskaitų ataskaita yra realizuojamas kaip „Management Reporter“ ataskaita, pateikiama LCS turto bibliotekos lokalizuotų finansinių ataskaitų aplanke.</td>
<td>Tokiu būdu vartotojams suteikiami visi tinkinimo privalumai ir laisvė naudojant finansines ataskaitas „Management Reporter“.</td>
</tr>
<tr>
<td>(ES) Mokėjimų mokėjimo pažymos, lydinčios pažymos ir kontrolės ataskaitos.</td>
<td>Visos šios ataskaitos yra realizuojamos kaip SSRS ataskaitos.</td>
<td>Šios ataskaitos buvo realizuotos kaip „Open XML“ šablonai, kuriuos galima naudoti „Microsoft Excel“.</td>
<td>Elektroninių mokėjimų konfigūracijose pateikiami mokėjimo failo formato sąranka ir šablonai. Tokiu būdu vartotojams suteikiami visi ataskaitų tinkinimo privalumai ir laisvė naudojant elektronines ataskaitas.</td>
</tr>
<tr>
<td>(ES) Konfigūruokite Intrastat apvalinimo parametrus.</td>
<td>Įvairių šalių / regionų Intrastat ataskaitų apvalinimo parametrai užprogramuoti naudojant X++ arba išplėstinės stiliaus aprašų kalbos transformaciją (XSLT).</td>
<td>Apvalinimo parametrai įtraukti į užsienio prekybos parametrus. Galite konfigūruoti apvalinimo tikslumą, apvalinimo metodą, išeigos tikslumą ir elgseną, kai sumos yra mažesnės už apvalinimo tikslumą.</td>
<td>Tokiu būdu suvienodinama ir supaprastinama Intrastat ataskaitų konfigūracija. Koreguojant apvalinimo parametrus nebereikia kūrėjų darbo.</td>
</tr>
<tr>
<td>(ES) Nustatykite Intrastat prekių kodus kategorijų hierarchijose.</td>
u<td>Intrastat prekių kodai yra atskiras sąrašas. Nors yra tipo Prekės kodas kategorijų hierarchija, šiuos prekių kodus „Retail HQ“ ir pardavimo kategorijoje galima nustatyti kaip numatytuosius.</td>
<td>Atskiras „Intrastat“ prekių kodų sąrašas yra suliejamas su tipo Prekės kodas produktų hierarchija.</td>
<td>Tokiu būdu suvienodinamas metodas, kuriuo prekių kodai priskiriami išleistiems produktams ir kategorijoms pardavimo ir pirkimo dokumentuose.</td>
</tr>
<tr>
<td>(ES) Teikite ataskaitas apie Intrastat papildomų vienetų kiekį, naudodami vienetų konvertavimo parametrą.</td>
<td>Intrastat prekės kode pateikiamas teksto laukas papildomiems vienetams nustatyti, o <strong>produkto</strong> kortelėje pateikiamas laukas papildomų vienetų kiekiui kilogramais nustatyti.</td>
<td>Intrastat prekės kodo papildomi vienetai parenkami iš vienetų sąrašo. Papildomų vienetų kiekis apskaičiuojamas naudojant vienetų konvertavimo parametrus.</td>
<td>Tokiu būdu suvienodinamas metodas, kuriuo operacijos vienetai perskaičiuojami kaip papildomi vienetai.</td>
</tr>
<tr>
<td>(ES) Numatytąjį transportavimo būdą priskirkite pristatymo būdui.</td>
<td>Nepasiekiama</td>
<td>Numatytojo transportavimo būdo laukas įtrauktas į pristatymo būdą.</td>
<td>Tokiu būdu supaprastinamas Intrastat ataskaitų rengimas.</td>
</tr>
<tr>
<td>(ES) Pažymėkite išleistą produktą, kuris neturi būti įtraukiamas į Intrastat ataskaitą.</td>
<td>Nepasiekiama</td>
<td>Į išleistą produktą įtraukta prekės neįtraukimo į Intrastat ataskaitą parinktis.</td>
<td>Tokiu būdu supaprastinamas Intrastat ataskaitų rengimas.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Gamyba

| Ką galite daryti? | Dynamics AX 2012 |
|------------------|------------------|
| Atskirame puslapyje, kuris atidaromas iš darbo srities **Gamybos vietos valdymas**, atlikite turimų gamybos užsakymų medžiagų patikrą. | Nėra |
| Pradėkite gamybos užduotis ir praneškite apie jų eigą, naudodami naująjį **Užduoties kortelės įrenginio** puslapį. | **Užduočių registracijos** forma yra pirmiausia skirta dideliems terminalų ekranams ir UI paprastai galima pasiekti pelės spustelėjimais. |

## <a name="master-planning-and-forecasting"></a>Bendrasis planavimas ir prognozavimas

| Ką galite daryti? | Dynamics AX 2012 | Dynamics AX 7.0 | Kodėl tai svarbu? |
|------------------|------------------|-----------------|------------------------|
| Įspėkite vartotoją, jei pardavimo užsakymas arba gamybos užsakymas neparuoštas pristatyti iki suplanuotos datos. | Įspėjimai, kuriuos sukuria bendrasis planavimas, vadinami *būsimųjų pranešimais*. *Būsimieji* yra sutartis tarp dviejų šalių pirkti arba parduoti turtą už kainą, sutartą šiandien (*būsimųjų kaina*), nors pristatoma ir mokama ateityje (*pristatymo data*). | *Ateities pranešimai* ir *ateities datos* atitinkamai pervardyti *apskaičiuotais atidėjimais* ir *atidėjimo datomis*. | Terminologija, naudota programoje „AX 2012“, buvo netiksli, ir dėl to atsirado neteisingų vertimų. |
| Gaukite sparčių įžvalgų apie vykdomo bendrojo planavimo būseną, skubius suplanuotus užsakymus ir suplanuotus užsakymus, dėl kurių atsiranda atidėjimų. | Informacija yra, tačiau išskaidyta įvairiose formose. | Darbo srityje **Bendrasis planavimas** vienu žvilgtelėjimu matoma informacija apie tai, kada buvo įvykdytas paskutinis bendrasis planavimas, ar įvyko klaidų, kokie yra skubūs suplanuoti užsakymai ir dėl kurių suplanuotų užsakymų atsiranda atidėjimų. | Galite pasinaudoti darbo srityje pateikiama apžvalga. Sujungiama aktuali informacija, kad būtų galima valdyti bendrąjį planavimą ir padėti gerinti produktyvumą. |
| Naudodami „Excel‟ naujinkite poreikio prognozes. | Nepasiekiama | Įvesdami poreikio prognozes, naujindami ir poreikio prognozes naikindami galite pasinaudoti nuoseklia integracija su „Excel‟. | Ji padeda padidinti efektyvumą ir produktyvumą. |
| Įvertinkite poreikį ateityje ir kurkite poreikio prognozes pagal praeities operacijų duomenimis. | Programoje „Microsoft Dynamics AX 2012 R3“ „Microsoft SQL Server“ analizės tarnybos prognozių modeliai naudojami kurti poreikio prognozėms. | Naudodami „Microsoft Azure“ mašininio mokymo debesies tarnybos pajėgumus ir išplečiamumą, vertinkite ateities poreikį. Mašininio mokymo tarnyboje prognozių modelius lengva naudoti ir išplėsti, kad būtų galima tenkinti klientų reikalavimus. Tarnyba parenka labiausiai atitinkantį modelį ir teikia pagrindinius našumo indikatorius (KPI), kurie gali būti naudojami apskaičiuoti prognozių tikslumui. | Generuokite tikslesnes prognozes naudodami mašininio mokymo metodus. |
| Optimizuokite užsakymo datą ir kiekį pagal vizualią susijusių vykdomo bendrojo planavimo veiksmų apžvalgą. | Veiksmų apžvalgos diagrama yra, bet joje rodomi visi susiję veiksmai. Veiksmus pritaikius, jie iš karto išnyksta iš vaizdo. | Veiksmų diagramoje pateikiama geresnė apžvalga. Ji apima parinktis, kurios leidžia rodyti tik pritaikytus veiksmus ir tiesiogiai susijusius veiksmus. Pritaikius veiksmus, jie rodomi blankiau, bet vis tiek matomi. Todėl apžvalga užlaikoma. Į veiksmų diagramą pridedama papildomos informacijos, kad duomenys būtų rodomi viename puslapyje. | Naudojatės pagerėjusiu produktyvumu, nes dėmesį skiriate tik aktualiems veiksmams. |

## <a name="procurement-and-sourcing"></a>Paraiškos

| Ką galite daryti? | Dynamics AX 2012 | Dynamics AX 7.0 | Kodėl tai svarbu? |
|------------------|------------------|-----------------|------------------------|
| Naudodami darbo sritį **Pirkimo užsakymų rengimas**, galite gauti sparčių įžvalgų apie rengiamų pirkimo užsakymų būseną. | Nepalaikoma | Darbo srityje **Pirkimo užsakymų rengimas** užsakymai apžvelgiami nuo to momento, kai jie sukuriami kaip juodraščiai ir sekami, darbo eigos patvirtinimo būsenomis ir toliau link patvirtinimo. | Pirkimo skyriui nebereikia informacijos ieškoti keliuose puslapiuose – dabar galima naudotis apžvalga, kuri pateikiama darbo srityje. |
| Naudodami darbo sritį **Pirkimo užsakymų gavimas ir apdorojimas**, galite gauti sparčių įžvalgų apie pirkimo užsakymus, kurie laukia gavimo, kad būtų lengviau juos apdoroti. | Nepalaikoma | Darbo srityje **Pirkimo užsakymų gavimas ir apdorojimas** apžvelgiami patvirtinti pirkimo užsakymai, kurie turi laukiančių gavimų ar siuntų. Darbo sritis apima po termino gautų kvitų ir laukiančių gavimų sąrašus, kad tiekėjui būtų lengviau atlikti iniciatyvią peržiūrą ir apdorojimą. Darbo srityje taip pat išvardyti pirkimo užsakymai, kuriems sandėlyje atlikta gavimo registracija, kad būtų galima užtikrinti, jog kvitas užregistruotas. Taip pat galima peržiūrėti tuos grąžintus pirkimo užsakymus, kurie dar neišsiųsti. | Jūsų pirkimo skyrius gali naudotis darbo srities teikiama apžvalga. Sujungiama aktuali informacija, kad būtų galima valdyti apdorojimą ir padėti gerinti produktyvumą. |
| Siųskite pirkimo užsakymus tvirtinti tiekėjo portale, nuomojamame „Dynamics AX“ kliente. Leiskite tiekėjui juos tvirtinti arba atmesti. | Nepalaikoma | Tiekėjo portalo sąsaja leidžia tiekėjams gauti pirkimo užsakymus ir juos patvirtinti arba atmesti. Ji taip pat tiekėjui leidžia apžvelgti visus jo sąskaitos patvirtintus pirkimo užsakymus. Pirkimo agentas gali siųsti pirkimo užsakymą ir prašyti tiekėjo jį patvirtinti. Tiekėjas turi būti registruotas „Microsoft Azure Active Directory“ („Azure AD“) vartotojas programoje „Dynamics AX“, tiekėjo kontaktinis asmuo ir turėti paskirtą saugos vaidmenį. | Jūsų pirkimo skyrius naudojasi sumažėjusiais biurokratiniais reikalavimais ir tuo, kad reikia mažiau neautomatiškai sekti atsakymus dėl pirkimo užsakymų, nes jų srautas tiesiogiai nukreiptas į sistemą. Kai yra vienas tiesos šaltinis, sumažėja nesusipratimų tarp kliento ir tiekėjo. |

## <a name="projects"></a>Projektai

| Ką galite daryti? | Dynamics AX 2012 | Dynamics AX 7.0 | Kodėl tai svarbu? |
|------------------|------------------|-----------------|------------------------|
| Darbuotojus rezervuokite kaip projektų išteklius. | Panašiai kaip ištekliai, darbuotojai rezervuojami tiesiogiai projektams bei ištekliams. | Darbo centro lentelėje, kurioje saugomi gamybos ištekliai, dabar galima darbuotojus rezervuoti kaip projekto išteklius. | Kai rezervuojate projektus, rezervuoti reikia tik išteklius. |

## <a name="retail-sales-marketing-and-customer-service"></a>Mažmeninė prekyba, rinkodara ir klientų aptarnavimas

### <a name="retail-hq"></a>Retail HQ

Naudojant „Microsoft Azure“ nuomojamą „Retail HQ“, žiniatinklio klientu galima centralizuotai valdyti ir visapusiškai matyti visus prekybos operacijų aspektus.

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Atlikite prekybos operacijas.</td>
<td>Norėdami tvarkyti šiuos duomenis, naudotojai turi naudoti kelias formas.
<ul>
<li>Kategorijų valdymas</li>
<li>Produkto valdymas</li>
<li>Kanalo produkto atributai</li>
<li>Asortimentai</li>
<li>Katalogų valdymas</li>
<li>Rinkiniai</li>
<li>Kainos &amp; nuolaidos</li>
</ul></td>
<td><strong>Kategorijų ir produktų valdymo</strong> darbo sritis įgalina toliau nurodytas funkcijas.
<ul>
<li>Asortimento valdymas.</li>
<li>Asortimento gyvavimo ciklo sekimas.</li>
<li>Išleistų produktų valdymas.</li>
</ul>
Darbo srityje <strong>Kainų ir nuolaidų valdymas</strong> galima naudoti toliau nurodytas funkcijas.
<ul>
<li>Konkretaus kanalo ir kategorijos kainų ir nuolaidų valdymas.</li>
<li>Kategorijų kainų taisyklių valdymas.</li>
<li>Kainų ir nuolaidų prioritetai, kurie leidžia priskirti prioritetus kainų grupėms ir nuolaidoms, kad galėtumėte kontroliuoti tvarką, kuria jos taikomos.</li>
<li>Priskyrimų ir katalogo nuolaidų valdymas.</li>
</ul>
Darbo srityje <strong>Katalogų valdymas</strong> galima naudoti toliau nurodytas funkcijas.
<ul>
<li>Aktyvių katalogų suvestinė.</li>
<li>Katalogų ciklo sekimas vienoje vietoje.</li>
</ul></td>
<td><ul>
<li>Darbuotojams leisdamos centralizuotai valdyti užduotis ir veiksmus, susijusius su prekybos vaidmeniu, darbo sritys pagerina jų efektyvumą ir produktyvumą.</li>
<li>Kainų ir nuolaidų prioritetų funkcija klientams leidžia labiau kontroliuoti, kaip naudojamos kainos ir nuolaidos. Ši funkcija taip pat įgalina naujus scenarijus, kai didesnėms parduotuvės kainoms teikiama pirmenybė už įprastas kainas.</li>
</ul></td>
</tr>
<tr>
<td>Valdykite mažmeninės prekybos kanalų diegimą ir operacijas.</td>
<td>Norėdamas atlikti toliau pateiktas užduotis, naudotojas turi naudoti kelias formas.
<ul>
<li>Kurti ir konfigūruoti naujus kanalus ir susijusius objektus.</li>
<li>Valdyti kasdienes parduotuvės veiklas.</li>
<li>Apdoroti „Microsoft Dynamics AX“ mažmeninės prekybos operacijas, generuoti mažmeninės prekybos išrašus ir naujinti „Microsoft Dynamics AX“ atsargas bei finansinius.</li>
</ul>
</td>
<td>Darbo srityje <strong>Kanalų diegimas</strong> galima atlikti toliau nurodytas užduotis.
<ul>
<li>Kurti naujus kanalus ir susijusius objektus.</li>
<li>Sekti mažmeninės prekybos parduotuvės konfigūracijos eigą.</li>
<li>Siekiant atlikti užduotį, atlikti reikiamus veiksmus arba pateikti informacijos.</li>
<li>Sekti įrenginių būseną ir tiesiogiai tikrinti ir atsisiųsti „Retail Modern POS“ (MPOS) programos diegimą parduotuvėse.</li>
<li>Naudoti visus susijusius puslapius.</li>
</ul>Darbo srityje 
<strong>Mažmeninės prekybos valdymas</strong> galima atlikti toliau nurodytas užduotis.
<ul>
<li>Valdyti darbuotojus ir darbuotojų elektroninio kasos aparato (EKA) teises.</li>
<li>Sekti konkrečios parduotuvės ar parduotuvių grupės pamainos būseną.</li>
<li>Tiesiogiai tikrinti ir atsisiųsti MPOS programos diegimą parduotuvėse.</li>
<li>Spausdinti ataskaitas ir naudoti susijusius puslapius.</li>
</ul>Darbo srityje 
<strong>Mažmeninės prekybos finansai</strong> galima atlikti toliau nurodytas užduotis.
<ul>
<li>Kurti, skaičiuoti ir registruoti konkretaus kanalo išrašus.</li>
<li>Planuoti paketines užduotis atsargoms naujinti ir apskaičiuoti bei užregistruoti išrašus.</li>
<li>Sekti atidarytus išrašus.</li>
<li>Sekti konkrečios parduotuvės ar parduotuvių grupės pamainos būseną.</li>
<li>Spausdinti ataskaitas ir sparčiai pasiekti visus susijusius puslapius.</li>
</ul></td>
<td>Darbuotojams leisdamos centralizuotai valdyti daugumą užduočių ir veiksmų, susijusių su kanalų diegimu, parduotuvių valdymu ir finansiniais, darbo sritys pagerina jų efektyvumą ir produktyvumą.</td>
</tr>
<tr>
<td>Valdykite mažmeninės prekybos IT operacijas.</td>
<td>Naudotojas turi naudoti kelias formas.</td>
<td>Naudojant darbo sritį <strong>Mažmeninės prekybos IT</strong> vienoje vietoje galima teikti konkretaus kanalo „Commerce Data Exchange“ užklausas, kad galėtumėte atlikti toliau pateiktas užduotis.
<ul>
<li>Atsisiųsti seansus.</li>
<li>Įkelti seansus.</li>
<li>Sekti nepavykusius seansus ir juos iš naujo inicijuoti arba paleisti.</li>
<li>Peržiūrėti arba vykdyti būsimas užduotis.</li>
</ul></td>
<td>Suteikdamos darbuotojams galimybę centralizuotai valdyti užduotis ir veiksmus, susijusius su mažmeninės prekybos IT operacijomis, darbo sritys pagerina jų efektyvumą ir produktyvumą.</td>
</tr>
<tr>
<td>Importuokite / eksportuokite duomenis naudodami duomenų objektus.</td>
<td>„AX 2012“ palaiko parengtos naudoti „Microsoft Dynamics Retail Management System“ (RMS) perkėlimą duomenų importavimo / eksportavimo sistemoje.</td>
<td>Mažmeninės prekybos duomenų objektai išplėsti ir palaiko visus bendruosius ir nuorodos duomenis, susijusius su mažmenine prekyba. Taip pat duomenų objektų palaikymas patobulintas visame „Dynamics AX“ sprendime.</td>
<td>Duomenų objektai klientams leidžia atlikti metaduomenimis grindžiamą duomenų importavimą ir eksportavimą. „OData“ objektai taip pat klientams leidžia „Dynamics AX“ integruoti su trečiųjų šalių programomis.</td>
</tr>
<tr>
<td>Atlikite išmaniąją analizę naudodami BI ataskaitas iš „Dynamics Microsoft AX“ ir EKA kliento.</td>
<td>Prieinamos daugiau nei 25 operacijų skyriaus ataskaitos ir penkios kanalų ataskaitos.</td>
<td>Prieinamos daugiau nei 30 operacijų skyriaus ataskaitų ir 10 kanalų ataskaitų.</td>
<td>Šios ataskaitos klientams leidžia turėti daugiau BI, kad galėtų prognozuoti tendencijas, atskleisti įžvalgas ir veikti nuolatiniu didžiausiu našumu.</td>
</tr>
<tr>
<td>Analizuokite mažmeninės prekybos kanalų pardavimo duomenis naudodami „Power BI“ turinį „Stebėti „Retail Channel Performance“.</td>
<td>Neprieinama</td>
<td>PowerBI.com pasirinkite <strong>Gauti duomenis</strong> ir tada pasirinkite turinio paketą <strong>Dynamics AX – Retail Channel Performance</strong>. Įveskite savo „Dynamics AX“ galinio punkto URL, kad jūsų duomenys atsispindėtų ataskaitų srityje.</td>
<td>Trimis–keturiais spustelėjimais organizacijos gali „Power BI“ ataskaitų sritį su svarbiais finansiniais duomenimis. Organizacija turinį gali prisitaikyti. Be to, vartotojai gali į savo pritaikytas darbo sritis programoje „Dynamics AX“ įdėti „Power BI“ ataskaitų sričių plytelių, kad vienu žvilgtelėjimu galėtų matyti analizės informaciją.</td>
</tr>
<tr>
<td>Konfigūruokite klientų teises.</td>
<td>Nepasiekiama</td>
<td>Klientai gali pasirinkti, ar EKA operacijos gali būti prieinamos klientams. „Retail Server‟ naudoja teises taikomojo programavimo sąsajos (API) skambučiams.</td>
<td>Jis suteikia galimybę konfigūruoti kliento lygio teises.</td>
</tr>
<tr>
<td>Valdykite ir tikrinkite objektų konfigūracijas.</td>
<td>Nepasiekiama</td>
<td>Konfigūracijų tvarkytuvo ir tikrintuvo funkcija įgalina toliau pateiktas funkcijas.
<ul>
<li>Masinis konfigūracijų duomenų įkėlimas</li>
<li>Verslo objektų tikrinimas</li>
</ul></td>
<td>Ji suteikia galimybę konfigūraciją paleisti pakartotinai ir tikrinti įvairių konfigūracijos elementų būseną ir užbaigtumą.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>„Retail Hardware Station“

| Ką galite daryti? | Dynamics AX 2012 | Dynamics AX 7.0 | Kodėl tai svarbu? |
|------------------|------------------|-----------------|------------------------|
| Leiskite EKA įrenginiams prisijungti prie išorinių įrenginių, pvz., spausdintuvų, kasos stalčių ar mokėjimo įrenginių. | MPOS aparatūros profilis naudojamas nurodyti naudojamiems įrenginiams. | Pridėtas aparatūros profilis palaiko įvairesnę aparatūrą iš vienos stoties į kitą. Naujas aparatūros stoties profilis palaiko unikalų kiekvienos aparatūros stoties terminalo ID, kai apdorojamos elektroninio lėšų pervedimo (EFT) operacijos. EFT palaikymas sulietas su aparatūros stotimi, kad, apdorojant EFT mokėjimus, mažiau dalyvautų MPOS. | Suteikiama daugiau diegimų lankstumo. Taip pat suteikiama didesnė sauga ir mažiau matomi kredito kortelių duomenys. |

### <a name="retail-server-and-data-management"></a>„Retail Server‟ ir duomenų valdymas

„Retail Server‟ ir duomenų valdymo funkcija naudotojams ir įmonėms leidžia kurti integruoto kanalo pirkimo patirtį interneto, parduotuvių ir skambučių centrų kanaluose.

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Prisijunkite prie „Commerce Runtime“ (CRT) duomenų bazės, kurioje, naudojant CRT tarnybas, saugomi kanalo verslo duomenys.</td>
<td>Palaikomi „OData V3‟.</td>
<td>Palaikomi „OData V4‟.</td>
<td>Klientui lengviau neatsilikti nuo „OData‟ standartų. Integruojant pardavimą parduotuvių, mobiliuosiuose ir interneto kanaluose, taip pat sukuriama patikima integruoto kanalo patirtis.</td>
</tr>
<tr>
<td>Mažmeninės prekybos paslaugoms palaikymą teikite kaip saugomam paslaugų rinkiniui.</td>
<td>Naudojant „Retail Server‟, „E-commerce‟ API nepalaikoma.</td>
<td>Naudojant „Retail Server‟, dabar prieinama „E-commerce‟ API, kad būtų palaikomi interneto scenarijai.</td>
<td>Teikiamos nuomojamos ir keičiamo dydžio e. prekybos paslaugos, kurias galima naudoti trečiosios šalies interneto parduotuvėse.</td>
</tr>
<tr>
<td>Perkelkite duomenis tarp „Microsoft Dynamics AX“ operacijų skyriaus ir kanalų naudodami „Commerce Data Exchange“.</td>
<td>„Commerce Data Exchange“ yra sistema, kuri perkelia duomenis tarp „Microsoft Dynamics AX“ ir mažmeninės prekybos kanalų, pvz., interneto parduotuvių ar fizinių parduotuvių. Daugiau informacijos rasite <a href="/dynamicsax-2012/appuser-itpro/commerce-data-exchange">Commerce Data Exchange [AX 2012]</a>.</td>
<td>Funkcijos atitinka „Microsoft Dynamics AX 2012 CU8“ funkcijas. Tačiau atminkite toliau pateiktą informaciją.
<ul>
<li>„Commerce Data Exchange“ iš naujo suprojektuota debesiui.</li>
<li>„Async‟ tarnyba naudoja tiesioginę duomenų bazės prieigą prie kanalų duomenų bazės.</li>
<li>„Commerce Data Exchange“: „Real-time Service“ prijungta kaip pasirinktinė „Microsoft Dynamics AX“ tarnyba.</li>
<li>MPOS valdo sinchronizavimą tarp autonominės duomenų bazės ir „Retail Server‟.</li>
</ul></td>
<td>„Commerce Data Exchange“ iš naujo suprojektuota debesies platformai. Toliau valdoma, kaip perkeliami duomenys tarp „Microsoft Dynamics AX“ ir mažmeninės prekybos kanalų, pvz., interneto parduotuvių ar fizinių parduotuvių.</td>
</tr>
<tr>
<td>Teikite palaikymą „prijungti ir leisti‟ funkcijai, pusiau integruotam kelių kanalų mokėjimų apdorojimui naudodami mokėjimų SDK.</td>
<td>„AX 2012“ suteikia toliau nurodytas funkcijas.
<ul>
<li>Visų kanalų – EKA, el. prekybos ir skambučių centrų – palaikymas.</li>
<li>Esančios ir nesančios kortelės palaikymas.</li>
<li>Mokėjimo priėmimo puslapis.</li>
<li>Išorinis „LS5300‟ ir „MX925‟ kaip mažmeninės prekybos SDK kodo pavyzdžio palaikymas.</li>
</ul></td>
<td>Dabartinė „Dynamics AX“ versija palaiko visas esamas „Microsoft Dynamics AX for Retail 2012“ kredito / debeto kortelių funkcijas ir keturis naujus patobulinimus.</td>
<td>Ji klientui leidžia apdoroti kredito / debeto kortelės mokėjimų operacijas.</td>
</tr>
<tr>
<td>Aktyvinkite įrenginius naudodami „Microsoft“ paskyrą („Microsoft Azure Active Directory“ („Azure AD“)).</td>
<td>Neprieinama</td>
<td>Suteikiamos toliau nurodytos funkcijas.
<ul>
<li>„Azure AD“ aktyvinimu padidinta debesies sauga.</li>
<li>Patobulinta atpažinimo ženklų valdymo sauga.</li>
<li>Pagerintas patikimumas, trikčių diagnostik ir klaidų pranešimai aktyvinant</li>
<li>Supaprastintos IT administravimo užduotys, susijusios su aktyvinimu.</li>
<li>Patikslintas grėsmių modelis ir ištaisytos saugos spragos.</li>
</ul></td>
<td>Suteikiami toliau nurodyti privalumai.
<ul>
<li>Naudojant „Azure AD“ ir įrenginio atpažinimo ženklą / ID (RS skambučiai, naudojantys atpažinimo ženklą, konkretaus naudotojo programų saugyklą), padidinta sauga.</li>
<li>Stabdomas neteisėtas nuotolinis MPOS naudojimas (įrenginys blokuojamas).</li>
<li>PCI atitikties tikslais sekami MPOS įrenginiai.</li>
<li>Naudojant įrenginio atpažinimo ženklą, fiziniai įrenginiai susiejami su verslo subjektu (registru).</li>
<li>Pirmajame MPOS sąlyčio taške inicijuojamos sklandžių MPOS funkcijų nuostatos (numeracijos ir aparatūros profiliai).</li>
<li>Iš būstinės pranešama įrenginio informacija.</li>
</ul></td>
</tr>
<tr>
<td>Valdykite raiškiųjų publikavimo kanalų turinį, skirtą autorizuoti ir naudoti medijos galerijai.</td>
<td>Nepasiekiama</td>
<td><ul>
<li>Teikite palaikymą išorinių nuomojamų ir „Retail‟ nuomojamų vaizdų įkėlimui ir peržiūrai, tvarkymui bei naikinimui medijos galerijoje.</li>
<li>Teikite palaikymą vaizdų įkėlai ir peržiūrai objektų puslapiuose (<strong>Produktai</strong>, <strong>Katalogai</strong> ir t. t.), vaizdą susiedami galerijoje ir vaizdą įkeldami iš darbalaukio.</li>
<li>Optimizuokite miniatiūros, pasirinktinio ir pradinio dydžių vaizdus.</li>
<li>Masiškai siekite objektus naudodami masinio susiejimo šabloną ir fono užduotis.</li>
<li>„Microsoft Excel“ integracija perrašo atributų grupės apribojimą pavadinimų suteikimo konvencijoms ir iš anksto nustatytiems maršrutams.</li>
<li>Teikite palaikymą neinternetiniams vaizdams ir apsaugokite asmeninio identifikavimo informacijos (PII) turinio vaizdus, pvz., „Retail‟ saugomus darbuotojų ir klientų vaizdus.</li>
</ul></td>
<td><ul>
<li>Dėmesys skiriamas išoriškai saugomų vaizdų probleminėms vietoms, kad nereikėtų naršyti pirmyn ir atgal, o būtų galima viską tvarkyti vienoje vietoje.</li>
<li>Suteikiama veiksminga turinio valdymo priemonė naudojant medijos galeriją įkeltiems ir išoriškai saugomiems vaizdams, bei suteikiama filtravimo funkcija, kad būtų lengviau rasti vaizdus.</li>
<li>Galima lengvai kurti masinius susiejimus taip išoriškai saugomų vaizdų ir objektų, pvz., produktų ir katalogų.</li>
<li>Palaikomas vaizdų saugojimas „Retail‟ ir „Excel‟ integracija, kad būtų lengva naujinti.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Turininga klientų patirtis

„Retail‟ siūlo įtraukiančią mobilią patirtį bet kur, bet kada ir bet kokiame įrenginyje. Ši funkcija įgalina patobulintą pirkimo ir parduotuvių patirtį visuose kanaluose.

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ieškokite, naršykite, peržvelkite ar nuskaitykite produktus, pridėkite produktus į krepšelį, priimkite mokėjimą ir atsiskaitykite naudodami intuityvią, liesti skirtą, turiningą ir įtraukiančią MPOS naudotojo patirtį.</td>
<td>„AX 2012“ įgalina toliau nurodytas funkcijas.
<ul>
<li>Atlikti pardavimus, grąžinimus ir anuliavimus.</li>
<li>Kurti, modifikuoti ir paimti klientų užsakymus.</li>
<li>Atlikti pamainos ir stalčiaus operacijas.</li>
<li>Paimti ir gauti užsakymus bei vykdyti inventorizacijas.</li>
<li>Peržiūrėti parduotuvių ataskaitas.</li>
</ul></td>
<td>Suteikiamas funkcijų atitikimas su „AX 2012 MPOS“. Iš jų galima paminėti toliau nurodytas funkcijas.
<ul>
<li>Klientų peržvalga visose parduotuvėse / kanaluose.</li>
<li>Galimybė kurti klientų užsakymus nenaudojant „Real-time Service‟.</li>
<li>Patobulintos įrenginių aktyvinimo darbo eigos, būsena ir klaidų pranešimai.</li>
<li>Išplečiamumo patobulinimai, pvz., išankstiniai ir vėlesni paleidikliai bei veiklos palaikymas tinkinimui gerinti.</li>
</ul></td>
<td>Bet kur parduotuvėje naudodami mobiliuosius įrenginius pardavėjai gali apdoroti pardavimo operacijas ir klientų užsakymus bei atlikti kasdienes operacijas ir atsargų valdymą.</td>
</tr>
<tr>
<td>EKA paleiskite kaip žiniatinklio programą naudodami Debesies EKA.</td>
<td>Nepasiekiama</td>
<td>Suteikiamas funkcijų atitikimas su MPOS. Iš jų galima paminėti toliau nurodytas funkcijas.
<ul>
<li>Įrenginio aktyvinimas naudojant AAD</li>
<li>Reaguojantis maketo dizainas</li>
<li>„Edge“, „Internet Explorer“ ir „Chrome“ naršyklių palaikymas.</li>
</ul></td>
<td>Pateikiama žiniatinklio programos EKA, turinti funkcijų, suderinamų su MPOS ir kuri gali būti naudojama visose platformose ir naršyklėse be jokių diegimo išlaidų.</td>
</tr>
<tr>
<td>Integruokite su turinio valdymo sistemomis, kad sukurtumėte integruoto kanalo el. prekybos svetainę.</td>
<td>Palaikoma „Microsoft SharePoint“ ir trečiųjų šalių parduotuvių pirmieji lygmenys.</td>
<td>Suteikiama el. prekybos platforma, kuri palaiko trečiųjų šalių parduotuvių pirmuosius lygmenis. Į platformą įeina toliau nurodytos funkcijos.
<ul>
<li>Išsami klientų API.</li>
<li>Autentifikavimo integracija su bet kokiais trečiosios šalies atviro ID teikėjais.</li>
<li>Mokėjimų integracija.</li>
</ul></td>
<td>Klientai dabar gali lanksčiai naudoti savo pasirinktą turinio valdymo sistemą.</td>
</tr>
<tr>
<td>Pasiekite tikslinius klientus naudodami paštu užsakomus katalogus ir racionalizuokite operacijas greitai įvesdami užsakymus, padėdami parduoti ir įvykdydami užsakymus naudodami skambučių centrą.</td>
<td><ul>
<li>Skambučių centro kanalas</li>
<li>Paštu užsakomi katalogai</li>
<li>Greitas užsakymų įvedimas ir padedamas pardavimas</li>
<li>Patobulintas užsakymų vykdymas</li>
<li>Klientų aptarnavimas</li>
<li>Integruota kainodara ir akcijos / nuolaidos</li>
</ul></td>
<td>Galimas funkcijų atitikimas su „AX 2012“ skambučių centro sprendimu, išskyrus kainų perrašymus.</td>
<td>Skambučių centrai yra mažmeninės prekybos kanalo tipas, kuris darbuotojams leidžia telefonu priimti užsakymus iš klientų ir kurti pardavimo užsakymus.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>„Commerce Essentials“

Į mažmeninę prekybą ir prekybą orientuota konfigūravimo parinktis padeda supaprastinti mažmeninei prekybai būdingus diegimus.

| Ką galite daryti? | Dynamics AX 2012 | Dynamics AX 7.0 | Kodėl tai svarbu? |
|------------------|------------------|-----------------|------------------------|
| Naudokite „Commerce Essentials‟ ataskaitų sritį. | Galimas vietos puslapis su saitais į meniu elementus. | „Commerce Essentials“ ataskaitų srityje pateikiami saitai į dažnas užduotis, įskaitant saitus į darbo sritis, „Power BI“ žiniatinklio valdymą, parankinius, vėliausius puslapius ir dabartinius darbo elementus. | Patobulinta ataskaitų sritis darbuotojams suteikia daugiau galimybių būti efektyvesniems ir suteikia lankstų pradžios tašką atlikti bet kokiai mažmeninei prekybai būdingai užduočiai. |
| Naudokite duomenų objektus pasiekti paskyros pokyčiams. | Paskyrų pokyčiai eksportuojami į failų sistemos aplanką. | Paskyrų pokyčius galima pasiekti naudojant duomenų objektus. | Ši funkcija suteikia daugiau lankstumo, kai duomenys perkeliami tarp atskirų sistemų. Šią funkciją galima taip pat patobulinti naudojant „OData‟ programas. |
| Naudokite Debesies EKA ir MPOS. | Iš karto palaikoma tik Įmonės EKA (EPOS). | MPOS ir Debesies EKA pakeičia EPOS klientą. Pagal numatytąsias nuostatas el. prekybos kanalas taip pat įtrauktas į „Commerce Essentials‟. | Ši funkcija įgaliną geresnį parengto naudoti kanalo palaikymą su sparčiai diegiamais elektroninio kasos aparato klientais. |
| Įdiekite ir prižiūrėkite dviejų pakopų architektūrą. | Duomenų importavimo / eksportavimo sistema suteikia galimybę perkelti duomenis tarp „AX 2012“ ir trečiųjų šalių sistemų. | Duomenų objektai sukurti pagerinti dviejų pakopų architektūros palaikymui. | Duomenų objektai ir „OData‟ programos suteikia abstraktųjį lygmenį, kad būtų lengviau įdiegti ir prižiūrėti dviejų pakopų scenarijus. |
| Supaprastinkite formas. | Norint supaprastinti UI, reikia pasirinktinio kodo. | Formų ir meniu plėtiniai suteikia standartizuotą UI supaprastinimą. | Ši funkcija leidžia greičiau ir lengviau derinti formas pagal pardavėjo poreikius. |

### <a name="pos-task-recorder"></a>EKA užduočių įrašytuvas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kurkite ir bendrinkite „Modern POS‟ užduočių vadovus ir dokumentus.</td>
<td>Nepasiekiama</td>
<td>MPOS užduočių įrašytuvas palaiko toliau nurodytas funkcijas.
<ul>
<li>Kurkite įvairių užduočių, kurios atliekamos MPOS, įrašus.</li>
<li>Generuokite dokumentą, kuriame yra veiksmų ir ekrano kopijų, ir susiekite jį su verslo proceso modelio mazgu.</li>
</ul></td>
<td>Partneriai ir nepriklausomi programinės įrangos tiekėjai (ISV) gali tinkinti MPOS ir pateikti palaikymo dokumentų, skirtų mokyti naudotojams.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Išplečiamumas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Teikite palaikymą išplečiamiems ir lengvai diegiamiems „Retail‟ komponentams visoje būstinėje, skambučių centre, el. prekyboje ir EKA.</td>
<td>Komponentus galima išplėsti naudojant „Retail SDK‟. Nepalaikomi jokie pakavimo ir diegimo pajėgumai.</td>
<td>Išplečiamumo gaudyklės patobulintos visuose komponentuose, kad būtų geriau palaikomas kodo atskyrimas ir aptarnaujamumas. Čia pateiktos kai kurios įtrauktos funkcijos.
<ul>
<li>Darbo eiga, veikla ir operacija.</li>
<li>Išankstiniai paleidikliai ir vėlesni paleidikliai, kurie leidžia lengvai pratęsti darbo eigą.</li>
<li>Programų ir operacijų paleidikliai.</li>
</ul>
Be to, galima naudoti sistemą, kuri suteikia galimybę kurti ir pakuoti šiuos komponentus su „MSBuild“, ir tada sklandžiai įdiegti savo tinkinimą naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).</td>
<td>Pardavėjai turi labai konkrečių reikalavimų, paremtų operacijos segmentais ir regionais. Suteikdami lengvai išplečiamą platformą, įgaliname naudojimą visuose segmentuose ir rinkose. Kadangi „Retail‟ architektūra taip pat yra labai paskirstyta, gebėjimas sklandžiai diegti labai pagerina produktyvumą.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Ciklo valdymas

„Lifecycle Services“ (LCS) pateikia paslaugų rinkinį, kurį klientai ir partneriai gali naudoti norėdami valdyti sistemos ciklą – nuo registracijos iki kasdienių operacijų.

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Valdykite programą naudodami debesies diegimo paslaugas.</td>
<td>Nepasiekiama</td>
<td>Diegti debesyje galima toliau nurodytas topologijas.
<ul>
<li>Mažmeninės prekybos vieno langelio bandomoji topologija.</li>
<li>Mažmeninės prekybos kelių langelių didelio pasiekiamumo topologija.</li>
<li>Kūrėjų topologija su „Retail SDK“.</li>
</ul>
Yra patobulintas „mažai liečiamas“ kliento komponento diegimas naudojant savitarnos diegimą.
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Pritaikytų paketų nusiuntimo ir paskirstymo naudojant savitarnos diegimą palaikymas.</li>
</ul></td>
<td>Debesies diegimo paslaugos suteikia toliau nurodytus privalumus.
<ul>
<li>Labai sumažintos „Retail HQ‟ komponentų diegimo pastangos ir sudėtingumas.</li>
<li>Vietinis diegimas į „Microsoft Azure“ viešąjį debesį.</li>
<li>Patobulintas parduotuvės komponentų savitarnos diegimas, kad konfigūravimas būtų lengvesnis ir intuityvesnis</li>
</ul></td>
</tr>
<tr>
<td>Stebėkite sistemos būklę ir diagnozuokite klaidas bei problemas.</td>
<td>Šiai funkcijai reikia <a href="https://www.microsoft.com/en-us/download/details.aspx?id=58205">System Center 2012 Management Pack for Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Stebėti ir diagnozuoti „Retail‟ komponentus dabar galima naudojant <strong>Valdymo įžvalgų</strong> ataskaitų sritį LCS.</td>
<td><strong>Valdymo įžvalgų</strong> ataskaitų sritis yra debesimi paremtas stebėsenos portalas, kuris pašalina poreikį įdiegti sistemos centro operacijų tvarkytuvo (SCOM) infrastruktūrą.</td>
</tr>
<tr>
<td>Kurkite, konfigūruokite, atsisiųskite ir įdiekite „Retail Hardware Station‟ bei įrenginius naudodami savitarną.</td>
<td>Naudodamas diegimo pakuotuvą ir įmonės portalą, naudotojas gali atlikti automatinį visų komponentų, kurių reikia konkrečiame kompiuteryje, diegimą ir konfigūravimą pagal apibrėžtą topologiją.</td>
<td>Kadangi yra tik du diegimo paketai (vienas – MPOS kliento ir kitas – „Retail Hardware Station‟ komponento), savitarna sumažino darbą, reikalingą kiekviename šių kliento komponentų diegimo lygmenyje.</td>
<td>Savitarna siekia minimizuoti reikalavimus ir palengvinti naudotojui atlikti diegimą.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Pardavimas

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sparčiai apžvelkite pristatymo alternatyvas, kai klientams pažadate užsakymų.</td>
<td>Kai yra produkto prieinamumo apribojimų ir negalima patenkinti kliento pageidaujamos vieno ar kelių užsakymo produktų pristatymo datos, užsakymų žadėjimo užduotis tampa iššūkiu. Norėdamas rasti alternatyvų, kurios galėtų kompensuoti prieinamumo ir siuntimo laiko problemas, kad būtų galima tenkinti kliento pageidaujamą datą, arba klientams pasiūlant pristatymo sprendimą, kurį jie galėtų priimti ir kuriuo galėtų pasitikėti, užsakymo apdorotojui gali tekti atidaryti kelias formas, kiekvienoje iš kurių pateikiama tik dalis reikiamos informacijos. Konkrečiau: vienoje formoje rodomas turimas kiekis visose teritorijose, kitoje formoje rodomas turimas kiekis vidinės įmonės aplinkoje, trečia forma naudotojams leidžia apskaičiuoti anksčiausią galimą datą vienai teritorijai / variantui vienu metu, o ketvirtoje formoje rodomi tiekimo užsakymai. Todėl naudotojai nėra tikri, ar apsvarstė visas aktualias galimybes, o ne tik pasirinko skubų, bet ne optimalų sprendimą. Naudotojai taip pat nesijaučia efektyvūs, nes užsakymų žadėjimo eigoje įvyksta daug pertraukų, jiems atidarant ir uždarant kelis puslapius ir sujungiant įžvalgas bei galimybes.</td>
<td>Pagal esamus pristatymo datos skaičiavimo algoritmus <strong>Pristatymo alternatyvų</strong> puslapyje pateikiama nauja užsakymų žadėjimo naudotojo patirtis.
<ul>
<li>Aktuali informacija iš kelių formų konsoliduojama į vieną vietą.</li>
<li>Siūlomi „paruošti“ alternatyvūs pristatymo paketai, pvz., kombinacinis vietos / sandėliavimo / varianto / transportavimo režimas, paremtas greičiausio pristatymo (anksčiausios galimos datos) kriterijumi, kurį vartotojas gali pasirinkti.</li>
<li>Naudotojui leidžiama pasirinti parinktis iš modeliavimo sąsajos ir jas perkelti į pardavimo užsakymo eilutę.</li>
</ul></td>
<td>Įmonės, kurios siekia teikti aukšto lygio klientų aptarnavimą, tuo pačiu įsipareigodamos vykdyti atsargų optimizavimo strategiją, turi gebėti užsakymus žadėti patikimai ir konkurencingai. Juk jų klientų verslui reikia, kad produktus būtų galima gauti laiku. <strong>Pristatymo alternatyvų</strong> užduočių puslapis užsakymų žadėjimo užduotį paspartina, lengvina ir labiau sistemina, vienoje interaktyvioje vietoje identifikuodamas ir rekomenuodamas geriausias užsakymų pristatymo datas.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Aptarnavimo valdymas

Nepridėta jokių naujų funkcijų.

## <a name="transportation-management"></a>Transportavimo valdymas

Nepridėta jokių naujų funkcijų.

## <a name="travel-and-expense"></a>Kelionės ir išlaidos

Nepridėta jokių naujų funkcijų.

## <a name="warehouse-management"></a>Sandėlio valdymas

| Ką galite daryti? | Dynamics AX 2012 | Dynamics AX 7.0 | Kodėl tai svarbu? |
|------------------|------------------|-----------------|------------------------|
| Atsisiųskite, diekite ir konfigūruokite sandėlio mobiliųjų įrenginių portalą. | Portalą atsisiųsti, įdiegti ir konfigūruoti galite „Microsoft Dynamics AX“ diegimo proceso metu, naudodami įprastą sąranką. Jis skirtas savarankiškam vietiniam diegimui ir konfigūravimui. | Galite atsisiųsti atskirą diegimo programą naudodami sandėlio valdymo srities meniu elementą. Jis skirtas savarankiškam vietiniam diegimui ir konfigūravimui. | Kai nustatote mobiliojo įrenginio funkciją, turite sandėlio mobiliųjų įrenginių portalą įdiegti ir konfigūruoti vietoje bei užmegzti ryšį su „Dynamics AX“ debesyje. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Kas naujo arba pakeista finansų ir operacijų pagrindiniame puslapyje](whats-new-changed.md)

[Nauji užduočių vedliai (2016 m. vasario mėn.)](new-task-guides-available-february-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

