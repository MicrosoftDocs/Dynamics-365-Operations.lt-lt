---
title: Operacijų planavimo parinktys
description: Šioje temoje aprašomos operacijų planavimo parinktys. Galite naudoti operacijų planavimą, norėdami bendrai įvertinti gamybos procesą per tam tikrą laikotarpį.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f042b5d2b06d6dc880195a3c0c7bb62e41b1d006
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011102"
---
# <a name="operations-scheduling-options"></a>Operacijų planavimo parinktys

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos operacijų planavimo parinktys. Galite naudoti operacijų planavimą, norėdami bendrai įvertinti gamybos procesą per tam tikrą laikotarpį.

Operacijų planavimo metu apskaičiuojama toliau nurodyta gamybos užsakymo informacija.

-   Nustatomos gamybos užsakymo ir kiekvienos operacijos pradžios ir pabaigos datos.
-   Ištekliai priskiriami operacijoms.

Keli parametrai nustato, kaip skaičiuojamas gamybos planavimas. Šiuos parametrus galite nustatyti puslapyje **Operacijų planavimas**. Toliau apibūdinamos planavimo pasirinktys.

## <a name="operations-scheduling"></a>Operacijų planavimas
### <a name="scheduling-direction"></a>Planavimo kryptis

Planavimo kryptis yra esminė planavimo proceso dalis. Gamybą galima planuoti pirmyn arba atgal nuo bet kurios datos, atsižvelgiant į laiko ir planavimo poreikius.

-   **Planavimas į priekį** – galite planuoti, kad gamyba būtų pradedama kaip įmanoma anksčiau. Gamybą galima pradėti šiandien, rytoj ar nuo bet kurios kitos konkrečios datos ateityje. Gamyba suplanuojama taip, kad būtų pradėta anksčiausią įmanomą datą ir būtų baigta anksčiausią įmanomą datą.
-   **Atgalinis planavimas** – galite planuoti, kad gamyba būtų pradedama kaip įmanoma vėliau. Grafikas paremtas data, kada gamyba turi būti užbaigta, ir skaičiuoja atgal iki vėliausios galimos datos, nuo kurios galima pradėti gamybą, nepraleidžiant jos tikslinio termino.

Galimos toliau nurodytos pasirinktys:

-   **Pirmyn nuo šiandien** – planavimas pirmyn nuo esamos datos. (Dabartinė data yra sistemos data.)
-   **Pirmyn nuo suplanuotos pradžios** – planavimas pirmyn nuo ankstesnės pradžios datos. Jei anksčiau planuota nebuvo, planavimo kryptis yra pirmyn nuo esamos datos.
-   **Pirmyn nuo planavimo datos** – planavimas pirmyn nuo datos, nurodytos lauke **Planavimo data**. Jei nenurodote planavimo datos, planavimo kryptis yra pirmyn nuo esamos datos.
-   **Atgal nuo pristatymo datos** – planavimas atgal nuo pristatymo datos, nurodytos gamybos užsakyme. Jei pasirinksite šią parinktį, o pristatymo data nebus nurodyta, esama data bus pristatymo data.
-   **Atgal nuo suplanuotos pabaigos** – planavimas atgal nuo anksčiau apskaičiuotos pabaigos datos. Jei nėra jokio ankstesnio planavimo, dabartinė data yra pabaigos data.
-   **Atgal nuo planavimo datos** – planavimas atgal nuo datos, nurodytos lauke **Planavimo data**. Jei nenurodote planavimo datos, naudojama esama data. Lauko Atgal nuo planavimo datos reikšmė apskaičiuojama pagal paskutinį kartą skaičiuotą gamybos užsakymo poreikį. Jei nenurodyta jokia gamybos užsakymo data, naudojama esama sistemos data.
-   **Atgal nuo ateities datos** – planavimas atgal nuo ateities datos, apskaičiuotos pagal paskutinį kartą skaičiuotą gamybos užsakymo poreikį. Jei nenurodyta jokia gamybos užsakymo ateities data, naudojama esama sistemos data.
-   **Kaip per paskutinį planavimą** – įrašant operacijas ir užduočių planavimą kartu įrašoma pasirinkta planavimo kryptis ir data. Todėl šią pasirinktį galite taikyti būsimiems planavimams. Jei anksčiau nevykdytas gamybos užsakymo planavimas, planavimas vykdomas atgal nuo esamos sistemos datos.
-   **Pradedant nuo rytojaus** – planavimas pradedant nuo esamos datos + viena diena.
-   **Pirmyn nuo ankstesnės užduoties** – ši funkcija tinkama tik užduotims planuoti. Jei operacijoms planuoti pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo esamos datos. Planuojant užduotis nustatomas vienos užduoties planavimas, o visos kitos gamybos užduotys planuojamos pagal tą užduotį.
-   **Atgal nuo ankstesnės užduoties** – ši parinktis tinkama tik užduotims planuoti. Jei pasirinksite šią operacijų planavimo kryptį, suplanuoti užsakymai bus planuojami atgal nuo esamos datos. Planuojant užduotis nustatomas vienos užduoties planavimas, o visos kitos gamybos užduotys planuojamos pagal tą užduotį.

