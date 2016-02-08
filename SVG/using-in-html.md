//@TODO Перечитать статьи, выбрать актуальное, протестить, дополнить.
# Использование SVG в HTML

Нормальный способ (в смысле, с нормальным фолбэком) это вставлять внутрь SVG fallback-картинку под старые браузеры.
"Старички" игнорируют ```<svg></svg>``` и парсят ```<image>``` как синоним ```<img>```. 

Семантично можно использовать для иллюстраций / логотипов. 


## SVG как файл:
```HTML
<svg width="96" height="96">
    <image xlink:href="svg.svg" src="svg.png" width="96" height="96"/>
</svg >
```
Cовременные браузеры будут парсить xlink:href, остальные по src.

## Инлайн SVG 
```HTML
<svg height="16" width="16">
    <path d="M5 1v14l9-7"/>
    <image src="next.png">
</svg>
```
Тут все аналогично. xlink:href отсутствует, значит современные браузеры ничего не отобразят, кроме path.

## Problems?
* IE грузит оба файла.
* Что-то еще


## Ссылки
 * [Найдено тут](http://lynn.ru/examples/svg/)
 * [Полезности по SVG у @mista_k](https://noteskeeper.ru/tag/svg/)
 * [Styling SVG <use> Content with CSS](http://tympanus.net/codrops/2015/07/16/styling-svg-use-content-css/)
 * [Quick Tip: SVG <use> Style Two Colors](http://codepen.io/FWeinb/post/quick-tip-svg-use-style-two-colors)
