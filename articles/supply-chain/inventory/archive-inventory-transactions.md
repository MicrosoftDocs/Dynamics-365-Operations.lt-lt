---
title: Archyvuoti atsargų operacijas
description: Šioje temoje aprašoma, kaip archyvuoti atsargų operacijų duomenis, kad būtų pagerintas sistemos našumas.
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b766d306f31fc531f33aa29e1f96048bbd90085
ms.sourcegitcommit: e18ea2458ae042b7d83f5102ed40140d1067301a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8736067"
---
# <a name="archive-inventory-transactions"></a>Archyvuoti atsargų operacijas

[!include [banner](../../includes/banner.md)]

Laikui bėgant atsargų operacijų lentelė (`InventTrans`) toliau plečiasi ir sunaudoja daugiau duomenų bazės vietos. Todėl dėl lentelės pateiktos užklausos palaipsniui veiks lėčiau. Šioje temoje aprašoma, kaip galima naudoti atsargų operacijų archyvo priemonę *duomenims apie atsargų operacijas archyvuoti* siekiant pagerinti sistemos našumą.

> [!NOTE]
> Tik finansiškai atnaujintas atsargų operacijas galima suarchyvuoti pasirinktu uždarytu DK laikotarpiu. Norint suarchyvuoti, finansiškai atnaujintų siunčiamų atsargų operacijų išdavimo būsena turi būti *Parduota*, o gavimo atsargų operacijų gavimo būsena turi būti *Nupirkta*.

Archyvuojant atsargų operacijas, visos susijusios operacijos perkeliamos į lentelę `InventTransArchive`. Atsargų išdavimo ir atsargų gavimo operacijos archyvuojamos atskirai, remiantis prekės ID (`itemId`) ir atsargų dimensijos ID (`inventDimId`) kombinacija, o tada jos pateikiamos į išdavimo ir gavimo operacijų suvestinę.

Jei `itemId` ir `inventDimId` kombinacijoje yra tik viena gavimo arba išdavimo operacija, operacija nebus archyvuota.

## <a name="turn-on-the-feature-in-your-system"></a>Funkcijos įjungimas sistemoje

Jei jūsų sistemoje dar nėra funkcijų, aprašytų šioje temoje, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite funkciją *Atsargų operacijų archyvas*. Atkreipkite dėmesį, kad įjungus šią funkciją, jos išjungti nebegalima.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Dalykai, į kuriuos reikia atsižvelgti archyvuojant atsargų operacijas

Prieš archyvuojant atsargų operacijas reikia atsižvelgti į šiuos verslo scenarijus, nes juos paveiks operacija:

- Kai audituojate atsargų operacijas iš susijusių dokumentų, pvz., pirkimo užsakymo eilučių, jos bus rodomos kaip suarchyvuotos. Norėdami peržiūrėti suarchyvuotas operacijas, turite eiti į **Atsargų valdymas\>Periodinės užduotys \>Valyti \> Atsargų operacijų archyvas**.
- Negalima atšaukti suarchyvuotų laikotarpių atsargų uždarymo. Prieš atšaukdami atsargų uždarymą, turite atšaukti atitinkamo laikotarpio atsargų operacijų archyvą.
- Suarchyvuotų laikotarpių standartinių išlaidų konvertuoti negalima. Prieš atlikdami standartinį savikainos konvertavimą, turite atšaukti atitinkamo laikotarpio atsargų operacijų archyvą.
- Atsargų ataskaitos, išgaunamos iš atsargų operacijų, bus paveiktos archyvuojant atsargų operacijas. Šios ataskaitos apima atsargų skirstymo ataskaitą ir atsargų vertės ataskaitas.
- Atsargų prognozės gali būti paveiktos, jei jos paleidžiamos archyvuotų laikotarpių laikotarpiu.

## <a name="prerequisites"></a>Būtinieji komponentai

Atsargų operacijos gali būti suarchyvuotos tik per laikotarpius, kai tenkinamos šios sąlygos:

