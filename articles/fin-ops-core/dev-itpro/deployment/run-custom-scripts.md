---
title: Vykdykite pasirinktinius X++ scenarijus be prastovos
description: Šioje temoje aprašoma, kaip įkelti ir paleisti diegiamus paketus, kuriuose yra pasirinktiniai X++ scenarijai, nesustabdant sistemos.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fcd0a472fa5116ca0b3a59561b6eeb72181a9113
ms.sourcegitcommit: 44e6875e974a3a1b3e1d7a24c1a3cff3d3697cdc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2022
ms.locfileid: "8088349"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Vykdykite pasirinktinius X++ scenarijus be prastovos

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Ši funkcija leidžia įkelti ir paleisti diegiamus paketus, kuriuose yra pasirinktiniai X++ scenarijai, jų nereikia atlikti Microsoft Dynamics gyvavimo ciklo paslaugas (LCS) arba sustabdykite savo sistemą. Todėl galite ištaisyti nedidelius duomenų neatitikimus nesukeldami jokių trikdančių prastovų.

X++ scenarijaus naudojimo, siekiant ištaisyti nedidelius duomenų neatitikimus, pranašumas yra tas, kad sistema automatiškai pakoreguos visas susijusias lenteles, kai reikia paleisti scenarijų. Šis metodas padeda užtikrinti korekcijos vientisumą ir padeda sumažinti naujų neatitikimų atsiradimo riziką.

> [!IMPORTANT]
> Ši funkcija skirta tik nedideliems duomenų neatitikimams ištaisyti. Jo negalima naudoti šiais ar kitais tikslais:
>
> - Duomenų rinkimas
> - Schemos pakeitimai
> - Duomenų perkėlimas ar kiti ilgai trunkantys procesai
> - Duomenų, kuriuos galima taisyti kitomis priemonėmis, pvz., įprastiniais verslo procesais, duomenų nuoseklumo įrankiais ar kitais savitarnos įrankiais, taisymas.
>
> Ši funkcija leidžia įgaliotiems vartotojams tiesiogiai keisti objektus ir jų įrašus, nenaudojant su tais objektais susietos verslo logikos. Šie pakeitimai gali sukelti duomenų vientisumo problemų. Todėl jūsų organizacija gali reikalauti, kad prieš ir (arba) paleidus scenarijų gautumėte patvirtinimą ir patvirtinimą iš vidaus ir išorės auditorių (arba kitų lygiaverčių suinteresuotųjų šalių). Siekiant atitikties sumetimais, pakeitimus, turinčius įtakos kai kurioms savybėms, taip pat gali reikėti atskleisti išorinėse ataskaitose (pvz., finansinėse ataskaitose) arba pranešti valdžios institucijoms. Jūsų organizacija yra išimtinai atsakinga už bet kokius jos duomenų pakeitimus, padarytus naudojant šią funkciją, bet kokį tų pakeitimų patvirtinimą, pasirašymą ar atskleidimą ir taikomų įstatymų laikymąsi. Jūs prisiimate visą riziką dėl šios funkcijos naudojimo.

Visi įdiegiami paketai, įkelti į sistemą, pereina privalomą darbo eigą. Saugos sumetimais ir siekiant padėti užtikrinti pareigų atskyrimą, vartotojui, kuris įkelia dislokuojamą paketą, neleidžiama jo patvirtinti kitiems darbo eigos veiksmams. Kitas vartotojas turi tai patvirtinti. Tačiau patvirtinus paketą jį įkėlusiam vartotojui bus leista atlikti likusius veiksmus.

Sistema reikalauja, kad visi diegiami paketai būtų išbandyti. Prieš leisdamas scenarijui paleisti gamybos duomenis, vartotojas turi patvirtinti, kad išvestis yra teisinga pasirinkdamas **Priimti bandymo žurnalą**. Jei išvestis neteisinga, vartotojas turi pažymėti paketą kaip nepavykusį pasirinkdamas **Apleisti**. Tokiu atveju scenarijui nebus leidžiama vykdyti gamybos duomenų.

Kiekvienas įkeltas paketas išsaugomas sistemoje ir praeina apibrėžtą įvykių eigą. Kiekvienam įvykiui sistema saugo žurnalą, kuriame yra laiko žyma ir įvykį atlikusio asmens tapatybė. Tokiu būdu sistema užtikrina audito seką.

Kaip parodyta toliau pateiktoje iliustracijoje, sistemoje pateikiama išsami informacija apie tai, kaip kiekvienas diegiamas paketas buvo paleistas naudojant X++ ir kurie objektai buvo paliesti.

![Scenarijaus informacijos puslapis.](media/script-details.png "Scenarijaus informacijos puslapis")

## <a name="assign-duties-to-users-to-control-access"></a>Priskirkite naudotojams pareigas kontroliuoti prieigą

Ši funkcija atlieka šias pareigas. Administratoriai gali naudoti šias pareigas, kad padėtų kontroliuoti prieigą prie funkcijos.

