---
title: B2B DUK svetainių „Commerce“ katalogai
description: Šiame straipsnyje pateikiamas atsakymas į dažnai užduodamus klausimus apie Microsoft Dynamics 365 Commerce katalogus.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: af69c3d27142a961049470dd1292ffbc3d8387a9
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027373"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>B2B DUK svetainių „Commerce“ katalogai

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiamas atsakymas į dažnai užduodamus klausimus apie Microsoft Dynamics 365 Commerce [katalogus "verslas verslui" (B2B)](catalogs-b2b-sites.md).

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Kodėl nesukonfigūruota konkrečiai katalogui būsi naršymo hierarchija ar peržiūrėti pasirinktį, kaip susieti klientų hierarchiją?

Įsitikinkite, kad **"Commerce Headquarters" funkcijų valdymo srityje įgalintas** **kelių katalogų** naudojimas mažmeninės prekybos kanaluose. Be to, įsitikinkite, kad jūsų aplinkoje naudojama "Commerce" 10.0.27 arba naujesnė versija.

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Ar "Commerce" svetainės generatoriuje galima peržiūrėti katalogo hierarchiją ir papildyti kategorijų puslapius?

Taip, "Commerce" svetainių generatoriaus **vartotojai**, kurie turi prieigą prie svetainės generatoriaus puslapio Produktai, gali pasirinkti katalogą ir peržiūrėti konkrečiai katalogui b konkrečią hierarchiją. **Puslapyje Produktai** vartotojai taip pat gali papildyti konkrečios katalogo kategorijos puslapį. Norėdami gauti daugiau informacijos, žr. [Kategorijos nukreipimo puslapio papildymas](enrich-category-page.md). Jei norite turėti konkretų katalogą papildymą, rekomenduojame turėti atskirą ir unikalią to katalogo naršymo hierarchiją.

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Ar B2B pardavėjo pirkimas iš kelių katalogų gali būti vienąkart išregistravimas?

Taip, leidžiama pirkti iš kelių katalogų vieno tikrinimo metu. B2B pirkėjai gali naudoti katalogo indikatorių krepšelio rodinyje, norėdami nustatyti, iš kurių katalogų buvo pridėtos prekės.

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Jei B2B pardavėjas tą pačią prekę perka iš skirtingų katalogų, koks yra numatomas jų veikimas?

Nors duotas vartotojas gali turėti prieigą prie kelių katalogų tam tikrą laiką, tikimasi, kad tų katalogų produktai būtų išskirtiniai. Kitaip tariant, geriausia, jei tas pats produktas neturi būti daugiau nei vieno tam vartotojo katalogo dalis.

Tačiau, jei iškyla problema, kai tas pats produktas priklauso keliems katalogams, sistema prižiūrės kelias to produkto krepšelio eilutes. Kiekvienam katalogui bus skirta atskira eilutė. Tas pats produktas iš dviejų skirtingų katalogų nebus sulietas išregistravimas.

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Kai B2B pirkėjas gali pirkti, ar nėra katalogo pasiekiamumo patikrinimo?

Taip. B2B pirkėjams bus leidžiama toliau tikrinti tik tuo atveju, jei visos krepšelio prekės yra iš galiojančio katalogo. Jei kurios nors krepšelio prekės nebegalioja arba yra atmestos į katalogus, jos bus pašalintos ir apie tai bus pranešta vartotojui.

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Ar pirkimo patirties metu ar su ieška ir produkto aptikimu (įskaitant susijusius ir rekomenduojamus produktų rinkinius) yra konkretus katalogas?

Taip. Vartotojui iš karto pasirinkus konkretų katalogą, visa pirkimo būsena tampa katalogui bingusi. Šiame lauke yra produktų aptikimo patirties, tokios kaip ieškos pasiūlymai, paieškos rezultatai, kategorijų rezultatai, tikslinimai, kainodara, atributai ir rekomenduojami produktai (pavyzdžiui, naujas, geriausias pardavimas, tendencijų kūrimas, dažnai perkamas kartu ir susiję produktai).

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Ar B2B pardavėjo pirkimas gali būti iš numatytojo asortimento (catalogID=0)?

Ne, B2B pardavėjui neleidžiama pirkti iš numatytojo asortimento. Šis asortimentas skirtas tik anoniminiam naršymui. Jei B2B pardavėjui trūksta katalogo priskyrimų (laukiančių savo administravimo atnaujinimų), jis negalės matyti nė vieno katalogo, iš kurio jis galės pasirinkti, ir nebus matoma nė vieno kategorijų hierarchijos.

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Ar gali rinkodaros turinys būti curated produktui, kuris yra konkretus katalogui?

Šiuo metu produkto papildymas palaikomas tik teritorijoje ir kanalo lygiuose. Kitaip tariant, jei produktas yra papildytas, jis bendrai naudojamas keliuose kataloguose, o atitinkamas to produkto informacijos puslapis (PDP) bus tokiu pat būdu pateikiamas visiems duotos svetainės katalogams.

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Ar katalogo palaikymas galimas ir B2B, ir verslo klientų (B2C) interneto kanalams?

Šiuo metu "Commerce" katalogai skirti dirbti tik su B2B kanalais.

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Ar galima nustatyti konkrečiam katalogui basas / kryžminio pardavimo prekes?

Šiuo metu palaikoma tik susijusių produktų funkcija. Tačiau skambučių centrams galima naudoti perpardacijų ir kryžminio pardavimo prekių konfigūracijas.

Šios funkcijos taip pat palaikomos tik skambučių centruose:

- Katalogo šaltinio kodai
- Šaltinio USD naudojimas išlaidų ir atsakymų tarifams sekti
- Katalogui būsūs užsakymo ir prekės scenarijai
- Katalogo puslapio analizė
- Katalogo užklausos
- Mokėjimo grafikai
- Nemokami produktai, pagrįsti šaltinio kodais

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Ar galime naudoti katalogo šaltinio kodus B2B užsakymams naudodami el. komercijos portalą?

Ne. Katalogo šaltinio kodai palaikomi tik skambučių centro kanaluose.

## <a name="additional-resources"></a>Papildomi ištekliai

[B2B svetainių „Commerce“ katalogų kūrimas](catalogs-b2b-sites.md)

[„Commerce“ katalogų išplečiamumo poveikis, skirtas B2B tinkinimams](catalogs-b2b-sites-dev.md)
