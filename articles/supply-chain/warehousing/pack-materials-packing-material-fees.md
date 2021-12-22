---
title: Pakavimo medžiagos ir mokesčiai
description: Šioje temoje pateikiama informacija apie pakavimo medžiagų mokesčius, kurie tam tikrais intervalais yra mokami perdirbimo įmonėms.
author: Mirzaab
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72d07365a5022a67b8868232fbbb04f610701009
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902026"
---
# <a name="packing-materials-and-fees"></a>Pakavimo medžiagos ir mokesčiai

[!include [banner](../includes/banner.md)]

Pakavimo medžiagų mokesčiai atliekų perdirbimo įmonei mokami konkrečiais intervalais. Už kiekvieną pakuotės sudedamosios dalies svorio vienetą mokama tam tikra suma. Nors pakavimo medžiagų mokesčiai skaičiuojami ir pateikiami ataskaitose, DK operacijos neregistruojamos, nes šie mokesčiai nelaikomi mokesčiais, kuriuos privalu mokėti valstybei.

Skaičiuojami pardavimo užsakymo eilučių ir pirkimo užsakymų eilučių pakavimo medžiagų svoriai ir mokesčiai.

Vienai prekei, prekių grupei (prekių pakavimo grupei) ar visoms prekėms galite apibrėžti vieną ar kelis pakavimo vienetus. Pakavimo vienetą sudaro pakavimo medžiagos, jų svoriai ir prekių, įeinančių į pakavimo vienetą, skaičius. Pakavimo medžiagos kodas priskiriamas kiekvienam apibrėžtam pakavimo medžiagos tipui. Pagal pakavimo medžiagos kodą galite nurodyti konkretaus laikotarpio kainą. Pagal šią informaciją skaičiuojamas pakavimo medžiagos mokestis.

> [!NOTE]
> Net jei jūsų įmonė nemoka pakavimo medžiagų mokesčių, galite šią funkciją naudoti pakavimo medžiagų svorių statistikai skaičiuoti.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Pakavimo medžiagų paskirstymo nustatymas

Prieš skaičiuodami pakavimo medžiagų svorį, pakavimo medžiagų mokesčius arba ir svorį, ir mokesčius, turite įjungti skaičiavimą ir nurodyti, kokios medžiagos ir mokesčiai bus taikomi konkrečioms prekėms.

1. Eikite į **Atsargų valdymas\> Sąranka \> Atsargų ir sandėlio valdymo parametrai**.
1. Skyriaus **Pakavimo medžiagos** skirtuke **Bendra** nustatykite parinkties **Skaičiuoti pakavimo medžiagų mokesčius** reikšmę **Taip**.
1. Eikite į **Atsargų valdymas \> Sąranka \> Pakavimo medžiagos \> Pakavimo grupės** ir sukurkite visas pakavimo grupes, kurias naudojate. Visos pakavimo grupės prekės naudos tą patį pakavimo medžiagų paskirstymą. Jei nenaudojate pakavimo grupių, galite praleisti šį veiksmą.

    > [!TIP]
    > Sukūrę pakavimo grupes, galite priskirti grupę kiekvienam produktui, kaip jums reikia. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**, pasirinkite produktą, tada lauke **Pakavimo grupė** esančiame „FastTab“ skirtuke **Tvarkyti atsargas** pasirinkite tinkamą pakavimo grupę.

