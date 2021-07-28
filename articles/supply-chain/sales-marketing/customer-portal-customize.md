---
title: Kliento portalo tinkinimas ir naudojimas
description: Šioje temoje paaiškinama, kaip tinkinti kliento portalą po to, kai jis buvo įtrauktas į jūsų sistemą.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b285cefc35654695ee631cc73baa0ccc2c1b5ac9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359890"
---
# <a name="customize-and-use-the-customer-portal"></a>Kliento portalo tinkinimas ir naudojimas

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomi skirtingi kliento portalo puslapiai, kurie iš karto palaikomi. Joje aiškinama, kokia yra šių puslapių paskirtis ir kaip juos galima tinkinti.

Kliento portale iš karto yra pasiekiami keli tinklalapiai ir veiksmai. Toliau pateiktoje svetainės struktūroje pateikiama šių tinklalapių ir veiksmų apžvalga, taip pat vaidmenys, kurie gali atlikti veiksmus.

![Kliento portalo svetainės struktūra.](media/customer-portal-site-map.png "Kliento portalo svetainės struktūra")

## <a name="typical-customizations"></a>Įprasti tinkinimai

Toliau nurodytose temose pateikiama pagrindinė informacija apie „Power Apps“ portalus ir kaip juos tinkinti.

- [Darbas su šablonais](/powerapps/maker/portals/work-with-templates) – Šioje temoje pateikiama bendra apžvalga apie tai, kaip „Power Apps“ portalai veikia ir kaip galite paprastai juos tinkinti.
- [Portalo turinio tvarkymas](/dynamics365/portals/manage-portal-content) – šioje temoje paaiškinama, kaip galite tvarkyti ir tinkinti turinį, kurį pateikiate savo portale.
- [CSS redagavimas](/powerapps/maker/portals/edit-css) – ši tema padeda atlikti sudėtingesnius jūsų portalo vartotojo sąsajos (UI) tinkinimus.
- [Portalo temos kūrimas](/dynamics365/portals/create-theme) – ši tema padeda sukurti jūsų portalo vartotojo sąsajos temą.
- [Kaip paprastai kurti ir rodyti portalo turinį](/dynamics365/portals/create-expose-portal-content) – ši tema padeda jums tvarkyti jūsų portale naudojamus pagrindinius duomenis ir lenteles.
- [Portale naudojamo kontakto konfigūravimas](/powerapps/maker/portals/configure/configure-contacts) – šioje temoje paaiškinama, kaip kurti ir tinkinti vartotojų vaidmenis ir kaip veikia sauga ir autentifikavimas „Power Apps“ portaluose.
- [Lentelių formų ir interneto formų pastabų konfigūravimas portaluose](/powerapps/maker/portals/configure-notes) – šioje temoje paaiškinama, kaip įtraukti dokumentus ir papildomą saugyklą į jūsų portalą.
- [Portalo svetainės klaidų tvarkymas](/powerapps/maker/portals/admin/view-portal-error-log) – šioje temoje paaiškinama, kaip peržiūrėti portalo klaidų žurnalus ir kaip juos įrašyti į „Microsoft Azure“ didelių dvejetainių objektų saugyklos paskyrą.

## <a name="customize-the-order-creation-process"></a>Užsakymų kūrimo proceso tinkinimas

Kai vartotojas pateikia užsakymą naudodamas kliento portalą, užsakymas automatiškai sinchronizuojamas su atitinkama „Dynamics 365 Supply Chain Management“ aplinka. Kadangi vartotojas yra išorinis klientas, nuo jo tyčia paslepiama dalis reikalingos informacijos. Ši informacija bus automatiškai įrašyta, kai forma pateikiama.

Šiame skyriuje parodyta, kaip nustatyti kontaktus, kad būtų išvengta klaidų. Čia paaiškinami automatiškai nustatyti laukai ir kaip prireikus galite modifikuoti tų laukų vertes.

### <a name="the-out-of-box-order-creation-process"></a>Parengtų naudoti užsakymų kūrimo procesas

Čia nurodyti standartiniai užsakymo pateikimo kliento portale veiksmai.

1. Pagrindiniame puslapyje pasirinkite plytelę **Užsakymo kūrimas**, kad kad atidarytumėte **Užsakymo kūrimo** vedlį.
1. Puslapyje **Užsakymo informacija** nustatykite toliau išvardytus laukus.

    - **Pageidaujama gavimo data** – nurodykite pristatymo datą.
    - **Pristatymo adresas** – įveskite adresą, kuriuo turi būti pristatomas užsakymas.
    - **Įmonė** – pasirinkite kliento įmonės pavadinimą. Šis laukas nustatomas automatiškai vartotojams, kurie nėra administratoriai.
    - **Paraiškos numeris** – įveskite užsakymo paraiškos numerį. Šis laukas nėra privalomas.
    - **Siuntimo šalis / regionas** – įveskite šalį arba regioną, į kurį bus pristatomos prekės. Šis laukas nustatomas automatiškai vartotojams, kurie nėra administratoriai.

    ![Informacijos apie užsakymą puslapis.](media/customer-portal-order-information.png "Informacijos apie užsakymą puslapis")

