---
title: Pirkimo užsakymų trikčių diagnostika
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pirkimo užsakymais.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 963a2363ee7cdca6ed25be805e69eeb41331b6f4773c1c59da903fda68ba570b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744755"
---
# <a name="troubleshoot-purchase-orders"></a>Pirkimo užsakymų trikčių diagnostika

Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pirkimo užsakymais.

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a>Veiksmą galima baigti tik tada, kai eilutės numeris yra visiškai paskirstytas.

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a>Kai pirkimo užsakymai importuojami naudojant duomenų valdymą, pirkimo užsakymo eilučių numeriai neatitinka sistemos parametruose nurodyto padidėjimo.

### <a name="issue-description"></a>Problemos aprašas

Numatyta, kad automatiškai sugeneruoti pirkimo užsakymo eilučių, kurios importuojamos per *Pirkimo užsakymo eilučių V2* duomenų objektą, numeriai nenaudoja sistemos parametruose nurodyto sistemos eilutės numerio padidėjimo. Jei kuriate pirkimo užsakymą rankiniu būdu ir pridedate eilutes per vartotojo sąsają (UI), eilučių numeriai yra padidinami tinkamai. Tačiau jei naudojate duomenų valdymo sistemą (DMF), jie nėra padidinami tinkamai.

Ši problema kyla dėl to, kad importuojant eilutes per DMF, jei eilučių numeriai dar nėra priskirti importuotam subjektui, sistema naudoja DMF metodą jiems priskirti. Šis metodas visada padidina eilučių numerius vienu skaičiumi.

### <a name="issue-workaround"></a>Problemos sprendimas

Įsitikinkite, kad norimų eilučių numeriai jau yra pateikti duomenų subjekto eilutės numerio laukuose, kai importuojate pirkimo užsakymų eilutes. Šiuo atveju DMF neperrašys eilučių numerių.

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a>Numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo.

Jei naudojate mokėtojo kodą, kuris skiriasi nuo kliento kodo, numatytoji mokesčių grupė ir numatytoji mokėjimo nuolaida nėra įrašoma iš mokėtojo kodo sukūrus pirkimo užsakymą.

Toks veikimo būdas yra numatytas. Numatytosios mokesčių grupės vertės, mokėjimo nuolaidos ir kita kainos informacija yra paremtos kliento, o ne mokėtojo kodu.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>Pirkimo užsakymo patvirtinimo metu gaunu klaidos pranešimą „Objekto nuoroda nenustatyta”, arba parodoma išimtis „Iškvietimo paskirties vieta pranešė apie išimtį” tiekėjo SF registravimo metu.

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Vienas ar daugiau apskaitos paskirstymų yra paskirstytas per daug arba per mažai.

### <a name="issue-description"></a>Problemos aprašas

Jūs gaunate šią klaidą: „Vienas ar daugiau apskaitos paskirstymų yra paskirstytas per daug arba per mažai.”

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ši problema gali atsirasti dėl pirkimo užsakymo paskirstymų nenuoseklumo.

