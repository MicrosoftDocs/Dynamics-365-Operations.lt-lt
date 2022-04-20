---
title: Kas nauja ar pasikeitė „Dynamics 365 for Operations“ 1611 versijoje (2016 m. lapkričio mėn.)
description: Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 for Operations“ 1611 versijos funkcijos.
author: sericks007
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 43a53d5940b2595abb305a08e6f52661bee8ca62
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/05/2022
ms.locfileid: "8548086"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Kas nauja ar pasikeitė „Dynamics 365 for Operations“ 1611 versijoje (2016 m. lapkričio mėn.)

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 for Operations“ 1611 versijos funkcijos.

## <a name="cost-accounting"></a>Kaštų apskaita

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nurodykite savikainos elemento dimensijos ir importuokite savikainos elemento dimensijos narius.</td>
<td>Išlaidų elementai naudojami išlaidų apskaitoje norint skirstyti išlaidas ir dokumentuoti išlaidų srautą. Pirminiai išlaidų elementai importuojami naudojant „Microsoft Dynamics 365 for Operations“ duomenų jungtį, kad būtų galima gauti pagrindines sąskaitas tiesiai iš „Operations“ arba naudojant bendrąją duomenų jungtį, kai pagrindinės sąskaitos gaunamos per „Microsoft Excel“ iš bet kurio kito tipo šaltinio sistemos. Importavus pagrindines sąskaitas į išlaidų apskaitą jos naudojamos kaip išlaidų elemento dimensijos nariai. Antrinius išlaidų elementus nurodo vartotojas ir jie naudojami paskirstymuose norint dokumentuoti išlaidų srautą.</td>
</tr>
<tr>
<td>Susieti išlaidų elemento dimensijas.</td>
<td>Jei jūsų juridiniuose subjektuose esančių pagrindinių sąskaitų negalima bendrinti dėl įstatymuose pateikiamų apskaitos reikalavimų, galite susieti importavę jas į išlaidų apskaitą, kad gautumėte visapusišką vaizdą organizacijoje.</td>
</tr>
<tr>
<td>Nurodyti išlaidų objekto dimensijas ir importuoti išlaidų objekto dimensijos narius.</td>
<td>Išlaidų objektai yra bet kokio tipo objektas, kuriam priskiriamos išlaidos. Dažniausiai pasitaikantys išlaidų objektai yra produktai, projektai, ištekliai, padaliniai, išlaidų centrai ir geografiniai regionai. Galite naudoti „Microsoft Dynamics 365 for Operations“ duomenų jungtį, kad gautumėte finansines dimensijas ir vertes iš „Operations“ arba naudoti bendrąją duomenų jungtį, kai galite gauti dimensijas ir vertes naudodami „Excel“ iš bet kurio kito tipo šaltinio sistemos. Pvz., jei išlaidų centro dimensiją naudojate kaip objekto dimensiją, visi importuoti išlaidų centrai yra išlaidų objekto dimensijos nariai.</td>
</tr>
<tr>
<td>Nurodyti arba importuoti statistines dimensijas</td>
<td>Statistikos dimensijos nariai matuojami nepiniginiais vienetais, pavyzdžiui, įrenginio valandos, darbuotojų skaičius ir kvadratas. Jie naudojami ataskaitose arba kaip paskirstymų pagrindas.</td>
</tr>
<tr>
<td>Sukurkite statistinės priemonės teikimo įrankio šablonus.</td>
<td>Statistinių priemonių teikimo įrankio šablonas naudojamas norint „Dynamics 365 for Operations“ duomenis paversti statistinėmis priemonėmis. Tada šablonas susiejamas su nurodytu statistinės dimensijos nariu. Šablonai iš anksto filtruojami, kad juose būtų rodomos tik su finansinėmis dimensijomis susietos lentelės.</td>
</tr>
<tr>
<td>Sukurkite savikainos apskaitos didžiąsias knygas.</td>
<td>Savikainos apskaitos didžioji knyga yra agnostinė didžioji knyga, naudojanti savo kalendorių ir valiutą. Ji atlieka svarbų vaidmenį apdorojant visas išlaidų operacijas. Pavyzdžiui, savikainos apskaitos didžiojoje knygoje išlaidos klasifikuojamos pagal savus savikainos elementus ir sujungiamos pagal savas objektų dimensijas. Norėdami parengti valdymo ataskaitas iš įvairių perspektyvų, galite sukurti tiek savikainos apskaitos didžiųjų knygų, kiek jums reikia.</td>
</tr>
<tr>
<td>Sukurkite savikainos kontrolės įtaisus.</td>
<td>Savikainos kontrolės įtaisai sudaro savikainos struktūrą ir nurodo išlaidų srautą savikainos apskaitos didžiojoje knygoje. Jie turi būti susieti su savikainos objekto dimensijomis, kad atitiktų savikainos objekto dimensijas didžiojoje knygoje.</td>
</tr>
<tr>
<td>Apdorokite didžiosios knygos įrašus.</td>
<td>Norėdami išmatuoti faktinį našumą, turite turėti duomenų. Duomenys importuojami naudojant jūsų nurodytas savikainos apskaitos didžiajai knygai skirtas jungtis. Jums apdorojant didžiosios knygos įrašus duomenys importuojami palaipsniui.</td>
</tr>
<tr>
<td>Apdorokite biudžeto įrašus.</td>
<td>Norėdami išmatuoti biudžetinį našumą, turite turėti duomenų. Duomenys importuojami naudojant jūsų nurodytas savikainos apskaitos didžiajai knygai skirtas jungtis. Jums apdorojant biudžeto įrašus duomenys importuojami palaipsniui.</td>
</tr>
<tr>
<td>Sukurkite ir taikykite savikainos veikimo būdo strategijas.</td>
<td>Norėdami klasifikuoti išlaidas išskirdami fiksuotąsias, kintamąsias arba pusiau kintamąsias išlaidas, galite naudoti savikainos veikimo būdo strategiją. Strategija sudaroma pagal taisyklę ir įsigalioja nuo tam tikros datos. Pagal numatytuosius parametrus visos išlaidos yra žymimos kaip neklasifikuotos tol, kol pritaikote savikainos veikimo būdo strategiją ir apskaičiuojate taisyklės poveikį. Apskaičiavus išlaidos klasifikuojamos.</td>
</tr>
<tr>
<td>Sekite išlaidas.</td>
<td>Norėdami lengviau suprasti savikainos strategijų poveikį, vesdami savikainos apskaitą galite atsekti išlaidas iki šaltinio verčių ir taikomų taisyklių, iš kurių jos kilusios. Ši funkcija suteikia galimybę atsekti visą informaciją apie tai, kada išlaidos įvyko, kokio tipo išlaidos įvyko ir kokios buvo pritaikytos išlaidų veikimo būdo taisyklės.</td>
</tr>
<tr>
<td>Nurodykite dimensijų hierarchijas.</td>
<td>Norėdami klasifikuoti, galite kurti dimensijų hierarchijas. Pvz., galite nurodyti klasifikavimo hierarchiją, kuri pagrįsta savikainos elemento dimensija ir jos nariais. Arba galite nurodyti klasifikavimo hierarchiją, kuri pagrįsta savikainos objekto dimensija ir jos nariais. Ataskaitų struktūros naudojamos šiais atvejais:
<ul>
<li>Nurodote paskirstymus, savikainos tarifus ir savikainos sumavimo taisykles.</li>
<li>Peržiūrite ataskaitas naudodami darbo sritį.</li>
<li>Nurodote prieigą, kad galėtumėte peržiūrėti apibendrintus duomenis.</li>
<li>Peržiūrite duomenis programoje „Excel“.</li>
</ul></td>
</tr>
<tr>
<td>Sukurkite išrašus, kuriuos galima peržiūrėti darbo srityje.</td>
<td>Naudodami darbo sritį greitai peržiūrėkite faktines ir biudžetines išlaidas ir nuokrypius. Galite filtruoti duomenis pagal laikotarpį arba savikainos lygį. Darbo sritis skirta vadovams, kurie atsakingi už savikainos kontrolę. Joje laikomasi dimensijos hierarchijoms nurodytų prieigos taisyklių.</td>
</tr>
<tr>
<td>Sukurkite ataskaitas naudodami „Excel“.
<blockquote>[!NOTE] Turite paleisti „Microsoft Excel 2016“.</blockquote>
</td>
<td>Naudodami duomenų objektus savikainos apskaitos duomenis galite eksportuoti tiesiogiai į „Excel“ o naudodami „Microsoft PivotTable“ galite sukurti ataskaitas.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Išlaidų valdymas

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Iš naujo priskirkite atleisto darbuotojo kredito kortelės operacijas. | Kartais, kai darbuotojas atleidžiamas, importuojant į išlaidų sąskaitą turimas įtraukti suaktyvintas kreditinės kortelės operacijas jo ar jos „Active Directory Domain Services“ (AD DS) abonementas išjungiamas. Anksčiau negalėdavote priskirti išlaidų įrašo atstovo arba į išlaidų ataskaitą įtraukti kredito kortelės operacijų. Dabar, kai susietasis darbuotojas atleidžiamas, naudodami puslapį **Kredito kortelės operacijos** bet kuriai kredito kortelės operacijai galite iš naujo priskirti darbuotoją. Kai iš naujo priskiriate kredito kortelės operaciją, galima pasirinkti išlaidų ataskaitos operaciją ir apmokėti ją įprastu išlaidų ataskaitos kompensacijos procesu. |
| Pakeiskite būsimų ir buvusių darbuotojų išlaidų kredito kortelės informaciją. | Galite pakeisti būsimų ir buvusių darbuotojų išlaidų valdymo kredito kortelės informaciją. Anksčiau galėdavote pakeisti tik aktyvaus darbuotojo išlaidų kredito kortelės informaciją. |
| Kopijuokite išlaidų ataskaitą. | Dabar toje pačioje išlaidų ataskaitoje sukūrę naujas išlaidas galite kopijuoti esamas išlaidas. Galite kopijuoti išlaidų ataskaitą ir visas susijusias ne kredito kortelės išlaidas į naują išlaidų ataskaitą. Bet, atsižvelgdami į nustatytas išlaidų strategijas ir kategorijas, vis tiek privalote atlikti visas reikiamas inventorizacijas ir pridėti reikiamus kvitus. Pasirinkdami įtraukti nesuderintas išlaidas, į išlaidų ataskaitą galite įtraukti kredito kortelės operacijas. |
| Masiškai redaguokite išlaidas. | Kai kurios kredito kortelės operacijos gali būti nesusietos su išlaidų kategorija arba jos gali būti netinkamai susietos importuojant. Šiuo atveju darbuotojai turi rankiniu būdu pakeisti susietą išlaidų kategoriją. Tvarkydami nesuderintas išlaidas dabar galite masiškai redaguoti pasirinktų išlaidų kategoriją. Be to, tvarkydami pasirinktas nurodytos išlaidų ataskaitos išlaidas galite masiškai redaguoti projektą ir papildomą informaciją. |
| Pakeiskite kredito kortelės operacijų valiutos kursą. | Faktinis kredito kortelės operacijoms naudojamas valiutos kursas gali skirtis nuo sistemoje nustatyto valiutos kurso. Anksčiau darbuotojai negalėdavo keisti visų į išlaidų valdymą importuotų kredito kortelių operacijų valiutos kurso. Dabar puslapyje **Išlaidų valdymo parametrai** galite nustatyti parametrą, kad būtų galima pakeisti kredito kortelės operacijų valiutos kursą. |
| Nustatykite išlaidų kovos su korupcija patvirtinimą. | Kai kurie organizacijos darbuotojai gali turėti verslo santykių su vyriausybės tarnautojais ir kai kurios dėl šių santykių atsirandančios išlaidos gali būti laikomos kyšiu. Išlaidų valdyme dabar galite nustatyti kovos su korupcija patvirtinimą, kuris rodomas pasirinktoms išlaidų kategorijoms, pavyzdžiui, maitinimas ir dovanos. Darbuotojai turi pasirinkti, ar kovos su korupcija patvirtinimui nustatytos išlaidos atitinka jūsų organizacijos strategijose nustatytus kriterijus. |
| Neleiskite rankiniu būdu įvesti konkrečioms išlaidų kategorijoms priskiriamų išlaidų. | Galima nustatyti, kad išlaidų kategorija atitiktų kredito kortelės operaciją, kurios kategorijos pakeisti negalima. Kaip pavyzdį būtų galima nurodyti delspinigius už kredito kortelės mokestį. Dabar galite nustatyti išlaidų kategoriją, kurią naudojant išlaidos gali būti kuriamos tik importuojant. Ši funkcija neleidžia darbuotojams kurti kategorijos išlaidų rankiniu būdu. Ji taip pat neleidžia keisti importuotų ir šią kategoriją naudojančių operacijų kategorijos. |
| Pridėkite kelių išlaidų kvitą. | Į išlaidų valdymą įkeltas kvitas gali būti susietas su keliomis išlaidomis. Anksčiau su keliomis išlaidomis susijusį kvitą reikėdavo įkelti atskirai po vieną kartą kiekvienai iš išlaidų. Dabar kvitą galite pridėti prie išlaidų, kurios jau įkeltos ir pridėtos prie kitų tos pačios išlaidų ataskaitos išlaidų. Be to, jei kvitą įkeliate į išlaidų ataskaitos antraštę, galite pasirinkti vieną ar kelias eilutes, prie kurių pridėsite kvitą. |
| Sukurkite ateityje numatytas išlaidas. | Pavyzdžiui, kai kopijuojate išlaidų ataskaitą, išlaidų operacijos data gali būti būsima data. Ankstesnėse versijose neleidžiama nurodyti būsimų išlaidų. Dabar galite sukurti ir įrašyti išlaidas, kurių data numatyta ateityje. Tačiau negalite pateikti ateityje numatytų išlaidų. |
| Sukonfigūruokite valstijos / provincijos išlaidų mokesčius. | Kai kuriose šalyse / regionuose skirtingose valstijose / provincijose patirtoms išlaidoms gali būti taikomi skirtingi pardavimo mokesčių tarifai. Dabar išlaidų mokesčių konfigūracijas galite nustatyti ne tik šalies / regiono lygmeniu, bet ir valstijos / provincijos lygmeniu. Jei puslapio **Mokesčio konfigūracija** lauką **Valstija / provincija** paliksite tuščią, pardavimo mokesčių grupė bus taikoma visoms nurodytos šalies / regiono valstijoms / provincijoms. |
| Nustatykite išlaidų kredito kortelių tipus. | Anksčiau nebuvo puslapio, kuriame galėdavote sukurti naujus kredito kortelių tipus, pvz., „Visa“, „MasterCard“ arba AMEX, kuriuos galėtumėte naudoti kartu su išlaidų valdymu. Dabar galite sukurti kredito kortelių tipus, kuriuos naudosite su išlaidų valdymu. Puslapis yra skyriaus **Skaičiavimai ir kodai** srityje **Sąranka**. |
| Nurodykite kelių lygių išlaidų ataskaitų patvirtinimo darbo eigą. | Nauja išlaidų ataskaitų darbo eiga palaiko kelių lygių patvirtinimo procesą. Kurdami išlaidų ataskaitą darbuotojai įveda laikinus tvirtintojus ir galutinius tvirtintojus. Tada darbo eiga nukreipia išlaidų ataskaitą pirmiausia laikiniems tvirtintojams. Patvirtinus išlaidų ataskaitą tame lygmenyje darbo eiga nukreipia ją galutiniams tvirtintojams galutiniam patvirtinimui. |
| Kurkite ir valdykite išlaidas, kurios nepridėtos prie išlaidų ataskaitos. | Dabar vartotojas gali kurti išlaidas ir jas valdyti (pavyzdžiui, pridėdamas arba inventorizuodamas kvitus arba priskirdamas svečius) nekurdamas išlaidų ataskaitos. Galima pasirinkti vieną ar kelias išlaidas ir įtraukti jas į naują išlaidų ataskaitą, kad būtų galima jas pateikti patvirtinimui. Naują išlaidų valdymo puslapį rasite dalyje **Išlaidų valdymas** &gt; **Mano išlaidos** &gt; **Išlaidos**. |