1. Pasirinkite **Toliau**.
1. Puslapyje **Prekės** pasirinkite **Įtraukti prekę**.

    ![Prekių puslapis.](media/customer-portal-items.png "Prekių puslapis")

1. Dialogo lange **Prekės informacija** nustatykite toliau nurodytus laukus.

    - **Produkto pavadinimas** – suraskite ir pasirinkite produktą, kurį norite įtraukti į užsakymą.
    - **Kiekis** – įveskite pasirinkto produkto kiekį.
    - **Vienetas** – nurodykite matavimo vienetą (pavyzdžiui, **vnt.**, **kg** arba **pakuotė**).
    - **Įvertinta grynoji suma** – ši vertė skaičiuojama kaip įvertinta prekės kaina × pasirinkto vieneto kiekis.

    ![Prekės informacijos dialogo langas.](media/customer-portal-item-information.png "Prekės informacijos dialogo langas")

1. Pasirinkite **Pateikti**, kad įtrauktumėte prekę į užsakymą.
1. Pakartokite 4–6 veiksmus, kol įtrauksite visas norimas prekes į užsakymą.
1. Baigę įtraukti prekes, puslapyje **Prekės** pasirinkite **Pirmyn**.
1. Puslapyje **Užsakymo informacija** pateikiama užsakymo suvestinė. Peržiūrėkite užsakymo turinį ir pristatymo informaciją. Jei viskas įvesta teisingai, pasirinkite **Pateikti**, kad pateiktumėte užsakymą.

    ![Įvykdyto užsakymo informacijos puslapis.](media/customer-portal-order-submit.png "Įvykdyto užsakymo informacijos puslapis")

### <a name="standard-data-setup"></a>Standartinių duomenų nustatymas

Siekiant užtikrinti sklandžią vartotojo patirtį, kliento portalas automatiškai įveda kelių privalomų laukų vertes. Šios vertės paremtos užsakymą teikiančio kliento kontakto įraše esančia informacija.

Kiekvienai klientui, kuris naudos kliento portalą užsakymams pateikti, priklausančio [kontakto eilutės](/powerapps/maker/portals/configure/configure-contacts) vertės turi būti nurodytos toliau pateiktuose privalomuose laukuose. To nepadarius įvyks klaidų.

- **Įmonė** – juridinis subjektas, kuriam priklauso užsakymas
- **Potencialus klientas** – kliento paskyra, kuri susijusi su pasirinktu užsakymu
- **Kainoraštis** – tinkintas kliento kainoraštis
- **Valiuta** – kainos valiuta
- **Siuntimo šalis / regionas** – šalis arba regionas, į kurį bus pristatomos prekės

Toliau nurodyti pardavimo užsakymo lentelės laukai nustatomi automatiškai:

- **Kalba** – užsakymo kalba (pagal numatytuosius parametrus vertė paimama iš kontakto įrašo.)
- **Siuntimo šalis / regionas** – šalis ar regionas, į kurį bus pristatytos prekės (pagal numatytuosius nustatymus, vertė paimama iš kontakto įrašo.)
- **Kontaktinis asmuo** – vartotojas, su kuriuo galima susisiekti dėl informacijos apie užsakymą (pagal numatytuosius parametrus ši vertė paimama iš kontakto įrašo.)
- **Įmonė** – juridinis subjektas, kuriam priklauso užsakymas (pagal numatytuosius parametrus ši vertė paimama iš kontakto įrašo.)
- **Potencialus klientas** – kliento paskyra, kuri susieta su užsakymu (pagal numatytuosius parametrus ši vertė paimama iš kontakto įrašo.)
- **SF klientas** – užsakymo atsiskaitymo paskyra (numatytoji vertė, paimta iš kontakto įrašo, yra potencialus klientas.)
- **Pardavimo užsakymo pavadinimas** – pardavimo užsakymo pavadinimas (numatytoji vertė yra **pardavimo užsakymas**.)
- **Valiuta** – kainos valiuta (pagal numatytuosius parametrus ši vertė paimama iš kontakto įrašo.)
- **Kainoraštis** – tinkintas kliento kainoraštis (pagal numatytuosius parametrus vertė paimama iš kontakto įrašo.)
- **Pristatymo adreso aprašas** – pardavimo užsakymo pristatymo adresas (numatytoji vertė yra **pristatymo adreso aprašas**.)

