---
title: Periodinio sutarties atsiskaitymo parametrai
description: Šiame straipsnyje paaiškinama, kaip nustatyti numatytąsias atsiskaitymo grafikų, kurie sukuriami periodiniame sutarties atsiskaitymo grafike, vertes. Taip pat paaiškinama, kaip sukurti atsiskaitymo grafiko grupes.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 64d6e21c2d8c588a64f0f4cf8b7a0bafc853bcab
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644009"
---
# <a name="recurring-contract-billing-parameters"></a>Periodinio sutarties atsiskaitymo parametrai

Naudokite periodinių **sutarties atsiskaitymo parametrų** puslapį, norėdami nustatyti numatytąsias atsiskaitymo grafikų, kurie sukuriami periodiniame sutarties sąskaitų išrašymo lape, vertes. Visi jūsų sukurti atsiskaitymo grafikai iš pradžių naudos šias numatytąsias vertes. Tačiau, jei reikia, galite pakeisti kiekvieno sąskaitų pateikimo grafiko vertes.

## <a name="general-tab"></a>Skirtukas Bendra

1. Pasikartojančios **sutarties atsiskaitymo parametrų** puslapio **skirtuko** Bendra lauke Atsiskaitymo **grafiko grupė** pasirinkite atsiskaitymo grafiko grupę. Informacijos, kaip nustatyti atsiskaitymo grafiko grupes, žr. atsiskaitymo [grafiko grupių skyrių](#set-up-billing-schedule-groups) toliau šiame straipsnyje.
2. Lauke Atleidimo **tipas pasirinkite**, kaip bus skaičiuojama galutinė SF, kai nutrauktas atsiskaitymo grafikas:

    - **Koreguoti grafiką** – nutraukimo atsiskaitymo grafiką atleidimo datą, pakeisti grafiko būseną į Paskutinis atsiskaitymas ir pakoreguoti susietą atidėjimo grafiką atšaukiant sumą, **kuri** daugiau neturi būti atpažinta. Jei sąskaitos pateikimo pradžios data yra po atleidimo datos, likę atsiskaitymo laikotarpiai pašalinami.
    - **Likęs** vekselis – įtraukite likusias sumas į atsiskaitymo grafiką į atleidimo laikotarpį, **pakeiskite** grafiko būseną į Paskutinis atsiskaitymas ir atnaujinkite atidėjimo grafiką. Jei atsiskaitymo pradžios data yra po atleidimo datos, į atsiskaitymo laikotarpį įtraukiama bendroji visų likusių atsiskaitymo laikotarpių suma, o likę atsiskaitymo laikotarpiai pašalinami.
    - **Nėra koregavimo** – atleisti atsiskaitymo grafiką atleidimo datą. Mokėjimo grafikas nėra koreguojamos.

3. Lauke Unikalus **grafiko tipas pasirinkite** Nėra, kad **nurodykite**, jog klientai ribojami pagal vieną atsiskaitymo grafiką. Norėdami **nurodyti, kad** **klientai gali naudoti tik unikalų** grafiką, pasirinkite Vienam klientui arba Galutiniam vartotojui.
4. Nustatykite mėnesio **lygiavimo** parinktį **taip,** kad sulygiuokite atsiskaitymo grafiko informacijos eilutes su mėnesio pabaiga, kai sukuriamas arba atnaujinamas atsiskaitymo grafikas. Jei norite naudoti didėjančias **datas**, nustatykite ne.
5. Nustatykite **parinktį Paskirstyti dalinius** laikotarpius **kaip Taip**, norėdami paskirstyti sąskaitų sumas pagal laikotarpio dienų skaičių. Nustatykite, **kad** kiekvieno atsiskaitymo laikotarpio suma būtų lygi Ne, neatsižvelgiant į dienų skaičių.
6. Jei dalinių **laikotarpių** **parinktį** nustatote Taip, **·** **nustatykite** lauke Skaičiavimo metodas kaip Kasdienis, norėdami paskirstyti sumas pagal laikotarpio dienų skaičių. Nustatykite, kad **kas** mėnesį sumos būtų lygios kas mėnesį.
7. Nurodyti, ar pagal numatytuosius nustatymus naujai sukurti atsiskaitymo grafikai sulaikyti.

    > [!NOTE]
    > Norint pašalinti atsiskaitymo grafiko sulaikymas, vartotojas turi būti vartotojų grupės dalis. Pasirinkite **Šalinti sulaikymo vartotojų grupės nepaisymus**, norėdami nustatyti vartotojų grupę, kurioje **įgalinta parinktis Leisti** šalinti sulaikymas.

8. Lauke SF **operacijos tipas pasirinkite** numatytąjį SF operacijos tipą naujiems sąskaitų pateikimo grafikams.
9. Nustatykite atidėjimo **lygiavimo pagal** **atsiskaitymo** parinktį kaip Taip, kad sulygiuokite atitinkamą atidėjimo grafiką, kad jis naudos tas pačias datas kaip ir atsiskaitymo grafike. Jei norite, kad **būtų nurodytos** skirtingos datos, nustatykite ne.
10. Jei naudojate įplaukų skaidymo funkciją, nustatykite parinktį Automatiškai kurti **įplaukų** skaidymo parinktį **kaip Taip**, kai prekės pridėtos prie sąskaitų pateikimo grafiko. Jei **prekė nustatyta** kaip įplaukų skaidymo prekė, sąskaitų pateikimo grafiko eilutėje bus automatiškai pažymėtas žymės langelis Įplaukų skaidymo. Nustatykite pasirinktį **Ne**, jei norite rankiniu būdu pažymėti žymės langelį **Įplaukų skaidymo**.
11. Nustatykite **kliento skaidymo** parinktį kaip **Taip**, jei norite leisti išrašyti sąskaitų pateikimo grafiką skirtingiems klientams. Kai nustatyta Kaip **Taip,** klientų **skaidymo** parinktis galima atsiskaitymo grafiko antraštėje ir atsiskaitymo grafiko eilutėje. 
12. Nustatykite pardavimo užsakymo kūrimo laukus:

    - SF gali būti konsoliduotos pagal laikotarpį, klientą arba prekę. Galima nustatyti bet **kokį** verčių **Taip ir Ne** derinį. SF taip pat galima skaidyti pagal prekių grupę.
    - Galimos šios SF registravimo pasirinktys:

        - **Kurti pardavimo užsakymą** – kurti tik pardavimo užsakymą.
        - **Rodyti SF registravimą** – išrašyti pardavimo užsakymo SF ir atidaryti puslapį, kuriame galite neautomatiniu būdu registruoti SF.
        - **Kurti mokesčio teksto** SF – pasirinkite šią parinktį, jei naudojate laisvos formos SF.
        - **Automatiškai registruoti SF** – išrašyti pardavimo užsakymo SF ir automatiškai registruoti.

    - Nustatykite **parinktį Įtraukti atsiskaitymo datas į prekės** aprašą kaip **Taip**, norėdami įtraukti aprašą, kuriame yra atsiskaitymo pradžios ir pabaigos datos.
    - Nustatykite parinktį **Neįtraukti nulinio suvartojimo** į **Taip, jei** norite pašalinti sąskaitų pateikimo grafiko eilutes, kuriose nėra suvartojimo. Nustatykite, kad **į** pardavimo užsakymą būtų įtrauktos tos eilutės, o ne.
    - Nustatykite **parinktį Nespausdinti antrinių** **prekių** kaip Taip, jei nenorite spausdinti antrinių įplaukų, suskaidytų į pardavimo užsakymą, prekių. SF bus rodoma tik pirminė prekė. Jei grynoji antrinių prekių suma (paslėpti) yra ne nulinė, pirminės eilutės grynoji suma rodo antrinių eilučių suvestinę. Nustatykite pasirinktį **Ne,** jei norite ant pardavimo SF išspausdinti visas ant pirminės prekės pateiktas ant jų ant pirminę prekę.

12. Nustatykite palaikymo ir atnaujinimo laukus:

    - Nustatykite **automatinio įgalinimo ir atnaujinimo parinktį** **kaip Taip,** norėdami automatiškai naudoti pardavimo užsakymo palaikymo ir atnaujinimo funkciją.
    - Lauke Palaikymas **ir atnaujinimo lygis** pasirinkite numatytąjį palaikymo ir atnaujinimo lygį.
    - Lauke Palaikymas **ir atnaujinimo kiekis** nurodykite palaikymo ir atnaujinimo kiekį.
    - Lauke Numatytoji **palaikymo ir atnaujinimo pradžios data** nurodykite datą, kurią reikia naudoti kaip numatytąją palaikymo ir atnaujinimo pradžios datą:

        - **Operacijos data** – naudokite operacijos datą kaip pradžios datą.
        - **Šio mėnesio pradžia** – naudoti pirmą esamo mėnesio datą kaip pradžios datą.
        - **Kito mėnesio pradžia** – naudokite pirmą kito mėnesio dieną kaip pradžios datą. Jei operacijos data yra pirma, naudojama pirmoji dabartinio mėnesio data.
        - **15 taisyklė** – naudoti pirmą esamo mėnesio pradžios datą, jei operacijos data yra tarp pirmosios ir penkioliktos mėnesio dienos. Jei operacijos data yra šešiolikta arba vėlesnė, kaip pradžios datą naudokite pirmą kito mėnesio datą.

    - Nustatykite **parinktį Įtraukti nuolaidą** į skaičiavimą **kaip Taip**, norėdami įtraukti nuolaidos sumą į palaikymo ar atnaujinimo sumą. Nustatykite, kad **nuolaidos** sumos nebūtų galima pašalinti.
    - Laukuose **Palaikymo dažnis** **ir** atnaujinimo dažnis pasirinkite dažnumą, kada palaikymo ir atnaujinimo prekės bus pridėtos prie sąskaitų pateikimo grafiko: Kasdienis **·**, **Mėnesinis**, Ketvirtinis **·**,**Pusiau** laiku arba **Kasmet.**
    - Nustatykite pasirinktį **Lygiuoti** pagal prekių **grupę** kaip Taip, kad pagal prekių grupę sulygiuokite naujų prekių pradžios ir pabaigos datas su esamomis prekėmis.
    - Nustatykite **parinkties** **Lygiuoti** į kitą neapledėtą laikotarpį pasirinktį Taip, norėdami nustatyti atnaujinimo prekės lygiuotės datą, pagrįstą kito neapledėto laikotarpio po atnaujinimo pradžios data.
    - Nustatykite **pasirinktį Kopijuoti** serijos numerį kaip **Taip,** jei norite kopijuoti prekės serijos numerį iš pradinio pardavimo užsakymo eilutės į atitinkamą atsiskaitymo grafiko eilutę.

13. Jei sąskaitų pateikimo grafike naudojate perskyrimą, pasirinkite metodą, naudojamą skaičiuojant vartotojo kainos indeksą.
14. Nustatykite **parinktį Sekti kainos keitimą** kaip **Taip**, jei norite, kad kainų pakeitimai būtų įrašyti atsiskaitymo grafiko eilutėse. Jei atsiskaitymo grafiko eilutė rankiniu būdu pakeičiama iš standarto į butą ir įvedama nauja kaina, audito informacija sekama atsiskaitymo grafiko eilutėje. Jei nenorite sekti **šių** keitimų, nustatykite pasirinktį Ne.
15. Nurodykite, ar įrašai pagal numatytuosius nustatymus filtruojami pagal pradžios datą, ar pagal numatytuosius nustatymus **sąskaitos faktūros generymo** puslapyje.
16. Jei naudojate neišskaitomos **įplaukų** funkciją, nurodykite naudojamas pasirinktis:

    - Jei norite **, kad bendrasis žurnalas būtų** kuriamas **ir** registruojamas tuo pačiu metu, automatiškai nustatykite pasirinktį Registruoti bendrąjį žurnalą kaip Taip. Nustatykite jį kaip **Ne**, jei norite sukurti bendrąjį žurnalą ir tada užregistruokite jį rankiniu būdu.
    - Lauke Numatytasis **žurnalo pavadinimas** pasirinkite numatytąjį žurnalo pavadinimą, kuris bus naudojamas kuriant bendrąjį žurnalą.
    - **Lauke Trumpalaikis neilgalaikį** metodą pasirinkite trumpalaikį neaplaikytą metodą, jei jį naudojate. Pasirinkus **Nėra**, trumpalaikis funkcionalumas nebus naudojamas su neišduotais įplaukomis. Pasirinkite **12** mėnesių arba fiksuotų metų ėjimo **laikotarpius, norėdami** naudoti likusius finansinius metus.

17. Nurodykite parinktis, naudojamas kai nutrauktas atsiskaitymo grafikas ir jo eilutės:

    - **Išdavimo** kreditas – kurti kredito pažymą, kai nutrauktas atsiskaitymo grafikas arba atsiskaitymo grafiko eilutė.
    - **Kredito koregavimas** – kurti sąskaitų pateikimo grafiko kredito koregavimą, kai eilutė nutraukta. Kredito koregavimas rodomas būsimam atsiskaitymo grafiko atsiskaitymo laikotarpiui. Kredito koregavimas atnaujins kito atsiskaitymo laikotarpio SF sumą, kol kreditas bus užbaigtas taikyti atsiskaitymo grafikui.
    - **Nėra kredito** – nekurti kredito koregavimo arba kredito pažymos, kai nutrauktas atsiskaitymo grafikas arba atsiskaitymo grafiko eilutė. Ši pasirinktis galima tik tada, kai **parinktis Nėra koregavimo** naudojama norint atleisti atsiskaitymo grafiką.
18. Kai **parinktis** **·** **Vieną** kartą gali būti nutraukta nuo grąžinimo, nustatyta kaip Ne ir atsiskaitymo grafikas, kurio atsiskaitymo dažnumas yra Vieną kartą, **atsiskaitymo** grafiko eilutės būsena pasikeičia į Atleista, kai išrašoma atsiskaitymo grafiko SF. Šio sąskaitų pateikimo grafiko nutraukti negalima ir negalima išduoti jokio kredito. Kai **vieną kartą galima atleisti** nuo grąžinimo, nustatyta parinktis Taip, atsiskaitymo grafiko eilutės, kurios atsiskaitymo dažnumas Yra Vieną kartą, būsena Bus Aktyvi po **to** **·** **·**, kai išrašoma sąskaitų faktūrų SF. Atsiskaitymo grafiko eilutę galima nutraukti ir apdoroti grąžinimą. 
19. Parametruose **nustatyta prorate daily** parinktis bus nustatyta masinio atleidimo puslapyje ir atsiskaitymo grafiko antraštėje bei eilutės atleidimo dialogo languose. Jis gali būti pakeistas atleidimo proceso metu. Kai nustatyta Kaip **Taip**, bet kokia grąžinimo suma bus skaičiuojama naudojant dienos tarifą. Kai nustatyta Ne, **kreditas** bus kreditas pagal atleidimo datą ir atsiskaitymo dažnumą. Pavyzdžiui, jei kas mėnesį buvo naudojama dažnumas ir sąskaitų $100 per mėnesį, kredito suma padidinama kas $100. Jei atsiskaitymo dažnumas yra vieną kartą, kredito suma yra $0.00. Jei norite gauti vienkartinio atsiskaitymo dažnumo grąžinimą, dienos prorate nustatykite kaip Taip. 
20. Nustatykite **kredito pasirinkties kurti atidėjimą** kaip **Taip, jei** norite kurti naują atidėjimo grafiką kredituojant esamą atidėjimo grafiką. Norėdami sukurti kreditą esamame **atidėjimo** grafike, palikite nustatytą pasirinktį Ne.

## <a name="sequence-number-tab"></a>Skirtukas Sekos numeris

Naudokite skirtuką **Eilės numeris** periodinių **sutarčių atsiskaitymo parametrų puslapyje**, norėdami nustatyti numatytąją atsiskaitymo grafiko numerių vertę. Numatytosios vertės yra nustatytos numeracijos **puslapyje** (Organizacijos **administravimo \> numeracijos \> numeracijos**).

## <a name="set-up-billing-schedule-groups"></a>Nustatyti atsiskaitymo grafiko grupes

Norėdami sukurti **pasikartojančios sutarties atsiskaitymo** planavimo grupę, naudokite atsiskaitymo grafiko grupės puslapį. Kai sukuriamas naujas atsiskaitymo grafikas ir jai taikoma atsiskaitymo grafiko grupė, vertės, kurios nustatytos atsiskaitymo grafiko grupės puslapyje, **įvedamos** kaip numatytosios atsiskaitymo grafiko vertės. Galite pakeisti bet kurią numatytąją konkretaus kuriamo atsiskaitymo grafiko vertę. Galite nustatyti kelias atsiskaitymo grafiko grupes, o tada vieną iš jų priskirti kaip numatytąją atsiskaitymo grafiko grupę **periodinės sutarties atsiskaitymo parametrų** puslapyje.

Norėdami sukurti pasikartojančio sutarties atsiskaitymo planavimo grupę, atlikite šiuos veiksmus.

1. Norėdami sukurti **atsiskaitymo grafiko** grupę, puslapyje **Atsiskaitymo** grafiko grupė pasirinkite Naujas.
2. Lauke Atsiskaitymo **grafiko grupė** įveskite unikalų identifikatorių.
3. Lauke **Aprašas** įveskite aprašą.
4. Lauke Atsiskaitymo **dažnumas** nurodykite, kaip dažnai klientui išrašomos sąskaitos pagal atsiskaitymo grafiką: **vieną** kartą, kas **dieną,** **kas** mėnesį, **ketvirtį**, **kas** pusmetį arba **kasmet.**
5. Lauke Atsiskaitymo **intervalas** įveskite atsiskaitymo intervalą. Pvz., nustatykite lauką **Atsiskaitymo dažnumas** kaip **Mėnesinis,** o atsiskaitymo **intervalo** lauke **nustatykite 2**, kad sąskaitos būtų išrašytos kas kitą mėnesį.
6. Lauke Kainos **metodas pasirinkite** numatytąjį kainų metodą prekėms, esančioms atsiskaitymo grafike:

    - **Standartinis** – skaičiuokite vieneto kainą, remiantis įvestu kiekiu, **ir** produkto informacijos valdymo puslapyje Išleisti produktai naudokite standartinę kainodarą.
    - **Butas** – taikyti butą kainą, įvestą atsiskaitymo grafiko eilutėje.
    - **Pakopa** – skaičiuoti vieneto kainą naudojant fiksuotą kiekį skirtinguose kainos skliaustuose. Prieš pereinant į kitą kainos skliaustą, būtina užpildyti kiekvieną pakopą.
    - **Buto** pakopa – skaičiuoti vieneto kainą naudojant fiksuotą kiekį ir išplėstą kainų sumą skirtingiems kainų skliaustams. Kaina, apmokestinta atsiskaitymo laikotarpiu, naudoja išplėstą kainą, kuri atitinka pakopą, kurioje yra atsiskaitymo kiekis.

7. **Lauke Prekės tipas** pasirinkite atsiskaitymo grupės prekės tipą:

    - **Standartinis** – pasirinkti šią vertę, jei kiekis statinis.
    - **Naudojimas** – pasirinkite šią vertę skaitiklio arba suvartojimo tipo prekėms. Jei pasirenkate šią vertę, nustatykite **naudojimo** **skaitymo** parinkties lauką kaip Skaitoma, kad būtų galima įvesti atsiskaitymo laikotarpio vertę (rodmenis) skaitiklio arba įrenginio sąskaitos pateikimo laikotarpiu. Suvartota vertė bus apskaičiuota remiantis ankstesniu atsiskaitymo laikotarpiu ir jūsų įvesti rodmeniu.
    - **Etapas** – pasirinkite šią vertę, norėdami naudoti rodyklės atsiskaitymo funkciją. Jei pasirinksite šią vertę, rodyklės šablono **lauke**, pasirinkite rodyklės šabloną, jei jį naudojate.
    - **Suvartojimas** – pasirinkite šią vertę, jei norite įvesti vertę, suvartotą sąskaitų pateikimo laikotarpiu.

8. Norėdami sukurti **konsoliduotų** SF **ir** atskirų to paties kliento SF derinį, atskirai nustatykite SF pasirinktį Taip. Pvz., klientas turi penkis sąskaitų pateikimo grafikus. Trys iš jų bus konsoliduotos vienoje SF, tačiau kiekviena iš kitų turės atskirą SF. Norėdami sukurti tik vieną **konsoliduotąją** kliento SF, nustatykite pasirinktį Ne.
9. Nustatykite **pasirinktį** Atnaujinti automatiškai kaip **Taip,** kad sukūrus SF būtų automatiškai atnaujintas kito atsiskaitymo laikotarpio periodinis atsiskaitymo grafikas. Nustatykite, kad neautomatiškai **atnaujintumėte** atsiskaitymo grafiką. Eilutėse **, kurias norite įtraukti į atnaujinimo** lauką, nurodykite, kiek eilučių įtraukti į kiekvieną atnaujinimą.
10. Nustatykite perskyrimo **parinktį** Taip **, jei** norite taikyti *perskyrimus* (kainos padidėjimus) atsiskaitymo grafikams, susietiems su šia sąskaitų pateikimo grafikų grupe.