## <a name="financial-management"></a>Finansų valdymas

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sekti ilgalaikio turto vertinimus naudojant vieną „knygos“ koncepciją.</td>
<td>Anksčiau sekant ilgalaikio turto vertes buvo naudojami du atskiri vertinimo tipai: vertinimo modeliai ir nusidėvėjimo knygos. Dabartinėje versijoje šios dvi koncepcijos sujungtos į vieną vertinimo koncepciją, kuri vadinama knygomis. Knygos turi visas vertinimo modelių ir nusidėvėjimo knygų funkcijas. Pavyzdžiui, galite išjungti registravimą didžiojoje knygoje. Didžiojoje knygoje registruojamos knygos paprastai naudojamos įmonių finansų registravimo tikslais. Knygos, kurios neregistruojamos DK, gali būti naudojamos mokesčių registravimo tikslais.</td>
</tr>
<tr>
<td>Atlikite kelių juridinių subjektų didžiosios knygos uždarymą metų gale.</td>
<td>Norėdami paspartinti metų pabaigos uždarymo procesą, metų pabaigos uždarymą dabar galite paleisti keliems juridiniams subjektams bendro naudojimo metų pabaigos uždarymo puslapyje. Galima nustatyti juridinių subjektų grupes ir nurodyti parametrus, kurie turi būti išlaikomi pereinant iš vienų metų į kitus. Taip pat buvo atlikti kiti metų pabaigos uždarymo proceso naudojimo patobulinimai.</td>
</tr>
<tr>
<td>Pasinaudokite DK užsienio valiutos kurso pasikeitimo patobulinimais.</td>
<td>Atlikti šie didžiosios knygos užsienio valiutos pasikeitimo proceso patobulinimai:
<ul>
<li>Valiutos kurso tipas įtrauktas į pagrindinę sąskaitą. Dabar šis valiutos kurso tipas naudojamas nustatant valiutos kursą vykstant valiutos kurso pasikeitimui. Jeigu valiutos kurso tipas nenurodytas, procesas ir toliau naudoja didžiojoje knygoje nurodytą valiutos kurso tipą.</li>
<li>Dabar lengviau pasirinkti kelias pagrindines sąskaitas ir valiutas, kurioms bus atliekamas perkainojimo procesas.</li>
<li>Perkainojimą galima atlikti keliems juridiniams subjektams.</li>
<li>Sistema dabar kaupia kiekvieno atlikto perkainojimo proceso, taip pat gaunamų sumų (AR) ir mokėtinų sumų (AP) perkainojimo proceso retrospektyvą.</li>
<li>Kai paleidžiate procesą, galite peržiūrėti perkainojimo rezultatus. Peržiūroje rodomi visų juridinių subjektų, kuriems buvo paleistas šis procesas, rezultatai. Tada iš rodinio galite registruoti visus juridinius subjektus arba jų pogrupį. Rodinio rezultatus taip pat galite eksportuoti į „Excel“.</li>
</ul></td>
</tr>
<tr>
<td>Peržiūrėti papildomų registravimo sluoksnių operacijas.</td>
<td>Sąrašo puslapyje <strong>Bandomasis balansas</strong> ir ataskaitoje <strong>Dimensijos išrašas</strong> dabar galite pasirinkti papildomus į didžiąją knygą įtrauktus registravimo sluoksnius. Kai pasirenkate papildomus registravimo sluoksnius, šių registravimo sluoksnių koregavimai įtraukiami į sąrašo puslapio arba ataskaitos balansus.</td>
</tr>
<tr>
<td>Prie finansinio laikotarpio uždarymo šablono pridėkite aiškinamąją dokumentaciją.</td>
<td>Anksčiau dokumentaciją galėdavote pridėti baigę užduotį. Pavyzdžiui, galėdavote pridėti sugeneruotą ataskaitą. Dabar prie šablono taip pat galite pridėti aiškinamąjį dokumentą. Tada šis aiškinamasis dokumentas nukopijuojamas į kiekvieną finansinio laikotarpio grafiko užduotį, kad užduoties savininkas galėtų peržiūrėti instrukcijas apie tai, kaip atlikti šią užduotį.</td>
</tr>
<tr>
<td>Bendro naudojimo puslapyje nurodykite įmonės vidinės apskaitos sąranką.</td>
<td><strong>Įmonės vidinės apskaitos sąrankos puslapis</strong> dabar naudojamas bendrai, kad organizacija galėtų nurodyti visas sandorį galinčias sudaryti juridinių subjektų poras. Be to, dabar galite įvesti pradinio juridinio subjekto, bet ne paskirties juridinio subjekto operaciją. Jei vidinį įmonės sandorį gali sudaryti bet kuris juridinis subjektas, turi būti nurodyta atsakančioji pora. Todėl paskirties juridinis subjektas taip pat nustatytas kaip pradinis juridinis subjektas.</td>
</tr>
<tr>
<td>Pateikite biudžeto planų pagrindimo dokumentus.</td>
<td>Bet kurioms pageidaujamoms biudžeto sumoms kaip papildomą dokumentaciją galite sukurti pagrindimo šabloną. Vartotojai gali užpildyti šablono duomenis ir pridėti šabloną prie biudžeto plano, kad jį būtų galima naudoti vykstant patvirtinimo procesui.</td>
</tr>
<tr>
<td>Įgalinkite išplėstines biudžeto registro įrašų taisykles.</td>
<td>Jei išplėstinės taisyklės sukonfigūruojamos didžiojoje knygoje, tas taisykles galima naudoti naujiems biudžeto registro įrašams ir perkėlimams.</td>
</tr>
<tr>
<td>Pasinaudokite išankstinio mokėjimo SF išrašymo veiklos patobulinto matomumo pranašumais.</td>
<td>Naujame sąrašo puslapyje <strong>Atviri išankstiniai mokėjimai</strong> pateikiama išankstinio mokėjimo SF išrašymo veiklos momentinė kopija. Puslapyje AP padaliniui pateikiama informacija apie pirkimo užsakymus, kuriuose yra likusių išankstinio apmokėjimo verčių, kurioms turi būti išrašyta sąskaita faktūra, išrašytų sąskaitų faktūrų verčių, kurios turi būti apmokėtos, ir apmokėtų sąskaitų faktūrų verčių, kurios turi būti taikomos standartinėms sąskaitoms faktūroms. Be to, dėl standartinėms sąskaitoms faktūroms taikomų apmokėtų išankstinio mokėjimo SF automatinio taikymo patobulinimų SF išrašymo tarnautojai duomenų įvedimą gali atlikti efektyviau.</td>
</tr>
<tr>
<td>Naudokite darbo sritį <strong>Tiekėjo bendradarbiavimo SF išrašymas</strong>.</td>
<td>Naujoje srities <strong>Tiekėjo bendradarbiavimas</strong> darbo srityje <strong>Sąskaitų faktūrų išrašymas</strong> išoriniai tiekėjai gali saugiai pasiekti savo sąskaitos faktūros informaciją. Pavyzdžiui, tiekėjai gali matyti, ar sąskaita faktūra apmokėta, ir pateikti savo sąskaitą faktūrą. Šis pakeitimas skatina veiksmingesnį ir laiku vykstantį bendradarbiavimą su išoriniais tiekėjais. Todėl rečiau pertraukiamas SF išrašymo tarnautojų darbas.</td>
</tr>
<tr>
<td>Perjunkite juridinius subjektus įvesdami sąskaitos faktūros įrašą.</td>
<td>Naudodamiesi patobulinimais sąskaitų faktūrų išrašymo tarnautojai, kurie turi įvesti SF keliems juridiniams subjektams, gali greitai pakeisti juridinį subjektą SF išrašymo puslapiuose. Naudodamiesi šia funkcija SF išrašymo tarnautojai sutaupo laiko, nes norėdami prisijungti prie kito juridinio subjekto jie nebeprivalo atsijungti nuo dabartinio juridinio subjekto. Puslapiuose <strong>Visuotinis sąskaitų faktūrų žurnalas</strong> ir <strong>Tiekėjo sąskaitos faktūros</strong> įvesdami duomenis vartotojai gali pakeisti juridinį subjektą.</td>
</tr>
<tr>
<td>Vidaus pajamų tarnybos (IRS) 1099 jungtinio federalinio / valstijos mokesčio įvedimo programos elektroninių failų palaikymas</td>
<td>Kai įgalintas konfigūracijos raktas <strong>JAV</strong>, pateikiama papildoma elektroninio pateikimo proceso funkcija, kuri atitinka jungtinio federalinio / valstijos mokesčio įvedimo programos IRS taisykles. IRS įkūrė šią programą, kad ji elektroniniu būdu galėtų persiųsti grąžinamą informaciją dalyvaujančioms valstijoms.</td>
</tr>
<tr>
<td>Sudengimo patobulinimai</td>
<td>Naudodamiesi patobulinimais mokėjimo tarnautojai gali efektyviau atlikti sudengimus, nes kelis neužregistruotus mokėjimus jie gali sudengti naudodami tą pačią sąskaitą faktūrą.</td>
</tr>
<tr>
<td>Visos įmonės rodinys</td>
<td>Centralizuoto mokėjimo tarnautojai dabar gali peržiūrėti sąskaitas faktūras, kurių terminas praėjęs, visose įmonėse. Darbo srityse <strong>Tiekėjo mokėjimai</strong> ir <strong>Kliento mokėjimai</strong> pateikiant būdą peržiūrėti ir filtrą visose įmonėse, kurios yra centralizuoto mokėjimo organizacinės hierarchijos dalis, dabar galima geriau matyti ir valdyti vėluojančias sąskaitas faktūras.</td>
</tr>
<tr>
<td>Naudokite darbo sritį <strong>Banko valdymas</strong>.</td>
<td>Nauja darbo sritis <strong>Banko valdymas</strong> padeda sekti jūsų juridinių subjektų banko sąskaitas ir balansus. Iš karto prieinami visų sąskaitų dabartinis ir laukiantis balansai ir jūs galite detalizuoti atgal nuo balansų į išsamius operacijų kvitus. Taip pat galite matyti kiekvienos banko sąskaitos balanso praeities duomenis arba visų įmonės banko sąskaitų suvestinę, pateikiamą trumpalaikiame ir ilgalaikiame rodiniuose. Jūs galite geriau suprasti banko sąskaitos suderinimą, nes skelbiama kiekvienos banko sąskaitos paskutinio suderinimo data ir atliekamą derinimą nurodo indikatorius.</td>
</tr>
<tr>
<td>Importuokite visų juridinių subjektų elektroninius banko išrašus vienu veiksmu.</td>
<td>Dabar galite importuoti visų juridinių subjektų elektroninius banko išrašus vienu veiksmu. Banko išrašo failuose gali būti daugelio banko sąskaitų ir juridinių subjektų išrašų, o pašto kodo failuose gali būti keli banko išrašo failai. Naudodami vieną importavimo procesą galite pradėti visų pateiktų banko sąskaitų derinimą visuose juridiniuose subjektuose. Ši funkcija padės sutaupyti laiko, nes jums nereikės perjungti įmonių ir kelių išrašo importavimų. Taip pat galite automatiškai paleisti gretinimo taisykles visuose importuotuose kiekvienos įmonės išrašuose.</td>
</tr>
<tr>
<td>Vertinimo sekimas</td>
<td>Vienas ilgalaikis turtas gali turėti kelių skirtingų apskaitos standartų vertinimus ir gali pasirinktinai registruoti susietas operacijas didžiojoje knygoje. Anksčiau šie vertinimai būdavo sekami naudojant vertinimo modelius arba nusidėvėjimo knygas. Dabar galite sekti šiuos knygomis vadinamus vertinimus naudodami bendrą žurnalų, užklausų ir ataskaitų rinkinį. Tokiu būdu supaprastinamas diegimas ir sumažinamas periodiniams procesams reikiamų sąsajų skaičius.</td>
</tr>
<tr>
<td>Pasinaudokite visos įmonės nusidėvėjimo vykdymų patobulinimais.</td>
<td>Dabar visų juridinių subjektų turto nusidėvėjimo vykdymą galite paleisti viename puslapyje. Taip pat galite automatiškai registruoti žurnalus juos sukūrę. Galite siųsti žurnalų kūrimo ir registravimo duomenis paketiniam apdorojimui, kad nusidėvėjimas vyktų fone. Šie patobulinimai sumažina neveiksmingumo atvejus, nes jums nereikia pradėti nusidėvėjimo vykdymų atskirai kiekvienai įmonei. Naudodami patobulinimus taip pat galite labiau centralizuotai valdyti savo ilgalaikį turtą.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Žmogiškojo kapitalo valdymas

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sukurkite našumo žurnalą.</td>
<td>Prieš užbaigdami savo apžvalgą dažnai renkate informaciją apie jūsų, kaip darbuotojo, sėkmei peržiūros laikotarpiu įtakos turėjusią veiklą ar įvykius. Įrašą galite įtraukti į savo našumo žurnalą, kad galėtumėte dokumentuoti tą veiklą ir įvykius. Norėdami pateikti daugiau informacijos redaktoriui, taip pat galite prijungti šią veiklą ir įvykius prie tikslo arba našumo rezultatų apžvalgos.</td>
</tr>
<tr>
<td>Sukurkite išsamesnius tikslus.</td>
<td>Turite daugiau galimybių valdyti išsikeltų tikslų turinį. Galite sukurti tikslų matavimus, susieti našumo žurnalo įrašus su matavimais ir pridėti naujų dokumentų. Galite saugoti tikslus kaip šablonus ir pakartotinai juos panaudoti norėdami atlikti greitą sąranką.</td>
</tr>
<tr>
<td>Sukurkite išsamesnes našumo apžvalgas.</td>
<td>Našumo apžvalgos, kurios oficialiai vadinamos diskusijomis, dabar yra pakankamai lanksčios, kad galėtų palaikyti nuolatinį grįžtamąjį ryšį ir oficialesnes apžvalgas. Galite įtraukti aktyvių tikslų, įrašyti apie juos komentarų ir įtraukti savo kompetencijos apžvalgos skyrių. Pateikiami papildomi skyriai, kuriuose galite įtraukti arba peržiūrėti su apžvalga susijusius matavimus, našumo žurnalo įrašus, priedus ir išsiregistravimus.</td>
</tr>
<tr>
<td>Susiekite papildomas pareigų hierarchijas su darbo eigomis.</td>
<td>Darbo eigą galite susieti su pareigų hierarchija. Taip pat galite keisti darbo eigos veiksmus, kad galėtumėte optimizuoti patvirtinimo procesą, kad jis atitiktų jūsų verslo poreikius. Todėl galite nurodyti efektyvią patvirtinimo struktūrą, kuri tiktų įvairiems jūsų organizacijos naudojamiems ataskaitų ryšiams.</td>
</tr>
<tr>
<td>Darbo eigos palaikymas darbuotojo savitarnoje įvedant asmeninio identifikavimo numerius (PIN).</td>
<td>Darbo eigos tinkamumas žmogiškiesiems ištekliams (HR) išplėstas ir dabar apima PIN numerių palaikymą. Darbuotojai gali pridėti ir redaguoti savo PIN, kad pagerintų efektyvumą. Tačiau prieš įtraukdami šią informaciją į darbuotojo įrašą HR darbuotojai gali patikrinti jos tikslumą ir užbaigtumą.</td>
</tr>
<tr>
<td>Sukurkite tikslų šablonus ir naudokite juos norėdami įtraukti naujų tikslų.</td>
<td>Galite sukurti daugelio įmonės darbuotojų bendrų tikslų šablonus. Darbuotojai gali įtraukti savo tikslus iš šablono, vadovai gali įtraukti savo komandos tikslus iš šablono, o HR komandos nariai gali įtraukti visos įmonės darbuotojų tikslus.</td>
</tr>
<tr>
<td>Sukurkite tikslų grupes ir naudokite jas norėdami įtraukti naujų tikslų.</td>
<td>Tikslų šablonus galite įtraukti į grupę ir naudoti grupę norėdami sukurti vieną ar kelis darbuotojo, komandos, pareigų, padalinio arba įmonės tikslus.</td>
</tr>
<tr>
<td>Lengviau valdykite peržiūros procesą.</td>
<td>Valdydami peržiūros procesą galite naudoti darbo eigą. Galite kurti peržiūros šablonus ir naudoti juos kurdami peržiūras. Taip pat galite įtraukti peržiūros vertinimus.</td>
</tr>
<tr>
<td>Norėdami nustatyti peržiūros laikotarpį, naudokite peržiūros laikotarpius.</td>
<td>Galite nurodyti našumo peržiūros laikotarpį, o peržiūros pradžios ir pabaigos datos įvedamos automatiškai. Tačiau galite keisti šias numatytąsias datas pagal savo poreikį.</td>
</tr>
<tr>
<td>Gaukite prieigą prie penkių naujų „Power BI“ turinio paketų, skirtų personalo skyriui</td>
<td>Nauji turinio paketai leidžia personalo organizacijoms ir vadovams išanalizuoti toliau išvardytus veiksnius.
<p>Darbo jėgos metrika</p>
<ul>
<li>Demografinį susiskirstymą pagal amžių, lytį ir šeimyninę padėtį</li>
<li>Palyginti kasmet prarandamų darbuotojų rodiklius ir pasitraukimo iš organizacijos priežasčių, kurias pateikė išėję darbuotojai, sąrašą</li>
<li>Peržiūrėti atvirų pareigų sąrašą ir atvirų bei uždarų pareigų palyginimą</li>
</ul>
<p>Kompensavimas ir išmokos</p>
<ul>
<li>Palyginti valandinį ir fiksuotą užmokestį gaunančius darbuotojus</li>
<li>Peržiūrėti galimoms išmokoms gauti užsiregistravusių darbuotojų skaičių</li>
<li>Peržiūrėti darbuotojus pagal įdarbinimo tipą</li>
</ul>
<p>Įdarbinimas</p>
<ul>
<li>Išanalizuoti pretendentus pagal pretendentų skaičių, iš kur jie atvyksta ir dėl kokių pareigų kreipiasi</li>
</ul>
<p>Organizacinis mokymas</p>
<ul>
<li>Kursų registraciją pagal vietą</li>
<li>Kursų lankomumą pagal būseną</li>
<li>Darbuotojų, užsiregistravusių į kursus, sąrašą</li>
</ul>
<p>Darbuotojų kompetencijos ir tobulinimas</p>
<ul>
<li>Darbuotojų turimų įgūdžių sąrašą</li>
<li>Įgūdžių tipų suskirstymą pagal komandos narį</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="localizations"></a>Lokalizacijos

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lokalizacijos galimos dar 18 šalių:
<ul>
<li>Austrija</li>
<li>Belgija</li>
<li>Brazilija</li>
<li>Kinija</li>
<li>Čekijos Respublika</li>
<li>Estija</li>
<li>Suomija</li>
<li>Vengrija</li>
<li>Italija</li>
<li>Latvija</li>
<li>Lietuva</li>
<li>Norvegija</li>
<li>Lenkija</li>
<li>Saudo Arabija</li>
<li>Ispanija</li>
<li>Švedija</li>
<li>Šveicarija</li>
<li>Tailandas</li>
</ul>
<p>Toliau nurodytose šalyse taip pat reikalinga mažmeninės prekybos lokalizacija. Šių šalių mažmeninės prekybos lokalizacija nebaigta ir yra planuojama tik H1 CY2017:</p>
<ul>
<li>Brazilija</li>
<li>Čekijos Respublika</li>
<li>Estija</li>
<li>Vengrija</li>
<li>Latvija</li>
<li>Lietuva</li>
<li>Malaizija</li>
<li>Lenkija</li>
<li>Švedija</li>
</ul>
</td>
<td>„Dynamics 365 for Operations“ galima dar 18 šalių. Siekiame, kad lokalizavimo procesas būtų paprastesnis ir kad būtų galima daugiau konfigūruoti, todėl kontrolės elektroninių ataskaitų funkcijos buvo konvertuotos į elektroninių ataskaitų (ER) konfigūracijas, o kai kurios kontrolės „Microsoft SQL Server Reporting Services“ (SSRS) ataskaitos buvo konvertuotos į „Excel“ šablonus naudojančias ER konfigūracijas. Šios konvertuotos funkcijos vėliau konkrečiai įvardijamos šioje lentelėje.</td>
</tr>
<tr>
<td>Japonija – grupuokite ilgalaikį turtą spausdindami 26 formą ir prie jos pridėtas lenteles.</td>
<td>26 forma turi būti pateikiama kiekviename mieste, kuriame įmonė veikia. Siekiant, kad jums reikėtų įdėti mažiau pastangų spausdinant 26 formą, ilgalaikį turtą galima automatiškai grupuoti ir rūšiuoti pagal vietą.</td>
</tr>
<tr>
<td>Japonija – šablone matomos paspartinto ir papildomo nusidėvėjimo sumos.</td>
<td>Šablone gali būti pateiktos tikslios apskaičiuotos paspartinto ir papildomo nusidėvėjimo sumos.</td>
</tr>
<tr>
<td>Japonija – palaipsniui skaičiuoti išskaitomą mokestį.</td>
<td>Japonijos vyriausybė reikalauja apskaičiuoti išskaitomą mokestį palaipsniui, pagal mokėjimo sumą.</td>
</tr>
<tr>
<td>Japonija – importuoti pašto kodo failą, specialiai pritaikytą dideliems įmonių pastatams.</td>
<td>Vadovybės pateikiamą specialiai dideliems įmonių pastatams pritaikytą pašto kodą galima importuoti į sistemą. Tada pagal pašto kodą galima nustatyti adresą.</td>
</tr>
<tr>
<td>Japonija – konfigūruoti ilgalaikio turto neveiklumo laikotarpį.</td>
<td>Neveiklumo laikotarpiu vartotojas gali nurodytam laikotarpiui pristabdyti ilgalaikio turto nusidėvėjimą. Ši funkcija reikalaujama įstatymuose.</td>
</tr>
<tr>
<td>Europa – konfigūruoti šalies pridėtinės vertės mokesčio (PVM) registracijos numerį pagal šalies adresą naudojant registracijos ID sistemą.</td>
<td>Galite sukonfigūruoti šalies adreso PVM registracijos numerį naudodami registracijos ID sistemą ir naują registracijos kategoriją <strong>PVM ID</strong>.</td>
</tr>
<tr>
<td>Suomija – konfigūruoti šalies adreso muitinės kliento numerį naudojant registracijos ID sistemą.</td>
<td>Galite konfigūruoti šalies adreso muitinės kliento numerį naudodami registracijos ID sistemą ir naują registracijos kategoriją <strong>Muitinės kliento ID</strong>.</td>
</tr>
<tr>
<td>Prancūzija – spausdinti kliento sąskaitas faktūras naudojant Prancūzijai skirtą maketą.</td>
<td>Kliento SF spaudinys koreguojamas, kad atitiktų Prancūzijai būdingus reikalavimus.</td>
</tr>
<tr>
<td>Prancūzija – įgalinti dokumentų numeravimą chronologine tvarka pagal ataskaitinį laikotarpį.</td>
<td>Siekdami patenkinti Prancūzijai būdingus kliento SF numeravimo reikalavimus, galite nustatyti kliento SF numeracijas pagal ataskaitinį laikotarpį.</td>
</tr>
<tr>
<td>Lokalizavimas Austrijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Austrijos ES pardavimo sąrašas XML formatu</li>
<li>Intrastat formatas, skirtas Austrijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Austrijai</li>
<li>ISO20022 tiesioginio debeto mokėjimo formatas, skirtas Austrijai</li>
<li>Austrijos EDIFACT-PAYMUL formatas</li>
<li>Austrijos PVM deklaracija</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Belgijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Belgijos BLWI formatas</li>
<li>Belgijos ES pardavimo sąrašas XML formatu</li>
<li>Belgijos ilgalaikio turto ataskaita</li>
<li>Belgijos Intervat formatas</li>
<li>Belgijos Intrastat formatas</li>
<li>Belgijos SF apyvartos ataskaita</li>
<li>Belgijos didžiosios knygos operacijos eksporto formatas</li>
<li>Belgijos SWIFT tiekėjo mokėjimo formatas</li>
<li>Belgijos CODA banko išrašo importavimo formatas</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Belgijai</li>
<li>ISO20022 tiesioginio debeto mokėjimo formatas, skirtas Belgijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Brazilijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Brazilijos GIA SP</li>
<li>Brazilijos GIA-ST</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Čekijos Respublikoje – ER konfigūracijos</td>
<td>
<ul>
<li>Čekijos Respublikos ES pardavimo sąrašas XML formatu</li>
<li>Intrastat formatas, skirtas Čekijos Respublikai</li>
<li>PVM deklaracija, skirta Čekijos Respublikai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Kinijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Klientų skirstymo pagal terminus ataskaitos formatas, skirtas Kinijai</li>
<li>Klientų mokėtinos sumos analizės ataskaitos formatas, skirtas Kinijai</li>
<li>Tiekėjų skirstymo pagal terminus ataskaitos formatas, skirtas Kinijai</li>
<li>Tiekėjų mokėtinos sumos analizės ataskaitos formatas, skirtas Kinijai</li>
<li>Gautinų mokėjimų skirstymo pagal terminus analizės formatas, skirtas Kinijai</li>
<li>Klientų balanso ataskaitos formatas, skirtas Kinijai</li>
<li>Klientų didžiosios knygos sąskaitos balanso ataskaitos formatas, skirtas Kinijai</li>
<li>Tiekėjų balanso ataskaitos formatas, skirtas Kinijai</li>
<li>Kinijos GBT failas</li>
<li>„Golden tax“ eksportavimo failo formatas</li>
<li>Gamybos suvartojimo nuokrypio ataskaitos formatas, skirtas Kinijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Estijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Estijos ES pardavimo sąrašas XML formatu</li>
<li>Intrastat formatas, skirtas Estijai</li>
<li>Atsargų perklasifikavimo išrašas, skirtas Estijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Estijai</li>
<li>Kliento ir tiekėjo balanso pranešimo ataskaita, skirta Estijai</li>
<li>Estijos PVM deklaracija</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Suomijoje – ER konfigūracijos</td>
<td>
<ul>
<li>ES pardavimo sąrašas TXT formatu, skirtas Suomijai</li>
<li>Intrastat formatas, skirtas Suomijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Suomijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Vengrijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Vengrijos ES pardavimo sąrašas XML formatu</li>
<li>Intrastat formatas, skirtas Vengrijai</li>
<li>Intrastat supaprastintas formatas, skirtas Vengrijai</li>
<li>Sąskaitų faktūrų sąrašo eksportavimo formatas, skirtas Vengrijai</li>
<li>Vengrijos PVM deklaracija</li>
<li>Detalizuota PVM deklaracija, skirta Vengrijai</li>
<li>Inventorizacijos aprašas, skirtas Vengrijai</li>
<li>„MultiCash“ mokėjimo formatas, skirtas Vengrijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Italijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Intrastat formatas, skirtas Italijai</li>
<li>Projekto sąskaitos faktūros formatas, skirtas Italijai</li>
<li>Pardavimo sąskaitos faktūros formatas, skirtas Italijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Italijai</li>
<li>ISO20022 tiesioginio debeto mokėjimo formatas, skirtas Italijai</li>
<li>RIBA perdavimo inkasacijai formatas, skirtas Italijai</li>
<li>Vietinių mokesčių operacijų ataskaita, skirta Italijai</li>
<li>Užblokuoto sąrašo ataskaita, skirta Italijai</li>
<li>„Modello770“ ataskaita, skirta Italijai</li>
<li>Kasmetinių mokesčių ryšio ataskaita, skirta Italijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Latvijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Grynųjų pinigų kvitų naudojimo ataskaita (LV)</li>
<li>ES pardavimo sąrašas XML formatu, skirtas Latvijai</li>
<li>ES pardavimo sąrašo taisymai XML formatu, skirti Latvijai</li>
<li>Intrastat (A) formatas, skirtas Latvijai</li>
<li>Intrastat (B) formatas, skirtas Latvijai</li>
<li>Atsargų skaičiavimo sąrašas, skirtas Latvijai</li>
<li>Atsargų skaičiavimo išrašas, skirtas Latvijai</li>
<li>Latvijos atsargų perkėlimas</li>
<li>Vidinio perkėlimo pristatymo pažyma, skirta Latvijai</li>
<li>Atsargų perklasifikavimo dokumentas, skirtas Latvijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Latvijai</li>
<li>Latvijos PVM deklaracija</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Lietuvoje – ER konfigūracijos</td>
<td>
<ul>
<li>Lietuvos ES pardavimo sąrašas XML formatu</li>
<li>Intrastat formatas, skirtas Lietuvai</li>
<li>Inventorizacijos aprašas, skirtas Lietuvai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Lietuvai</li>
<li>Kliento ir tiekėjo tarpusavio suderinimo ataskaita, skirta Lietuvai</li>
<li>Lietuvos PVM deklaracija</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Norvegijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Priminimo laiško formatas, skirtas Norvegijai</li>
<li>AutoGiro mokėjimo formatas, skirtas Norvegijai</li>
<li>AvtaleGiro kliento mokėjimo formatas, skirtas Norvegijai</li>
<li>eFaktura kliento mokėjimo formatas, skirtas Norvegijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Norvegijai</li>
<li>NETS mokėjimo formatas, skirtas Norvegijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Lenkijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Intrastat formatas, skirtas Lenkijai</li>
<li>Sandėlio dokumentai, skirti Lenkijai</li>
<li>Atsargų perklasifikavimo dokumentas, skirtas Lenkijai</li>
<li>„MultiCash“ mokėjimo formatas, skirtas Lenkijai</li>
<li>„MultiCash“ užsienio mokėjimo formatas, skirtas Lenkijai</li>
<li>Kliento ir tiekėjo balanso patvirtinimo ataskaita, skirta Lenkijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Saudo Arabijoje – ER konfigūracijos</td>
<td>Banko LC papildomų išlaidų paskirstymo formatas, skirtas Saudo Arabijai</td>
</tr>
<tr>
<td>Lokalizavimas Ispanijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Ispanijos ES pardavimo sąrašas TXT formatu</li>
<li>Intrastat formatas, skirtas Ispanijai</li>
<li>Projekto sąskaitos faktūros formatas, skirtas Ispanijai</li>
<li>Pardavimo sąskaitos faktūros formatas, skirtas Ispanijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Ispanijai</li>
<li>ISO20022 tiesioginio debeto mokėjimo formatas, skirtas Ispanijai</li>
<li>Ispanijos PVM registravimo knygos formatas</li>
<li>Ispanijos PVM registravimo knygos suvestinės formatas</li>
<li>Deklaracijos 347 eksportavimas į ASCII, skirtas Ispanijai</li>
<li>Deklaracijos 347 ataskaita, skirta Ispanijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Švedijoje – ER konfigūracijos</td>
<td>
<ul>
<li>Intrastat formatas, skirtas Švedijai</li>
<li>Bankgirot Autogiro kliento mokėjimo formatas, skirtas Švedijai</li>
<li>Bankgirot tiekėjo mokėjimo formatas, skirtas Švedijai</li>
<li>SWIFT tiekėjo mokėjimo formatas, skirtas Švedijai</li>
<li>SIE eksportavimo formatas, skirtas Švedijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Švedijai</li>
</ul>
</td>
</tr>
<tr>
<td>Lokalizavimas Šveicarijoje – ER konfigūracijos</td>
<td>
<ul>
<li>DebitDirect mokėjimo formatas, skirtas Šveicarijai</li>
<li>LSV tiesioginio debeto mokėjimo formatas, skirtas Šveicarijai</li>
<li>ISO20022 kredito perkėlimo mokėjimo formatas, skirtas Šveicarijai</li>
<li>ISO20022 tiesioginio debeto mokėjimo formatas, skirtas Šveicarijai</li>
<li>ESR banko išrašo importavimo formatas, skirtas Šveicarijai</li>
</ul>
</td>
</tr>
<tr>
<td>Vokietija – tiekėjo mokėjimų eksportavimas DTAZV formatu</td>
<td>Vokietijoje reikalingas DTAZV su užsienio formato specifikacija, kuris nurodo kredito pervedimo (tiekėjo mokėjimo) pranešimą pagal tarptautinių mokėjimų iš Vokietijos į užsienio banko sąskaitą arba į vietinį banką užsienio valiuta specifikaciją.</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektroninės ataskaitos

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Konfigūruokite ER ataskaitas, kad galėtumėte įterpti kelių formatų duomenis iš dokumentų valdymo saugyklos į sugeneruojamus elektroninius pranešimus. | ER ataskaitos gali įterpti duomenis į iš duomenų valdymo saugyklos sugeneruojamus elektroninius pranešimus. Todėl verslo dokumento priedai gali būti įtraukiami į šiam dokumentui laikantis teisinių reikalavimų sugeneruotus elektroninius pranešimus. Šiuo metu šie priedai MIME formatu gali būti įtraukiami į sugeneruotą XML pranešimą. Arba priedai Base64 formatu gali būti įtraukiami į sugeneruotą dvejetainį pranešimą. |
| Konfigūruokite ER ataskaitas, kad galėtumėte generuoti „Excel“, „Microsoft Word“ arba PDF formato elektroninius dokumentus. | Naudojant vieną konfigūraciją ER ataskaitos gali generuoti elektroninius dokumentus trimis skirtingais formatais: „OpenXML“ darbalapio („Excel“), „Word“ ir XML formos duomenų formatu (XFDF) (PDF). Vartotojai gali pasirinkti formatą į ER ataskaitą kaip „Excel“, „Word“ ar PDF dokumentą įtraukdami formato šabloną. |
| Konfigūruokite ER ataskaitas, kad galėtumėte įterpti duomenis į „OpenXML“ darbalapio formatu sugeneruotų elektroninių dokumentų puslapio antraštes ir poraštes ir valdyti puslapio lūžius. | ER ataskaitos gali įvesti verslo dumenis į puslapio antraštes ir poraštes ir valdyti, kur įvyksta puslapio lūžis. Todėl ataskaitos gali palaikyti sugeneruotų elektroninių dokumentų puslapių statinius viršutinius ir apatinius skyrius. Jos taip pat gali palaikyti konkrečią tų dokumentų puslapių kaitą, kad jie atitiktų teisinius reikalavimus. |
| Konfigūruokite ER ataskaitų paskirties vietą, kad išvestis būtų siunčiama kaip el. laiškas ir taip, kad verslo duomenis ir ER logiką (išraiškas) būtų galima naudoti vykdymo metu norint nurodyti naudotiną el. pašto adresą. | Anksčiau sukonfigūravus ER paskirties vietą, išvesties gavėjo el. pašto adresą būdavo galima nurodyti kūrimo metu. Dabar galite konfigūruoti išraišką ER formatu. Tada šią išraišką galima pasirinkti paskirties vietoje kaip atskirą kiekvienos formato konfigūracijos ir kiekvieno išvesties komponento (aplanko arba failo) el. pašto adreso šaltinį. Todėl paleidus ER ataskaitą kiekvieną sugeneruotą failą galima išiųsti kitam gavėjui, o el. pašto adresą galima nurodyti pagal ER logiką ir verslo duomenis. |
| Sukonfigūruokite ER ataskaitų paskirties vietą, kad išvestis į „Microsoft SharePoint“ aplanką būtų siunčiama kaip failas nauju pavadinimu arba nauja esamo failo versija ir kad verslo duomenis sistemoje „Microsoft Power BI“ būtų galima naudoti kaip duomenų rinkinį arba ataskaitą. | Jeigu sukonfigūravote ER ataskaitas, dabar galite lengvai (be kodavimo) paruošti pageidaujamus verslo duomenis, kad juos būtų galima naudoti sistemoje „Power BI“. Paleidę tas ER ataskaitas sistemai „Power BI“ galite pateikti atitinkamus jau esamus verslo duomenis ir (arba) „Excel“ ataskaitas. Jei ataskaitą planuojate paleisti pasikartojančiu režimu, galite nustatyti suplanuotą verslo duomenų skirstymą iš „Dynamics 365 for Operations“ į „Power BI“, kad būtų palaikomas „Power BI“ paremtų ataskaitų atnaujinimo grafikas. |
| Sukonfigūruokite ER ataskaitas, kad jau sugeneruotą elektroninio dokumento dalį jos naudotų kaip duomenų šaltinį, kad galėtų sugeneruoti likusią dokumento dalį. | Galite sukonfigūruoti išvestį tekstiniu formatu kuriančias ER ataskaitas taip, kad jos atliktų dokumento eilučių skaičiavimą. Tada šią informaciją galima naudoti kitose dokumento dalyse, kad būtų galima sukurti eilutes, kuriose yra suvestinės informacija. Suvestinės informacija (bendrosios sumos ir skaičiai) gali būti apskaičiuojama ir spausdinama elektroniniuose dokumentuose, kurie sugeneruojami nereikalaujant papildomų duomenų pakeitimų. Todėl ši funkcija pagerina ataskaitos vykdymo našumą ir padeda supaprastini tolesnę sukonfigūruoto ER formato priežiūrą. |
| Sukonfigūruokite ER ataskaitas taip, kad jose būtų nurodomas teksto formatu sugeneruotų elektroninų dokumentų failo pavadinimo plėtinys. | Galite sukonfigūruoti ER ataskaitas taip, kad išvestis būtų kuriama tekstiniu formatu ir ją būtų galima išsaugoti kaip tam tikrą plėtinį turintį failą. Be numatytojo .txt plėtinio atsižvelgdami į formato specifikaciją galite sukonfigūruoti kitus plėtinius, pvz., .csv ir .prn. |
| Sukurkite naujas konkrečia ER modelio versija pagrįstas ER ataskaitas. | Anksčiau sukūrus naują ER formatą kaip formato duomenų šaltinio vietą būdavo galima naudoti tik naujausią pasirinkto ER modelio versiją. Dabar galite pasirinkti bet kurią pasirinkto ER modelio versiją. Ši funkcija leidžia tvarkyti šių metų ER ataskaitas ir tuo pat metu kurti naują kitų metų ER modelio versiją. |
| Ieškokite duomenų šaltinių ir formatų / modelių pagal tekstą arba pasirinktą artefaktą vienu spustelėjimu. Efektyviai spręskite pritaikymo kitoje vietoje konfliktus ir spręskite konfliktus tarp konfigūracijų. Konfigūruokite ER ataskaitas, kad galėtumėte sukurti kelis tikrinimo pranešimus, skirtus iki ataskaitos vykdymo sustabdymo aptiktoms klaidoms. | Naudodamiesi keliais ER sistemos vartotojo aplinkos (UX) patobulinimais vartotojai naudodami ER sistemą gali dirbti efektyviau ir lengviau. |
| Rodykite **ER** darbo sritį „Power BI“ ataskaitose. | Vartotojai puslapį **ER darbo sritis** gali sukonfigūruoti taip, kad į jį būtų įtraukiami nauji meniu elementai ir sąveikiosios plytelės, kuriose paleidžiamos „Power BI“ pagrįstos ataskaitos. |

