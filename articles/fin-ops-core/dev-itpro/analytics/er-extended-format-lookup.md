---
title: Elektroninių ataskaitų (ER) išplėstinė formatų peržvalga
description: Šiame straipsnyje aprašoma, kaip ER formato nuorodą galima nustatyti ER formato peržvalga, kai reikalingas formatas saugomas visuotinė saugykla.
author: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: 624f5c347c27cc2075f9602087c1c49e84340565
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274926"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Leidimo nustatyti ER formato nuorodą, pateikiančią užklausą dėl formato bendrojoje saugykloje, suteikimas vartotojams

[!include [banner](../includes/banner.md)]

Elektroninių [ataskaitų](general-electronic-reporting.md) (ER) sistemą galite naudoti siunčiamų dokumentų formatams konfigūruoti, atsižvelgiant į teisinius įvairių šalių / regionų reikalavimus. ER sistemą taip pat galite naudoti, kad sukonfigūruotumėte gaunamų dokumentų analizavimo formatus ir naudotumėte šių dokumentų informaciją programos duomenims papildyti arba atnaujinti. Kiekvienas iš šių formatų gali būti naudojamas jūsų "Dynamics 365" finansų egzemplioriuje gaunamų ir siunčiamų verslo dokumentų tvarkymui kaip tam tikro verslo proceso dalis.

