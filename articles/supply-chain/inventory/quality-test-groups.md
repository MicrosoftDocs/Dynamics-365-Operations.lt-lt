---
title: Kokybės valdymo bandymo grupės
description: Šioje temoje aprašoma, kaip sukurti grupes, kurias galima naudoti keliems bandymams su kokybės užsakymais „Microsoft Dynamics 365 Supply Chain Management“.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e0adac76d7b5ecf993ab75c60eced41050034f8
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956761"
---
# <a name="quality-management-test-groups"></a>Kokybės valdymo bandymo grupės

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti grupes, kurias galima naudoti keliems bandymams su kokybės užsakymais „Microsoft Dynamics 365 Supply Chain Management“.

Naudojate **Bandymo grupių** puslapį siekiant nustatyti, redaguoti ir peržiūrėti bandymų grupei priskirtas bandymų grupes bei atskirus bandymus. Viršutinėje puslapio dalyje rodomos tikrinimų grupės, o apatinėje srityje rodomi pasirinktai tikrinimų grupei priskirti tikrinimai.

Tikrinimų grupei priskiriate keletą strategijų, įskaitant pavyzdžių ėmimo planą, priimtiną kokybės lygį (PKL) ir ardomojo tikrinimo reikalavimus. Kai bandymų grupei priskiriate atskirą bandymą, apibrėžiate papildomą informaciją, pvz., seką, dokumentus ir galiojimo datas. Atliekant kiekybinį bandymą, jūsų apibrėžta informacija taip pat apima priimtinas matavimo reikšmes. Atliekant kokybinį bandymą, informacija apima bandymo kintamąjį ir numatytąjį rezultatą.

Kokybės užsakymui priskirta bandymų grupė apibrėžia numatytąjį konkrečios prekės bandymų, kuriuos reikia atlikti, rinkinį. Tačiau kokybės užsakymo bandymus galite pridėti, naikinti arba keisti. Pateikiami kiekvieno kokybės užsakymo tikrinimo rezultatai.

Nurodydami bandymo grupę galite pasirinktinai nurodyti prekės pavyzdžių ėmimą. Prekių pavyzdžių ėmimas naudojamas produktų kiekiui, kurį reikia patikrinti, nustatyti. Daugiau informacijos ieškokite Kokybės [prekės bandymo valdymo tikrinimo](quality-item-sampling.md) priemonės. Taip pat galite nurodyti, ar bandymo grupės bandymai yra ardomasis. Ardomojo bandymo metu prekės ėmimas sunaikintas ir kiekis pašalinamas iš turimų atsargų.

## <a name="example-of-a-test-group"></a>Bandymo grupės pavyzdys

Gamybos įmonė apibrėžia kiekvieno kokybės gairių varianto tikrinimų grupę. Įvairios bandymų grupės atspindi pavyzdžių ėmimo planų skirtumus, bandymų, kuriuos reikia atlikti vienu metu, rinkinius, AQL ir kitus veiksnius. Taip pat skiriasi kiekybinių bandymų priimtinos matavimo reikšmės. Siekiant įgyvendinti kokybės gaires, įmonė priskiria tikrinimo grupę kiekvienai taisyklei, kuri naudojama automatiškai generuoti kokybės užsakymus **kokybės susiejimų** puslapyje. Be to, ji priskiria tikrinimo grupę kokybės užsakymams, kurie kuriami rankiniu būdu.

## <a name="create-a-test-group"></a>Kurti bandymų grupę

Norėdami bandymo grupę, atlikite tolesnius veiksmus.

1. Eikite į **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Bandymo grupės**.
1. Veiksmų juostoje rinkitės **Naujas** norėdami įtraukti eilutę į tinklelį viršutinėje puslapio dalyje. Tada nustatykite šiuos laukus naujai eilutei:

    - **Bandymo grupė** – įveskite unikalų bandymo grupės ID arba pavadinimą.
    - **Aprašas** – įveskite išsamų bandymo grupės aprašą.
    - **Priimtinas kokybės** lygis – įveskite bendrą bandymo rezultatų, kurie turi būti laikomi sėkmingai patvirtintais, grupės procentinę dalį.
    - **Prekės** ėmimas – pasirinkite prekės pavyzdžių ėmimą. Daugiau informacijos ieškokite Kokybės [prekės bandymo valdymo tikrinimo](quality-item-sampling.md) priemonės.
    - **Ardomasis – pasirinkite šį žymės langelį, jei norite** nurodyti, kad tikrinimo grupė užtruks tikrinamas prekes.