### <a name="scheduling-date"></a>Planavimo data

Ši data naudojama planavimo kryptyse **Pirmyn nuo planavimo datos** ir **Atgal nuo planavimo datos**. Planuojama atgal arba pirmyn nuo šios datos. Daugiau informacijos žr. ankstesniame skyriuje „Planavimo kryptis“.

### <a name="recalculate-bom-levels"></a>Perskaičiuoti KS lygius

Kai pasirenkate **Perskaičiuoti KS lygius**, bus perskaičiuoti pasirinktos komplektavimo specifikacijos (KS) lygiai, kad būtų užtikrinta teisinga planavimo tvarka.

## <a name="limitations"></a>Apribojimai
### <a name="finite-capacity"></a>Ribotas pajėgumas

Planavimas priklauso nuo išteklių centrų, reikalingų gamybai užbaigti, prieinamumo. Jei nėra pakankamai pajėgumų, gamybos užsakymus galima atidėti arba net sustabdyti. Jei operacijų planavime taikomas ribotas pajėgumas, naudojami esami išteklių pajėgumų rezervavimai ir tas pajėgumas rodomas kaip negalimas. Gamybos užsakymas planuojamas pagal reikalingų išteklių pajėgumo prieinamumą. Operacijų planavime naudojama nurodyta operacijų seka, kad būtų nustatyta gamybos maršruto operacijų tvarka. Operacijų planavimas rezervuoja pajėgumą išteklių grupėse pagal operacijų laiką, nurodytą gamybos maršruto. Išteklių grupių pajėgumas yra visų išteklių grupių išteklių galimų pajėgumų suma.

### <a name="finite-material"></a>Ribotos medžiagos

Planavimas taip pat yra priklausomas nuo gamybai reikalingų medžiagų prieinamumo. Nepakankamas komponentų prieinamumas taip pat gali būti gamybos atidėjimo priežastis. Planavimas taip pat gali būti paremtas ir medžiagų naudojimu. Tiesiog nurodykite gamybos medžiagas, kurios turi būti prieinamos, o ne medžiagas, kurios nėra svarbios. Tokio tipo planavimas vadinamas planavimu turint ribą medžiagų kiekį. Kai nurodote ribotas medžiagas, gamyba planuojama pagal tai, ar medžiagos prieinamos. **Pastaba.** Optimizuojant ir pajėgumą, ir medžiagas, gamyba apskaičiuojama taip, kad atitiktų abu apribojimus. Įvertinamas pajėgumo ir medžiagų prieinamumas ir negalima suplanuoti gamybos užsakymo operacijų vykdymo pradžios, jei tuo pačiu metu nėra reikiamo kiekio pajėgumo ir medžiagų. Pažymėkite šį žymės langelį, jei planavimo metu medžiagas reikėtų laikyti ribotomis. Jei medžiagos yra ribotos, bus atsižvelgiama į to laikotarpio medžiagų padengimą. Kitaip tariant, planuojant atsižvelgiama į apskaičiuotas prekių ateities datas. Planuojant rezervuojamos žaliavos ir išskleidžiama esama gamyba. Jei planavimas vyksta keletą kartų, tik pirmojo planavimo metu vykdomas išskleidimas ir atliekami rezervavimai. Jei gamybos KS arba maršrute atliksite pakeitimų, išskleidžiama bus kito planavimo metu. Išskleidžiant bus manoma, kad medžiagos reikalingos tą pačią dieną. Kadangi gamyba nesuplanuojama išskleidžiant bendrąjį planą, dabartinė data yra tinkamiausias įvertinimas, kada bus galima gauti prekes. Tada išskleidimo metu tikrinama, ar prekės galimos. Jei prekės yra prieinamos, galima patenkinti gamybos poreikį. Jei šiuo metu prekės neprieinamos, sugeneruojamas suplanuotas užsakymas ir atliekamas korespondentinis suplanuoto užsakymo pasirinkimas. Jei nustatytas automatinis suplanuoto užsakymo patvirtinimas, tada suplanuotas pirkimo ar gamybos užsakymas bus automatiškai patvirtintas. Gamybos būsena automatiškai pasikeis į būseną, nurodytą dialogo lango **Padengimo grupės** lauke **Reikalaujama gamybos būsena**. Jei žymės langelis nepažymėtas, bus laikoma, kad medžiagų yra. Dėl to planuojant neatsižvelgiama į tai, ar medžiagos yra pasiekiamos reikalavimo metu.