Paprastai turite nurodyti, koks ER formatas turi būti naudojamas konkrečiame verslo procese. Norėdami nurodyti formatą, peržvalgos lauke, sukonfigūruotame nustatant su verslo procesu susijusius parametrus, pasirinkite vieną ER formatą. Šie peržvalgos laukai paprastai įgyvendinami naudojant atitinkamą ER sistemos API. Norėdami gauti daugiau informacijos, žr. [ER sistemos API kodas, kad būtų rodoma formato susiejimo peržvalga](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Pavyzdžiui, sukonfigūravę [užsienio prekybos parametrus](../../../finance/localizations/emea-intrastat.md#set-up-foreign-trade-parameters), turite nustatyti nuorodas į atskirus ER formatus, kurie bus naudojami generuojant Intrastat deklaraciją ir Intrastat deklaracijos kontrolės ataskaitą. Toliau pateiktose ekrano nuotraukose parodyta, kaip ER formatų peržvalgos laukas atrodo puslapyje **Užsienio prekybos parametrai**.

Jeigu dabartiniame „Finance“ egzemplioriuje nėra ER formatų, susijusių su Intrastat verslo procesu, šis peržvalgos laukas bus tuščias.

[![Užsienio prekybos parametrų puslapis, tuščias Ataskaitos formato susiejimo laukas.](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Jeigu dabartiniame „Finance“ egzemplioriuje yra ER formatų, susijusių su Intrastat verslo procesu, šiame peržvalgos lauke pateikiami ER formatai.

[![Užsienio prekybos parametrų puslapis, Ataskaitos formato susiejimo laukas su parinktimis.](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Šioje peržvalgoje pateikiami tik tie ER formatai, kurie jau importuoti į dabartinį „Finance“ egzempliorių. Norėdami [importuoti](./tasks/er-import-configuration-lifecycle-services.md) ER sprendimus į dabartinį „Finance“ egzempliorių, turite turėti teises vykdyti atitinkamą ER sistemos funkciją, kuri palaiko ER sprendimų, kuriuose yra ER formatų, [ciklą](general-electronic-reporting-manage-configuration-lifecycle.md).

Pradedant nuo „Finance“ 10.0.9 versijos (2020 balandžio mėn. leidimo), ER formato peržvalgos, įgyvendinamos naudojant ER sistemos API, vartotojo sąsaja buvo patobulinta. Vis tiek galite pasirinkti esamus ER formatus, kurie yra „FastTab“ **Pasirinkti formato konfigūraciją**. Be to, išplėstinėje peržvalgoje suteikiama nauja parinktis ieškoti bendrojoje saugykloje (BS) norint rasti konkrečių ER formatų. Visi BS esantys ER formatai pateikiami „FastTab“ **Importuoti iš bendrosios saugyklos**.

[![Užsienio prekybos parametrų puslapis, Importavimas iš visuotinės saugyklos "FastTab".](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Panašiai kaip ir „FastTab“ **Pasirinkti formato konfigūraciją**, „FastTab“ **Importuoti iš bendrosios saugyklos** rodomi tik tie ER formatai, kurie taikomi verslo procesui, kuriam šiame peržvalgos lauke yra pasirinktas ER formatas. Šiame pavyzdyje – Intrastat deklaracijos generavimas. ER formatas taikomas įmonei, prie kurios vartotojas yra šiuo metu prisijungęs, atsižvelgiant į įmonės šalies kontekstą.

Kai pasirenkate ER formatą „FastTab“ **Importuoti iš bendrosios saugyklos**, pasirinkta ER formato [konfigūracija](general-electronic-reporting.md#Configuration) importuojama iš BS į dabartinį „Finance“ egzempliorių.

[![Užsienio prekybos parametrų puslapis, Apdorojimo operacijos pastaba.](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Tada, jei importavimas atliekamas sėkmingai, nuoroda į importuotą ER formatą saugoma šiame peržvalgos lauke. Pirmą kartą norėdami pasiekti BS turite pasinaudoti pateiktu saitu ir užsiregistruoti naudoti [Regulatory Configuration Service](https://aka.ms/rcs) (RCS), kuri naudojama prieigai prie BS valdyti.

[![Užsienio prekybos parametrų puslapis, Nuoroda registruotis RCS.](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Pagal numatytuosius nustatymus „FastTab“ **Importuoti iš bendrosios saugyklos** pateikiamas sąrašas ER formatų iš laikinos saugyklos, kuri automatiškai sukuriama pagal BS turinį našumui patobulinti. Tai atsitinka, kai „FastTab“ **Importuoti iš bendrosios saugyklos** atidaromas pirmą kartą, o tai gali užtrukti keletą sekundžių.

Jei „FastTab“ **Importuoti iš bendrosios saugyklos** nematote reikiamo ER formato, bet esate tikri, kad šis ER formatas saugomas BS, pasirinkite parinktį **Sinchronizuoti**. Taip atnaujinsite laikiną saugyklą ir sinchronizuosite ją su dabartiniu BS turiniu.

## <a name="feature-activation"></a>Funkcijų aktyvinimas

Šios funkcijos pasiekiamumas valdomas funkcijoje **Išplėstinė ER formato konfigūracijų peržvalga, leidžianti pateikti užklausą į bendrąją saugyklą**, esančioje puslapyje **Funkcijų valdymas**. Pagal numatytuosius nustatymus ši funkcija įjungta.

[![Puslapis Funkcijų valdymas.](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Saugos klausimai

Teisė **Prižiūrėti konfigūracijų saugyklas** (**ERMaintainSolutionRepositories**) valdo vartotojo, atidarančio ER formatų peržvalgą su įgalintu „FastTab“ **Importuoti iš bendrosios saugyklos**, prieigą prie BS. Kad vartotojai galėtų pasiekti BS turinį iš ER formatų peržvalgų, turite pakeisti saugos parametrus, suteikdami vartotojams teisę **ERMaintainSolutionRepositories** arba tiesiogiai, arba naudodami jau priskirtus vaidmenis ir pareigas.

Toliau pateikiamoje ekrano nuotraukoje parodyta, kaip šią teisę suteikti vartotojams, kuriems priskirtas vaidmuo **Buhalteris**. Šis vaidmuo leidžia vartotojams konfigūruoti užsienio prekybos parametrus ir nustatyti nuorodas į ER formatus laukuose **Failo formato susiejimas** ir **Ataskaitos formato susiejimas** puslapyje **Užsienio prekybos parametrai**.

[![Puslapis Saugos konfigūracija.](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Apribojimai

Prieiga prie BS ER formatų peržvalgoje šiuo metu palaikoma tik ER formatų, naudojamų siunčiamiems dokumentams generuoti, atveju.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Kodėl negaliu pasiekti bendrosios saugyklos iš ER formatų peržvalgos?

Jei įgalinote funkciją **Išplėstinė ER formato konfigūracijų peržvalga, leidžianti pateikti užklausą į bendrąją saugyklą** puslapyje **Funkcijų valdymas**, tačiau vartotojai nemato ER formatų „FastTab“ **Importuoti iš bendrosios saugyklos**, o parinktis **Sinchronizuoti** matoma, bet išjungta, įsitikinkite, kad vartotojui suteikta teisė **Prižiūrėti konfigūracijų saugyklas** (**ERMaintainSolutionRepositories**). Kreipkitės į sistemos administratorių, kad jums būtų suteikta ši teisė.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų (ER) sistemos API](er-apis-app73.md)
- [Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