1. Eikite į **Atsargų valdymas \> Sąranka \> Pakavimo medžiagos \> Pakavimo medžiagų kodai**, nustatykite visus jūsų naudojamų pakavimo medžiagų tipus ir nurodykite vienetus, kuriais matuojama naudojama pakavimo medžiaga, kai ruošiate siuntas.
1. Eikite į **Atsargų valdymas \> Sąranka \> Pakavimo medžiagos \> Pakavimo medžiagų mokesčiai** ir nustatykite mokestį, taikomą kiekvienam pakavimo medžiagų tipui, kuriuos ką tik nustatėte. Mokesčiai apskaičiuojami remiantis sunaudoto vieneto kaina.
1. Norėdami paskirstyti pakavimo medžiagas pagal prekes, eikite į **Atsargų valdymas \> Sąranka \> Pakavimo medžiagos \> Pakavimo medžiagų paskirstymas** ir atlikite paskirstymus. Galite sukurti tiek paskirstymų, kiek reikia. Galite paskirstyti pakavimo medžiagas pagal atskiras prekes, prekių grupes (prekių pakavimo grupes) arba visas prekes, atsižvelgdami į tai, kiek išsamūs turėtų būti jūsų paskirstymai.

    Kurdami kiekvieną paskirstymą, atlikite šiuos veiksmus.

    1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

        - **Prekės kodas** – pasirinkite paskirstymo apimtį:

            - **Lentelė** – sukurkite paskirstymą, skirtą vienai konkrečiai prekei.
            - **Grupė** – sukurkite paskirstymą, skirtą visoms prekėms, priklausančioms pakavimo grupei, kuri yra nustatyta puslapyje **Pakavimo grupės**.
            - **Visos** – sukurkite paskirstymą, skirtą visoms prekėms.

            > [!NOTE]
            > Paprastai visus savo paskirstymus turite atlikti tame pačiame lygyje (**Lentelė**, **Grupė** arba **Visos**). Jei naudojate daugiau nei vieną lygį, kiekvienai prekei bus naudojamas labiausiai tinkantis paskirstymas. (Lygis **Lentelė** yra viršesnis už lygį **Grupė**, o abu šie lygiai yra viršesni už lygį **Visos**.)

        - **Prekės ryšys** – jeigu atliekate vienos prekės paskirstymą, pasirinkite šią prekę. Jei atliekate prekių grupės paskirstymą, pasirinkite pakavimo grupę. Jei atliekate visų prekių paskirstymą, palikite šį lauką tuščią.
        - **Konfigūracija**, **Dydis**, **Spalva** ir **Stilius** – įveskite šių dimensijų vertes, kaip jums reikia, kad toliau nustatytumėte prekę, kurios paskirstymą atliekate.
        - **Pakavimo vienetas** – pasirinkite vienetą, kuriuo yra matuojama naudojama pakavimo medžiaga. Šis vienetas gali skirtis nuo vieneto, kuris naudojamas prekei parduoti ir laikyti.
        - **Pakavimo vieneto koeficientas** – įveskite konvertavimo koeficientą, kuris yra naudojamas konvertuojant iš atsargų vieneto į pakavimo vienetą. (Konvertavimui naudojama formulė: *Pakavimo vienetai* = *Prekės vienetai* × *Pakavimo vieneto koeficientas*.)

    1. „FastTab“ skirtuke **Pakavimo medžiagos** įtraukite eilutę, skirtą kiekvienai pakavimo medžiagai, kuri yra reikalinga dabartiniam paskirstymui atlikti. Kiekvienoje eilutėje nurodykite medžiagos tipą (kaip nurodyta puslapyje **Pakavimo medžiagų kodai**) ir jos kiekį, sunaudojamą kiekvienam šios prekės siuntimo vienetui.

## <a name="packing-units-on-sales-order-lines"></a>Pakavimo vienetai pardavimo užsakymo eilutėse