## <a name="payroll"></a>Algalapis

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sukonfigūruokite mokėjimo įrašus ir apdorokite atlyginimą „Microsoft Dynamics AX 2012 R3“ naudodami modulio <strong>Atlyginimas</strong> funkciją atitinkančią funkciją.</td>
<td>Dabar sukonfigūruoti ir apdoroti JAV algalapį galite naudodami nustatytą funkciją, kuri atitinka AX 2012 R3 nustatytą funkciją.
<ul>
<li>Galite sukonfigūruoti mokėjimo ciklus ir mokėjimo laikotarpius, darbo ciklus ir darbo laikotarpius, pajamų kodus ir pajamų kodų grupes, grafikus, atostogų tipus, ir išmokų kaupimo planus.</li>
<li>Taip pat galite nustatyti išmokų ir mokesčių privalomuosius atskaitymus ir įrašyti pareigų ir darbuotojų algalapio informaciją, naudojamą ataskaitų ir analizės tikslais.</li>
<li>Taip pat galite nustatyti ir valdyti pinigų areštų ir mokesčių ir bet kokių susijusių administracinių mokesčių atskaitymus.</li>
</ul>
</td>
</tr>
<tr>
<td>Stebėkite ir apdorokite savo mokėjimo laikotarpio procesą naudodami naują darbo sritį <strong>Atlyginimų valdymas </strong>.</td>
<td>Dabar galite lengvai stebėti savo darbo užmokesčio apdorojimą. Atlyginimų administratoriai gali iš karto matyti uždarbio ir mokėjimo išrašus, kuriuos jie turi peržiūrėti, kad būtų mokėjimo vykdymas būtų užbaigtas ir tikslus. Naudodami darbo sritį <strong>Atlyginimų valdymas </strong>vartotojai iš vienos srities gali stebėti ir vykdyti visus procesus.</td>
</tr>
<tr>
<td>Sugeneruokite atlyginimo čekio teigiamų mokėjimų failus.</td>
<td>Yra nauja grynųjų pinigų ir banko vadovybės teigiamų mokėjimų funkcija, skirta atlyginimų mokėjimams. Į pagrindinį procesą įtraukti atskiri meniu elementai, kad būtų galima atlikti atskirą specialiai atlyginimui skirtą konfigūraciją. Funkcija yra tokia pati, kaip pagrindinė teigiamo mokėjimo funkcija, kuri buvo išleista programos „Microsoft Dynamics AX“ versijoje 7.0.1 (2016 m. gegužės mėn.). Dėl šio plėtinio atlyginimų duomenys yra visiškai atskirti nuo visų kitų jūsų teigiamo mokėjimo operacijų. Šis atskyrimas padeda užtikrinti, kad su atlyginimu susijusius duomenis galėtų pasiekti ir matyti tik atlyginimų vartotojai.</td>
</tr>
<tr>
<td>Importuokite pajamų išrašo eilutes iš išorinio šaltinio naudodami naują duomenų objektą Pajamų išrašo eilutė.</td>
<td>Naudojant svarbių naujų duomenų objektą galima integruoti su išorinėmis laiko ir uždarbio skaičiavimo sistemomis. Duomenų objektas importuoja pajamų išrašo eilutes ir atlieka visas tas pačias numatytąsias logines operacijas, kurias vartotojas įvedė tiesiogiai pajamų išraše. Importavus eilutes jos automatiškai susiejamos su atitinkamu pajamų išrašo dokumentu. Jei tinkamo pajamų išrašo dokumento nėra, dokumentas sukuriamas automatiškai.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Planavimas ir grafiko sudarymas

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Nustatykite numatytuosius pardavimo ir pirkimo užsakymo parametrus pagal bet kurią aktyvią bendrojo produkto dimensiją. Todėl galite nurodyti numatytuosius sandėliavimo vieneto (SKU) arba dalinio SKU užsakymo parametrus. | Galite nurodyti produkto dimensijai arba produkto dimensijų kombinacijai taikomus numatytuosius užsakymo parametrus.<p>**Pavyzdys:**</p><p>Parduodate produktą, kurio pavadinimas Polo marškinėliai. Šis produktas yra dviejų spalvų: žalios ir mėlynos. Jis taip pat yra dviejų dydžių: „Small“ (mažas) ir „Medium“ (vidutinis). Spalva ir dydis yra aktyviosios produkto Polo marškinėliai dimensijos. Galima užblokuoti visų žalios spalvos Polo marškinėlių pirkimus, nepriklausomai nuo jų dydžio.</p> |

