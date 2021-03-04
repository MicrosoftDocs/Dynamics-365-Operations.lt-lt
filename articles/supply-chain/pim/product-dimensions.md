---
title: Produktų dimensijos
description: Yra penkios produkto dimensijos - spalva, konfigūracija, dydis, stilius ir versija. Produktų dimensijos jungiamos į dimensijų grupes, o dimensijų grupės priskiriamos bendriesiems produktams. Produktų dimensijų kombinacijomis nustatoma, kaip apibrėžiami produktų variantai.
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bdfd9482d30bd65cf84fae032df78e1243e05239
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433366"
---
# <a name="product-dimensions"></a>Produktų dimensijos

[!include [banner](../includes/banner.md)]

Yra penkios produkto dimensijos: spalva, konfigūracija, dydis, stilius ir versija. Produktų dimensijos jungiamos į dimensijų grupes, o dimensijų grupės priskiriamos bendriesiems produktams. Produktų dimensijų kombinacijomis nustatoma, kaip apibrėžiami produktų variantai.

Produkto dimensijos – tai charakteristikos, naudojamos produkto variantui nustatyti. Galite naudoti produkto dimensijų derinius produkto variantams nustatyti. Norėdami sukurti produkto variantą, turite nustatyti bent vieną bendrojo produkto dimensiją.

## <a name="product-variants"></a>Produkto variantai

Produkto variantai taip pat vadinami prekėmis. Elementas yra apčiuopiamas produktas, kuris nėra toks pats kaip ir paslauga. Galima taip pat nustatyti pagrindinį produktą su aptarnavimo tipu. Naudodami aptarnavimo tipą, galite nurodyti produkto variantus, kurie apima paslaugas. Pavyzdžiui, galite nurodyti pagrindinį produktą konsultacijos darbui ir produkto variantus darbui, kurį atlieka vyresnieji konsultantai ir jaunesnieji konsultantai.

## <a name="product-dimensions"></a>Produktų dimensijos

Produkto variantas gali būti kuriamas pagal produkto dimensijų reikšmes.

Produkto dimensijos vertė dydžio, spalvos ir stiliaus dimensijoms gali būti sukurti šiose vietose:

- **Dydis** puslapis (**Produkto informacijos valdymas \> Nustatymai \> Dimensijos ir varianto grupės \> Dydžiai**)
- **Spalva** puslapis (**Produkto informacijos valdymas \> Nustatymai \> Dimensijos ir varianto grupės \> Spalvos**)
- **Stiliaus** puslapis (**Produkto informacijos valdymas \> Nustatymai \> Dimensijos ir varianto grupės \> Stiliai**)

Produkto dimensijos vertės konfigūravimo dimensijai yra dažniausiai sukurti naudojant, ar Produkto konfigūravimo įrankį ar Dimensija pagrįsta konfigūravimo įtaisą. 

Produkto versijos yra dažniausiai sukuriams konkrečioms versijoms, nes produktas vystosi jo naudojimo metu. Produkto versijos yra išsamiai aprašytos toliau šioje temoje.

Produkto dimensijos taip pat gali būti kuriamos ir tvarkomos puslapyje **Produktų dimensijos**, kurį galima pasiekti šiose vietose:

- Eikite į **Produkto informacijos valdymas \> Produktai \> Bendrieji produktai**. Veiksmų juostoje pasirinkite **Produkto dimensijos**.
- Eikite į **Produkto informacijas tvarkymas \> Produktai \> Visi produktai ir produkto šeimininkai**. Pasirinkite bendrąjį produktą. Veiksmų juostoje pasirinkite **Produkto dimensijos**.
- Eikite į **Produkto informacijas tvarkymas \> Išleisti produktai**. Pasirinkite bendrąjį produktą. Veiksmų juostoje, **Produkto** skirtuke, **Produkto šeimininkas** grupėje, pasirinkite **Produkto matmenys**.

Variantų, kuriuos galite sukurti prekei, kiekis ribojamas pagal galimų produkto dimensijų derinių kiekį.

> [!TIP]
> Jums naudojant produktą užsakymo eilutėje, pavyzdžiui, pasirenkate produkto matmenis siekiant atpažinti produkto variantą, su kuriuo norite dirbti.

## <a name="example"></a>Pavyzdys

