---
title: Žiniomis apie atsargas pagrįstas produktų sąrašas
description: Šiame straipsnyje aprašoma, kaip organizacijos gali konfigūruoti produktų sąrašų puslapius savo Microsoft Dynamics 365 Commerce el. komercijos svetainėje, kad būtų žinoma apie atsargas.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473744"
---
# <a name="inventory-aware-product-listing"></a>Žiniomis apie atsargas pagrįstas produktų sąrašas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip organizacijos gali konfigūruoti produktų sąrašų puslapius savo Microsoft Dynamics 365 Commerce el. komercijos svetainėje, kad būtų žinoma apie atsargas. Produktų sąrašo puslapiai apima kategorijos pagal puslapius ir ieškos rezultatų puslapius.

Pirkėjai paprastai tikisi, kad produktų suradimas visoje el. komercijos svetainėje žino atsargas, kad jie galėtų nuspręsti, ką daryti, jei produktas nėra atsargose. " [Commerce" modulio](starter-kit-overview.md) bibliotekos kategorijos ir ieškos rezultatų moduliai gali būti konfigūruoti, kad būtų įtraukti atsargų duomenys. Tokiu būdu jie gali suteikti tokią patirtį:

- Kartu su produktais rodyti atsargų lygio etiketes.
- Slėpti ne atsargose produktus iš produktų sąrašo.
- Perkelti produktus iš atsargų į produktų sąrašo puslapių apačią.
- Palaiko atsargų produktų filtravimą.

Norėdami įgalinti šią patirtį, pirmiausia turite įgalinti išplėstinę **el. komercijos** produktų aptikimo funkciją, kad ji būtų žinoma apie atsargas "Commerce Headquarters".

> [!NOTE]
> Pagal numatytuosius nustatymus "Commerce" versijoje 10.0.29 **ir vėlesnėje versijoje patobulinta el. komercijos** produktų aptikimo funkcija yra įgalinta kaip atsargų funkcija.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Nustatyti atsargų prieinamumo produkto atributą

Žinotų atsargų produktų sąrašas naudoja produkto atributų sistemą. Norint fiksuoti atsargų prieinamumo duomenis, būtina sukurti paskirtą produkto atributą.

Norėdami "Commerce Headquarters" nustatyti atsargų prieinamumo produkto atributą, atlikite šiuos veiksmus.

1. Eikite į **"Retail" \> ir "Commerce Retail" ir "Commerce IT \> Products" ir atsargas \> produkto atributus automatiškai įvesti atsargų lygiu**.
1. Dialogo lange **Automatiškai** įvesti produkto atributus atsargų lygio lauke **Produkto** atributas ir tipo pavadinimas įveskite pasirinktinį skirtojo produkto atributo, kuris bus sukurtas norint fiksuoti atsargų duomenis, pavadinimą.
1. Lauke Atsargos **turimose atsargose pagal** lauką pasirinkite kiekio tipą, pagal kurį turėtų būti skaičiuojamas atsargų lygis: **turimas faktinis** arba bendras **kiekis**.
1. Nustatykite paketinio **vykdymo pasirinktį** kaip **Taip**.
1. Pasirinkite **Gerai**.

> [!NOTE]
> Norėdami nuosekliai apskaičiuoti atsargų lygį savo el. komercijos svetainės puslapiuose, įsitikinkite, kad **pasirenkate** **tą patį kiekio tipą tiek atsargų prieinamumą,** **tiek** pagal lauką Atsargos, pagal produkto atributų lauką Automatiškai įvesti į atsargų lygio užduotį, o atsargų lygį – pagal Komercijos svetainės generatoriaus nustatymą.

Sukūrus paskirtą produkto atributą, kitas žingsnis yra interneto kanalo atributo konfigūravimas.

Norėdami konfigūruoti "Commerce Headquarters" interneto kanalo atributą, atlikite šiuos veiksmus.

1. Pasirinkite **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai**.
1. Pasirinkite interneto kanalą, kad įgalintumėte žinotų atsargų produktų sąrašo patirtį.
1. Pasirinkite ir atidarykite susietą atributų grupę, tada prie jos pridėkite naują produkto atributą.
1. Eikite į **"Retail" ir "Commerce \> Retail" ir "Commerce IT \> Distribution**" grafiką ir vykdykite **užduotį 1150** (**Katalogas**). Rekomenduojame suplanuoti šią užduotį kaip paketinį **procesą, kuris vykdomas tuo pačiu dažnumu kaip ir produkto atributus automatiškai įvesti naudojant atsargų lygio** užduotį.

> [!NOTE]
> Į atributų grupę įtraukę atsargų prieinamumo produkto atributą "Commerce" 10.0.26 ir anksčiau turite **pasirinkti Nustatyti atributo metaduomenis,** o tada įjungti atributą Rodyti **kanale,** **·** **·** **Galima patikslinti ir užklausti naujo produkto atributo parinktis Galima užklausti.**

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Konfigūruoti ne atsargų produktų rodymo elgseną produktų sąrašo puslapiuose

Kai visi ankstesni konfigūravimo veiksmai yra atlikti, kategorijos ir ieškos rezultatų puslapių tikslinimo priemonės turės atsargų filtro pasirinktį. Bus rodoma kiekvienos puslapyje rodomos produkto išklotinės dalies atsargų lygio etiketė.

Kategorijų ir ieškos rezultatų puslapyje produktai rodomi pagrindiniame, o ne produkto varianto lygyje. Atsargų lygis, rodomas kartu su kiekvienu produktu, yra jungtinis atsargų lygis, kurį nustato visų produkto variantų atsargų lygis. Varianto atsargų lygis apskaičiuojamas remiantis turimos to varianto atsargomis, kurios yra "Commerce Headquarters" numatytoje interneto kanalo sandėlyje. Bendrojo produkto atsargų lygis turi dvi galimas vertes, kurios atitinka atsargų ir ne atsargų teigiamas atsargas. Bendrasis produktas laikomas atsargose, kai visų variantų nėra atsargose. Kitu atveju produktas laikomas atsargose. Vertės žymė nuskaitoma iš atsargų lygio [apibrėžimo](inventory-buffers-levels.md). Jei atsargų lygis nėra nustatytas, numatytosios žymės (anglų kalba) yra **galimos ir** **net atsargose**.

Galite konfigūruoti produktų **sąrašo puslapių** parametrų parametrus "Commerce" svetainės generatoriuje, kad kontroliuoti, kaip kategorijos ir paieškos rezultatų puslapyje rodomi produktai, kurių atsargų nėra. Daugiau informacijos žr. [Atsargų parametrų taikymas](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