## <a name="product-master-data"></a>Bendrojo produkto duomenys

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vienu metu viename puslapyje nustatykite visus numatytuosius užsakymo parametrus ir nuo vietos priklausomus užsakymo parametrus.</td>
<td>Naudojant šią funkciją pateikiama aiškesnė prekės parametrų apžvalga.</td>
</tr>
<tr>
<td>Sukurkite produkto variantų numerių nomenklatūrą.</td>
<td>Į savo produktų variantų numerius galite įtraukti elementus, pavyzdžiui, prekės dimensijas, atributus ir simbolius. Kurdami pardavimo užsakymą arba pirkimo užsakymą galite greitai rasti konkretaus produkto variantą.</td>
</tr>
<tr>
<td>Ieškokite produktų ir produkto variantų pardavimo ir pirkimo scenarijuose.</td>
<td>Kai sukuriate pardavimo eilutę arba pirkimo eilutę, galite ieškoti produktų naudodami produkto dimensijas ir bet kokius produkto numerius, išskyrus pasaulinius prekybos identifikacijos numerius (GTIN) ir brūkšninius kodus. Ši ieška yra viso teksto ieška, kuri pakeičia esamą pardavimo ir pirkimo peržvalgos sąraše naudojamą paiešką „Prasideda“. Naudodami šią funkciją galite surasti panašias ypatybes turinčias produktų grupes arba vieną unikalios charakteristikos produktą. Norėdami įjungti šią funkciją, puslapyje <strong>Ieškos parametrai</strong> pažymėkite parametrą <strong>Įjungti produkto ieškos peržvalgą</strong>.</td>
</tr>
<tr>
<td>Nurodykite produkto variantą tiesiogiai kurdami pardavimo arba pirkimo operaciją. Arba galite pasirinkti iš galimų dimensijų kombinacijų sąrašo.</td>
<td>Ši funkcija yra produktyvumo patobulinimas.
<p><strong>Pavyzdys:</strong></p>
<p>Parduodate produktą, kurio pavadinimas Polo marškinėliai. Šis produktas yra dviejų spalvų: žalios ir mėlynos. Jis taip pat yra dviejų dydžių: „Small“ (mažas) ir „Medium“ (vidutinis). Spalva ir dydis yra aktyviosios produkto Polo marškinėliai dimensijos. Įvedus Polo marškinėlių pardavimo eilutę, kurioje nurodyta žalia spalva ir dydis „Small“ (mažas), į laukus <strong>Prekės numeris</strong>, <strong>Spalva</strong> ir <strong>Dydis</strong> duomenų įvesti nebereikia. Eilutę galite sukurti atlikdami vieną iš šių veiksmų:</p>
<ul>
<li>Lauke <strong>Prekės numeris</strong> įveskite produkto varianto numerį, spalvą ar dydį. Paieškoje raskite konkretų norimą parduoti variantą ir sukurkite pardavimo eilutę.</li>
<li>Lauke <strong>Prekės numeris</strong> įveskite prekės numerį. Eikite į bet kurį produkto dimensijos lauką. Peržvalgoje <strong>Produkto dimensija</strong> pamatysite visas išleistas Polo marškinėliams taikomas dimensijų kombinacijas. Vienu veiksmu galite pasirinkti norimą parduoti produkto variantą.</li>
</ul>
</td>
</tr>
<tr>
<td>Nurodykite, ar produkto numeriai bus rodomi operacijų puslapiuose.</td>
<td>Operacijų puslapiuose, pavyzdžiui, pardavimo ir pirkimo užsakymuose rodomi tik laukai <strong>Prekės numeris</strong> ir <strong>Produkto pavadinimas</strong>. Norėdami pamatyti lauką <strong>Produkto numeris</strong>, dalyje <strong>Produkto informacijos valdymo parametrai</strong> pažymėkite parametrą <strong>Rodyti produkto numerius formose</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Projektų valdymas ir apskaita

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Naudokite toliau pateikiamą pasirinkimą registruodami sąskaitos faktūros pasiūlymus kaip paketinę užduotį. | Projektų apskaitininkai gali nustatyti, kad paketinė užduotis automatiškai pasirinktų registruojamus sąskaitos faktūros pasiūlymus, jei tie pasiūlymai atitinka paketinėje užduotyje nurodytus kriterijus. Ši funkcija pagerina ąskaitos faktūros registravimo automatizavimą, nes paketinė užduotis gali būti nuolat paleista ir automatiškai pasirenka registruojamus pasiūlymus. |
| Sukurkite analizę „Power BI“ darbalaukyje. | Su projektu ir ištekliais susijusį verslo įžvalgų (BI) turinį galima lengvai sukurti „Power BI“ darbalaukyje. |
| Naudokite pirkimo užsakymo išankstinius mokėjimus ir tinkamai įtraukite juos į projekto vertinimo procesą. | Projekto pirkimo užsakymų išankstiniai mokėjimai turi būti apdorojami prieš galint tiekėjams pateikti bet kokį mokėjimą. Šios išankstinių mokėjimų sąskaitos faktūros dabar rodomos projektų, kurių tipas **Fiksuota kaina** įvertinimo / atpažinimo procese. |
| Pasiekite ir valdykite išlaidų ir įplaukų įvertinimus ir prekių reikalavimus tiesiogiai iš darbo paskirstymo struktūros (WBS) užduoties. | Tam tikros WBS užduoties WBS planavimo rodinio informacijos dialogo lange galite valdyti tos užduoties išlaidų įvertinimus, įplaukų įvertinimus ir prekių poreikius. |
| Mokesčių žurnaluose pasirinkite lėšų skyrimo šaltinį. | Jei projekto sutartyje yra keli lėšų skyrimo šaltiniai, registruodami mokesčius galite pasirinkti vieną konkretų lėšų skyrimo šaltinį. Nepasirinkus konkretaus lėšų skyrimo šaltinio, sutartyje nurodytos lėšų skyrimo taisyklės naudojamos norint paskirstyti mokestį. |
| Atidarykite projekto išrašus naudodami „Excel“. | Naudodami naujus didžiosios knygos atnaujinimus ir biudžeto atnaujinimus galite atidaryti projekto išrašo duomenis programoje „Excel“ ir sukurti analizę naudodami „Excel“ funkciją. |
| Įjunkite projekto valdymo ir apskaitos (PMA) funkciją naudodami tik vieną konfigūracijos klavišą. | Projekto konfigūracijos klavišai pakeisti vienu projekto konfigūracijos klavišu, kuris įjungia PMA funkciją. |

