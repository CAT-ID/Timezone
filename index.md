# World Map Generator 

# WorldMapGenerator is a jQuery-based

![WorldMap](http://i.imgur.com/i22GQ74.png?1)

# Description

This WorldMapGenerator is jquey plugin for creates a Map using SVG using this plugin user can
select and get timezone value of selected area.

# Usage
---------------------
`<script type="text/javascript" src="//cdn.jsdelivr.net/jquery/1/jquery.min.js"></script>`

`<script type="text/javascript" src="[yourpath]/WorldMapGenerator.js"></script>`

 >Select any element you want and create map inside that element

```javascript
$(selector).WorldMapGenerator();
```

> You can customize WorldMapGenerator with options.

```javascript
$(selector).WorldMapGenerator({
        width: 500,
        height: 250,
        hoverColor: '#5A5A5A',
        selectedColor: '#496A84',
        mapColor: '#BBB',
        defaultCss: true,
        quickLink: ["ACT", "CET", "EAT", "EST", "GMT","IST","MST"],
        selectBox: true,
        showHoverText: true
})
```
 >NOTE : No need to include css, it is created inside plugin but if you don't want to create css inside then use **defaultCss:false** and write your css.

# Options
---------------------

* **width** : (type:number) Set width of map.
* **height** : (type:number) Set height of map.
* **defaultCss** : (type:boolean)  No need to include css if it is true
* **hoverColor** :(type:string) It will show color on hover 
* **selectedColor** :(type:string) set selected ** timezone**  color
* **mapColor** :(type:string) set map color
* **quickLink** :(type:Array of string) It will create shortcuts to select zone **["IST","MST".......]** 
* **selectBox** :(type:boolean) If it is **false** select box will not create
* **showHoverText**  : (type:boolean)  If it is **false** hover text is not shown



# Methods
---------------------

###.setValue(string,string)
>```javascript
$(selector).data('WorldMapGenerator').setValue(string,string)
```
>First parameters take timezone string example: 'Asia/Kolkata' so it will select India in map but if you want to select using offset then use.

```javascript
$(selector).data('WorldMapGenerator').setValue('5.5','offset')
```
>or you can select using country also.

```javascript
$(selector).data('WorldMapGenerator').setValue('IN','country')
```

###.getValue()

> It will return object of seleted area:

```javascript
$(selector).data('WorldMapGenerator').getValue()
```
> Return Object
```javascript
{
country: "IN"
offset: 5.5
pin: "373,94"
selected: true
timezone: "Asia/Kolkata"
zonename: "IST"
}
```

## License
---------------------
It is available under the MIT LICENSE
