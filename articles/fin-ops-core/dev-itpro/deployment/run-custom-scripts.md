---
title: Paleisti pasirinktinius X++ scenarijus su nuline prastova
description: Šiame straipsnyje aprašoma, kaip įkelti ir paleisti diegiamus paketus, kuriuose yra pasirinktiniai X++ scenarijai, neprivalant sulaikyti sistemos.
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
ms.openlocfilehash: ff01e2ff8ec105603bb91e0b555301f36e8985b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867335"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Paleisti pasirinktinius X++ scenarijus su nuline prastova

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Naudojant šią funkciją galima įkelti ir paleisti diegiamus paketus, kuriuose yra pasirinktiniai X++ scenarijai, neprivalant eiti per vykdymo ciklo tarnybas Microsoft Dynamics (LCS) arba sustabdyti savo sistemą. Dėl to galite pataisyti neesminius duomenų nenuoseklumo atvejus nenuosekluminių trikčių.

X++ scenarijaus naudojimas smulkių duomenų nenuoseklumo koreguoti naudinga, nes paleidus scenarijų sistema automatiškai koreguos visas susijusias lenteles. Šis būdas padeda užtikrinti pataisymų vientisumą ir padeda sumažinti naujų nenuoseklumo pristatyti riziką.

> [!IMPORTANT]
> Ši funkcija skirta tik smulkių duomenų nenuoseklumo koregavimui. Jis negali būti naudojamas šiais ar kitais tikslais:
>
> - Duomenų rinkimas
> - Schemos pakeitimai
> - Duomenų perkėlimas arba kiti ilgalaikiai procesai
> - Duomenų, kuriuos galima koreguoti kitomis priemonėmis, pvz., reguliariais verslo procesais, duomenų nuoseklumo įrankiais ar kitais savitarnos įrankiais, koregavimas
>
> Naudojant šią funkciją įgaliotieji vartotojai tiesiogiai keičia objektus ir jų įrašus, nenaudodami verslo logikos, susijusios su šiais objektais. Dėl šių pakeitimų gali kilti duomenų vientisumo problemų. Todėl jūsų organizacija gali reikalauti, kad prieš paleisdami scenarijų ir (arba) po to gautumėte patvirtinimą ir pasirašytus iš vidinių ir išorinių auditorių (ar kitų ekvivalentinių subjektų). Dėl atitikties priežasčių pakeitimai, kurie turi įtakos kai kurioms charakteristikoms, gali reikėti atitikti išorines ataskaitas (pvz., finansines ataskaitas) arba pranešti valdžios institucijoms. Jūsų organizacija yra tik atsakinga už visus pakeitimus, atliktus jos duomenyse naudojant šią priemonę, bet kokius patvirtinimus ir tų pakeitimų patvirtinimus arba atskleidimo bei atitikimą taikomiems įstatymams. Jūs prisiimate visas su šia funkcija susijusią riziką.

Visi į sistemą įkelti diegtini paketai pereis per privalomą darbo eigą. Siekiant užtikrinti pareigų atskyrimą, siekiant užtikrinti pareigų atskyrimą, vartotojui, kuris nusiunčia diegtinas pakuotes, neleidžiama jo patvirtinti dėl kitų darbo eigos veiksmų. Kitas vartotojas turi jį patvirtinti. Tačiau, kai paketas patvirtinamas, jį įkėlusiems vartotojui bus leidžiama atlikti likusius veiksmus.

Sistemai reikia, kad visi diegtini paketai būtų paleisti per bandomąjį diegimą. Prieš vartotojui leidžiant vykdyti scenarijų gamybos duomenyse, pasirinkdamas Priimti tikrinimo žurnalą vartotojas turi patikrinti, ar **išvestis teisinga**. Jei išeiga neteisinga, vartotojas turi pažymėti pakuotę kaip nepavykusią, pasirinkdamas **Atsidėti**. Šiuo atveju gamybos duomenyse nebus leidžiama vykdyti scenarijaus.

Kiekvienas įkeltas paketas įrašomas į sistemą ir pereina per nustatytą įvykių darbo eigą. Kiekvienam įvykiui sistema išlaikė žurnalą, kuriame yra laiko žyma ir asmens, kuris atliko įvykį, tapatybė. Taip sistema užtikrina, kad yra audito sekimą.

Kaip parodyta šioje iliustracijoje, sistema pateikia išsamią informaciją apie tai, kaip kiekvienas diegtinas paketas buvo paleistas X++ ir kokie objektai buvo sulieti.

![Informacijos apie scenarijų puslapis.](media/script-details.png "Informacijos apie scenarijų puslapis")

## <a name="assign-duties-to-users-to-control-access"></a>Priskirti pareigas vartotojams, kad būtų galima valdyti prieigą

Šioje priemonėje pateikiamos šios pareigos. Administratoriai gali naudoti šias pareigas, kad padėtų valdyti prieigą prie funkcijos.