## <a name="retail-and-commerce"></a>Mažmeninė prekyba ir prekyba

### <a name="advanced-warehouse-management-in-a-retail-store"></a>Patobulintas mažmeninės prekybos parduotuvės sandėlio valdymas

Mažmenininkai savo parduotuvėse gali naudoti patobulintą sandėlio valdymo (WHS) sprendimą ir atitinkamai atnaujinti dabartines elektroninio kasos aparato (POS) funkcijas, kad jis būtų palaikomas. Rankinio sprendimo procesai parduotuvėje turėtų veikti kaip ir bet kuriame kitame sandėlyje. Visi dabartiniai mažmeninės prekybos parduotuvės atsargų procesai ir visi atsargų operacijas kuriantys ar atnaujinantys POS procesai atnaujinami, kad jie naudotų specialius WHS įgalintiems sandėliams keliamus reikalavimus.

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Naudokite EKA ieškodami WHS įgalintose parduotuvėse turimų atsargų. | Peržiūrint atsargas procesas turėtų veikti taip pat, kaip veikė anksčiau. Peržvalgoje turėtų būti rodomi sandėlio lygmenyje turimi kiekiai ir neturėtų būti atsižvelgiama į vietą, atsargų būseną arba numerio lentelės dimensijas. |
| Naudodami EKA apdorokite WHS įgalintos parduotuvės perkėlimo užsakymo produkto kvitą. | Būdami EKA galite gauti WHS įgalintos parduotuvės ir prekių perkėlimo užsakymus. Vartotojas turi turėti galimybę pasirinkti gavimo vietas ir galimybę įvesti numerio lentelės ID, kad automatiškai užpildytų gavimo eilutes. |
| Naudodami EKA apdorokite WHS įgalintos parduotuvės pirkimo užsakymo produkto kvitą. | Būdami EKA galite gauti WHS įgalintos parduotuvės ir prekių pirkimo užsakymus. Vartotojas turi turėti galimybę pasirinkti gavimo vietas ir galimybę įvesti numerio lentelės ID, kad automatiškai užpildytų gavimo eilutes. |
| Naudodami EKA apdorokite produktų siuntimą iš WHS įgalintos parduotuvės. | Galite registruoti WHS įgalintos parduotuvės ir prekių perkėlimus iš EKA. Vartotojas turėtų turėti galimybę pasirinkti, iš kurios vietos siųsti, atsargų būsena turėtų būti sugeneruojama automatiškai, o numerio lentelės turėtų būti nepaisoma. |

