---
title: "Tiekėjų supažindinimas"
description: "Šioje temoje aprašomas naujų tiekėjų supažindinimas. Jame paaiškinami veiksmai, reikalingi įvairiems vaidmenims šio proceso metu."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests,SysUserRequestListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 325cf12345afcf531181f65a41d0e5262798c14f
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="onboard-vendors"></a>Tiekėjų supažindinimas
[!include [banner](../includes/banner.md)]

---

Naujus tiekėjus galima supažindinti ir užregistruoti kaip tiekėjus „Microsoft Dynamics 365 for Finance and Operations“ remiantis informacija, surinkta iš asmens, kuris atstovauja tiekėją.

Procesą sudaro toliau nurodyti veiksmai, kai įvairius vaidmenis turintys asmenys atlieka veiksmus sistemoje.

1. **Duomenų valdymo „OData“** – Objekto importavimas – pradinė užklausa yra galimo tiekėjo registravimo užklausa. Paprastai ši užklausa gaunama iš šaltinio, pvz., kliento nuomojamos svetainės, kuri suteikia anoniminę prieigą. Tiekėjai gali užsiregistruoti pateikdami pagrindinę informaciją, pvz., tiekėjo pavadinimą, pagrindimą, organizacijos numerį ir kontaktinio asmens vardas, pavardę bei el. pašto adresą. Užklausos importuojamos naudojant sąsają Duomenų valdymas.
2. **Galimo tiekėjo registravimo užklausų sąrašo puslapis** – atsižvelgiant į galimo tiekėjo registravimo užklausoje pateiktą informaciją, įsigijimo specialistas nusprendžia, ar tiekėjas turi būti supažindintas. Įsigijimo specialistas peržiūri gaunamą užklausą „Finance and Operations“ sąrašo puslapyje **Galimo tiekėjo registravimo užklausos**.
3. **Vartotojų parengimo darbo eiga** – kai įsigijimo specialistas patikrina gaunamos užklausos informaciją ir nusprendžia tęsti supažindinimo procesą, vartotojo užklausos darbo eiga parengia naują vartotoją ir el. paštu išsiunčia kvietimą priimti kontaktinį asmenį kaip autentifikuotą „Microsoft Dynamics 365“ vartotoją.
4. **Tiekėjo registravimo vedlys** – tiekėjo kontaktinis asmuo prisijungia prie „Finance and Operations“ naudodamas naują vartotojo paskyrą. Jis atlieka tiekėjo registravimo vedlį ir pateikia informaciją, pvz., adresus, verslo informaciją, įsigijimo kategorijas ir atsakymus į klausimyną.
5. **Patvirtinimo darbo eiga** – sukuriama tiekėjo užklausa, kurioje yra registracijos informacija. Ši tiekėjo užklausa pateikiama į darbo eigą ir nukreipiama peržiūrėti bei patvirtinti.
6. **Tiekėjo bendrųjų duomenų kūrimas ir vartotojo vaidmens modifikavimas** – patvirtinus tiekėjo užklausą, sukuriamas tiekėjo įrašas. Tiekėjo kontaktinio asmens vartotojo paskyrai suteikiama arba išjungiama prieigos prie tiekėjo bendradarbiavimo teisė.

Toliau pateikiamoje lentelėje parodomi proceso veiksmai ir vaidmenys.

| Vaidmuo ir „procesas“       | Duomenų valdymo „OData“ – Objekto importavimas | Galimo tiekėjo registravimo užklausų sąrašo puslapis | Vartotojo parengimo darbo eiga | Tiekėjo registravimo vedlys | Patvirtinimo darbo eiga | Tiekėjo bendrųjų duomenų kūrimas ir vartotojo vaidmens modifikavimas |
|--------------------------|---|---|---|---|---|---|
| System                   | Importuojama naujo tiekėjo užklausa. | | | | | Priėmus tiekėjo užklausą, sukuriamas tiekėjo įrašas. |
| Įsigijimo specialistas | | Pradėkite supažindinimo procesą. | | | Peržiūrėkite ir priimkite arba atmeskite tiekėjo užklausą. | |
| Administratorius            | | | Sukurkite vartotoją „Finance and Operations“ ir „Microsoft Azure“. | | | |
| Tiekėjo kontaktinis asmuo    | | | Siųskite el. laišką kontaktiniam asmeniui. | Užregistruokite tiekėjo informaciją. | | |

