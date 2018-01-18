---
title: Pirkimo sutartys
description: "Šiame straipsnyje pateikta informacija apie pirkimo sutartis. Pirkimo sutartis yra sutartis, kurią pasirašiusi organizacija įsipareigoja per tam tikrą laiką keliais pirkimo užsakymais įsigyti nurodytą kiekį arba sumą. Už šį įsipareigojimą pirkėjas gauna specialias kainas ir nuolaidas."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a47c631b265262f78e0fb3d956a98a7c9e9f5172
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-agreements"></a>Pirkimo sutartys

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikta informacija apie pirkimo sutartis. Pirkimo sutartis yra sutartis, kurią pasirašiusi organizacija įsipareigoja per tam tikrą laiką keliais pirkimo užsakymais įsigyti nurodytą kiekį arba sumą. Už šį įsipareigojimą pirkėjas gauna specialias kainas ir nuolaidas. 

Pirkimo sutartis galima taikyti konkrečiam produktui, konkrečiai produkto piniginei vertei arba konkrečiai produkto piniginei vertei įsigijimo kategorijoje. Pardavimo sutarties kainos ir nuolaidos turi pirmenybę prieš kainas ir nuolaidas, nurodytas bet kuriose esamose prekybos sutartyse.  

Puslapyje **Pirkimo sutartys** galite sukurti, pritaikyti ir vykdyti tolesnius veiksmus dėl pirkimo sutarčių, sudarytų tarp jūsų organizacijos ir kliento. Pvz., sukūrę pirkimo sutartį galite užsakyti tiesiogiai iš jos. Kiekviena pirkimo sutartis turi galiojimo laikotarpį, kurį nustato asmuo, kuriantis pirkimo sutartį. Pageidaujama pirkinio pristatymo data turi būti šiame pirkimo sutarties galiojimo laikotarpyje.  

Kai sukuriate pirkimo sutartį, prieš jai įsigaliojant, turite ją aktyvuoti. Norėdami suaktyvinti pirkimo sutartį, parinktį **Pažymėti sutartį kaip galiojančią** nustatykite į **Taip**.

## <a name="commitment-types"></a>Įsipareigojimo tipai
Kiekviena pirkimo sutarties eilutė įpareigoja ką nors pirkti. Galite naudoti kelių pirkimo užsakymų (PU) eilutes, norėdami įvykdyti įsipareigojimą. Yra keturi įsipareigojimų tipai:

-   **Produkto kiekio įsipareigojimas**– įsigyjate konkretų produkto kiekį.
-   **Produkto vertės įsipareigojimas**– įsigyjate konkrečią produkto valiutos sumą.
-   **Produktų kategorijos vertės įsipareigojimas**– įsigyjate konkrečią valiutos sumą įsigijimo kategorijoje. Suma gali būti katalogo prekių arba prekių ne iš katalogo.
-   **Vertės įsipareigojimas**– įsigyjate konkrečią bet kurio produkto ar produktų bet kurioje įsigijimo kategorijoje valiutos sumą.

## <a name="pricing-terms-for-purchase-agreements"></a>Pirkimo sutarčių kainodaros sąlygos
Kainodaros sąlygos gali skirtis, atsižvelgiant į įsipareigojimo tipą. Pirkimo sutarčių kainodaros sąlygos turi pirmenybę prieš bet kurias kitas kainodaros sąlygas, nustatytas prekybos sutartyse. Toliau pateikiamoje lentelėje aprašomi kainos laukai, kuriuos paveikia kiekvienas įsipareigojimo tipas. Laukuose, kuriuose yra **Taip** užsakymo eilutę galima atnaujinti.

| Įsipareigojimo tipas                   | Vnt. kaina | Kainos vienetas | Nuolaidos procentas | Mokėjimo nuolaidos suma |
|-----------------------------------|------------|------------|------------------|----------------------|
| Produkto kiekio įsipareigojimas       | Taip        | Taip        | Taip              | Taip                  |
| Produkto vertės įsipareigojimas          |            |            | Taip              |                      |
| Produkto kategorijos vertės įsipareigojimas |            |            | Taip              |                      |
| Vertės įsipareigojimas                  |            |            | Taip              |                      |

## <a name="policies-for-purchase-agreements"></a>Pirkimo sutarčių strategijos
Toliau nurodytos strategijos turi įtakos tam, kaip veikia ryšys tarp įsipareigojimo pirkimo sutartimi ir atitinkamos PU eilutės.

-   **Maksimaliai vykdoma**– bendras kiekis arba visų užsakymo eilučių suma negali viršyti susijusiame įsipareigojime nurodyto kiekio arba sumos.
-   **Kaina ir nuolaida fiksuotos** – užsakymo eilutės kaina ir susijusio įsipareigojimo kaina turi būti tokia pati. Jei kaina užsakymo eilutėje pakeičiama, nutraukiama sąsaja su įsipareigojimu. Jei sąsaja su įsipareigojimu nutraukiama, užsakymo eilutė nebepridedama prie įsipareigojimo vykdymo.
-   **Minimali išduodama suma ir Maksimali išduodama suma** – jei suma nurodyta, gaunate pranešimą apie tai, ar galite atlikti kokius pokyčius užsakymo eilutėje, kuriuos atlikus užsakymo eilutė skirtųsi nuo susijusio įsipareigojimo.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Pirkimo sutarčių įvykdymo skaičiavimas
Įvykdymo kiekiai ir sumos rodomi **Įvykdymo** skirtuke, esančiame **Eilučių informacijos** „FastTab‟, **Pirkimo sutarčių** puslapyje.  