[Įjungus pakavimo medžiagų mokesčių skaičiavimą ir nustačius paskirstymus](#allocations), sistema patikrina, ar kiekvienai prekei, įtrauktai į pardavimo užsakymą, nurodyti pakavimo vienetai. Tada ji apskaičiuoja visus reikalingus mokesčius. Kai prekė įtraukiama į pardavimo užsakymą, atliekamas vienas šių veiksmų:

- **Jie pakavimo paskirstymas taikomas prekei:** sistema pardavimo užsakymo eilutę atnaujina įrašydama nurodytą pakavimo vienetą ir pakavimo vienetų kiekį. (Pakavimo vienetų kiekis skaičiuojamas taikant formulę: *Pakavimo vienetų kiekis* = *Užsakytas kiekis* ÷ *Pasirinkto pakavimo vieneto prekių skaičius*.)
- **Jei nėra prekei taikomų pakavimo paskirstymų:** pardavimo užsakymo eilutėje pakavimo vienetą ir pakavimo vieneto kiekį galima įrašyti rankiniu būdu.

Keisti pakavimo vienetą ir pakavimo vienetų kiekį taip pat galite registruodami pardavimo užsakymo eilutę. Ši galimybė yra aktuali, jei pardavimo užsakymo eilutė pristatyta arba jai SF išrašyta tik iš dalies.

Kai pardavimo užsakymui išrašote SF, sistema sukuria pakavimo medžiagų operacijas. Pakavimo medžiagų operacijose yra pardavimo eilutės pakavimo medžiagų svoriai. Galite modifikuoti operacijas, išrašę SF. Tada galite kurti naujų operacijų.

## <a name="packing-units-on-purchase-order-lines"></a>Pakavimo vienetai pirkimo užsakymo eilutėse

Sistema nesukuria pakavimo medžiagų operacijų, skirtų pirkimo užsakymo eilutėms. Vietoj to pirkimo užsakymo, kuriam išrašyta SF, eilučių operacijos kuriamos rankiniu būdu puslapyje **Pakavimo medžiagų operacijų**.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Licencijų numerių nustatymas klientams, kuriems yra taikomi pakavimo medžiagų mokesčiai

Jeigu į konkrečiam klientui skirtą pardavimo užsakymą turi būti įtraukti pakavimo medžiagų, naudojamų kiekvienam užsakymui, mokesčiai, atlikite šiuos veiksmus.

1. Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.
1. Pasirinkite klientą, kuriam turi būti taikomas pakavimo medžiagų mokestis.
1. „FastTab“ skirtuke **SF ir pristatymas** nustatykite toliau pateikiamus laukus.

    - Lauko **Pakavimo muito mokesčio licencijos numeris** skyriuje **PVM** įveskite įmonės licencijos numerį.
    - Lauko **Licencijos numeris** skyriuje **Pakavimo medžiagų mokestis** įveskite įmonės licencijos numerį.

Dabar, kai sukūrėte pardavimo užsakymą, į kurį įtraukta viena ar daugiau prekių, kurioms supakuoti naudojamos pakavimo medžiagos, ir išrašėte SF, SF bus parodyti pakavimo medžiagų mokesčiai.

Klientų, kuriems netaikomi pakavimo medžiagų mokesčiai, atveju atlikite tuos pačius veiksmus, bet išvalykite licencijos numerius iš laukų **Pakavimo muito mokesčio licencijos numeris** ir **Licencijos numeris**. Sąskaitose faktūrose, pateikiamose klientams, kuriems netaikomi pakavimo medžiagų mokesčiai, yra nurodomi pakavimo medžiagų svoriai, bet nenurodomi mokesčiai.

Norėdami sukurti ataskaitą, kurioje bus parodyti visi pakavimo medžiagų mokesčiai, kuriuos jūsų įmonė skolinga už tam tikrą laikotarpį, eikite į **Atsargų valdymas \> Užklausos ir ataskaitos \> Pakavimo medžiagos ataskaitos \> Pakavimo medžiagos mokesčio apskaičiavimas**, nurodykite datų diapazoną, tada pasirinkite **Gerai**.

## <a name="print-packing-material-weights-on-invoices"></a>Pakavimo medžiagų svorio spausdinimas sąskaitose faktūrose

Galite ant SF spausdinti pakavimo medžiagų svorius ir nurodyti, kas mokės susijusius mokesčius. Svoriai sumuojami pagal pakavimo kodą.

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
1. „FastTab“ skirtuke **Sąskaita faktūra** esančiame skirtuke **Naujiniai** nustatykite parinkties **Spausdinti pakavimo medžiagos svorį** reikšmę **Taip**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]