### <a name="enable-seamless-omni-channel-commerce"></a>Įgalinkite nuoseklią „Omni“ kanalo komerciją

Nuosekli „Omni“ kanalo komercija reiškia valdymą ir užsakymų apdorojimą fizinėse parduotuvėse, internetinėse parduotuvėse, skambučių centruose ir mobiliosios komercijos patirtyse. Šiame leidime minėtoje srityje buvo atliktos šios investicijos:

- Publikavimo el. komercijos parduotuvėms patobulinimai
- Nauja vartotojams skirta mobilioji programėlė, kurią naudojant galima rasti produktus, valdyti paskyrą ir apsipirkti internete.

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Vartotojas: dabartiniame vartotojams skirtos programėlės leidime įgalintos šios funkcijos: produkto paieška, kategorijų naršymas, įdėjimas į krepšelį ir svečio kontrolės punktas. Mažmenininkai taip pat gali taikyti savo įmonės prekės ženklą programėlei, o po to jį patraukliai pateikti „Android“ ir „iOS“ parduotuvėse. | Mažmenininkai gali lengvai kurti vartotojams skirtą programėlę, kurią naudodami klientai gali naršyti, ieškoti produktų ir siųsti produktus iš savo mobiliųjų įrenginių kaip svečiai. |
| C komercijos internetinių parduotuvių klientų pageidavimų sąrašai | Nepriklausomi programinės įrangos tiekėjai (ISV) naudodami pageidavimų sąrašo valdiklį gali leisti vartotojams savo internetinėje parduotuvėje kurti ir valdyti kelis sąrašus ir peržiūrėti tuos sąrašus naudojant EKA. |
| Asinchroninių klientų kūrimas naudojant el. komercijos internetines parduotuves | Dabar ISV gali kurti klientų sąskaitas net tada, kai paslauga „Commerce Data Exchange: Real-time Service“ nepasiekiama. |
| Publikuokite kanalo produktus iš mažmeninės prekybos serverio trečiųjų šalių parduotuvėms. | Mažmeninės prekybos serveris dabar palaiko „service-to-service“ paslaugų autentifikavimą. ISV gali pasinaudoti galimybe publikuoti kanalo produktą iš mažmeninės prekybos serverio trečiųjų šalių parduotuvėms. |

### <a name="extensibility"></a>Išplečiamumas

- Komercijos vykdymo projektai dabar atribojami nuo mažmeninės prekybos SDK.
- Lengvesnis diegimas ir priežiūra naudojant EKA, mažmeninės prekybos serveriui, duomenų bazėms, mokėjimui ir aparatinės įrangos stotims skirtas komponentines „Microsoft“ pakuotes ir ISV pakuotes.

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| CRT/Parduotuvės serveris Mažmenininkai arba ISV gali pratęsti CRT per prailginimo kablius. Eilutės kodo keitimai nebepalaikomi. | Norint įjungti nuolatinį integravimą ir nuolatinį diegimą, negalimi jokie eilutės kodo pakeitimai. Taip pat norint, kad būtų palaikomas lengvas karštųjų pataisų naudojimas, kai nereikia jokio kodų sujungimo ir CRT komponentų diegimo. |

### <a name="personalized-product-recommendations"></a>Personalizuotų produktų rekomendacijos

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Peržiūrėkite personalizuotas produkto rekomendacijas keliuose elektroninio kasos aparato (EKA) sąlyčio taškuose, kad nustatytumėte, kas galėtų sudominti klientą atsižvelgiant į jo pirkimo istoriją, prekes, kurias klientas įtraukė į savo norų sąrašą, ir prekes, kurias kiti klientai įsigijo internetu ir įprastose parduotuvėse | Mažmenininkų, turinčių didelius prekių katalogus, klientams personalizuotos rekomendacijos padeda surasti produktus ir suteikia teisę parduotuvės atstovams naudoti reklaminę komunikaciją su klientais. Kadangi pateikiant produkto rekomendacijas demonstruojami į kliento pomėgius ir pirkimo įpročius orientuoti produktai, mažmenininkams tai gali padėti atlikti papildomą pardavimą ir išsaugoti klientus. Naudojant „Retail“ produkto rekomendacijos pateikiamos pagal pažintines paslaugas ir „Microsoft Azure“ mašininį mokymą. |

### <a name="pos-task-recorder"></a>EKA užduočių įrašymo priemonė

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Naudodami EKA užduočių įrašymo priemonę mažmenininkai gali gaminti mokymo medžiagą, verslo procesų modeliavimo įrankio (BPM) diagramas ir generuoti žinyno turinį, kad pagerintų našumą ir atliktų geresnę programų analizę ir kurtų geresnes programas. | Norint įjungti nuolatinį integravimą ir nuolatinį diegimą, negalimi jokie eilutės pakeitimai. Taip pat norint, kad būtų palaikomas lengvas karštųjų pataisų naudojimas, kai nereikia jokio kodų sujungimo ir CRT komponentų diegimo. |
| Pagalba realiuoju laiku naudojant EKA. | Kasininkas / vadybininkas iš EKA gali gauti su verslo procesu susijusios pagalbos realiuoju laiku neperjungdamas konteksto. |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Parduotuvės sistema: nuosekli vietinės parduotuvės patirtis

Parduotuvės sistema yra mažmenininkams skirtas diegimo pasirinkimas, padedantis valdyti parduotuvės operacijų rinkinį vietinėje parduotuvėje, „Microsoft“ viešajame debesyje arba kliento privačiajame debesyje. Šį leidimą galima naudoti tik parduotuvėje. Norėdami, kad būtų geriau palaikomos aplinkos, kuriose lėtas arba nepatikimas tinklo ryšys, mes turime pateikti parinktį mažmenininkams diegti kanalo duomenų bazę ir mažmeninės prekybos serverį parduotuvėje. Tada jie gali toliau vykdyti pagrindinius savo verslo scenarijus net tada, kai nėra ryšio su būstine (HQ). Remdamiesi įvairiais duomenų taškais, į kuriuos įtrauktos inžinerijos grupės diskusijos, klientų apklausos rezultatai ir konkurentų analizė, toliau pateikiamą sprendimo sritį mes laikome labiausiai tinkama mūsų paskirties vietos klientams:

- Pateikiamas parduotuvės sistemos savitarnos paketas.
- Numatytasis diegimas – vieno langelio diegimas, bet leidžiamas pasirinktinis diegimas.
- Įgalinkite lengvą diegimą / savitarną.
- Parduotuvėje yra mažmeninės prekybos serveris ir parduotuvės duomenų bazė bei „Async Client“ paslauga.
- Parduotuvės mažmeninės prekybos serveris užmezga tiesioginį ryšį su „HQ for Store“ sistemos programos objektų serveriu (AOS).
- Kai nėra HQ ryšio, palaikyti terminalo scenrijus.
- „Retail Modern POS“ ir „Cloud POS“ visada užmezga ryšį su „Retail Server“ parduotuvėje.
- Kai nėra HQ ryšio, palaikyti „Retail Modern POS“ ir „Cloud POS“.
- Kai nėra HQ ryšio, palaikyti specialiai „Retail Modern POS“ skirtą autonominę duomenų bazę (izoliuota kiekvienam „Retail Modern POS“ atvejui).
- Principu „paslauga už paslaugą“ pagrįstas autentifikavimas naudojamas tik parduotuvės sistemai.
- Jeigu nėra interneto ryšio, paslaugų skambučiai realiuoju laiku nepalaikomi.
- Tiesioginis „Retail Modern POS“ duomenų bazės ryšys su kanalo duomenų baze nepalaikomas.
- Įgalinti telemetriją / stebėjimą.

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Mažmenininkas iš „Dynamics AX HQ“ kanalo duomenų bazės puslapio atsisiunčia parduotuvės sistemos savitarnos diegimo programą ir konfigūracijos failą. | Mažmenininkas gali nuosekliai atsisiųsti savitarnos paketą. |
| Mažmenininkas įdiegia parduotuvės sistemą naudodamas savitarnos diegimo programą. | Mažmenininkas gali įdiegti parduotuvės sistemą naudodamas savitarnos paketą. |
| IT vadovas sukonfigūruoja „Dynamics 365 for Operations“ parduotuvės sistemą (kanalų duomenų bazę, kanalo šabloną, parduotuvę ir diegiamą paketą). | IT vadovas gali lengvai ir efektyviai sukonfigūruoti parduotuvės sistemą. |
| Mažmenininkas valdo „Retail Modern POS“ vietinėje parduotuvėje ir, kai yra ryšys, gali atlikti operacijas realiuoju laiku, pavyzdžiui, išduoti dovanų korteles. | Kai yra ryšys, mažmenininkas realiuoju laiku gali atlikti parduotuvės sistemos veiksmus. |
| Kai tik yra ryšys, mažmenininkas gali sinchronizuoti duomenis iš vietinės parduotuvės sistemos į HQ. | Kai yra ryšys, mažmenininkas gali sinchronozuoti iš parduotuvės sistemos ir į ją. |
| Mažmenininkas gali turėti saugų ryšį tarp vietinės parduotuvės sistemos ir HQ. | Kai yra ryšys, mažmenininkas gali užmegzti saugų ryšį iš parduotuvės sistemos. |
| IT vadovas ir „Microsoft Operations“ gali stebėti ir pranešti vietinėje parduotuvės sistemoje (diagnostikos ir ataskaitų pakeitimus). | IT vadovas ir „Microsoft Operations“ gali saugiai stebėti parduotuvės sistemą saugiai ir efektyviai šalinti triktis. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>„Universal Windows Platform“ programa, skirta „Retail Modern POS“