Įmonė parduoda džinsus. Prekė, *Džinsai* naudoja spalvą ir produkto matmenų dydį. Parduodami trijų skirtingų spalvų ir šešių skirtingų dydžių džinsai. Spalvos yra mėlyna, juoda ir ruda. Dydžiai yra XS, S, M, L, XL ir XXL. Ne visi dydžiai yra prienami visų trijų spalvų. Jei visos kombinacijos yra prieinamos, gali būti 18 skirtingų džinsų tipų. Nepaisant to, šiame pavyzdyje tik toliau pateikti devyni produkto variantų deriniai yra sukurti.

| Spalva | Dydis |
|-------|------|
| Mėlyna  | XS   |
| Mėlyna  | Š.    |
| Mėlyna  | P    |
| Juoda | P    |
| Juoda | L    |
| Juoda | XL   |
| Ruda | L    |
| Ruda | XL   |
| Ruda | XXL  |

## <a name="the-version-product-dimension"></a>Produkto matmenų versija

Produkto matmenų versija yra skirta padėti jums palaikyti ir stebėti daugelį produkto versijų per tiekimo grandinę. Versijos sekimas yra itin svarbus gamintojų sėkmei, kurie veikia nuolat besitraukiančio produkto gyvavimo ciklo, pagerintos kokybės ir patikimumo reikalavimų ir padidinto produkto saugos dėmesio pasaulyje.

Kaip įprasti produkto matmenys, versija elgsis panašiai į esančio produkto matmenis (dydis, stilius, spalva ir konfigūravimas). Dėl to, galite naudoti jį kitais tikslais kartu su produkto versijų sekimu.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Produkto matmenų versijos dimensija

#### <a name="before-you-turn-on-the-version-dimension"></a>Prieš jums įjungiant versijo dimensiją

Jums įjungus versijos matmenis, kai kurios funkcijos gali sugesti arba nustoti veikti kaip tikėtasi, jei jūs įdiegsite kitus sprendimus, apimančius atsargų matmenų tinkinimus. Tam, kad versijos matmenys veiktų visiškai, jums gali reikėti atnaujinti tuos sprendimus, taip, kad jie apimtų versijos matmenis jų ataskaitose atsargų matmenyse.

Jums bandant jūsų sprendimą suderinamumui su versijos matmenimis, ieškokite šių elementų:

1. **Funkcionalumas:** Svarbiausia, visi tinkinimai apimantys atsargų matmenis turi būt įvertinti siekiant užtikrinti jų darbą kartu su versijos matmenimis.
1. **Ataskaitos atsargų dimensijoms:** Ieškokite ataskaitų atsargų dimensijoms (tai yra, vietomis, kai matmenimis yra atskirai remiamasi). Ataskaitos `InventDimId` turėtų dirbti ne laukelyje, tačiau ieškokite ataskaitų stiliui ar spalvai. Pavyzdžiui, užsitikrinkite, kad patikrinote tolesnius elementus:

    - API skambučiai išplėstomis klasėmis
    - Visos ataskaitos į konkrečių atsargų matmenis plėtinio kode (Šis kodas turi tekėti kartu su versijos matmenimis ir stiliumi, spalva ir dydžio matmenimis.).

1. **Nuorodos į pasenusius API skambučius:** Savo versijos matmenų įžangoje „Microsoft“ bandė sukurti kuo mažiau pasenusių API. Keli pasenę API atsiųs perspėjimo pranešimą jums įjungus **Produkto matmenų - versijos** konfigūravimo raktą. Iškviečia tuose API, kurie turi būti sutaisyti jūsų plėtinio sprendimuose prieš jums įjungiant versijos matmenims gamybos sistemoje. Čia pateikta versijos konkretūs pasenę API:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Žemėlapiai:** Jei bet kurie žemėlapiai naudoja atsargų dimensijas, atitinkantis susijęs žemėlapio kūrimas su šiais žemėlapiais turi būti atnaujintas taip, kad apimtų versijos matmenis. Praplėstame modelyje ar lentelės plėtiniuose ieškokite lentelių, kuriose laukeliai apima atsargų matmenis.
1. „**Microsoft Dynamics 365 Commerce“ funkcijos:** Jį įjungus, versijos matmenys pasirodys per prekybai priskirtą kodą „Dynamics 365 Supply Chain Management“. Nepaisant to, versijos matmenys nėra dar palaikomi prekybos kanalo duomenų bazėse, elektroninio kasos aparato (EKA) ir „E-commerce“ programose. Šios prekybos programos nepalaikys atsargų pardavimo/siuntimo arba grąžinimo/gavimo vartotojams pagal versijos dimensiją. Atsargų prieinamumo peržvalgos funkcijos negalės išskirti atsargų pagal versijos dimensiją prekybos programose. Šis elgesys atspindi esamą konfigūravimo matmenų elgesį per prekybą.