1. Kol nauja eilutė vis dar pasirinkta, **viršutinėje** puslapio dalyje pasirinkite skirtuką Bendra. Čia kartojami kai kurie skirtuke Peržiūra pasirinktos **bandymo** grupės parametrai. Taip pat, galite nustatyti tolesnius laukelius grupei:

    - **Atnaujinti atsargų paketo atributą – kai čia nustatote šią pasirinktį kaip Taip, jis bus automatiškai nustatytas kaip Taip kiekvienam naujam bandymui, kuris įtraukiamas į bandymo** grupės *apatinėje* puslapio *dalyje*.
    - **Atnaujinti paketo perdavimą – kai nustatote šią pasirinktį kaip Taip, jei patikrinta prekė yra kontroliuojama paketo, paketo perdavimas bus automatiškai atnaujintas naudojant reikšmę, kuri pasirinkta nesėkmingo kokybės užsakymo paketo perdavimo arba kokybės užsakymo** kokybės *užsakymo* paketo **perdavimo** ir **lauke**.
    - **Nesėkmingo kokybės užsakymo paketo perdavimas – pasirinkite paketo perdavimo kodą, kuris turėtų būti priskirtas, kai kokybės užsakymas, kuriame yra ši bandymo grupė, neatitinka** AQL.
    - **Sėkmingo kokybės užsakymo paketo perdavimas – pasirinkite paketo perdavimo kodą, kuris turėtų būti priskirtas, kai kokybės užsakymas, kuriame yra ši bandymo grupė, atitinka** AQL.
    - **Atnaujinti atsargų būseną – kai nustatote šią pasirinktį kaip Taip, jei atsargų būsena įgalinta patikrintos prekės saugojimo dimensijų grupėje, būsena bus automatiškai atnaujinta naudojant būseną, pasirinktą lauke Nepavyko kokybės** *užsakymo* būsena **kokybės** arba **užsakymo** būsena **būsena**.
    - **Nesėkmingo kokybės užsakymo būsena – pasirinkite atsargų būseną, kuri turėtų būti priskirta prekei, kai kokybės užsakymas, kuriame yra ši bandymo grupė, neatitinka** AQL.
    - **Sėkmingo kokybės užsakymo būsena – pasirinkite atsargų būseną, kuri turėtų būti priskirta prekei, kai kokybės užsakymas, kuriame yra ši bandymo grupė, atitinka** AQL.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Kokybinio tikrinimo įtraukimas į bandymo grupę

Norėdami į bandymo grupę įtraukti kokybės testą, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Bandymo grupės**.
1. Viršutinės **puslapio** dalies skirtuke Peržiūra pasirinkite tikrinimo grupę, į kurią norite įtraukti bandymą.
1. Apatinėje puslapio dalyje, skirtuke **Peržiūra**, pasirinkite Įtraukti į įrankių **juostą**, kad įtraukumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Eilės numeris** – įveskite sloginius skaičius, jei norite nurodyti užsakymą, pagal kurį turi būti atliekami bandymai. Bandymai, kurių eilės numeriai mažesni, bus paleisti prieš bandymus, kurių eilės numeris didesnis.

        > [!NOTE]
        > Rekomenduojame palikti tarpą tarp eilės numerių. Pavyzdžiui, nustatykite pirmojo tikrinimo sekos numerio lauką kaip 10, tada kiekvieno papildomo tikrinimo **vertę** *padidinate* 10. Tokiu būdu vėliau naujas paieškas galėsite įtraukti nenaudodami ir iš naujo sukurdami eilutes, kad jos būtų nurašomos norima tvarka.

    - **Bandymas** – Pasirinkti bandymą, kurį norite atlikti. Kokybės bandymui, rinkitės bandymą, kai **Tipas** laukelis nustatytas į *Parinktis*.
    - **Galiojantis** – Pasirinkite pirmą datą, kai bandymas galioja. Jei apribojimo nereikia, palikite laukelį tuščią.
    - **Galiojimo pabaiga** – Pasirinkite paskutinę datą, kai bandymas galioja. Jei paliekate šį lauką tuščią arba nustatote jį kaip *Niekada*, limito nėra.
    - **Tikrinimo vertės nustatymas** – pasirinkite, kaip turi būti nustatomas PKL, kai įrašomi keli to paties tikrinimo rezultatai. Kokybinio tikrinimo atveju galima *pasirinkti* tik Rankinį. Jei pasirenktate vieną iš kitų verčių (*Vidurkis*, *Minimali* ar *Maksimali*), gausite klaido pranešimą įrašinėdami bandymo grupę.
    - **Atributas – jei norite įrašyti paketo atributo bandymo rezultatus, čia pasirinkite atributą ir pažymėkite žymės langelį Atnaujinti** atsargų **paketo** atributą.
    - **Naujinti atsargų paketo atributą** – Rinkitės šį žymimą laukelį, kad rašytumėte bandymo rezultatus paketo atributui, kuris pasirinktas **Atributo** laukelyje.