Šiuo metu „Retail Modern POS“ galima naudoti tik kaip staliniams ir planšetiniams kompiuteriams skirtą „Windows 8.1“ programą ir kaip stalinių arba planšetinių kompiuterių naršyklėms skirtą „Cloud POS“. Šiame leidime „Retail Modern“ EKA konvertuojama į „Universal Windows Platform“ (UWP) programą. Atlikus šį pakeitimą „Retail Modern POS“ bus galima paleisti bet kuriame „Windows 10“ prietaise (staliniame, planšetiniame kompiuteryje arba telefone) ir netgi perjungti „Continuum“ įgalintų prietaisų rodinius.

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Įjunkite svarbią mažiems prietaisams skirtą EKA funkciją. | Mažmeninės prekybos EKA funkciją galima naudoti telefonuose ir kituose mažuose prietaisuose, kuriuose įdiegta sistema „Windows 10“. |

## <a name="supply-chain-management"></a>Tiekimo grandinės valdymas

### <a name="consignment-inventory"></a>Konsignacijos atsargos

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Jeigu esate tiekėjas, žaliavas galite saugoti kliento sandėlyje. Jeigu esate klientas, galite atidėti faktinį pirkimą, kol žaliavos bus reikalingos gaminant. | Laikant žaliavų atsargas gali susidaryti didelių išlaidų. Naudodamas konsignacijos atsargas, tiekėjas žaliavas gali laikyti kliento sandėlyje. Tada klientas gali atidėti faktinį pirkimą, kol žaliavos bus reikalingos gaminant. Žaliavos užsakomos ir gaunamos naudojant konsignacijos papildymo užsakymą. Šiame papildymo užsakyme įrašomos faktinės operacijos, tačiau tai nedaro jokio poveikio didžiajai knygai. Norėdami atskirti klientui priklausančias prekių atsargas ir tiekėjui priklausančias prekių atsargas, galite naudoti savininko atsargų dimensiją. Atsargų nuosavybės pakeitimą atlieka žurnalo procesas, kuris atlieka žaliavų nuosavybės perkėlimą iš tiekėjui priklausančių atsargų į klientui priklausančias atsargas. Šis procesas sužadina pirkimo užsakymo ir produkto kvito kūrimą.<blockquote>[!NOTE] Šią funkciją galima naudoti tik gaunamai gamyboje naudojamų žaliavų konsignacijai. Ji neintegruota su sandėlio valdymu (WHS) ir transportavimo valdymu (TMS).</blockquote> |
| Jeigu esate tiekėjas, gaukite informaciją apie klientui perkeliamų konsignacijos atsargų kiekį. | Norėdamas pateikti sąskaitą klientui, tiekėjas reikalauja informacijos apie iš konsignacijos atsargų nupirktas žaliavas ir jų pirkimo datą. Naudodamas tiekėjo bendradarbiavimo sąsają, tiekėjas taip pat gali stebėti kliento vietoje turimas atsargas. |
| Perkelkite tiekėjui priklausančias atsargas naudodami perkėlimo žurnalą. | Norėdami sekti tiekėjui priklausančių atsargų faktinę vietą, turite galėti įrašyti vietą sistemoje. Naudodami perkėlimo žurnalą galite įrašyti faktinį atsargų perkėlimą, pavyzdžiui, perkėlimą iš vienos sandėlio vietos į kitą to paties sandėlio vietą. |
| Pakoreguokite tiekėjui priklausančias atsargas naudodami skaičiavimo žurnalą. | Svarbu, kad sistemoje turimos atsargos sutaptų su faktinėmis atsargomis. Tiekėjui priklausančias atsargas galima koreguoti naudojant skaičiavimo procesus (pavyzdžiui, kiekio koregavimą) ir skaičiavimo žurnalo procesus. |
| Sužinokite daugiau apie konsignacijos palaikymą „Dynamics 365 for Operations“ | Norėdami gauti daugiau informacijos apie konsignacijos procesų palaikymą, žr. [Konsignacija](../../../supply-chain/inventory/consignment.md), [Konsignacijos nustatymas](/d365F-O/fin-ops-core/fin-ops/get-started/consignment), [Sukurti konsignacijos papildymo užsakymą (užduočių vedlys)](../../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) ir [Pakeisti konsignacijos atsargų savininką pagal produkcijos paklausą (užduočių vedlys)](../../../supply-chain/inventory/tasks/change-ownership-consignment.md). |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Tiekėjo bendradarbiavimas (ankstesnis pavadinimas – tiekėjo portalas)

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Įgalinkite tiekėjus atsakyti į kiekvieną pirkimo užsakymo eilutę ir siūlyti pakeitimus. | Kai kuriais atvejais tiekėjai kai kurias pirkimo užsakymo eilutes nori priimti, o kitas – atmesti. Dabar tiekėjai gali atskirai valdyti kiekvieną pirkimo užsakymo eilutę. Kiekvieną eilutę galima atmesti, priimti arba priimti su pakeitimais. Pavyzdžiui, tiekėjai gali pakeisti pristatymo datą, paskirstyti pristatymą ir kiekį arba pasiūlyti alternatyvią prekę. |
| Įgalinkite tiekėjus valdyti kontaktinio asmens informaciją. | Tiekėjai gali tvarkyti savo įmonės kontaktinio asmens informaciją. Ši informacija apima vardus, el. pašto adresus ir telefono numerius. Prieiga prie šios priemonės suteikiama paskiriant saugos vaidmenį. |
| Su pirkimo užsakymais susijusius dokumentus naudokite bendrai su tiekėjais. | Kai dokumentą (pavyzdžiui, dokumentą apie reikalavimus) turite naudoti bendrai su tiekėju, patogu jį susieti su atitinkamu pirkimo užsakymu. Tada tiekėjas, susiedamas dokumentą su savo atsakymu į pirkimo užsakymą, gali bendrai su klientu naudoti pastabas ir priedus. Dokumentų tvarkymas yra žemesnio lygio palaikanti sistema, ir su tiekėjais bendrai naudoti galima tik tas pastabas ir priedus, kurie klasifikuojami kaip „išoriniai“. |
| Pateikti naujus tiekėjo vartotojus. | Jei jūsų tiekėjai naudoja tiekėjo bendradarbiavimo sąsają, kai nauji kontaktai reikalauja prieigos prie tiekėjo bendradarbiavimo, jie gali nuosekliai prašyti naujo vartotojo abonementų. Pirkimų specialistai gali pateikti užklausą suteikti vartotojo abonementą kontaktiniam tiekėjo organizacijos asmeniui. Tiekėjo kontaktinis asmuo, kuris jau yra tiekėjo bendradarbiavimo vartotojas, taip pat gali pateikti tokio tipo užklausą. Užklausa galiausiai sukuria naują tiekėjui priskiriamus vaidmenis atliekantį „Dynamics 365 for Operations“ vartotoją. Ji taip pat supaprastina „Microsoft Azure“ portalui pateikiamą užklausą suteikti vartotojui naują „Azure Active Directory“ („Azure AD“) vartotojo paskyrą. Tiekėjai taip pat gali prašyti, kad būtų išjungti tam tikri su tiekėju susijusio vartotojo abonementai arba kad būtų pakeisti saugos vaidmenys. |
| Sužinokite daugiau apie tiekėjo bendradarbiavimo palaikymą „Dynamics 365 for Operations“. | Norėdami gauti daugiau informacijos apie tiekėjo bendradarbiavimą, žr. [Tiekėjo bendradarbiavimas su išoriniais tiekėjais](../../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Tiekėjo bendradarbiavimas su klientais](../../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Valdyti tiekėjo bendradarbiavimo vartotojus](../../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Nustatyti ir išlaikyti tiekėjo bendradarbiavimą](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) ir [Tiekėjo bendradarbiavimo sąskaitų faktūrų išrašymo darbo sritis](../../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). |