**Įvykdymo** srityje rodoma likusi suma ar kiekis, kurio reikia įsipareigojimo įvykdymui.  

**Sutarties** srityje rodomas bendras kiekis arba bendra suma, kuriems yra taikoma pardavimo sutarties eilutė.  

Naudoti PU eilutes ir SF eilutes, kurios turi įtakos skaičiuojant įvykdymą, galite eilutėse arba pirkimo sutarties antraštėje pasirinkdami **Susijusios informacijos** veiksmą.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Pirkimo sutarčių tvirtinimas ir versijų retrospektyva
Patvirtinus pirkimo sutartį esama pirkimo sutarties versija yra saugoma retrospektyvos lentelėje. Jei pakeisite pirkimo sutartį, galite ją patvirtinti dar kartą, norėdami saugoti kitą pirkimo sutarties versiją retrospektyvoje. Jei pirkimo sutarties nepatvirtinote, vis tiek galite ją naudoti, norėdami kurti PU. Tačiau pirkimo sutarties retrospektyvos informacija nesaugoma. Galite peržiūrėti arba spausdinti visas sutarties versijas. Pakeitimais galite pasidalinti su tiekėju, norėdami gauti patvirtinimą.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Pirkimo sutarčių taikymas užsakymo procese
Kurdami PU, jam galite taikyti pirkimo sutartį. Tada į PU antraštę kopijuojama informacija iš sutarties sąlygų, pvz., mokėjimo sąlygos, pristatymo sąlygos ir pristatymo adresas. Jei PU yra viena ar kelios produktų ar kategorijų eilutės, kurioms taikoma sutartis, tose eilutėse naudojamos kainos ir nuolaidos iš pirkimo sutarties. Užsakymo eilutės suma arba kiekis prisideda prie pirkimo sutarties įsipareigojimo įvykdymo. Tame pačiame PU gali būti eilučių, kurios nesusijusios su pirkimo sutartimi ir eilučių, kurios susijusios su pirkimo sutarties įsipareigojimu.  

Pasirinkti pirkimo sutartį galite tik tada, kai kuriate PU. Kai PU sukurtas, pirkimo sutarties pasirinkti negalite.  
Kai kuriose situacijose, kuriose PU kuriami netiesiogiai, galite valdyti, ar „Finance and Operations“ turi automatiškai ieškoti taikytinų pirkimo sutarčių. Pavyzdžiui, galite tai atlikti automatiškai patvirtindami suplanuotus PU arba kurdami PU pagal pirkimo užsakymus.

## <a name="purchase-agreements-and-intercompany-trade"></a>Pirkimo sutartys ir vidinės įmonės prekyba
Vidinės įmonės prekybiniai ryšiai gali būti sukurti tarp tiekėjo ir kliento sąskaitų, esančių skirtinguose juridiniuose subjektuose. Kai sukuriamas vienos iš šalių pardavimo užsakymas arba PU, sukuriama vidinės kompanijos užsakymų grandinė. Užsakymų grandinėje pardavimo užsakymas ir PU yra sukuriami atitinkamuose teisiniuose subjektuose.  

Galite kurti pirkimo sutartį arba pardavimo sutartį vienai savo vidinės įmonės prekybos pusei. Tada galite generuoti atitinkamą pardavimo sutartį arba pirkimo sutartį kitos vidinės įmonės prekybos šalies juridiniame subjekte.  

Jei sukuriate vidinės įmonės PU, kuris naudoja vidinės įmonės pirkimo sutartį viename juridiniame subjekte, atitinkamas vidinės įmonės pardavimo užsakymas naudoja atitinkamos vidinės įmonės pardavimo sutartį kitame juridiniame subjekte. Pardavimo sutarties įsipareigojimų vykdymas ir pirkimo sutarčių vykdymas sinchronizuojami, kaip sinchronizuojami vidinės įmonės pardavimo užsakymas ir vidinės įmonės PU.

## <a name="financial-dimensions-on-purchase-agreements"></a>Pirkimo sutarčių finansinės dimensijos
Galite nukopijuoti finansines dimensijas į dokumento antraštes arba į atskiras pirkimo sutarties eilutes. Jei pakeičiate dimensijas sutarties antraštėje arba sutarties eilutėje, pakeitimas neturi įtakos jokiems išleistiems užsakymams, tačiau jis atsispindės visuose naujuose užsakymuose.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kurti pirkimo sutartį (užduočių vedlys)](tasks/create-purchase-agreement.md)

[Kurti pirkimo leidimo užsakymą iš pirkimo sutarties (užduočių vedlys)](tasks/create-purchase-release-order-purchase-agreement.md)