1. Apatinėje puslapio dalyje pasirinkite skirtuką **Bendra**. Čia kartojami kai kurie skirtuke Peržiūra **pasirinkto** tikrinimo parametrai. Taip pat, galite nustatyti tolesnius laukelius bandymui:

    - **Analizės sertifikato ataskaita – nustatykite šią pasirinktį kaip Taip, norėdami nurodyti, kad tikrinimo rezultatai turi būti spausdinami analizės** *sertifikate* (CoA). Ši ataskaita gali būti generuojama iš kokybės užsakymo.
    - **Veiksmas trikties metu – pasirinkite Priimti arba Neišlaikyti, norėdami nustatyti, ar tikrinimas turi būti pamestas, ar** ar *neišlaikytas* jo *AQL* nėra įvykdytas.
    - **Priimtinas kokybės** lygis – įveskite bendrą bandymo rezultatų, kurie turi būti laikomi sėkmingai patvirtintais, bandymo procentinę dalį.

1. Apatinėje puslapio dalyje, skirtuke **Tikrinimas**, nustatykite šiuos laukus:

    - **Kintamasis** – Rinkitės bandymo kintamąjį, kad įrašytumėte kokybės bandymo rezultatus.
    - **Numatytasis rezultatas** – pasirinkite numatytąjį rezultatą, kuris turėtų būti įrašytas tikrinimo rezultatams.
    - **Bandymo instrumentas** – pasirinkite prietaisą, kuris turi būti naudojamas bandymams. Jei nurodytas tikrinimo prietaisas, jis automatiškai įvedamas bandymui bandymo grupėje.

1. Uždarykite puslapį.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Kokybinio bandymo įtraukimas į bandymo grupę

Norėdami į bandymo grupę įtraukti kokybės testą, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Bandymo grupės**.
1. Viršutinės **puslapio** dalies skirtuke Peržiūra pasirinkite tikrinimo grupę, į kurią norite įtraukti bandymą.
1. Apatinėje puslapio dalyje, skirtuke **Peržiūra**, pasirinkite Įtraukti į įrankių **juostą**, kad įtraukumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Eilės numeris** – įveskite sloginius skaičius, jei norite nurodyti užsakymą, pagal kurį turi būti atliekami bandymai. Bandymai, kurių eilės numeriai mažesni, bus paleisti prieš bandymus, kurių eilės numeris didesnis.

        > [!NOTE]
        > Rekomenduojame palikti tarpą tarp eilės numerių. Pavyzdžiui, nustatykite pirmojo tikrinimo sekos numerio lauką kaip 10, tada kiekvieno papildomo tikrinimo **vertę** *padidinate* 10. Tokiu būdu vėliau naujas paieškas galėsite įtraukti nenaudodami ir iš naujo sukurdami eilutes, kad jos būtų nurašomos norima tvarka.

    - **Bandymas** – Pasirinkti bandymą, kurį norite atlikti. Kokybės bandymui, pasirinkite bandymą, kai **Tipas** laukelis nustatytas į *Frankcija* ar *Sveikas skaičius*.
    - **Galiojantis** – Pasirinkite pirmą datą, kai bandymas galioja. Jei apribojimo nereikia, palikite laukelį tuščią.
    - **Galiojimo pabaiga** – Pasirinkite paskutinę datą, kai bandymas galioja. Jei paliekate šį lauką tuščią arba nustatote jį kaip *Niekada*, limito nėra.
    - **Tikrinimo vertės nustatymas** – pasirinkite, kaip turi būti nustatomas PKL, kai įrašomi keli to paties tikrinimo rezultatai. Galimos pasirinktys *yra* Vidurkis, *Minimalus*, *Maksimalus* ir *Rankinis*.
    - **Atributas – jei norite įrašyti paketo atributo bandymo rezultatus, čia pasirinkite atributą ir pažymėkite žymės langelį Atnaujinti** atsargų **paketo** atributą.
    - **Naujinti atsargų paketo atributą** – Rinkitės šį žymimą laukelį, kad rašytumėte bandymo rezultatus paketo atributui, kuris pasirinktas **Atributo** laukelyje.

