---
title: Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale
description: Šiame straipsnyje aprašoma, kaip sukurti arba susieti su Azure Active Directory esamu (Azure AD) įmonės (B2C) nuomininku Microsoft Azure portale.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785828"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti arba susieti su Azure Active Directory (Azure AD) "verslas vartotojui" (B2C) nuomininku Microsoft Azure portale. Norėdami gauti daugiau informacijos, žr [. mokymo programą: sukurkite Azure Active Directory B2C nuomininką](/azure/active-directory-b2c/tutorial-create-tenant).

Norėdami sukurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale, atlikite šiuos veiksmus.

1. Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).
1. „Azure“ portalo meniu pasirinkite **Kurti išteklius**. Įsitikinkite, kad naudojate prenumeratą ir katalogą, kurie bus susieti su jūsų „Commerce“ aplinka.

    ![Išteklių „Azure“ portale kūrimas.](./media/B2CImage_1.png)

1. Eikite į **Tapatybė \> „Azure Active Directory“ B2C**.
1. Kai būsite puslapyje **Kurti naują B2C nuomotoją arba susieti su esamu nuomotoju**, pasirinkite vieną iš toliau apteiktų parinkčių, kuri geriausiai atitinka jūsų įmonės poreikius.

    - **Sukurkite naują Azure AD B2C nuomininką**: naudokite šią parinktį, kad sukurtumėte naują Azure AD B2C nuomininką.
        1. Pasirinkite **Kurti naują „Azure AD“ B2C nuomotoją**.
        1. Dalyje **Organizacijos pavadinimas** įveskite organizacijos pavadinimą.
        1. Dalyje **Pradinis domeno pavadinimas** įveskite pradinį domeno pavadinimą.
        1. Dalyje **Šalis arba regionas** pasirinkite šalį arba regioną.
        1. Pasirinkite **Kurti**, kad sukurtumėte nuomotoją.

     ![Naujo „Azure AD“ nuomotojo kūrimas.](./media/B2CImage_2.png)

     - **Susieti esamą „Azure AD“ B2C nuomotoją su mano „Azure“ prenumerata**: naudokite šią parinktį, jei jau turite „Azure AD“ B2C nuomininką, su kuriuo norite susieti.
        1. Pasirinkite **Susieti esamą „Azure AD“ B2C nuomotoją su mano Azure prenumerata**.
        1. Jei **„Azure AD“ B2C nuomotojas**, pasirinkite atitinkamą B2C nuomotoją. Jei pasirinkimo lauke rodomas pranešimas „Nerasta tinkamų B2C nuomotojų“, neturite tinkamo B2C nuomotojo ir turite sukurti naują.
        1. Jei **Išteklių grupė**, pasirinkite **Kurti naują**. Įveskite išteklių grupės, kurioje bus nuomotojas, **Pavadinimas**, pasirinkite **Išteklių grupės vieta**, tada pasirinkite **Kurti**.

    ![Esamo „Azure AD“ B2C nuomotojo susiejimas su „Azure“ prenumerata.](./media/B2CImage_3.png)

1. Kai sukuriamas naujas „Azure AD“ B2C katalogas (tai gali užtrukti kelias akimirkas), ataskaitų srityje bus pradėtas rodyti saitas į ataskaitų sritį. Šis saitas nukreips jus į puslapį „Sveiki atvykę į „Azure Active Directory“ B2C“.

    ![Naujo katalogo Azure AD saitas](./media/B2CImage_4.png)

> [!NOTE]
> Jei turite kelias savo „Azure“ sąskaitos prenumeratas arba nustatėte B2C nuomotoją nesusiedami su aktyvia prenumerata, nesusiejant su aktyvia prenumerata, juosta **Trikčių diagnostika** jus nukreips, kad susietumėte nuomotoją su prenumerata. Pasirinkite trikčių diagnostikos pranešimą ir sekite instrukcijas, kad išspręstumėte prenumeratos problemą.

Šiame vaizde parodytas „Azure AD“ B2C **Trikčių diagnostika** juosta.

![Įspėjimas, rodantis, kad kataloge nėra aktyvios prenumeratos.](./media/B2CImage_5.png)

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti B2C nuomininkų nustatymo komercijos procesą, tęskite [B2C programos kūrimo procesą](create-b2c-app.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](set-up-b2c-tenant.md)

[B2C programos kūrimas](create-b2c-app.md)

[Vartotojo srauto strategijų kūrimas](create-user-flow-policies.md)

[Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)](add-social-identity-providers.md)

[Naujinti "Commerce Headquarters" naudojant naują Azure AD B2C informaciją](update-hq-aad-b2c-info.md)

[Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje](config-b2c-tenant-site-builder.md)

[Papildoma B2C informacija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