### <a name="intercompany-order-processing"></a>Vidinio įmonės užsakymo apdorojimas

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nurodykite tiesiogiai pardavimo užsakymo eilutėse, iš kokio šaltinio turėtų būti gaunama paklausa ir kaip turėtų būti gaunamas šaltinis.
<p><strong>Pavyzdys:</strong></p>
<p>Sukurkite pardavimo užsakymo eilutę ir nurodykite tiesioginį pristatymą kaip pristatymo tipą. Pirminis tiekėjas įtraukiamas į pardavimo užsakymo eilutę kaip šaltinio gavimo taškas.</p>
</td>
<td>Užsakymų priėmimo srautas pastebimai pagerėjo. Dabar tiesiogiai pardavimo užsakymo eilutėse galite nurodyti, iš kokio šaltinio turėtų būti gaunama paklausa ir kaip turėtų būti gaunamas šaltinis. Jums nebereikia laukti, kol į pardavimo užsakymą bus įtrauktos visos eilutės. Naudodamiesi naujomis pardavimo užsakymo eilučių parinktimis, kai nurodote tiekėją, galite nurodyti pristatymo tipą. Kai susiejate tiekėją su pardavimo užsakymo eilutėmis, užsakymo grandinės sukuriamos pristatymui iš tiekėjo.
<ul>
<li>Tiekėjas gali būti vidinės įmonės tiekėjas, naudojantis vidinį pirkimo užsakymą ir pardavimo užsakymą, arba tai gali būti išorinis tiekėjas, naudojantis išorinį pirkimo užsakymą.</li>
<li>Pristatymo tipas gali būti <strong>Tiesioginis pristatymas</strong> arba <strong>Atsargos</strong>. Pristatymo tipas <strong>Atsargos</strong> nurodo, kad tiekėjas turi tiekti žaliavas į vidines atsargas, kol jos išsiunčiamos klientui.</li>
</ul>
</td>
</tr>
<tr>
<td>Sukurkite užsakymo pasižadėjimą tiesiogiai iš pardavimo užsakymo eilučių.
<p><strong>Pavyzdys:</strong></p>
<p>Sukurkite pardavimo užsakymo eilutę, kurios šaltinis gaunamas iš vidinės įmonės tiekėjo. Palikite eilutę. Pristatymo datos apskaičiuojamos pagal išteklių tiekimo įmonės užimtumą.</p>
</td>
<td>Kai kuriate naują šaltinio informaciją naudojančias pardavimo užsakymo eilutes, pristatymo datos apskaičiuojamos pagal valdiklį <strong>Pristatymo data</strong>. Pavyzdžiui, pasirinkus vidinės įmonės tiekėją, apskaičiuojamas pasiekiamumas išteklių tiekimo įmonėje. Tokiu būdu užsakymo grandinės sukuriamos automatiškai kartu su pardavimo užsakymo eilutėmis. Ši funkcija padeda užtikrinti, kad pristatymo datos būtų matomos išteklių tiekimo įmonėje, kad profiliai, kuriuos galima pažadėti (ATP) gali susidoroti su numatoma paklausa tiesiogiai sukūrus pardavimo užsakymus.</td>
</tr>
<tr>
<td>Peržiūrėkite produkto prieinamumą visose išteklių tiekimo vietovėse ir parinkite geriausią išteklių tiekimo parinktį.</td>
<td>Puslapis <strong>Pristatymo alternatyvos</strong> pertvarkytas ir dabar jame pateikiama vertinga informacija apie visus patvirtintus vidinius ir išorinius tiekėjus. Ši informacija apima tiekėjo įsigijimo išteklių tiekimo parinktis. Kai pasirenkate pristatymo būdą, sistema apskaičiuoja galimas pristatymo datas. Galite nuosekliai pasirinkti geriausią kliento parinktį ir taikyti šią parinktį kiekvienai pardavimo užsakymo eilutei.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Didelės apimties paskirstymo centrų sandėlio patobulinimai

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Sukurkite darbą, kai prekės jau supakuotos pakavimo stotyje. | Ši funkcija yra naudinga, kai yra papildomų procesų po to, kai atliekamas rankinio pakavimo darbas (pvz., sukrovimas ant padėklų, kokybės tikrinimas, siuntų konsolidavimas arba pakrovimo rampų pakeitimai). Naudodami naują darbo tipą **Supakuoto konteinerio paėmimas** galite modeliuoti šias užduotis naudodami atskiras darbo eilutes. Dabar modeliuodami pakavimo stotis galite generuoti darbą po pakavimo. Šį darbą galima naudoti norint organizuoti supakuotų atsargų judėjimą. |
| Grupuokite konteinerius pakavimo stotyje. | Naudojant šią funkciją kelios pakuotės gali būti grupuojamos į vieną pakavimo stoties konteinerį arba numerio lentelę. Pavyzdžiui, el. komercijos / didmeninės prekybos operatorius gali grupuoti 100 atskirai supakuotų paketų į vieną konteinerį (pvz., padėklą arba narvą). Tada šį konteinerį galima patraukti, suskirstyti į etapus arba įkelti naudojant vieno darbo instrukciją, kurią darbuotojas sugeneruoja nuskaitydamas vieną grupuoto konteinerio brūkšninį kodą (numerio lentelę). Naudojant šią funkciją, kai perkeliama daug į mažesnes pakuotes supakuotų konteinerių, sumažėja darbo operacijų. Norėdami gauti daugiau informacijos, žr. [Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas (užduočių vedlys)](../../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md). |
| Sukurkite supakuotų konteinerių išleidimo strategiją. | Darbą, kuris sužadinamas išleidus konteinerį, galima sukurti automatiškai arba rankiniu būdu. Kai jis automatinis, darbas sugeneruojamas uždarius konteinerį naudojant vietos nurodymą ir darbo šablono sistemą. Kai leidimas rankinius, pakuotojas gali nuspręsti, ar darbą reikėtų generuoti vienam konteineriui, ar konteinerių grupei. Naudojant šią funkciją sumažinama rizika, kad uždaryti konteineriai bus paimti ir perkelti, kai jie dar nebus parengti, kad juos būtų galima perkelti iš pakavimo stoties. Naudojant ją taip pat galimas ne sistemos valdomas drupuotas leidimas. |
| Trumpo paėmimo perskirstymas | Įtrauktas trumpo paėmimo procesų palaikymas, kad būtų lengviau susieti, kas negali paimti prekių ir nori įvykdyti užsakymą, kai reikiama prekė pateikiama kitoje vietoje. Galite naudoti automatinio perskirstymo procesą, kuris naudoja tuos pačius vietos nurodymus prekėms gauti, jei jų yra kitoje vietoje. Arba, kai naudojamas rankinis perskirstymas, mobiliajame prietaise rodomas vietų sąrašą kartu su galimu kiekiu. Tada sandėlio darbuotojas gali pasirinkti, iš kurios vietos naudoti atsargas. Šiuos du metodus galima nustatyti atskirai arba kartu kaip vieną sandėlio darbuotojo meniu komandą. Kai naudojamas neautomatinis perskirstymas, sandėlio darbuotojas gali paimti trumpai paimamos prekės kiekį iš kelių vietų. Norėdami gauti daugiau informacijos, žr. [Trumpalaikio išrinkimo elementų perskirstymo nustatymas (užduočių vedlys)](../../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md). |
| Perkelkite atsargas su kuriomis susietas darbas. | Dabar galite perkelti atsargas su kuriomis susietas darbas. Ši funkcija gali būti naudinga, jei, pavyzdžiui, darbuotojas nori atlaisvinti šiek tiek atvežimo rampos vietos ir perkelti registruotus padėklus, kurie turi būti perkelti į kitą gavimo vietą. Rampa atlaisvinama ir gali gauti papildomą prekių krovinį, o perkeltos atsargos atnaujinamos naudojant naują padėjimo informaciją. Šią funkciją taip pat galima naudoti norint atlaisvinti vietos paėmimo vietose perkeliant atsargas, su kuriomis susietas darbas, ir sukuriant vietos papildymui. Taip pat galite ją naudoti norėdami perkelti krovinius iš vienos etapo vietos į kitą neprarasdami sugeneruoto krovimo darbo. Tokiu būdu funkcija gali padėti optimizuoti laiką, kurio reikia norint įkelti atvykstančius sunkvežimius. Galite perkelti pardavimo užsakymams, perkėlimo užsakymo problemoms, perkėlimo užakymo kvitams ir pirkimo užsakymams rezervuotas atsargas. Jeigu perkeliant bus padalintos eilutės, perkėlimas neleidžiamas. Pavyzdžiui, jei turite 100 prekės vienetų darbo eilutę, į kitą vietą negalima perkelti tik 30 tos prekės vienetų. |
| Suliekite numerio lenteles, su kuriomis susietas darbas. | Galite sulieti numerio lenteles, su kuriomis susietas išsiunčiamas darbas. Pavyzdžiui, kai paėmimas buvo suskirstytas į keletą darbo dalių, pristačius numerio lenteles į surinkimo vietą, gali būti naudinga leisti jas sulieti. Numerio lenteles galima konsoliduoti tik tada, jei jos yra toje pačioje vietoje, yra to pačio krovinio narės ir turi tą pačią siuntimo informaciją. |
| Užblokuokite su papildymu eilutės lygmenyje susietą išrinkimo darbą. | Dabar galite užblokuoti darbą eilutės lygmeniu, o ne antraštės lygmeniu, kad darbuotojai galėtų atlikti paėmimo eilutes, kurios neužblokuotos paklausos papildymu. Todėl didelius pardavimo užsakymus turintis didmenininkas arba didelius pardavimo užsakymus arba papildymo perkėlimo užsakymus turintis mažmenininkas gali leisti paleisti išrinkimo darbą visose eilutėse, kurioms nėra taikomas papildymo darbas. Tada tuo pačiu metu galima pabaigti išrinkimo ir papildymo darbą. Šią funkciją galite sukonfigūruoti taip, kad galėtumėte pasirinkti, ar užblokuoti antraštės lygmenyje, ar eilutės lygmenyje. Taip pat galite naudoti abu metodus ir sukurti kiekvieno metodo darbo šabloną. Antraštės / eilutės konfigūracija nustatoma darbo šablonuose, bet galite ją pakeisti tiesiogiai sugeneruotame darbe. |
| Atšaukite darbą naudodami mobilųjį įrenginį. | Dabar galite atšaukti darbą naudodami mobilųjį įrenginį su poreikio papildymu arba be jo. Anksčiau, turėdavote naudoti raiškiąją kliento programą. Norėdami įgalinti šią funkciją, sukurkite mobiliojo įrenginio meniu elementą, kuriame nustatytas režimas **Netiesioginis** ir veiklos kodas **Atšaukti darbą**. |

### <a name="warehouse-operation-enhancements"></a>Sandėlio operacijos patobulinimai

| Ką galite daryti | Kodėl tai svarbu |
|-----------------|-----------------------|
| Modelio skirtingi konteinerių tipai. | Sandėlyje galite naudoti skirtingus konteinerių tipus, kad galėtumėte optimizuoti saugyklą ir dėl kitų priežasčių. Naujas konteinerio tipo objektas turi fizines konteinerių tipų savybes. Dabar galite susieti numerio lenteles su konkrečiu konteinerio tipu ir naudoti vietos sandėliavimo limitus. Pavyzdžiui, galite naudoti šią funkciją norėdami kontroliuoti, kiek padėklų (ar kitokio tipo konteinerio) leisite tam tikroje vietoje. Konteinerių tipai taip pat įtraukti į vienetų sekų grupes, kad būtų galima įtraukti numatytuosius gavimo proceso konteinerių tipus. Konteinerių tipai gali būti naudojami su paėmimo ir pakrovimo vietos direktyvomis. Jie taip pat gali būti naudojami turimų atsargų rodinyje, kad jums būtų lengviau nustatyti, kiek konteinerių tipų saugoma šiuo metu. Norėdami gauti daugiau informacijos, žr. tinklaraščio įrašą [Su paleisti sandėlio valdymo procesus naudojamu konteinerio tipu susietų numerio lentelių naudojimas](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Nors šiame tinklaraščio įraše aprašomas atnaujinimas į „Microsoft Dynamics AX 2012“, tas pats palaikymas dabar įtrauktas į „Dynamics 365 for Operations“. |
| Siuntų atšaukimas | Sandėlyje turite turėti galimybę tvarkyti vėluojančius pakeitimus. Pavyzdžiui, kai kurios prekės gali būti pažeistos, todėl negalėsite jų siųsti. Arba klientas gali per vėlai pateikti užklausą, kad būtų galima ją atšaukti arba pakeisti. Naudodami „Dynamics 365 for Operations“ dabar galite atšaukti siuntą. Todėl galite atšaukti važtaraštį, kad vėliau galėtumėte jį atnaujinti nurodydami teisingus kiekius. Panašiai gaunamame sraute galite atšaukti produkto kvitus, kad būtų galima sukurti atnaujintą versiją. |
| Naudokite skirtingas prekes turinčius padėklus. | Dabar galite gauti ir registruoti „mišrų“ padėklą. Mišrų padėklą sudaro skirtingos prekės, surinktos ant vienam ar keliems pirkimo užsakymams ar eilutėms skirto padėklo. Visas registracijas galima apibendrinti į vieną paskirties numerio lentelę. Šis procesas įgalinamas naudojant sandėlio mobilųjį įrenginį. Pavyzdžiui, kai mišrių prekių padėklas atvyksta į sandėlį, prieš perkeliant jį į paskirtą padėjimo vietą, priimantis darbuotojas identifikuoja prekes ir jų kiekį ant padėklo. Padėjimo vietos identifikuojamos naudojant darbo šablonus ir vietos nurodymus. Jei padėjimo vietos paskirstomos kelioms fiksuotą vietą turinčioms prekėms, naudojant šią funkciją sukuriama tiek padėjimo darbo eilučių, kiek yra skirtingų prekių ant mišraus padėklo. Naudojant šią funkciją gautų mišrių prekių padėklų registracija ir padėjimas pagreitėja ir tampa lankstesnis. Norėdami gauti daugiau informacijos, žr. tinklaraščio įrašą [Gauti ir registruoti padėklą su mišriomis išteklių dokumento eilutėmis naudojant vieną numerio lentelę](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) ir informaciją apie mišrių padėklų palaikymą [skelbime apie jūsų naujausią kaupiamąjį naujinimą](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Nors šiame tinklaraščio įraše aprašomas atnaujinimas į „AX 2012“, tas pats palaikymas dabar įtrauktas į „Dynamics 365 for Operations“. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Nedideli tiekimo grandinės valdymo funkcijos patobulinimai

<table>
<thead>
<tr>
<th>Ką galite daryti</th>
<th>Kodėl tai svarbu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Norėdami importuoti ir eksportuoti duomenis, naudokite naujus duomenų objektus.</td>
<td>Importuoti ir eksportuoti duomenis galite naudodami šiuos duomenų objektus:
<ul>
<li>Transportavimo sąskaita faktūra</li>
<li>Sujungti turimas atsargas pagal sandėlį ir atsargų būseną</li>
<li>Atsargų mokesčiai</li>
<li>Pasiūlymas</li>
</ul>
</td>
</tr>
<tr>
<td>Naudodami patobulintą „Gantt“ valdiklį sukurkite interaktyvius planavimo scenarijus.</td>
<td>Naudodami patobulintą „Gantt“ valdiklį galite sukurti naujų interaktyvių planavimo scenarijų ir pateikti patobulintus API sąsajas, kurias galima naudoti norint tinkinti veiklų išvaizdą. Štai keletas naujų API sąsajų:
<ul>
<li>Vertikalus veiklų nuvilkimas</li>
<li>Veiklų įtraukimas / šalinimas</li>
<li>Užimtų laikotarpių peržiūra suvestinės juostoje</li>
<li>Veiklos ribų spalvos ir stiliaus keitimas</li>
<li>Tinklelio teksto spalvos, stiliaus ir fono keitimas</li>
</ul>
</td>
</tr>
<tr>
<td>Geriau atlikite medžiagų bei išteklių planavimą.</td>
<td>Atlikta keletas medžiagų ir išteklių planavimo patobulinimų:
<ul>
<li>Dabar išdavimo laiko rezervas tvarkomas turint prekę.</li>
<li>Patvirtinę suplanuotus užsakymus pakeiskite pristatymo datą.</li>
<li>Pirmenybę teikite užsakymų vykdymui, o ne atsargų pakankamumui.</li>
<li>Neleiskite planuoti praeityje suplanuotų užsakymų.</li>
</ul>
</td>
</tr>
<tr>
<td>Praneškite faktinį gamybos suvartojimą ir peržiūrėkite atsargų būseną.</td>
<td>Galite peržiūrėti faktinį gamybos suvartojimą. Be to, naudodami naują žymės langelį <strong>Rodyti atsargų būseną</strong>, kuris įtrauktas į meniu elemento <strong>Darbo kūrimas</strong> dalį <strong>Perkėlimas</strong>, galite peržiūrėti atsargų būseną.</td>
</tr>
<tr>
<td>Jeigu jūsų vežėjo tarifai apskaičiuojami pagal tūrinį svorį, apskaičiuokite tūrinį svorį.</td>
<td>Tam, kad galėtumėte apskaičiuoti tūrinį svorį, pridėtas naujas TMS tarifų mechanizmas, skaičiuojantis pagal tūrinį svorį.</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildomi ištekliai

[Kas nauja ar pasikeitė „Finance and Operations“ pagrindiniame puslapyje](whats-new-changed.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]