1. Apatinėje puslapio dalyje pasirinkite skirtuką **Bendra**. Čia kartojami kai kurie skirtuke Peržiūra **pasirinkto** tikrinimo parametrai. Taip pat, galite nustatyti tolesnius laukelius bandymui:

    - **Analizės sertifikato ataskaita – nustatykite šią pasirinktį kaip Taip, norėdami nurodyti, kad tikrinimo rezultatai turi būti spausdinami analizės** *sertifikate* (CoA). Ši ataskaita gali būti generuojama iš kokybės užsakymo.
    - **Veiksmas trikties metu – pasirinkite Priimti arba Neišlaikyti, norėdami nustatyti, ar tikrinimas turi būti pamestas, ar** ar *neišlaikytas* jo *AQL* nėra įvykdytas.
    - **Priimtinas kokybės** lygis – įveskite bendrą bandymo rezultatų, kurie turi būti laikomi sėkmingai patvirtintais, bandymo procentinę dalį.

1. Apatinėje puslapio dalyje, skirtuke **Tikrinimas**, nustatykite šiuos laukus:

    - **Standartinis** – įveskite sumą (s integer arba trupmeną), kuri turi būti skirta tikrinimo rezultatams. Jūsų įvesta vertė bus įvesta kaip numatytoji tikrinimo rezultatuose. Be to, ji bus automatiškai įvesta kaip numatytoji vertė laukuose **Minimalus** ir **Maksimalus**.
    - **Min.** – įveskite mažiausią leidžiamą tikrinimo rezultatų vertę. Jūsų įvedama vertė turi būti mažesnė už sumą, nustatytą lauke **Standartinis**. Atnaujinus lauką **Minimalus**, automatiškai **atnaujinamas laukas Min.** leistinas nuokrypis (%) . Taip pat, atnaujinus lauką **Minimalus**, automatiškai **atnaujinamas laukas Min.** leistinas nuokrypis (%) .
    - **Maks.** – įveskite didžiausią leidžiamą tikrinimo rezultatų vertę. Jūsų įvedama vertė turi būti didesnė už sumą, nustatytą lauke **Standartinis**. Atnaujinus lauką **Maksimalus**, automatiškai **atnaujinamas laukas Maks.** leistinas nuokrypis (%) . Taip pat, atnaujinus lauką **Maksimalus**, automatiškai **atnaujinamas laukas Maks.** leistinas nuokrypis (%) .
    - **Bandymo instrumentas** – pasirinkite prietaisą, kuris turi būti naudojamas bandymams. Jei nurodytas tikrinimo prietaisas, jis automatiškai įvedamas bandymui bandymo grupėje.

1. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo bandymo instrumentai](quality-management-processes.md)
- [Kokybės valdymo bandymai](quality-management-processes.md)
- [Kokybės valdymo bandymo kintamieji](quality-management-processes.md)
- [Kokybės susiejimai](quality-management-processes.md)
- [Paketo atributai](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