- DK laikotarpis turi būti uždarytas.
- Atsargų uždarymas turi būti vykdomas archyvo dieną arba laikotarpiu po jos.
- Laikotarpis turi būti bent metus prieš archyvo pradžios laikotarpio datą.
- Neturi būti jokių esamų atsargų perskaičiavimų.

## <a name="archive-inventory-transactions"></a>Archyvuoti atsargų operacijas

Norėdami archyvuoti atsargų operacijas, atlikite toliau nurodytus veiksmus.

1. Eikite į **Atsargų valdymas** \> **Periodinės užduotys** \> **Valymas** \> **Atsargų operacijų archyvų**.

    Rodomas puslapis **Atsargų operacijų archyvas** bei archyvuotų proceso įrašų sąrašas.

    ![Atsargų operacijų archyvo puslapis.](media/archive-inventory-empty.png "Atsargų operacijų archyvo puslapis")

1. Veiksmų srityje pasirinkite **Atsargų operacijų archyvas**, kad sukurtumėte atsargų operacijų archyvas.
1. Dialogo lange **Atsargų operacijų archyvas** „FastTab“ skirtuke **Parametrai** nustatykite šiuos laukelius:

    - **Nuo uždarymo DK laikotarpio pradžios datos** – pasirinkite anksčiausią operacijos datą, kuri bus įtraukta į archyvą.
    - **Iki uždarymo DK laikotarpio pradžios datos** – pasirinkite vėliausią operacijos datą, kuri bus įtraukta į archyvą.

    ![Atsargų operacijų archyvo dialogo langas.](media/archive-inventory-dates.png "Atsargų operacijų archyvo dialogo langas")

    > [!NOTE]
    > Bus galima pasirinkti tik laikotarpius, kurie atitinka [būtinas sąlygas](#prerequisites).

1. Prireikus, „FastTab“ skirtuke **Vykdyti fone** nustatykite paketinio vykdymo informaciją. Atlikite įprastus „Microsoft Dynamics 365 Supply Chain Management“ paketinių užduočių veiksmus.
1. Pasirinkite **Gerai**.
1. Gaunate pranešimą, kuriuo prašoma patvirtinti, kad norite tęsti. Atidžiai perskaitykite pranešimą ir pasirinkite **Taip**, jei norite tęsti.

    Gaunate pranešimą, kuriame teigiama, kad jūsų atsargų operacijų archyvo užduotis buvo įtraukta į paketinių užduočių eilę. Dabar užduotis pradės archyvuoti atsargų operacijas nuo pasirinkto laikotarpio.

## <a name="view-archived-inventory-transactions"></a>Peržiūrėti archyvuotas atsargų operacijas

Puslapyje **Atsargų operacijų archyvas** rodoma visa archyvavimo retrospektyva. Kiekvienoje tinklelio eilutėje rodoma tokia informacija kaip archyvo sukūrimo data, jį sukūręs naudotojas ir jo būsena.

![Atsargų operacijų archyvavimo retrospektyvos puslapis.](media/archive-inventory-full.png "Atsargų operacijų archyvavimo retrospektyvos puslapis")

Norėdami filtruoti tinklelyje rodomus archyvus, puslapio viršuje pateiktame išskleidžiamajame sąraše pasirinkite vieną iš nurodytų verčių:

- **Aktyvūs** – rodyti tik aktyvius archyvus, bet ne atšauktus archyvus.
- **Visi** – rodyti visus archyvus – tiek aktyvius, tiek atšaukus.

Kiekvienam tinklelio archyvui pateikiama ši informacija:

- **Aktyvus** – varnelė rodo, kad archyvas yra aktyvus.
- **Pradžios data** – seniausios operacijos, kurią galima įtraukti į archyvą, data.
- **Pabaigos data** – naujausios operacijos, kurią galima įtraukti į archyvą, data.
- **Suplanuota** – naudotojo, sukūrusio archyvą, paskyra.
- **Įvykdyta** – archyvo sukūrimo data.
- **Atšauktas** – varnelė rodo, kad archyvas buvo atšauktas.
- **Stabdyti dabartinį atnaujinimą** – varnelė rodo, kad archyvavimas vyksta, bet buvo pristabdytas.
- **Būsena** – archyvo apdorojimo būsena. Galimos vertės: *Laukiama*, *Vykdoma* ir *Baigta*.

Įrankių juostoje virš tinklelio yra šie mygtukai, kuriuos galima naudoti darbui su pasirinktu archyvu:

- **Archyvuotos operacijos** – visos pasirinkto archyvo informacijos peržiūra. Rodomame puslapyje **Archyvuotos operacijos** rodomos visos archyvo operacijos.

    ![Archyvuotų operacijų puslapis.](media/archive-inventory-transactions.png "Archyvuotų operacijų puslapis")

    Norėdami peržiūrėti daugiau informacijos apie konkrečias operacijas puslapyje **Archyvuotos operacijos**, pasirinkite tinklelį, o tada, veiksmų srityje pasirinkite **Archyvuotos operacijos duomenys**. Rodomame puslapyje **Archyvuotos operacijos duomenys** rodoma tokia informacija kaip DK registravimas, susijusios papildomos DK nuorodos ir finansinės dimensijos.

- **Archyvavimo pristabdymas** – šiuo metu apdorojamo pasirinkto archyvavimo pristabdymas. Pristabdymas vykdomas tik sugeneravus archyvavimo užduotį. Todėl prieš įsigaliojant pauzei galimas nedidelis uždelsimas. Pristabdžius archyvavimą laukelyje **Stabdyti dabartinį atnaujinimą** pasirodo varnelė.
- **Archyvavimo tęsimas** – šiuo metu apdorojamo pasirinkto archyvavimo vykdymo tęsimas.
- **Atšaukti** – pasirinkto archyvavimo atšaukimas. Archyvavimą galima atšaukti tik jei jo laukelis **Būsena** nustatytas kaip *Baigta*. Atšaukus archyvavimą laukelyje **Atšaukti** pasirodo varnelė.

## <a name="extend-your-code-to-support-custom-fields"></a>Išplečiate kodą, kad būtų palaikomi pasirinktiniai laukai

Jei lentelėje `InventTrans` yra vienas ar daugiau pasirinktinių laukų, gali reikėti išplėsti kodą, kad jį palaikytų, atsižvelgiant į tai, kaip jie pavadinti.

- Jei pasirinktinių laukų iš lentelės `InventTrans` laukų `InventtransArchive` pavadinimai yra tokie patys kaip lentelėje, tai reiškia, kad jie susieti 1:1. Todėl pasirinktinius laukus galite tiesiog įtraukti į `InventoryArchiveFields` lentelės laukų `inventTrans` grupę.
- Jei pasirinktinių laukų pavadinimai `InventTrans``InventtransArchive` lentelėje nesutampa su lentelės laukų pavadinimais, tada, norėdami juos susieti, turite pridėti kodą. Pavyzdžiui, jei `InventTrans.CreatedDateTime` esate iškviestas sistemos laukas, `InventTransArchive` lentelėje turite sukurti lauką su kitu pavadinimu (`InventtransArchive.InventTransCreatedDateTime` pvz.) `InventTransArchiveProcessTask``InventTransArchiveSqlStatementHelper` ir pridėti plėtinius prie laukų ir klasių, kaip parodyta toliau pateiktame pavyzdyje.

Šiame pavyzdyje pateikiamas pavyzdys, kaip į klasę įtraukti reikiamą plėtinį `InventTransArchiveProcessTask`.

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

Šiame pavyzdyje pateikiamas pavyzdys, kaip į klasę įtraukti reikiamą plėtinį `InventTransArchiveSqlStatementHelper`.

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