Greita tiekėjų supažindinimo proceso demonstracija parodyta šiame trumpame „YouTube“ vaizdo įraše: 
> [!Video https://www.youtube.com/embed/0KUc3AGaTKk]

## <a name="importing-the-prospective-vendor-registration-request"></a>Galimo tiekėjo registravimo užklausos importavimas

Galimo tiekėjo registravimo užklausa yra objektas „Finance and Operations“. Galite nustatyti sistemą importuoti duomenis naudojant šį objektą. 

Tolesnėje lentelėje rodoma šiame objekte pateikta informacija, kurią galima importuoti.

| Laukas                        | aprašymas |
|------------------------------|-------------|
| Tiekėjo vardas                  | Tiekėjo pavadinimas. |
| Verslo pagrindimas       | Tiekėjo užklausos priežastis arba priežastys. |
| Organizacijos numeris          | Oficialiai patvirtintas registracijos numeris. |
| Verslo šaka             | Verslo šaka, kurioje dirba tiekėjas. |
| Kontaktinio asmens vardas  | Asmens, kuris bus kviečiamas užregistruoti tiekėjo informaciją, vardas. |
| Kontaktinio asmens antras vardas | Asmens, kuris bus kviečiamas užregistruoti tiekėjo informaciją, antras vardas. |
| Kontaktinio asmens pavardė   | Asmens, kuris bus kviečiamas užregistruoti tiekėjo informaciją, pavardė. |
| Kontaktinio asmens el. pašto adresas       | El. pašto adresas, kuris bus naudojamas kuriant naują vartotoją „Finance and Operations“ ir kuris bus užregistruojamas nuomotojo „Azure Active Directory“ („Azure AD“) paskyroje. |
| Pateikimo data               | Diena, kurią užklausa buvo sukurta išorinėje sistemoje. |
| Juridinis subjektas                 | Juridinis subjektas, kuriame tiekėjas pageidauja tapti tiekėju. Ši reikšmė turi būti juridinio subjekto kodas, užregistruotas „Finance and Operations“. Jei importavimo proceso metu negaunama jokia reikšmė, taikoma reikšmė iš paraiškų parametrų. |
| Tiekėjo tipas                  | Tiekėjas gali būti organizacija arba asmuo. Tiekėjo tipas nustato, kaip tiekėjas galiausiai sukuriamas. |

Importavus galimo tiekėjo registravimo užklausą, ji rodoma sąrašo puslapyje **Galimo tiekėjo registravimo užklausa**. Iš šio sąrašo puslapio įsigijimo specialistas gali pakviesti vartotoją. Vartotojo parengimo užklausa išsiunčiama į darbo eigą.

## <a name="submitting-a-prospective-vendor-user-request"></a>Su galimu tiekėju susijusio vartotojo užklausos pateikimas

Su galimu tiekėju susijusio vartotojo užklausos vartotojo užklausos paskirtis yra parengti asmenį, pateikusį pradinę užklausą, kad jis galėtų prisijungti prie „Finance and Operations“ naudodamas el. pašto paskyrą, kuri pateikta galimo tiekėjo registravimo užklausoje.

Su galimu tiekėju susijusio vartotojo užklausą apdoroja vartotojo užklausos darbo eiga. Ši darbo eiga susisiekia naudodama „Azure AD“ B2B bendradarbiavimą. Ji sukuria vartotoją „Finance and Operations“, kuriam priskirti atitinkami saugos parametrai.

Naujiems nustatytiems vartotojams priskiriami toliau nurodyti saugos vaidmenys.

- Išorinis sistemos vartotojas
- Galimas tiekėjas (išorinis)

Naujas vartotojas gaus el. laišką, kurį sugeneruoja vartotojo užklausos darbo eiga. Šiuo el. laišku vartotojas kviečiamas prisijungti prie sistemos.

Informacijos apie el. laiško konfigūravimą ir darbo eigą apskritai žr. vartotojo užklausos darbo eigos aprašyme: [Tiekėjo bendradarbiavimo nustatymas ir tvarkymas](set-up-maintain-vendor-collaboration.md).

## <a name="vendor-registration"></a>Tiekėjo registracija

Su galimu tiekėju susijęs vartotojas, kuris prisijungia prie „Finance and Operations“, matys pirmąjį tiekėjo registravimo vedlio puslapį, kuriame jis gali įvesti tiekėjo informaciją.

Vedlys atspindi tiekėjo užklausos konfigūraciją. Nuo šalies arba regiono, kuriame tiekėjas vykdo veiklą, priklauso, kokią informaciją prašoma nurodyti vedlyje ir kokia informacija yra privaloma.

Daugiau informacijos apie tiekėjo užklausos konfigūraciją žr. [Tiekėjo bendradarbiavimo saugos nustatymas ir tvarkymas](set-up-maintain-vendor-collaboration.md). Tolesnėje lentelėje pateikiama vedlio puslapių apžvalga ir kiekvieno puslapio paskirtis.

| Puslapis                       | aprašymas |
|----------------------------|-------------|
| Šalis/regionas             | Nuo šalies arba regiono priklauso tiekėjo užklausos konfigūracija, taikoma kituose vedlio puslapiuose. Nuo to taip pat priklauso peržvalgoje **Mokesčių regionas** pateikiamos reikšmės. |
| Sąlygos       | Šis puslapis gali būti pasiekiamas priklausomai nuo tiekėjo užklausos konfigūracijos. Jei jis pasiekiamas, vartotojas turi patvirtinti sąlygas, kad galėtų tęsti. |
| Informacija apie tiekėją         | Šiame puslapyje pateiktas tiekėjo pavadinimas, kuris automatiškai įvedamas iš pradinės galimo tiekėjo registravimo užklausos. Jame taip pat nurodyti organizacijos numeris, tiekėjo telefono numeris, fakso numeris ir el. pašto adresas, taip pat – tiekėjo adresų (įvairioms paskirtims). |
| Informacija apie kontaktinį asmenį | Šiame puslapyje pateikti kontaktinio asmens vardas ir pavardė, kurie automatiškai įvedami iš pradinės galimo tiekėjo registravimo užklausos. Jame taip pat pateikiami kontaktinio asmens telefono numeris ir el. pašto adresas, taip pat – kontaktinio asmens adresai (įvairioms paskirtims). |
| Verslo informacija       | Šiame puslapyje pateikiami mokesčių mokėtojo kodai (skirti įvairioms šalims arba regionams) ir darbuotojų skaičius. Jame taip pat nurodoma, ar verslas priklauso mažumų atstovams. |
| Įsigijimo kategorijos     | Šiame puslapyje nurodomos įsigijimo kategorijos, kurių patvirtinimo tiekėjas prašo. Vartotojas gali pasirinkti kategorijas įsigijimo kategorijų hierarchijoje. Galite konfigūruoti, kiek lygių rodoma pasirinkus **Paraiškų parametrai** &gt; **Tiekėjo bendradarbiavimas**, dalyje **Paraiškos** &gt; **Sąranka**. |
| Klausimynai             | Vedlys gali apimti tiekėjui skirtų klausimynų rinkinį. Vedlyje rodomi klausimynai konfigūruojami tiekėjo užklausoje arba pagal įsigijimo kategoriją. Jei klausimynai konfigūruojami pagal įsigijimo kategoriją, nuo įsigijimo kategorijų, kurių patvirtinimo tiekėjas prašo, priklauso, kurie klausimynai rodomi vedlyje. Puslapyje **Įsigijimo kategorijos** galite įtraukti klausimyną į atitinkamą kategoriją ir nustatyti veiklos tipą į parinktį **Tiekėjo supažindinimas**. |

Kai su galimu tiekėju susijęs vartotojas įvykdo tiekėjo registravimo vedlį, sukuriama tiekėjo užklausa.

## <a name="manually-or-automatically-submit-a-vendor-request"></a>Neautomatinis arba automatinis tiekėjo užklausos pateikimas

Tiekėjo užklausą galima kurti kaip juodraštį ir neautomatiškai pateikti į darbo eigą. Taip pat tiekėjo užklausą galima automatiškai pateikti į darbo eigą, kai tiekėjo registravimo vedlys įvykdytas. Užklausą galima pateikti neautomatiškai, jei, pavyzdžiui, įsigijimo specialistas nori įvertinti, ar užklausą reikia nukreipti į patvirtinimo procesą prieš ją pateikiant į darbo eigą.

- Pasirinkite **Paraiškų parametrai** &gt; **Tiekėjo bendradarbiavimas**, tada pasirinkite **Į darbo eigą automatiškai pateikti galimų tiekėjų registraciją**, norėdami sukonfigūruoti tiekėjo užklausą, kad ji būtų automatiškai pateikiama į darbo eigą, kai tiekėjo registravimo vedlys įvykdytas.

## <a name="vendor-requests"></a>Tiekėjo užklausos

Tiekėjo užklausas galima peržiūrėti puslapyje **Tiekėjo bendradarbiavimo vartotojo užklausos**.

Tiekėjo užklausos apima informaciją, kurią su galimu tiekėju susijęs vartotojas įveda tiekėjo registravimo vedlyje.

Užklausa suteikia galimybę peržiūrėti tiekėjo informaciją ir nuspręsti, ar tiekėjas turėtų tapti registruotu tiekėju „Finance and Operations“.

Tiekėjo užklausą reikia pateikti į darbo eigą ir nukreipti atitinkamiems tikrintojams ir tvirtintojams. Pagrindinės informacijos, kaip nustatyti darbo eigas, žr. [Paraiškų darbo eigos](procurement-sourcing-workflows.md).

Toliau pateikiamoje lentelėje parodomos galimos tiekėjo užklausų būsenos.

| Būsena                     | aprašymas |
|----------------------------|-------------|
| Juodraštis                      | Tiekėjo užklausa dar nepateikta. |
| Užklausa pateikta          | Tiekėjo užklausa pateikta ir pirmasis darbo eigos veiksmas apdorotas. |
| Laukiama peržiūra             | Jei yra darbo eigos užduotį atlieka keli tikrintojai, tikrintojas gali priimti tiekėjo užklausos tikrinimo užduotį ir atlikti tikrinimą. Jei yra tik vienas tikrintojas, tas dalyvis gali baigti tikrinimą darbo eigos veiksme pasirinkdamas **Baigta**. Jis neprivalo pirmiausia patvirtinti darbo elemento. |
| Užklausa, laukianti patvirtinimo   | Tiekėjo užklausa nukreipta dalyviams patvirtinti ir galima prašyti papildomos informacijos. Papildomos informacijos užklausa nukreipia darbo elementą atgal į teikėjui. Tiekėjo užklausą taip pat galima patvirtinti arba atmesti, kol ji yra šios būsenos. |
| Prašymo keitimo užklausa | Tvirtintojas paprašė papildomos informacijos ir tiekėjo užklausą buvo nukreipta asmeniui, kuris pateikė tiekėjo užklausą. Teikėjas gali įtraukti reikiamos informacijos ir pateikti tiekėjo užklausą iš naujo. Jei tiekėjo užklausa pateikta iš naujo, būsena pakeičiama būseną **Užklausa, laukianti patvirtinimo**. |
| Užklausa patvirtinta           | Ši būsena yra galutinė būsena. |
| Užklausa atmesta           | Ši būsena yra galutinė būsena. |

## <a name="approving-a-vendor-request"></a>Tiekėjo užklausos tvirtinimas

Patvirtinus tiekėjo užklausą, sukuriama tiekėjo paskyra ir būsena **Patvirtinta** rodoma tiek pradinėje galimo tiekėjo registravimo užklausoje, tiek tiekėjo užklausoje.

Prieš patvirtindami tiekėjo užklausą, puslapio **Naujo tiekėjas** „FastTab“ **Bendra** pasirinkite **Tiekėjų grupės**, kad pasirinktumėte tiekėjų grupę.

Jei su galimu tiekėju susijusiam vartotojui reikia priskirti prieigą prie „Finance and Operations“ kaip tiekėjo bendradarbiavimo vartotojui, kuris atstovauja tiekėją, nustatykite tiekėjo bendradarbiavimo prieigos teisę į parinktį **Taip**. Norėdami išjungti vartotojo paskyrą, kurią naudodamas galimas tiekėjas užsiregistravo, nustatykite šią teisę į parinktį **Ne**.

Jei tiekėjo bendradarbiavimo prieigos teisė nustatyta į parinktį **Taip**, kai tiekėjo užklausa patvirtinama, užklausa pateikiama modifikuoti vartotojo vaidmenis, kad vartotojui būtų priskirti vaidmenys, dalyje **Išoriniai vaidmenys** nurodyti kaip tipo **Tiekėja** vaidmenys. Jei ši teisė nustatyta į parinktį **Ne**, kai tiekėjo užklausa patvirtinama, užklausa pateikiama išjungtam vartotojui. Tokiu atveju reikia nustatyti vartotojo užklausos išjungimo darbo eigą.

Norint tiekėjo paskyrą kurti patvirtinus tiekėjo užklausą, tiekėjų kūrimo iš tiekėjų užklausų numeracija turi būti nustatyta į parinktį **Automatiškai**.

Tiekėjo bendradarbiavimo vartotojų prieigos teisių apžvalgą galite peržiūrėti [Tiekėjo bendradarbiavimo nustatymas ir tvarkymas](set-up-maintain-vendor-collaboration.md).

## <a name="rejecting-a-vendor-request"></a>Tiekėjo užklausos atmetimas

Atmetus tiekėjo užklausą, tiekėjo užklausoje turi būti pasirinkta atmetimo priežastis.

Atmetus tiekėjo užklausą, vartotojo užklausa pateikiama išjungtam vartotojui. Tokiu atveju reikia nustatyti vartotojo užklausos išjungimo darbo eigą. Daugiau informacijos žr. [Tiekėjo bendradarbiavimo nustatymas ir tvarkymas](set-up-maintain-vendor-collaboration.md).

Atmetus tiekėjo užklausą, būsena **Atmesta** rodoma tiek pradinėje galimo tiekėjo registravimo užklausoje, tiek tiekėjo užklausoje.

## <a name="deleting-a-prospective-vendor-registration-request-in-various-statuses"></a>Galimo tiekėjo registravimo užklausos naikinimas esant įvairioms būsenoms

Įvairios galimo tiekėjo registravimo užklausos būsenos suteikia užklausos patvirtinimo proceso apžvalgą.

Naudodami galimo tiekėjo registravimo užklausos veiksmą **Naikinti**, galite išvalyti ir pašalinti sukurtą įrašų tinklą ir išjungti vartotojo paskyrą. Veiksmo **Naikinti** rezultatas priklauso nuo galimo tiekėjo registravimo užklausos būsenos, kaip parodyta toliau pateiktoje lentelėje.


|          Būsena          |                                                                                     Būsenos aprašas                                                                                      |                                                                                                                                                            Veiksmo Naikinti rezultatas                                                                                                                                                             |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|           Naujas            |                                                                         Su užklausa nebuvo imtasi jokių veiksmų.                                                                          |                                                                                                                                              Galimo tiekėjo registravimo užklausa panaikinama.                                                                                                                                               |
|      Vartotojo užklausa pateikta      | Kai pasirenkate <strong>Kviesti vartotoją</strong>, būsena pakeičiama <strong>Vartotojo užklausa pateikta</strong> ir su galimu tiekėju susijusio vartotojo užklausa sukuriama bei pateikiama į vartotojo užklausos darbo eigą. |                                                                                                          Šios būsenos galimo tiekėjo registravimo užklausos naikinti negalima, nes vartotojo užklausos darbo eiga nebaigta.                                                                                                          |
|       Vartotojas pakviestas       |                                                               Vartotojo užklausos darbo eiga patvirtinama ir sukuriamas vartotojas.                                                               |                                                                                                                      Sukuriama užklausa išjungti vartotoją ir galimo tiekėjo registravimo užklausa panaikinama.                                                                                                                      |
| Vykdoma registracija |                                                         Naujas vartotojas yra prisijungė ir pradėjo tiekėjo registravimo vedlį.                                                          |                                                                                     Sukuriama užklausa išjungti vartotoją ir galimo tiekėjo registravimo užklausa bei tiekėjo registravimo vedlyje įvesti duomenys panaikinami.                                                                                      |
|  Tiekėjo užklausa sukurta  |                                                                     Tiekėjo registravimo vedlys baigtas.                                                                      | Sukuriama užklausa išjungti vartotoją ir galimo tiekėjo registravimo užklausa, tiekėjo registravimo vedlyje įvesti duomenys bei tiekėjo užklausa panaikinami.<blockquote>[!NOTE]<br>Negalima naudoti veiksmo <strong>Naikinti</strong>, kai vykdomas tiekėjo užklausos darbo eigos tikrinimo procesas.</blockquote> |
|         Aprobuota         |                                                                               Tiekėjo užklausa patvirtinama.                                                                               |                                                                                                   Galimo tiekėjo registravimo užklausa, tiekėjo registravimo vedlyje įvesti duomenys ir tiekėjo užklausa panaikinami.                                                                                                    |
|         Atmestas         |                                                                               Tiekėjo užklausa atmetama.                                                                               |                                                                                                   Galimo tiekėjo registravimo užklausa, tiekėjo registravimo vedlyje įvesti duomenys ir tiekėjo užklausa panaikinami.                                                                                                    |