### <a name="finite-property"></a>Ribota ypatybė

Pažymėti šį žymės langelį, jei norima leisti ypatybių reikalavimus planuojant užduotis.

### <a name="keep-production-unit"></a>Išlaikyti gamybos vienetą

Pasirinkite, ar planavimo mechanizmas turėtų planuoti tik išteklius, kurie jau yra nurodyti gamybos vienete.

### <a name="keep-warehouse-from-resource"></a>Išlaikyti sandėlį iš išteklių

Pasirinkite, ar planavimo mechanizmas turėtų planuoti tik išteklius, susietus su nurodytu ištekliaus tiekimo sandėliu.

## <a name="references"></a>Nuorodos
### <a name="schedule-references"></a>Grafiko nuorodos

Kai nuorodos priklauso nuo gamybos užsakymų, jos taip pat vadinamos tarpinėmis gamybomis. Tarpines gamybas galima planuoti kaip gamybos užsakymo planavimo dalį. Pažymėkite šį žymės langelį, jei tarpinių gamybų planavimas turi būti pagrįstas pagrindinės gamybos planavimu. Siejant su pagrindine gamyba, aukščiau esanti gamyba planuojama į priekį, o žemiau esanti gamyba – atgal. Gamybos užsakymo nuorodas galima peržiūrėti puslapio **Gamybos užsakymai** lauke **Nuorodos lygis**.

### <a name="synchronize-references"></a>Sinchronizuoti nuorodas

Jūs taip pat galite nuorodas sinchronizuoti su gamybos užsakymu. Jei pasirenkama ši parinktis, tarpinės gamybos datos perkeliamos sulygiuojamos, kai keičiamas gamybos užsakymo grafikas. Jei produkto užsakymui priskirta viena ar daugiau tarpinių gamybų, galite tarpines gamybas planuoti kartu su pagrindine gamyba. Šiuo atveju pagrindinės gamybos negalima pradėti, kol susijusios tarpinės gamybos nebus baigtos. Todėl pažymėkite šį žymės langelį, jei tarpinių gamybų planavimas turi būti pagrįstas pasirinktos gamybos pradžios ir pabaigos laiku. Galite pažymėti šį žymės langelį tik jei žymės langelis **Grafiko nuorodos** yra taip pat pažymėtas.

## <a name="cancellation"></a>Atšaukimas
### <a name="cancel-queue-time"></a>Atšaukti laukimo darbo grupėje laiką

Pažymėkite šį žymės langelį norėdami laukimo eilėje laiko neįtraukti į planavimą.

### <a name="cancel-setup"></a>Atšaukti nustatymus

Pažymėkite šį žymės langelį norėdami sąrankos laiko neįtraukti į planavimą.

### <a name="cancel-process"></a>Atšaukti procesą

Pažymėkite šį žymės langelį norėdami vykdymo laiko neįtraukti į planavimą.

### <a name="cancel-overlap"></a>Atšaukti persidengimą

Pažymėkite šį žymės langelį norėdami persidengiančio laiko neįtraukti į planavimą.

### <a name="cancel-transport"></a>Atšaukti transportavimą

Pažymėkite šį žymės langelį norėdami tranzito laiko neįtraukti į planavimą.

## <a name="set-default"></a>Nustatyti numatytąją
Galite išsaugoti dabartines reikšmes kaip numatytąsias reikšmes. Galima naudoti dvi parinktis.

-   Nustatyti kaip mano numatytąjį parametrą
-   Nustatyti kaip visų numatytąjį parametrą


<a name="additional-resources"></a>Papildomi ištekliai
--------

[Operacijų planavimas](operations-scheduling.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]