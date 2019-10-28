# js-developer

Cieľom úlohy je vytvoriť mini-aplikáciu nákupný košík. Komponent nákupný košík bude vytvorený vo Vue.js frameworku, pomocou vue-cli.  

## vue-cli install
```
yarn global add @vue/cli
```

## Zadanie

1. krok: Narezanie nákupného košíka podľa dizajnu design/cart.xd 
    - dizajn je vytvorený pomocou free softwaru Photoshop XD 
    - stránka bude full page a content bude centrovaný na stred
    - stránka bude responzívna do 320px 
    - stránku bude možné prehliadať na všetkých moderných prehliadačoch (Chrome, Firefox, Safari, Edge)

[logo]: https://raw.githubusercontent.com/m1l4n/riesenia-hr/master/js-developer/design/result.png

2. krok: Interakcia
    - produkty môžu byť definované ako statické pole, viď. v komponente Cart.vue
    - po kliknutí na obrázok produktu, zobraziť galériu (napr. fancybox)
    - input na počet kusov produktu
        - implementovať spinner komponent (napr. jquery spinner)
        - musí byť vždy vyplnený
        - musí obsahovať len číselné hodnoty
        - hodnota inputu nesmie byť menšia ako 1
        - pri zmene počtu kusov, mení sa total produktu a zároveň aj total objednávky
    - odstránenie produktu
        - kliknutím na “x” pri produkte, vymazať celý produkt z nákupného košíka
        - v prípade, že objednávka už nemá žiadny produkt, zobrazí sa informácia o prázdnom košíku
    - formulár na zľavový kupón
        - musí mať vyplnený input pre zľavový kupon pri odoslaní
        - po odoslaní sa zobrazí notifikácia o úspešnom pridaní kupónu a zo sumy Total sa odráta zlava 10 €

## Nepovinné kroky

3. krok: Implementovať pridanie produktu do košíka
    - zobrazovať sa budú všetky dostupné produkty
    - produkt, ktorý nebude v košíku, bude mať namiesto "x", button "Add"
    - do košíka sa pridá toľko ks produktu, koľko uživateľ definuje v quantity inpute
    - po kliknutí na button "Add", produkt sa pridá do košíka. To znamená:
        - button "Add" sa zmení na "x"
        - prepočítajú sa totals objednávky

4. krok: Ukladanie stavu košíka do localStorage
    - ukladať produkty v košíku
    - ich počet kusov
    - použitý kupón
    - stav ukladať pri každej zmene objednávky: pridanie produktu, odstránenie produktu, zmena počtu kusov, pridanie kupónu,...
    - pri každom refreshe stránky zobraziť košík podľa tohto stavu

5. krok: Implementácia jednoduchej API s endpointami na:
    - načítanie zoznamu produktov
    - odoslanie objednávky
    - zisťovanie dostupnosti ks produktu

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