Norėdami atblokuoti šią problemą ir iš naujo nustatyti pirkimo užsakymą į būseną *Juodraštis*, eikite į **Įsigijimas ir šaltinio pasirinkimas \> Periodinės užduotys \> Valymas \> Pirkimo užsakymo paskirstymo nustatymas iš naujo**. Norėdami gauti daugiau informacijos, peržiūrėkite šį tinklaraščio įrašą: [Pašalinti PO paskirstymo klaidas „Dynamics 365 Supply Chain Management”](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Ar galima rodyti tik savo sukurtus pirkimo užsakymus?

Šiuo metu ši funkcija negalima.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Ar galiu rezervuoti atsargas ir sukurti operacijas su užregistruotomis atsargomis pirkimo užsakyme?

### <a name="issue-description"></a>Problemos aprašas

Net kai pirkimo užsakymo prekių būsena yra *Registruota*, jūs vis tiek galite rezervuoti atsargas. Kitaip tariant, galite sukurti operacijas su užregistruotomis atsargomis.

### <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Sukurkite pirkimo užsakymą.
2. Užregistruokite pirkimo užsakymo eilutę.
3. Atkreipkite dėmesį, kad galite generuoti rezervavimus arba operacijas su užregistruotomis atsargomis.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. Tikimasi, kad užregistruotos prekės faktiškai atvyko į sandėlį arba į atsargas ir todėl jas galima rezervuoti.

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Pirkimo užsakymai neatspindi juridinio subjekto kalbos nustatymų.

### <a name="issue-description"></a>Problemos aprašas

Produkto pavadinimas pirkimo užsakyme rodomas sistemos kalba, o ne kalba, nustatyta juridiniam subjektui, kuriame buvo sukurtas pirkimo užsakymas.

### <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Nustatykite sistemos kalbą į *EN-US* (JAV anglų kalba).
1. Įsitikinkite, kad egzistuoja produktas, kuriame *EN-US* ir *DE* (vokiečių) kalbos yra palaikomos produkto pavadinimo vertimams.
1. Pakeisti juridinio subjekto kalbą į *DE*.
1. Juridiniame subjekte, kuriame *DE* yra nustatyta kaip kalba, sukurkite pirkimo užsakymą, kuriame yra produktas.
1. Atkreipkite dėmesį, kad produkto pavadinimas vis dar rodomas JAV anglų kalba (sistemos kalba).

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. Pirkimo užsakymuose produktas visada rodomas sistemos kalba. Pirkimo užsakymo kalba yra naudojama, kai kuriamas patvirtinimo žurnalas.

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a>Patvirtintų tiekėjų sąrašas pagal produkto objektą neleidžia pakeisti įsigaliojimo datos.

### <a name="issue-description"></a>Problemos aprašas

Produktas turi patvirtintą tiekėją, kurio įsigaliojimo data, pavyzdžiui, yra 2018 m. sausio mėn. 11 d. (*11/01/2018*) ir galiojimo data yra *Niekada*. Jeigu bandysite pakeisti įsigaliojimo datą iki 2018 m. sausio mėn. 10 d. (*10/01/2018*) arba 2018 m. sausio mėn. 12 d., (*12/01/2018*), gausite šią klaidą:

> Negalima sukurti įrašo patvirtintame tiekėjų sąraše (PdsApproveVendorList). Vertė „Galiojimas” turi būti didesnė arba lygi vertei „Įsigaliojimas”.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Galite pratęsti tik tokį laikotarpį, kuriam tiekėjas yra patvirtintas. Galioja šios taisyklės:

- Norėdami pakeisti įsigaliojimo datą taip, kad ji būtų ankstesnė nei bet kuris esamas faktinis prekės tiekėjo įrašas (laikotarpiai), naujo laikotarpio galiojimo pabaigos data turi būti ankstesnė už visas esamų įrašų galiojimo datas.
- Norėdami pakeisti galiojimo datą taip, kad ji būtų vėlesnė nei bet kuris iš esamų laikotarpių, galiojimo data turi būti vėlesnė nei vėliausia data iš esamų įrašų.
- Norėdami sumažinti bendrą laikotarpį, kuriam tiekėjas buvo patvirtintas, turite panaikinti arba modifikuoti esamus įrašus. Taip pat galite naudoti jungiklį **Sutrumpinti** importavimo metu. Šis jungiklis panaikina visus esamus įrašus, esančius patvirtintų tiekėjų pagal prekę lentelėje.

Scenarijaus pavyzdyje, kuris aprašytas problemos aprašyme, kur įrašo įsigaliojimo data yra *11/01/2018* ir galiojimo pabaigos data yra *Niekada* galite importuoti naują įrašą, kurio įsigaliojimo data yra *10/01/2018* ir galiojimo pabaigos data yra *Niekada*. Tačiau negalite sutrumpinti laikotarpio taip, kad įsigaliojimo data būtų atnaujinta į *12/01/2018* per duomenų valdymą. Turite atlikti šį keitimą per vartotojo sąsają.

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a>Pakeitus pristatymo adresą pirkimo užsakymo antraštėje, pristatymo pavadinimas nėra sinchronizuojamas.

### <a name="issue-description"></a>Problemos aprašas

Pirkimo užsakymo antraštėje esantis adresas atnaujinamas į adresą, kuris nėra pristatymo adresas. Nors adresas yra atnaujinamas pirkimo užsakyme, pristatymo pavadinimas nėra atnaujinamas pagal atnaujintą adresą.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. Pasirinktas adresas turi būti klasifikuojamas kaip pristatymo adresas. Kitu atveju pristatymo pavadinimas nėra atnaujinamas pagal pasirinktą adresą.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Ar galima rasti vartotoją, kuris atšaukė pirkimo užsakymą?

Ši informacija sekama tik tada, kai pirkimo užsakymui taikomas pakeitimų valdymas. Jei naudojate keitimų valdymą, galite matyti, kas pateikė pakeitimą (atšaukimą) ir kas jį patvirtino.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]