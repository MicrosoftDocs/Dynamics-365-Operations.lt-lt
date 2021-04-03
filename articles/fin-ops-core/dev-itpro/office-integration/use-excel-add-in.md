---
title: Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“
description: Šioje temoje paaiškinama, kaip programoje „Microsoft Excel“ atidaryti objektų duomenis ir naudojant „Microsoft Dynamics“ „Excel“ papildinį peržiūrėti, atnaujinti ir redaguoti šiuos duomenis.
author: jasongre
manager: AnnBe
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7da9867ed86921f3487077081ec63e8b44e92c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562554"
---
# <a name="view-and-update-entity-data-with-excel"></a>Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“ 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip programoje „Microsoft Excel“ atidaryti objektų duomenis ir naudojant „Microsoft Dynamics“ „Excel“ papildinį peržiūrėti, atnaujinti ir redaguoti šiuos duomenis. Norėdami atidaryti objekto duomenis, galite juos atidaryti iš „Excel“ arba „Finance and Operations“ programų.

Kai programoje „Excel“ atidarysite objektų duomenis, naudodami „Excel“ papildinį galėsite greitai ir paprastai peržiūrėti bei redaguoti šiuos duomenis. Norint įdiegti šį papildinį, būtina naudoti 2016 m. ar vėlesnių versijų „Microsoft Excel“.

> [!NOTE]
> Jei „Microsoft Azure Active Directory“ („Azure AD“) nuomotojas bus sukonfigūruotas naudoti „Active Directory“ susiejimo tarnybą (AD FS), būtinai turi būti įdiegtas 2016 m. gegužės mėn. „Office“ skirtas naujinimas – tuomet naudojant „Excel“ papildinį bus galima tinkamai jus prijungti.