- **Palaikykite pasirinktinius scenarijus** – Ši pareiga suteikia galimybę įkelti, tikrinti, patikrinti ir paleisti tinkintus X++ scenarijus aplinkoje (vartotojo priėmimo testavimas\[ UAT\] ir gamyba).
- **Patvirtinti pasirinktinius scenarijus** – Ši pareiga suteikia galimybę patvirtinti įkeltą tinkintą X++ scenarijų. Patvirtinimas yra privalomas veiksmas prieš bet kurį scenarijų išbandant, patikrinant ir paleidžiant.

Kad būtų sumažinta kenkėjiškų veiksmų rizika, kiekvienas scenarijus turi būti aiškiai patvirtintas kito vartotojo, o ne jį įkėlusio vartotojo. Kad galėtumėte naudoti šią funkciją savo organizacijoje, administratorius turi priskirti pirmiau nurodytas pareigas bent dviem svarbiems ir labai patikimiems vartotojams. Nors vienas vartotojas gali turėti abi pareigas, jis vis tiek negalės patvirtinti savo scenarijų.

## <a name="create-a-deployable-package"></a>Visuotinai diegiamo paketo kūrimas

Funkcijai reikalingas įprastas įdiegiamas paketas, kurį galima sukurti Visual Studio. Instrukcijas žr [Sukurkite diegiamus modelių paketus](../deployment/create-apply-deployable-package.md).

Jūsų įdiegiamame pakete turi būti tiksliai viena paleidžiama X++ klasė. Kitaip tariant, ji turi turėti vieną klasę, apimančią metodą, turintį tokį parašą.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Pagrindinio metodo pavadinimas turi būti mažosios raidės.

## <a name="code-example"></a>Kodo pavyzdys

Toliau pateiktame kodo pavyzdyje parodyta, kaip galima struktūrizuoti diegiamą paketą.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Geriausia praktika

Šiame sąraše aprašomi keli geriausi sėkmingo scenarijaus rašymo, diegimo ir vykdymo būdai. Sąrašas nėra baigtinis ir turėtų būti laikomas tik gairėmis.

- **Daryk** scenarijaus pabaigoje parašykite sėkmės pranešimą. Tokiu būdu pamatysite, kad scenarijus buvo paleistas be išimčių.
- **Daryk** pridėti aiškų operacijos apimties tvarkymą.
- **Daryk** naudoti esamą verslo logiką, pvz`update()` metodai, bet **nereikia** apeiti verslo logiką naudojant`doUpdate()`,`doInsert()`, ir`doDelete()` metodus. Šis metodas padės užtikrinti, kad priklausomi duomenys būtų tvarkomi teisingai. Tai taip pat žymiai sumažins tolesnių duomenų neatitikimų riziką.
- **Daryk** įtvirtinti įmonės kontekstą. Šis metodas atskleis dažniausias scenarijaus vykdymo klaidas. Pavyzdžiui, jis parodys, ar scenarijus vykdomas netinkamoje įmonėje.
- **Daryk** tvirtinti, kad paveiktų įrašų skaičius atitinka jūsų lūkesčius. Šis metodas parodys, ar duomenys netikėtai pasikeitė sistemoje, kol buvo ruošiamas scenarijus.
- **Daryk** kiekvienam scenarijui naudokite unikalius klasės pavadinimus (pavyzdžiui, į pavadinimą įtraukite nuorodą į darbo elementą). Šis metodas padės išvengti vardų nesuderinamumo problemų, kai įkelsite scenarijų. Jei reikalinga nauja scenarijaus iteracija, būtinai suteikite jam naują pavadinimą.
- **Daryk** Pirmiausia patikrinkite kiekvieną scenarijų ne gamybinėje aplinkoje. Išbandykite, ar nėra numatomo poveikio ir netyčinio šalutinio poveikio susijusiems duomenims. Užtikrinkite, kad vėliau visi verslo procesai, kurie gali būti paveikti, būtų sėkmingai ir visiškai užbaigti.

## <a name="upload-and-run-a-deployable-package"></a>Įkelkite ir paleiskite dislokuojamą paketą

Norėdami įkelti ir paleisti scenarijų, naudokite šią procedūrą.

1. Programoje „Finance and Operations“ eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenų bazė \> Pasirinktiniai scenarijai**.
1. Pasirinkite **Nusiųsti**.
1. Pasirinkite įdiegiamą paketą, kurį sukūrėte, kaip aprašyta anksčiau šioje temoje. Būsite paraginti nurodyti scenarijaus tikslą.
1. Dabar scenarijų turi patvirtinti vartotojas, kuris nėra jį įkėlęs. Tvirtinėjas turi atlikti šiuos veiksmus:

    1. Eiti į **Sistemos administravimas \> Periodinis \> Duomenų bazė \> Pasirinktiniai scenarijai**.
    1. Pasirinkite scenarijų, kurį norite patvirtinti, tada pasirinkite **Detalės**.
    1. Veiksmų srityje, ant **Proceso darbo eiga** skirtuke **Pradėti** grupę, pasirinkite **Patvirtinti** arba **Atmesti**. Jei pasirinksite **Patvirtinti**, scenarijus pažymėtas kaip patvirtintas ir atrakintas testavimui. Jei pasirinksite **Atmesti**, scenarijus užrakintas. Abiem atvejais įvykis registruojamas, o scenarijaus kopija saugoma sistemoje.

