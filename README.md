# Welkom bij de eerste versie van VR Brandonderzoek. (Proof of Concept).

Dit is een demo van een Virtual Reality omgeving om brandonderzoekers online mee te nemen naar een incident-locatie. Het is een 360 graden galerij. Je navigeert door **de cursor stil te laten staan** op de **oranje knoppen.** 

Dit project is gemaakt in opdracht van Brandweer Rotterdam-Rijnmond van 22 september tot 14 december. [Meer over het project.](https://docs.google.com/document/d/1WU4VQPSPNxa0Wu4xbLuHCb1h7Dva6uuTcB6Cp4ZMAZA/edit?usp=sharing)

**Built with [A-Frame](https://aframe.io/)**

___________________
### ➡ Build status
Version 1 is klaar. Het project heeft verdere development van bekwame Javascript/HTML devs nodig om volledig te maken.
___________________

### ➡ Important to know!

- ⬤ !! **De GUI in de hub doet het nog niet.** Tot zo ver werken alleen de oranje buttons met pijlen. Ik kreeg dit niet gedaan met Javascript, omdat ik (waarschijnlijk) een beginner ben. 
- ⬤ !! Nogmaals, Je navigeert door schermen heen door **de cursor stil te laten staan** op de **oranje knoppen.** 
- ⬤ !! **De foto's kunnen makkelijk veranderd worden.** Dit zijn geen real-time foto's van de Brandweer zelf. Deze zullen zij zelf in het project zetten. Zie de kop ``"veranderen van galerij?"`` voor instructies.
- ⬤ !! **WebXR doet het niet goed op Safari.** Voor Ios users: gebruik Chrome als het kan.
- ⬤ !! Remember: **dit is niet een eindproduct.** Dit is een **begin** van een 360 graden galerij tool waarin operationele medewerkers van de Brandweer online een locatie kunnen bezoeken. Het heeft nog veel verbeteringen en toevoegingen nodig, zoals de GUI, een betere navigatie, een quiz-element, en een map van de locatie(s).

___________________

### ➡ Installeren
WebXR is onder anderen enabled op Oculus Rift, HTC Vive, PlayStation VR, Google Cardboard, Chromium. Vaak hebben deze devices een **browser.** Vul de volgende link in deze browser om te starten: [https://brandweer-vr-onderzoek.glitch.me/](https://brandweer-vr-onderzoek.glitch.me/.) Dat is alles! 
* Ga naar [deze link](http://a-way-to-go.com/webvr/index.html) om te zien hoe WebVR op jouw device werkt. 
* Bezoek [deze site](https://caniuse.com/?search=webxr) om te zien of jouw browser WebXR support.

___________________
### ➡ Known bugs
- Soms **doet de oranje button met de pijl niets** wanneer je er overheen hovert. Voornamelijk degene in het tweede scherm. Beweeg dan weg van de button en probeer het nog een keer. Na twee of drie keer zou hij zeker moeten werken.
- Als er een **zwarte balk** verschijnt in het tweede scherm, betekent dit waarschijnlijk dat je browser moeite heeft met WebXR. Probeer dan Chrome i.p.v Safari of Internet Explorer.
- Op sommige mobiele browsers (vooral Safari) is het niet mogelijk om naar boven en naar beneden te kijken. Dit is een A-Frame bug en kan verholpen worden door de `look-controls` te veranderen. Ik weet niet hoe, vandaar dat dit nog niet gedaan is.
___________________

### ➡ Development: Veranderen van galerij?
Om de 360 graden afbeeldingen te veranderen, hoef je alleen maar een nieuwe asset te uploaden bij `assets`, en deze vervolgens de veranderen in `index.html` Je kopieert de url van de asset. Deze zet je in `src=""`. Elke afbeelding heeft een aparte URL.

````
<a-assets>
        <img id="point1" 
        crossorigin="anonymous" 
        src="https://cdn.glitch.com/d0ec5c38-0f7f-4a26-8acb-0f6626ed597f%2FBackground%20menu.png?v=1606582956177"/>
</a-assets>
````
___________________
### ➡ Development: Veranderen van content in een scherm?
Elk scherm bevindt zich in een eigen `group.` Scherm 1 (menu) is `group1 en point1`, bijvoorbeeld. Elk scherm (`group en point`) heeft een eigen sectie met content in `index.html`. Waar elk scherm begint is aangegeven met comments. In zo'n sectie kan je de code voor hotspots, 3D-modellen, text, enzovoort vinden en zo nodig veranderen. 

>Voorbeeld van een groep:

```
  <!--scherm1: main menu-->
      <a-entity id="spots" hotspots>
        <a-entity id="group-point1">
          <a-image
            spot="linkto:#point2;spotgroup:group-point2"
            position="-1 1 6"
            scale="2 2 2">
          </a-image>
     </a-entity>  
````
___________________

### ➡ Assets & Attribution

> _All 3D assets fall under **Attribution 4.0** –
> "This license lets others distribute, remix, tweak, and build upon someone's work,
> even commercially, as long as they credit them for the original creation. This is
> the most accommodating of licenses offered. Recommended for maximum dissemination
> and use of licensed materials."_

> `Source`: [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)


- **"Fire truck toy model"** by Nico van Dijk -- [https://skfb.ly/69p7R](https://skfb.ly/69p7R) is licensed under CC Attribution.
- **"Fire extinguisher"** by Nick Pekarsky -- [https://skfb.ly/6A9Ds](https://skfb.ly/6A9Ds) is licensed under CC Attribution.
- **"Mark descrip- the fireman"** by yoman564 -- [https://skfb.ly/6TZRL](https://skfb.ly/6TZRL) is licensed under CC Attribution.
- **"AS350 B2"** by ArcheoteryxFr -- [https://skfb.ly/6VsZR](https://skfb.ly/6VsZR) is licensed under CC Attribution.

___________________

### ➡ Thanks
Ik bedank mijn begeleiders op Hogeschool Rotterdam en Brandweer Rotterdam-Rijnmond voor het bewerkstelligen van dit individuele project. Dit project is gedaan voor de minor IT-Innovatie voor Defensie en Veiligheid. 
___________________
### ➡ Author
#### Made by Tony Schrevelius 
##### Signed on 3 december 2020

---