#### <a name="turn-on-the-version-dimension"></a>Matmenų versijos matmenų įjungimas

Prieš naudodami versijos matmenis, turite jas įjungti savo sistemoje. Šiai užduočiai reikalingos administratoriaus teisės.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.
1. Įjunkite funkciją pavadinimu *Produkto matmenų versija*. (Dėl išsamesnės informacijos, žr. [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Padėkite savo sistemą į [Palaikymo režimą](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
1. **Konfigūravimo raktai** skirtuke išplėskite **Prekyba** ir tuomet pasirinkite žymimą laukelį **Produkto matmenys - versija**.
1. Išjunkite [Palaikymo režimą](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Sritys, kuriose versijos matmenys nėra palaikomi

Tolesnės sritys nepalaiko versijos matmenų, nes šių matmenų nustatymas sukeltų sugedimo pakeitimus:

- Mėnesio pareiškimo objekto kaina
- Išlaidų objektų išrašų podėlis
- MRC prekybos statistika vienai prekei
- Tiekėjų katalogai
- EcoResProductDimensionGroupEntity

Taip pat, užsakymo sukūrimas ir užsakymo apdorojimo funkcijos prekyboje (pavyzdžiui, POS, skambučių centro ir el. prekybos užsakymams) nepalaiko versijos matmenų. Nėra jokios patvirtintos laiko juostos, kai prekybos užsakymai bus praplėsti jų palaikymui.

### <a name="functional-characteristics-of-the-version-dimension"></a>Versijos matmenų funkcijų savybės

Versijos matmenys veikia taip pat kaip kiti produkto matmenys. Nepaisant to, dėl jų ypatingo pobūdžio ir dėl to, kad jie yra skirti palaikyti ir sekti keletą produkto versijų, jie elgiasi šiek tiek kitaip. Čia pateikiame keletą skirtumų ir panašumų:

- **Nėra jokios versijos grupės.**

    Nepaisant to, kad grupių sąvoka egzistuoja dydžiui, spalvai ir stiliui (spalvos grupė, dydžio grupė ir stiliaus grupė), nėra egzistuojančios jokios sąvokos grupės. Grupės leidžia jums iš anksto nustatyti taikomas vertes taip, kad jums, pavyzdžiui, priskiriant spalvos grupę produktui, produktas gali naudoti visas spalvas toje spalvos grupėje. Ši sąvoka netaikoma versijos matmenims, nes versijos, kurias produktas paima nėra iš anksto nustatytas sukuriant produktą. Vietoje to, versijos yra sukuriams per produkto gyvavimo laiką, kaip tai būtina. Dažniausiai, jei produkto forma, atitikimas ir funkcija lieka nepakitę, sukuriate naują versiją vietoje naujo produkto.

- **Produkto varianto pasiūlymai veikia taip kaip jiems dažniausiai įprasta.**

    Produkto varianto pasiūlymai sukurs pasiūlymus visoms versijos matmenų vertėms, taip kaip jie daro kitiems matmenims. Versijos produktų sukūrimo ir išleidimo procesas yra toks pats kaip ir produktų, kurie naudoja kitus matmenis. Jums sukuriant versijų produktą, pirmoji versija (V1) bus sukuriama kaip produkto matmenys ir bus išleisti variantai. Produktui keičiantis reikalinga nauja versija, naujos versijos vertė (V2) bus įtraukta ir būtini variantai bus išleisti. Nėra jokios išimties, kad versijos (V1, V2 ir V3) bus sukuriamos iš anksto produktui.

> [!IMPORTANT]
> Jei įjungiate ir naudojate versijos matmenims, kai kurie sprendimai rodantys atsargų matmenis gali nustoti veikti kaip tikėtasi. Šių problemų patvirtinimui ir išsprendimui, susisiekite su nepriklausomu programinės įrangos tiekėjui (ISV) dėl jūsų paveiktų sprendimų. Dėl platesnės informacijos, žr. [Įjungti versijos matmenis](#enable-version-dim).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]