- **Tvarkyti pasirinktinius scenarijus** – ši pareiga suteikia galimybę įkelti, tikrinti, tikrinti ir vykdyti pasirinktinius X++ scenarijus aplinkose (vartotojo priėmimo \[tikrinti UAT\] ir gamybą).
- **Tvirtinti pasirinktinius scenarijus** – ši pareiga suteikia galimybę patvirtinti įkeltą pasirinktinį X++ scenarijų. Patvirtinimas yra privalomas žingsnis prieš bet kokį scenarijų patikrinti, patikrinti ir paleisti.

Norėdami sumažinti piktavališkas veiksmų riziką, kiekvieną scenarijų turi aiškiai patvirtinti kitas, o ne jį įkėlusis vartotojas. Prieš tai kai galėsite naudoti šią funkciją savo organizacijoje, administratorius turi priskirti šias pareigas bent dviem atitinkamiems ir labai patikimiems vartotojams. Nors vienas vartotojas gali turėti abi pareigas, tas vartotojas vis dar negalės patvirtinti savo scenarijų.

## <a name="create-a-deployable-package"></a>Visuotinai diegiamo paketo kūrimas

Funkcijai reikia įprasto diegti paketo, kurį galima sukurti Visual Studio. Instrukcijų ieškokite [Modelių paketų, kuriuos galima diegti, kūrimas](../deployment/create-apply-deployable-package.md).

Jūsų diegiamame pakete turi būti lygiai viena vykdyklė X++ klasė. Kitaip tariant, jis turi turėti vieną klasę, kurioje yra tokį parašą turėti gali turėti metodas.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Pagrindinio metodo pavadinimas turi būti didžioji raidė.

## <a name="code-example"></a>Kodo pavyzdys

Toliau pateiktame kodo pavyzdyje parodyta, kaip gali susisteminti diegiamą paketą.

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

Šiame sąraše aprašomos geriausios sėkmingo scenarijaus rašymo, vykdymo ir vykdymo praktikos. Sąrašas nėra išsamus ir jis turi būti laikomas tik patarimais.

- **Scenarijaus** pabaigoje įrašykite sėkmės pranešimą. Tokiu būdu galėsite matyti, kad scenarijus buvo rastas be išimčių.
- **Pridėti** aiškų operacijos apimties tvarkymą.
- **Naudoti** esamą verslo logiką, pvz`update()`., metodus **, bet neateina** verslo logikos naudojant `doUpdate()` ir `doInsert()``doDelete()` metodus. Šis būdas padės užtikrinti, kad priklausomi duomenys bus tvarkomi teisingai. Taip pat pastebimai sumažins tolimesnių duomenų nenuoseklumo riziką.
- **Ar** patvirtinti įmonės kontekstą. Šis būdas parodys bendras klaidas, kai vykdomas scenarijus. Pavyzdžiui, ji parodo, ar scenarijus vykdomas ne šioje įmonėje.
- **Negalima** patvirtinti, kad paveiktų įrašų skaičius atitinka jūsų lūkesčius. Šis būdas parodo, ar sistemoje netikėtai pakeisti duomenys, kol scenarijus buvo paruoštas.
- **Kiekvienam** scenarijui naudokite unikalius klasių pavadinimus (pvz., pavadinime įtraukiant darbo elemento nuorodą). Šis būdas apsaugo pavadinimo pasvirio brūkšnio problemas, kai įkeliate scenarijų. Jei reikia naujo scenarijaus paterpto, būtinai suteikite jam naują pavadinimą.
- **Iš** pradžių patikrinkite kiekvieną scenarijų ne gamybos aplinkoje. Numatomo poveikio ir neapsilaikyto susijusio duomenų šalutinio poveikio tikrinimas. Užtikrinkite, kad visi verslo procesai, kurie gali būti paveikti, gali būti sėkmingai ir visiškai užbaigti vėliau.

## <a name="upload-and-run-a-deployable-package"></a>Įkelti ir paleisti diegiamą paketą

Norėdami įkelti ir vykdyti scenarijų, naudokite nurodytą procedūrą.

1. Savo finansų ir operacijų programoje eikite į Sistemos administravimo **periodinių \> užduočių duomenų \> bazės \> pasirinktinius scenarijus**.
1. Pasirinkite **Nusiųsti**.
1. Pasirinkite diegiamą paketą, kurį sukūrėte kaip anksčiau aprašyta šiame straipsnyje. Jums bus pasiūlyta nurodyti scenarijaus paskirtį.
1. Scenarijų dabar turi patvirtinti kitas vartotojas, o ne jį įkėlusis vartotojas. Tvirtintojas turi atlikti šiuos veiksmus:

    1. Pereikite prie **sistemos administravimo periodinių \>\> duomenų bazės pasirinktinių \> scenarijų**.
    1. Pasirinkite scenarijų, kuris bus tvirtinti, tada pasirinkite **Išsami informacija**.
    1. Veiksmų srities skirtuko Proceso darbo **eiga grupėje Pradžia** pasirinkite **Patvirtinti arba** **Atmesti**.**·** Jei pasirenkate **Patvirtinti**, scenarijus pažymimas kaip patvirtintas ir neblokuojamas tikrinti. Jei pasirenkate **Atmesti**, scenarijus yra užrakintas. Abiem atvejais įvykis užregistruojamas ir scenarijaus kopija saugoma sistemoje.