Norėdami daugiau sužinoti, kaip naudotis „Excel“ papildiniu, peržiūrėkite trumpą vaizdo įrašą [„Excel” šablono kūrimas antraštėms ir linijų šablonams](https://youtu.be/RTicLb-6dbI).

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Paleidus „Finance and Operations“ programą, atidarykite objekto duomenis „Excel“ programoje
1. „Finance and Operations“ programos puslapyje pasirinkite **Atidaryti programoje „Microsoft Office“**.

    Jei puslapio šakninis duomenų šaltinis (lentelė) sutaps su bet kurių objektų šakniniu duomenų šaltiniu, puslapyje bus sukuriamos numatytosios parinktys **Atidaryti naudojant „Excel“**. Parinktis **Atidaryti naudojant „Excel“** galima rasti dažnai naudojamuose puslapiuose, pvz., **Visi tiekėjai** ir **Visi klientai**.
 
2. Pasirinkite parinktį **Atidaryti naudojant „Excel“** ir atidarykite sukurtą darbaknygę. Šioje darbaknygėje pateikiama su objektu susijusi informacija, aplinkos žymiklis ir „Excel“ papildinio žymiklis.
3. Programoje „Excel“ pasirinkite **Įjungti redagavimą**, kad įjungtumėte „Excel“ papildinį. „Excel“ papildinys paleidžiamas dešinėje „Excel“ lango pusėje esančioje srityje.
4. Jei „Excel“ papildinį paleisite pirmą kartą, pasirinkite **Pasitikėti šiuo papildiniu**.
5. Jei pasirodė langas, reikalaujantis prisijungti, pasirinkite **Prisijungti**, tada prisijunkite naudodami tuos pačius kredencialus, kuriuos naudojote jungdamiesi prie „Finance and Operations“ programos. „Excel“ papildinys naudos ankstesnį prisijungimo kontekstą iš naršyklės, ir esant galimybei, automatiškai jus prijungs. (Daugiau informacijos apie naršyklę, naudojamą remiantis operacine sistema, žr. [„Office” papildinių naudojamos naršyklės](https://docs.microsoft.com/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins.) Norėdami užtikrinti, kad sėkmingai prisijungėte, viršutiniame dešiniajame „Excel” papildinio kampe patikrinkite vartotojo vardą. 

Naudojant „Excel“ papildinį automatiškai nuskaitomi pasirinkto objekto duomenys. Atminkite, kad darbaknygėje duomenys bus pateikiami tik „Excel“ papildiniui juos nuskaičius.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Kaip paleidus „Excel“ atidaryti objektų duomenis programoje „Excel“
1. „Excel“ skirtuko **Įterpti** grupėje **Papildiniai** pasirinkę **Parduotuvė** atidarykite „Office“ parduotuvę.
2. „Office“ parduotuvėje ieškokite raktažodžio **Dynamics**, tada prie **„Microsoft Dynamics Office“ papildinio** („Excel“ papildinys) pasirinkite **Įtraukti**.
3. Jei „Excel“ papildinį paleisite pirmą kartą, pasirinkę **Pasitikėti šiuo papildiniu** jį įjunkite. „Excel“ papildinys paleidžiamas dešinėje „Excel“ lango pusėje esančioje srityje.
4. Pasirinkite **Įtraukti serverio informaciją**, kad atidarytumėte sritį **Parinktys**.
5. Naršyklėje nukopijuokite „Finance and Operations“ programos URL, jį įklijuokite į lauką **Serverio URL**, tada panaikinkite visą po pagrindinio kompiuterio pavadinimo esantį tekstą. Gautame URL turi likti tik pagrindinio kompiuterio vardas.

    Pavyzdžiui, jei URL yra `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage`, panaikinkite viską, išskyrus `https://xxx.dynamics.com`.

6. Pasirinkite **Gerai**, tada pasirinkite **Taip**, kad patvirtintumėte pakeitimą. „Excel“ papildinys paleidžiamas iš naujo ir įkeliami metaduomenys.

    Jau galima naudoti mygtuką **Dizainas**. Jei „Excel“ papildinyje yra mygtukas **Įkelti programėles**, tikriausiai neprisijungėte kaip tinkamas vartotojas. Jei reikia daugiau informacijos, žr. šios temos skyriaus [Trikčių diagnostika](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) dalį „Rodomas mygtukas Įkelti programėles“.

7. Pasirinkite **Dizainas**. Naudojant „Excel“ papildinį gaunami objektų metaduomenys.
8. Pasirinkite **Įtraukti lentelę**. Pateikiamas objektų sąrašas. Jame objektai nurodomi „Pavadinimas – žyma“ formatu.
9. Sąraše pasirinkite objektą, pvz., **Klientas – klientai**, tada pasirinkite **Pirmyn**.
10. Norėdami į sąrašą **Pasirinkti laukai** įtraukti sąrašo **Galimi laukai** lauką, pasirinkite lauką, tada pasirinkite **Įtraukti**. Taip pat galite du kartus spustelėti sąraše **Galimi laukai** pateikiamą lauką.
11. Įtraukę laukus į sąrašą **Pasirinkti laukai** įsitikinkite, kad žymiklis yra tinkamoje darbalapio vietoje (pavyzdžiui, A1 langelyje), tada pasirinkite **Atlikta**. Tada pasirinkite **Atlikta**, kad išeitumėte iš dizaino įrankio.
12. Pasirinkite **Atnaujinti**, kad būtų nuskaitytas duomenų rinkinys.

## <a name="view-and-update-entity-data-in-excel"></a>Kaip peržiūrėti ir atnaujinti objektų duomenis programoje „Excel“
Kai naudojant „Excel“ papildinį bus nuskaityti ir darbaknygėje pateikti objektų duomenys, bet kada galėsite juos atnaujinti „Excel“ papildinyje pasirinkdami **Atnaujinti**.

## <a name="edit-entity-data-in-excel"></a>Kaip redaguoti objektų duomenis programoje „Excel“
Pagal poreikius galite keisti objektų duomenis, tada juos galite vėl publikuoti Finance and Operations programose pasirinkdami **Skelbti** „Excel” papildinyje. Norėdami redaguoti įrašą, darbalapyje pasirinkite langelį, tada pakeiskite langelio reikšmę. Norėdami įtraukti naują įrašą, atlikite vieną iš toliau nurodytų veiksmų.

- Spustelėkite bet kurioje duomenų šaltinio lentelės vietoje, tada „Excel“ papildinyje pasirinkite **Naujas**.
- Spustelėkite bet kur paskutinėje duomenų šaltinio lentelės eilutėje, tada spauskite klavišą „Tab“, kol žymiklio nebebus paskutiniame šios eilutės stulpelyje ir bus sukurta nauja eilutė.
- Spustelėkite bet kur po pat duomenų šaltinio lentele esančioje eilutėse ir langelyje pradėkite įvesti duomenis. Kai šiame langelyje nustosite įvesti tekstą ir žymiklį perkelsite į kitą įvesties vietą, lentelė bus išplėsta ir bus įtraukta nauja eilutė.
- Susiedami antraštės įrašų laukus, pasirinkite vieną iš laukų, o tada „Excel“ papildinyje pasirinkite **Naujas**.

Atkreipkite dėmesį, kad naują įrašą galima kurti tik jei visi pagrindiniai ir privalomi laukai yra susieti darbalapyje arba jei numatytosios vertės buvo įvestos naudojant filtro sąlygą.

Norėdami panaikinti įrašą, atlikite vieną iš toliau nurodytų veiksmų.

- Dešiniuoju pelės mygtuku spustelėkite eilutės numerį, esantį prie naikintinos darbalapio eilutės, tada pasirinkite **Naikinti**.
- Dešiniuoju pelės mygtuku spustelėkite bet kur naikintinoje darbalapio eilutėje, tada pasirinkite **Naikinti** &gt; **Lentelės eilutės**.

Jei duomenų šaltiniai buvo įtraukti kaip susiję duomenų šaltiniai, antraštė publikuojama prieš eilutes. Jei yra nustatyta priklausomybė tarp kitų duomenų šaltinių, gali tekti pakeisti numatytąją publikavimo tvarką. Norėdami pakeisti publikavimo tvarką, „Excel“ papildinyje pasirinkite mygtuką **Pasirinktys** (krumpliaračio simbolis), tada **Duomenų jungties** „FastTab“ pasirinkite **Konfigūruoti publikavimo tvarką**.

## <a name="add-or-remove-columns"></a>Įtraukti arba pašalinti stulpelius
Naudodami dizaino įrankį galite koreguoti automatiškai į darbalapį įtraukiamus stulpelius.

> [!NOTE]
> Jei „Excel“ papildinyje po mygtuku **Filtras** nepasirodo mygtukas **Dizainas**, turite įgalinti duomenų šaltinio dizaino įrankį. Pasirinkite mygtuką **Pasirinktys** (krumpliaračio simbolis), tada pasirinkite žymės langelį **Įgalinti dizainą**.

1. „Excel“ papildinyje pasirinkite **Dizainas**. Pateikiami visi duomenų šaltiniai.
2. Prie duomenų šaltinio pasirinkite mygtuką **Redaguoti** (pieštuko simbolis).
3. Sąraše **Pasirinkti laukai** pagal poreikius pakoreguokite laukų sąrašą:

    - Norėdami į sąrašą **Pasirinkti laukai** įtraukti sąrašo **Galimi laukai** lauką, pasirinkite lauką, tada pasirinkite **Įtraukti**. Taip pat galite du kartus spustelėti sąraše **Galimi laukai** pateikiamą lauką.
    - Norėdami sąraše **Pasirinkti laukai** pašalinti lauką, pasirinkite šį lauką, tada pasirinkite **Šalinti**. Galite ir dukart spustelėti lauką.
    - Norėdami keisti laukų tvarką, sąraše **Pasirinkti laukai** pasirinkite lauką, tada pasirinkite **Aukštyn** arba **Žemyn**.

4. Norėdami pritaikyti duomenų šaltinio keitimus, pasirinkite **Naujinti**. Tada pasirinkite **Atlikta**, kad išeitumėte iš dizaino įrankio.
5. Jei įtraukėte lauką (stulpelį), pasirinkite **Atnaujinti**, kad būtų nuskaitytas atnaujintas duomenų rinkinys.

## <a name="change-the-publish-batch-size"></a>Publikavimo paketo dydžio keitimas
Kai vartotojai paskelbia duomenų įrašų pakeitimus naudodami „Excel” papildinį, naujinimai pateikiami paketais. Numatytasis publikavimo paketo dydis yra 100 eilučių. 10.0.17 ir vėlesnėse versijose funkcija **Leisti konfigūruoti skelbiamo paketo dydį „Excel” papildinyje** leidžia lanksčiai reguliuoti skelbiamo paketo dydį.

Sistemos administratoriai gali nurodyti sistemoje taikomą skelbiamo paketo dydžio limitą „Atidaryti „Excel” darbaknygėse nustatydami lauką **Skelbiamo paketo limitas** **Programos parametrai** dalyje **„Office” programų parametrai** puslapyje.

Naudodami „Excel” papildinį, skelbiamo paketo dydį taip pat galite keisti atskiroje darbaknygėje.

1. Atidarykite darbaknygę programoje „Excel”.
2. Viršutiniame „Excel” papildinio dešiniajame puslapio kampe pasirinkite (krumpliaračio) mygtuką **Parinktis**.
3. Nustatykite norimą **Skelbiamo paketo dydis** lauką. Jūsų nustatyta vertė turi būti mažesnė nei visos sistemos publikuotas paketo limitas.
4. Pasirinkite **Gerai**.
5. Įrašykite darbaknygę. Jei atlikę papildinio nustatymų pakeitimus, darbaknygės neįrašote, šie pakeitimai neišsaugomi darbaknygę atidarius iš naujo.

„Excel” darbaknygės šablonų autoriai gali naudoti tą pačią procedūrą, kad nustatytų šablonų skelbiamo paketo dydį prieš juos įkeliant į sistemą.

## <a name="copy-environment-data"></a>Kopijuoti aplinkos duomenis

Į darbaknygę nuskaitomus duomenis iš vienos aplinkos galima nukopijuoti į kitą. Tačiau negalite tiesiog pakeisti ryšio URL, nes darbaknygėje esanti duomenų talpykla duomenis toliau laikys esamais. Vietoj to turite naudoti funkciją Kopijuoti aplinkos duomenis, kad duomenis naujoje aplinkoje galėtumėte paskelbti kaip naujus.

1. Pasirinkite mygtuką **Pasirinktys** (krumpliaračio simbolis), tada **Duomenų jungties** „FastTab“ pasirinkite **Kopijuoti aplinkos duomenis**. 
2. Įveskite naujos aplinkos serverio URL. 
3. Pasirinkite **Gerai**, tada pasirinkite **Taip**, kad patvirtintumėte veiksmą. „Excel“ papildinys paleidžiamas iš naujo ir prisijungia prie naujos aplinkos. Visi darbaknygėje esantys duomenys yra laikomi naujais.

    „Excel“ papildinį paleidus iš naujo, pranešimų lauke nurodoma, kad darbaknygė veikia aplinkos kopijavimo režimu.

4. Norėdami duomenis į naują aplinką nukopijuoti kaip naujus, pasirinkite **Publikuoti**. Norėdami atšaukti aplinkos kopijavimo operaciją ir peržiūrėti naujoje aplinkoje esamus duomenis, pasirinkite **Atnaujinti**.

## <a name="troubleshooting"></a>Trikčių šalinimas
Kelias triktis galima pašalinti atlikus paprastus veiksmus.

- **Rodomas mygtukas Įkelti programėles** – jei prisijungus „Excel“ papildinyje yra mygtukas **Įkelti programėles**, tikriausiai neprisijungėte kaip tinkamas vartotojas. Norėdami išspręsti šią problemą, patikrinkite, ar viršutiniame dešiniajame „Excel“ papildinio kampe pateikiamas teisingas vartotojo vardas. Jei pateikiamas neteisingas vartotojo vardas, jį pasirinkite, atsijunkite, tada prisijunkite iš naujo.
- **Gaunate pranešimą „Uždrausta“** – jei „Excel“ papildiniui įkeliant metaduomenis gausite pranešimą „Uždrausta“, paskyrai, kurios duomenis naudojant yra prisijungta prie „Excel“ papildinio, nesuteiktos teisės naudoti paskirties paslaugą, egzempliorių ar duomenų bazę. Norėdami išspręsti šią problemą, patikrinkite, ar viršutiniame dešiniajame „Excel“ papildinio kampe pateikiamas teisingas vartotojo vardas. Jei pateikiamas neteisingas vartotojo vardas, jį pasirinkite, atsijunkite, tada prisijunkite iš naujo.
- **Programoje „Excel“ pateikiamas tuščias tinklalapis** – jei per prisijungimo procesą atidaromas tuščias tinklalapis, paskyroje būtinai turi būti naudojama AD FS, tačiau įdiegta nepakankamai nauja papildinį paleidžianti „Excel“ versija ir prisijungimo dialogo langas neįkeliamas. Norėdami pašalinti šią triktį, atnaujinkite naudojamą „Excel“ versiją. Norėdami atnaujinti „Excel“ versiją įmonėje, kurioje naudojamas atidėtų naujinimų kanalas, naudodami [„Office“ diegimo įrankį](https://technet.microsoft.com/library/jj219422.aspx) [pakeiskite atidėtų naujinimų kanalą į dabartinių naujinimų kanalą](https://technet.microsoft.com/library/mt455210.aspx).
- **Gausite pranešimą apie pasibaigusį skirtą laiką, kol paskelbsite duomenų pakeitimus** – jei gaunate pranešimus apie pasibaigusį skirtą laiką, kol bandote paskelbti objekto duomenų pakeitimus, pabandykite sumažinti paveiktos darbaknygės skelbiamo paketo dydį. Objektai, kurių įrašų pakeitimų atlikimas yra sudėtingesnis, jų pakeitimus reikia siųsti mažesniais paketais, kad išvengtumėte pranešimų apie pasibaigusį skirtąjį laiką.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]