### <a name="modify-the-order-creation-process"></a>Užsakymų kūrimo proceso modifikavimas

Galite laisvai modifikuoti kliento portalo vartotojo sąsajos išvaizdą, jei nepakeičiate pagrindinio užsakymo kūrimo proceso. Jei norite pakeisti užsakymo kūrimo procesą, atminkite kelis dalykus.

Nepašalinkite toliau nurodytų stulpelių iš „Microsoft Dataverse“ esančio pardavimo užsakymo lentelės, nes šie laukai reikalingi norint sukurti pardavimo užsakymą naudojant dvigubo rašymo funkciją.

- **Įmonė** – juridinis subjektas, kuriam priklauso užsakymas
- **Pavadinimas** – pardavimo užsakymo pavadinimas
- **Valiuta** – kainos valiuta
- **Kainoraštis** – tinkintas kliento kainoraštis
- **Siuntimo šalis / regionas** – šalis arba regionas, į kurį bus pristatomos prekės
- **Potencialus klientas** – kliento paskyra, kuri susijusi su pasirinktu užsakymu
- **Kalba** – užsakymo kalba (paprastai ši kalba yra potencialaus kliento kalba.)
- **Pristatymo adreso aprašas** – pardavimo užsakymo pristatymo adresas

Prekėms reikia nurodyti toliau išvardytus stulpelius:

- **Produktas** – užsakomas produktas
- **Kiekis** – pasirinkto produkto kiekis
- **Vienetas** – matavimo vienetas (pavyzdžiui, **vnt.**, **kg** arba **pakuotė**)
- **Siuntimo šalis / regionas** – pristatymo šalis ar regionas
- **Pristatymo adreso aprašas** – užsakymo pristatymo adresas

Turite įsitikinti, kad jūsų kliento portalas pateikia visų šių stulpelių vertes:

Jei norite įtraukti stulpelių į puslapį arba juos pašalinti, žiūrėkite [Sparčiųjų formų kūrimas ar redagavimas, siekiant užtikrinti supaprastintą duomenų įvestį](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Jei norite pakeisti stulpelių išankstines nuostatas ir tai, kaip nustatomos vertės, kai puslapis įrašomas, žiūrėkite toliau pateiktą informaciją „Power Apps“ portalų dokumentacijoje.

- [Išankstinis lauko užpildymas](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Vertės nustatymas įrašius](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Pagrindinio puslapio tinkinimas

Visi kliento portale esantys valdikliai yra įtaisytieji „Power Apps“ portalų valdikliai. Galite juos tinkinti atlikdami tolesnius veiksmus, kurie pateikti temoje [Puslapio kūrimas](/powerapps/maker/portals/compose-page), Power Apps portalų dokumentacijoje.

Vienintelis pasirinktinis valdiklis, įtrauktas į kliento portalo šabloną, naudojamas kuriant plyteles pagrindiniame puslapyje.

![Plytelės pagrindiniame puslapyje.](media/customer-portal-home-page-tiles.png "Plytelės pagrindiniame puslapyje")

Norėdami modifikuoti plyteles, atlikite toliau pateiktus veiksmus.

1. Atidarykite [portalo valdymo programėlę](/powerapps/maker/portals/configure/configure-portal).
1. Kairėje esančioje naršymo srityje pasirinkite **Puslapio šablonai**.

    ![Portalo valdymo naršymo sritis.](media/customer-portal-nav.png "Portalo valdymo naršymo sritis")

1. Pasirinkite puslapio šabloną su pavadinimu **Pagrindinis**.
1. Lauke **Žiniatinklio šablonas** pasirinkite saitą **Pagrindinis**, kad atidarytumėte to puslapio šaltinio kodą.

    ![Žiniatinklio šablono laukas.](media/customer-portal-web-template.png "Žiniatinklio šablono laukas")

1. Dabar turėtumėte matyti visą pagrindinio puslapio šaltinio kodą, kuri galite modifikuoti pagal poreikį.

## <a name="resources"></a>Ištekliai

Norėdami sužinoti daugiau apie tai, kaip galima nustatyti ir tinkinti kliento portalą, žr. toliau pateiktus išteklius.

- [„Power Apps“ portalų dokumentacija](/powerapps/maker/portals/overview)
- [Dvigubo rašymo dokumentacija](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [Apie portalo ciklą](/powerapps/maker/portals/admin/portal-lifecycle)
- [Portalo naujovinimas](/powerapps/maker/portals/admin/upgrade-portal)
- [Portalo konfigūracijos perkėlimas](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Sprendimo ciklo valdymas – „Dynamics 365 for Customer Engagement“ programos](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]