1. Scenarijus turi būti išbandytas, siekiant įsitikinti, kad jis atlieka tai, ką jis turi padaryti. Bandytojas gali būti tas pats, kas įkėlėjas ar patvirtinėjas, arba tai gali būti trečiasis naudotojas, turintis reikiamus leidimus. Testuotojas turi atlikti šiuos veiksmus:

    1. Eiti į **Sistemos administravimas \> Periodinis \> Duomenų bazė \> Pasirinktiniai scenarijai**.
    1. Pasirinkite scenarijų, kurį norite išbandyti, tada pasirinkite **Detalės**.
    1. Veiksmų srityje, ant **Proceso darbo eiga** skirtuke **Testas** grupę, pasirinkite **Vykdykite testą**. Scenarijus vykdomas laikinoje operacijoje, kurią sistema automatiškai nutraukia rinkdama įvairius žurnalus ir SQL sakinius.
    1. Kai scenarijus baigsis, peržiūrėkite žurnalus ir patikrinkite, ar rezultatai atitinka jūsų lūkesčius. Atlikite vieną iš toliau nurodytų veiksmų.

        - Jei esate patenkinti bandymo rezultatu, pasirinkite **Priimti bandymo žurnalą** viduje konors **Testas** grupė ant **Proceso darbo eiga** Veiksmų srities skirtuką, kad būtų galima paleisti scenarijų. Įvykių žurnalas atspindės faktą, kad scenarijus buvo išbandytas, ir bus nurodyta, kas ir kada jį išbandė.
        - Jei nesate patenkinti bandymo rezultatu, pasirinkite **Apleisti** viduje konors **Pabaiga** grupė ant **Proceso darbo eiga** Veiksmų srities skirtuką, kad scenarijus nebūtų paleistas. Sistema saugos scenarijaus kopiją kartu su jo istorijos žurnalu.

1. Kai esate tikri, kad scenarijus atitinka jūsų lūkesčius, pasirinkite **Bėk** viduje konors **Bėk** grupė ant **Proceso darbo eiga** Veiksmų srities skirtuką, kad jį paleistumėte. Ši komanda atlieka tą patį, ką ir ankstesnis bandomasis paleidimas, tačiau operacija bus įvykdyta pabaigoje.
1. Scenarijui pasibaigus, patikrinkite rezultatą ir patvirtinkite, kad scenarijus veikė taip, kaip norėjote. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei esate patenkinti rezultatu, pasirinkite **Tikslas išspręstas** viduje konors **Pabaiga** grupė ant **Proceso darbo eiga** Veiksmų srities skirtuką. Įvykių žurnale bus rodomas faktas, kad scenarijus buvo sėkmingai paleistas, ir bus nurodyta, kas ir kada patvirtino scenarijų. Scenarijus išsaugotas, bet dabar jis užrakintas ir negali būti paleistas dar kartą.
    - Jei nesate patenkinti rezultatu, pasirinkite **Tikslas neišspręstas** viduje konors **Pabaiga** grupė ant **Proceso darbo eiga** Veiksmų srities skirtuką. Įvykių žurnalas atspindės faktą, kad scenarijus neatitiko numatyto tikslo, ir bus nurodyta, kas ir kada paleido scenarijų. Scenarijus išsaugotas, bet dabar jis užrakintas ir negali būti paleistas dar kartą. Tačiau sistema automatiškai neatšaukia scenarijaus veiksmo. Gali tekti parašyti, importuoti ir paleisti naują scenarijų, kad panaikintumėte nesėkmingo scenarijaus poveikį jūsų sistemoje.

Jūsų pasirinkimas paskutiniame veiksme apibrėžia galutinę scenarijaus būseną. Galite pakartoti procesą, kaip jums reikia.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Įkelkite ir paleiskite diegiamą paketą per LCS

Užuot diegę diegiamą paketą naudodami programos „Finance and Operations“ vartotojo sąsają, kaip aprašyta ankstesniame skyriuje, galite įkelti jį į LCS ir naudoti įprastą diegimo procedūrą. Daugiau informacijos žr [Įdiekite dislokuojamus paketus iš komandinės eilutės](../deployment/install-deployable-package.md).

Nors šis metodas turi mažiau apribojimų, jis suteikia mažesnę apsaugą nuo klaidų. Be to, kadangi tam reikia iš naujo paleisti visus serverius, tai sukels šiek tiek prastovos.