1. Scenarijų reikia patikrinti, siekiant užtikrinti, kad jis ką daro. Testavimo priemonė gali būti ta pati, kaip ir įkėlimo priemonė ar tvirtintojas, arba tai gali būti trečiasis vartotojas, kuris turi reikiamas teises. Testavimo priemonė turi atlikti šiuos veiksmus:

    1. Pereikite prie **sistemos administravimo periodinių \>\> duomenų bazės pasirinktinių \> scenarijų**.
    1. Pasirinkite tikrintitą scenarijų ir pasirinkite Išsami **informacija**.
    1. Veiksmų srities skirtuko Proceso darbo **eiga grupėje Tikrinimas** **pasirinkite Vykdyti** testą **·**. Scenarijus vykdomas laikinoje operacijoje, kurią sistema automatiškai nutrauktų, kol rinks įvairius žurnalus ir SQL sakinius.
    1. Baigę vykdyti scenarijų, peržiūrėkite žurnalus ir patikrinkite, ar rezultatai atitinka jūsų poreikius. Atlikite vieną iš toliau nurodytų veiksmų.

        - Jei tikrinimo rezultatai jus tenkina, pasirinkite Priimti tikrinimo žurnalą veiksmų srities skirtuke Proceso darbo eiga, **·** **·** **kad** būtų leidžiama vykdyti scenarijų. Įvykių žurnalas nurodys faktą, kad scenarijus buvo patikrintas ir nurodys, kas jį ir kada tik išbandė.
        - Jei testo rezultatai jus tenkina, **·** **·** **veiksmų** srities skirtuke Proceso darbo eiga pasirinkite Baigimas, kad scenarijų nebūtų galima vykdyti. Sistema išlaikys scenarijaus kopiją kartu su savo retrospektyvos žurnalu.

1. Kai įsitikinkite, kad scenarijus atitinka jūsų poreikius, norėdami jį vykdyti **pasirinkite** **·** **veiksmų** srities skirtuko Proceso darbo eiga grupėje Vykdyti. Ši komanda daro tą patį patį, kas ir ankstesnis tikrinimas, tačiau operacija bus vykdoma pabaigoje.
1. Baigę vykdyti scenarijų, patikrinkite rezultatą ir patvirtinkite, kad scenarijus veiktų taip, kaip tikėjote. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei rezultatas jus tenkina, **veiksmų srities skirtuke Proceso** **·** **darbo** eiga pasirinkite Paskirtis, išspręsta grupėje Baigti. Įvykių žurnalas nurodys faktą, kad scenarijus įvykdytas sėkmingai ir nurodys, kas patikrino scenarijų ir kada. Scenarijus įrašytas, bet dabar užrakintas ir jo negalima vykdyti dar kartą.
    - Jei rezultatas jums netenkina, **veiksmų srities skirtuko Proceso darbo** **·** **eiga** dalyje Pabaiga pasirinkite Neišspręsta paskirtis. Įvykių žurnalas nurodys faktą, kad scenarijus neatitiko numatytos paskirties, ir nurodys, kas ir kada įvykdys scenarijų. Scenarijus įrašytas, bet dabar užrakintas ir jo negalima vykdyti dar kartą. Tačiau sistema automatiškai neat anuliuos scenarijaus veiksmo. Gali tekti rašyti, importuoti ir vykdyti naują scenarijų, kad būtų anulitas nepavykusio scenarijaus poveikis jūsų sistemai.

Jūsų pasirinkimas paskutiniame veiksme apibrėžia galutinę scenarijaus būseną. Jei reikia, galite pakartoti procesą.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Įkelti ir paleisti diegiamą paketą naudojant LCS

Užuot dislokuoti savo diegiamą paketą naudodami savo finansų ir operacijų programos vartotojo sąsają, kaip aprašyta ankstesniame skyriuje, galite jį įkelti į LCS ir naudoti įprastą procedūrą jai įdiegti. Norėdami gauti daugiau informacijos, [įdiekite diegiamus paketus iš komandų eilutės](../deployment/install-deployable-package.md).

Nors šis būdas turi mažiau apribojimų, jis mažiau apsaugoti nuo klaidų. Be to, kadangi serverius reikia paleisti iš naujo, tai gali sukelti prasto laiko.
