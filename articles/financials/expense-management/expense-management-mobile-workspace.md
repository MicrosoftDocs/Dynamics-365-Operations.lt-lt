---
title: "Mobilioji darbo sritis Išlaidų valdymas"
description: "Šioje temoje pateikiama informacija apie mobiliąją darbo sritį Išlaidų valdymas. Ši darbo sritis vartotojams suteikia galimybę fiksuoti ir įkelti kvitą, kad jie galėtų jį pridėti prie išlaidų ataskaitos vėliau. Be to, vartotojai gali greitai kurti išlaidų eilutę naudodami pridėtą kvitą ir kurti bei valdyti savo išlaidų ataskaitas."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 7ce4c9d13a8686c82af8acad39d68858e52ba520
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="expense-management-mobile-workspace"></a>Išlaidų valdymo mobilioji darbo sritis

[!include[banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie mobiliąją darbo sritį **Išlaidų valdymas**. Ši darbo sritis vartotojams suteikia galimybę fiksuoti ir įkelti kvitą, kad jie galėtų jį pridėti prie išlaidų ataskaitos vėliau. Be to, vartotojai gali greitai kurti išlaidų eilutę naudodami pridėtą kvitą ir kurti bei valdyti savo išlaidų ataskaitas. Be to, mobiliąją darbo sritį **Išlaidų valdymas** tvirtintojai gali naudoti norėdami peržiūrėti jiems priskirtas išlaidų ataskaitas ir jas tvirtinti arba atmesti.


Ši mobilioji darbo sritis skirta naudoti kartu su mobiliąja programa „Microsoft Dynamics 365 for Unified Operations“.


## <a name="overview"></a>Apžvalga

Daugelis organizacijų reikalauja, kad prie kompensacijai gauti darbuotojo pateikiamos išlaidų ataskaitos būtų pridėta su kelionėmis arba verslu susijusio kvito kopija. Mobilioji darbo sritis **Išlaidų valdymas** vartotojams suteikia galimybę greitai kurti naujas išlaidų eilutes pasirinktame mobiliajame įrenginyje naudojant pridėtą kvito nuotrauką. Taip pat vartotojai gali nufotografuoti kvitą ir kopiją pridėti prie išlaidų ataskaitos vėliau. Darbuotojai taip pat gali kurti bei valdyti savo išlaidų ataskaitas ir tada pateikti jas patvirtinti bei kompensacijai gauti naudojant savo mobilųjį įrenginį.


Tiksliau sakant, naudodami mobiliąją darbo sritį **Įmonės katalogas** vartotojai gali atlikti toliau nurodytas užduotis.

- Nufotografuoti kvitą ir tada nuotrauką įkelti į „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą. Tada tą nuotrauką pridėti prie išlaidų ataskaitos vėliau.
- Įkelkite failą kaip kvito nuotrauką. Tada tą failą pridėti prie išlaidų ataskaitos vėliau.
- Sukurkite naują išlaidų eilutę naudodami pridėtą kvitą. Tada eilutės elementą galima pridėti prie išlaidų ataskaitos vėliau ir pateikti ją patvirtinti bei kompensacijai gauti.

Jei naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), taip pat galite naudoti toliau nurodytas funkcijas.

- Kurti naują išlaidų ataskaitą.
- Pridėti kredito kortelės operacijas ir kitais anksčiau sukurtas išlaidas prie išlaidų ataskaitos.
- Kurti naujas išlaidų ataskaitos išlaidas.
- Pridėti kvitą prie išlaidų ataskaitos išlaidų nufotografuojant kvitą arba nusiunčiant failą kaip kvito nuotrauką.
- Atsižvelgiant į įmonės išlaidų strategiją, prie išlaidų pridėti svečių sąrašą.
- Atsižvelgiant į įmonės išlaidų strategiją, išvardyti išlaidas.
- Pateikti išlaidų ataskaitą patvirtinti ir kompensacijai gauti.
- Patvirtinti arba atmesti išlaidų ataskaitas, kurių priskirtasis tvirtintojas esate.

## <a name="prerequisites"></a>Būtinieji komponentai
Būtinosios sąlygos skiriasi priklausomai nuo jūsų organizacijoje visuotinai įdiegtos „Microsoft Dynamics 365“ versijos.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Būtinosios sąlygos, jeigu naudojate „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) 
Jei jūsų organizacijoje visuotinai įdiegtas „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), sistemos administratorius turi publikuoti mobiliąją darbo sritį **Išlaidų valdymas**. Instrukcijų ieškokite dalyje [Mobiliosios darbo srities publikavimas](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojate „Microsoft Dynamics 365 for Operations“ 1611 versiją su 3 platformos naujinimu arba naujesnę versiją
Jei jūsų organizacijoje visuotinai įdiegta „Microsoft Dynamics 365 for Operations‟ 1611 versija su 3 platformos naujinimu arba naujesnė versija, sistemos administratorius turi įvykdyti tolesnes būtinąsias sąlygas. 

<table>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Vaidmuo</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Įdiegti KB 4019015.</td>
<td>Sistemos administratorius</td>
<td>KB 4019015 yra X++ atnaujinimas arba metaduomenų karštoji pataisa, kurioje yra mobilioji darbo sritis <strong>Išlaidų valdymas</strong>. Norėdamas įdiegti KB 4019015, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Atsisiųsti metaduomenų karštąsias pataisas iš „Microsoft Dynamics Lifecycle Services“ (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Sukurkite diegiamą paketą</a>, kuriame yra modeliai <strong>ApplicationSuite</strong> ir <strong>ExpenseMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Visuotinai diegiamo paketo taikymas</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publikuokite mobiliąją darbo sritį <strong>Išlaidų valdymas</strong>.</td>
<td>Sistemos administratorius</td>
<td>Žr. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiliosios darbo srities publikavimas</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Mobiliosios programos „Dynamics 365 for Operations“ atsisiuntimas ir diegimas
Atsisiųskite ir įdiekite mobiliąją programą „Dynamics 365 for Unified Operations“:

- [„Android“ telefonams](https://go.microsoft.com/fwlink/?linkid=850662)
- [„iPhone“ telefonams](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prisijunkite prie mobiliosios programos
1. Paleiskite programą savo mobiliajame įrenginyje.
2. Įveskite savo „Dynamics 365“ URL.
4. Kai prisijungsite pirmą kartą, bus rodomas raginimas įvesti savo vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
5. Prisijungus rodomos galimos jūsų įmonės darbo sritys. Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau turėsite atnaujinti mobiliųjų darbo sričių sąrašą.


[![Patraukite norėdami atnaujinti](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Kvito kopijos kūrimas naudojant mobiliąją darbo sritį Išlaidų valdymas

1. Savo mobiliajame įrenginyje atidarykite darbo sritį **Išlaidų valdymas**.
2. Pasirinkite **Kvito kopija**.
3. Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
4. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei pasirinkote **Fotografuoti**, atlikite tolesnius veiksmus.

        1. Atidaromas jūsų mobiliojo įrenginio fotoaparatas, kad galėtumėte nufotografuoti kvitą. Nufotografavę pasirinkite **Gerai**, kad nuotrauką priimtumėte.
        2. Pasirinktinai: įveskite nuotraukos pavadinimą ir bet kokias pastabas.

    - Jei pasirinkote **Pasirinkti vaizdą**, atlikite tolesnius veiksmus.

        1. Sąraše pasirinkite vaizdą.
        2. Pasirinktinai: įveskite vaizdo pavadinimą ir bet kokias pastabas.

5. Pasirinkite **Atlikta**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Greitas išlaidų įvedimas naudojant mobiliąją darbo sritį Išlaidų valdymas
1. Savo mobiliajame įrenginyje atidarykite darbo sritį **Išlaidų valdymas**.
2. Pasirinkite **Greitas išlaidų įrašas**.
3. Pasirinkite išlaidų kategoriją. Matysite išlaidų kategorijų, kurios įkeltos į jūsų programą ir kurias galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jei jūsų kategorijos sąraše nėra, pasirinkite **Ieškoti**, kad atliktumėte iešką internete. Ieškokite pagal išlaidų kategoriją arba perjunkite iešką pagal išlaidų tipą.
4. Įveskite išlaidų operacijos datą.
5. Pasirinktinai: įveskite išlaidų prekybininką.
6. Įveskite išlaidų sumą.
7. Pasirinkite išlaidų valiutą. Matysite išlaidų kodų, kurie įkelti į jūsų programą ir kuriuos galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 400 valiutų, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jei jūsų valiutos sąraše nėra, pasirinkite **Ieškoti**, kad atliktumėte iešką internete. Ieškokite pagal valiutą arba perjunkite iešką pagal pavadinimą.
8. Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
9. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei pasirinkote **Fotografuoti**, atidaromas jūsų mobiliojo įrenginio fotoaparatas, kad galėtumėte nufotografuoti kvitą. Nufotografavę pasirinkite **Gerai**, kad nuotrauką priimtumėte.
    - Jei pasirinkote **Pasirinkti vaizdą**, sąraše pasirinkite vaizdą.

10. Pasirinkite **Atlikta**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Išlaidų ataskaitos tvirtinimas naudojant mobiliąją darbo sritį Išlaidų valdymas (jei naudojamas 2017 m. liepos mėn. naujinimas)
1. Savo mobiliajame įrenginyje atidarykite darbo sritį **Išlaidų valdymas**.
2. **Išlaidų patvirtinimai** rodo jums priskirtų patvirtinti išlaidų ataskaitų skaičių. Šis skaičius atnaujinamas maždaug kas 30 minučių. Pasirinkite **Išlaidų patvirtinimai**.

    Rodomas jums priskirtų patvirtinti išlaidų ataskaitų sąrašas.
    
3. Pasirinkite išlaidų ataskaitą norėdami peržiūrėti jos išlaidų informaciją.
4. Pasirinkite išlaidas norėdami peržiūrėti jų informaciją. Rodoma išlaidų informacija apima visą kvitų, svečių ir išvardijimo informaciją.
5. Vėl atidarę puslapį **Išlaidų ataskaita** pasirinkite patvirtinti arba atmesti išlaidų ataskaitą.
6. Įvesti tvirtinimo veiksmo komentarus.
7. Pasirinkite **Atlikta**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Naujos išlaidų ataskaitos kūrimas ir jos teikimas patvirtinti naudojant mobiliąją darbo sritį Išlaidų valdymas (jei naudojamas 2017 m. liepos mėn. naujinimas)
1. Savo mobiliajame įrenginyje atidarykite darbo sritį **Išlaidų valdymas**.
2. Pasirinkite **Išlaidų įrašas**.
3. Pasirinkite **Nauja ataskaita** arba sąraše pasirinkite esamą išlaidų ataskaitą.
4. Pasirinkę kurti naują išlaidų ataskaitą, įveskite paskirtį ir bet kokią turimą papildomą informaciją. Ši informacija priklauso nuo to, kaip sukonfigūruotas jūsų įmonės išlaidų valdymas.
5. Pasirinkite **Atlikta**.
6. Norėdami įtraukti esamas išlaidas, pvz., kredito kortelės operacijas, į išlaidų ataskaitą, pasirinkite **Įtraukti**.
7. Sąraše pasirinkite vieną arba kelias išlaidas.
8. Pasirinkite **Atlikta**.
9. Norėdami į išlaidų ataskaitą įtraukti naujas išlaidas, pasirinkite **Naujos išlaidos**.
10. Pasirinkite išlaidų kategoriją. Matysite išlaidų kategorijų, kurios įkeltos į jūsų programą ir kurias galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jei jūsų kategorijos sąraše nėra, pasirinkite **Ieškoti**, kad atliktumėte iešką internete. Ieškokite pagal išlaidų kategoriją arba perjunkite iešką pagal išlaidų tipą.
11. Pasirinktinai: įveskite išlaidų prekybininką.
12. Įveskite išlaidų operacijos datą.
13. Įveskite išlaidų sumą.
14. Pasirinkite išlaidų valiutą. Matysite išlaidų kodų, kurie įkelti į jūsų programą ir kuriuos galima tvarkyti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 400 valiutų, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jei jūsų valiutos sąraše nėra, pasirinkite **Ieškoti**, kad atliktumėte iešką internete. Ieškokite pagal valiutą arba perjunkite iešką pagal pavadinimą.
15. Pasirinkite **Atlikta**.
16. Norėdami į išlaidas įtraukti daugiau informacijos, pasirinkite **Įtraukti daugiau informacijos**. Redaguojami laukai priklauso nuo jūsų įmonės išlaidų valdymo konfigūracijos.
17. Jei įmonės strategija nurodo, kad reikalingas išlaidų kvitas, pasirinkite **Kvitai** ir tada atlikite tolesnius veiksmus.

    1. Pasirinkite **Fotografuoti kvitą** arba **Pridėti kvitą**.
    2. Atlikite vieną iš toliau nurodytų veiksmų.

        - Jei pasirinkote **Fotografuoti kvitą**, atlikite tolesnius veiksmus.

            1. Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
            2. Atlikite vieną iš toliau nurodytų veiksmų.

                - Jei pasirinkote **Fotografuoti**, atlikite tolesnius veiksmus.

                    1. Atidaromas jūsų mobiliojo įrenginio fotoaparatas, kad galėtumėte nufotografuoti kvitą. Nufotografavę pasirinkite **Gerai**, kad nuotrauką priimtumėte.
                    2. Pasirinktinai: įveskite nuotraukos pavadinimą ir bet kokias pastabas.

                - Jei pasirinkote **Pasirinkti vaizdą**, atlikite tolesnius veiksmus.

                    1. Sąraše pasirinkite vaizdą.
                    2. Pasirinktinai: įveskite vaizdo pavadinimą ir bet kokias pastabas.

            3.  Pasirinkite **Atlikta**.

        - Jei pasirinkote **Pridėti kvitą**, atlikite tolesnius veiksmus.

            1.  Sąraše pasirinkite vieną arba kelis vaizdus.
            2.  Pasirinkite **Atlikta**.

    3. Norėdami vėl atidaryti išlaidų informaciją, pasirinkite mygtuką **Atgal**.

18. Jei įmonės strategija nurodo, kad reikalingi išlaidų svečiai, pasirinkite **Svečiai** ir tada atlikite tolesnius veiksmus.

    1. Pasirinkite **Svečias**, **Ankstesni svečiai** arba **Bendradarbiai**.
    2. Atlikite vieną iš toliau nurodytų veiksmų.

        - Jei pasirinkote **Svečias**, atlikite tolesnius veiksmus.

            1. Įveskite svečio vardą bei pavardę.
            2. Pasirinktinai: įveskite svečio organizaciją ir (arba) šalį.
            3. Pasirinktinai: įveskite svečio pareigas.
            4. Pasirinkite **Atlikta**.

        - Jei pasirinkote **Ankstesni svečiai**, atlikite tolesnius veiksmus.

            1. Sąraše pasirinkite vieną arba kelis ankstesnius svečius. Matysite ankstesnių svečių, įtrauktų į jūsų ankstesnes išlaidų ataskaitas, kurios įkeltos į programą naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jei jūsų ankstesnio svečio sąraše nėra, pasirinkite **Ieškoti**, kad atliktumėte iešką internete. Ieškokite pagal vardą ir pavardę arba perjunkite iešką pagal organizaciją, šalį ar pareigas.
            2. Pasirinkite **Atlikta**.

        - Jei pasirinkote **Bendradarbiai**, atlikite tolesnius veiksmus.

            1. Sąraše pasirinkite vieną arba kelis bendradarbius. Matysite bendradarbių, kurie įkelti į jūsų programą naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jei jūsų bendradarbio sąraše nėra, pasirinkite **Ieškoti**, kad atliktumėte iešką internete. Ieškokite pagal vardą ir pavardę arba perjunkite iešką pagal įmonę ar pareigas.
            2. Pasirinkite **Atlikta**.

    3. Norėdami vėl atidaryti išlaidų informaciją, pasirinkite mygtuką **Atgal**.

19. Jei įmonės strategija nurodo, kad išlaidas būtina išvardyti, pasirinkite **Išvardyti** ir tada atlikite tolesnius veiksmus.

    1. Pasirinkite pirmą išvardijimo datą.
    2. Pasirinkite **Įtraukti išvardijimą**.
    3. Pasirinkite antrinę išlaidų išvardijimo kategoriją. Matysite antrinių išlaidų kategorijų, kurios įkeltos į jūsų programą naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 prekių, tačiau kūrėjas šį skaičių gali keisti. Norėdami gauti daugiau informacijos, programuotojai turėtų peržiūrėti temą [Mobilioji platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Jei jūsų antrinės kategorijos sąraše nėra, pasirinkite **Ieškoti**, kad atliktumėte iešką internete. Ieškokite pagal antrinės išlaidų kategorijos pavadinimą.
    4. Įveskite išvardijimo operacijos sumą.
    5. Redaguokite operacijos datą, jei reikia.
    6. Pasirinkite **Atlikta**.
    7. Kartokite ankstesnius veiksmus, kol įtrauksite visus pasirinktos datos išvardijimus.
    8. Jei norite pridėti papildomų dienų, galite pasirinkti **Kopijuoti į kitą dieną**, kad išvardijimus nukopijuotumėte į kitą dieną. Taip pat galite pasirinkti išvardijimo datą ir tada įtraukti išvardijimus, kaip tai padarėte atlikdami pirmosios datos veiksmus.
    9. Baigę išlaidų išvardijimą pasirinkite mygtuką **Atgal**, kad vėl atidarytumėte išlaidų informaciją.

20. Norėdami vėl atidaryti puslapį **Išlaidų ataskaita**, pasirinkite mygtuką **Atgal**.
21. Kartokite ankstesnius veiksmus, kol įtrauksite visas išlaidas.
22. Pasirinkite **Pateikti**.
23. Įveskite tvirtintojo komentarus.
24. Pasirinkite **Atlikta**.

