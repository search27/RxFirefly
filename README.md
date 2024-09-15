# RxFirefly
* Light Viscosity Polygon Canvas Effect
* CSS + CANVAS

![스크린샷 2024-09-15 오후 3 01 07](https://github.com/user-attachments/assets/7ecd94d3-f191-4d2f-8bc2-8603778bbb6f)
![스크린샷 2024-09-15 오후 3 01 11](https://github.com/user-attachments/assets/a53a525c-8929-43aa-82ce-d0ce88ddd043)
![스크린샷 2024-09-15 오후 3 01 21](https://github.com/user-attachments/assets/c89473ca-8c05-4d36-a5e8-66ec92c27525)
![스크린샷 2024-09-15 오후 3 01 32](https://github.com/user-attachments/assets/bc1860e9-a742-4f8b-8b54-cc4b5ad06dc9)


Support By [ Cloud Rx (<a href='https://rxapis.com'>https://rxapis.com</a>) ].
* Testing is available until the end of the year.

## Table of Contents

- [Rx Firefly](#rx-firefly)
    - [Folder Steps](#folder-steps)
    - [Default Function](#default-function)
    - [Rx Viscosity Polygon](#rx-viscosity-polygon)
    - [Firefly](#firefly)
    - [RxViscosityUtil](#rx-viscosity-util)



### Folder Steps

* step1 : Application Viscosity Polygon + CSS
* step2 : Principle Viscosity Polygon + CSS



### Default Function

* Create Canvas
* func CreateCanvas : (target, canvasCount, resize) return (Array) canvas

```javascript
const canvas = RxFirefly.CreateCanvas(document.body, 2, true);
```


### Rx Viscosity Polygon

* Step Polygon
- Polygon Outside Draw Polygon Step by Step
* Constructor
* new RxFirefly.RxViscosityPolygon(x,y, vertexCount, distance, stepCount, stepDistance)

* func update : ()
* func draw : (ctx)
* func Follow : ({x, y})
* func GetPosition : () return { x, y }
* func SetColor : (color - String)
* func GetColor : () return color

```javascript
const poly = new RxFirefly.RxViscosityPolygon(
    window.innerWidth/2, window.innerHeight /  2,           // x, y
    7,                                                      // Vertex Count
    70,                                                     // Radius Or Distance by Center
    2,                                                      // Step Count : How Many Create Polygon. 1 : 1, 2 : 2
    105                                                     // Step Distance : Increase Distance
);
poly.SetColor(`rgba(255, 255, 255, 0.7)`);
```





### Firefly

* Circle Random Mover
* Constructor
* new RxFirefly.Firefly(x,y, radius)

* func update : ()
* func draw : (ctx)
* func SetEnvironmentInfo : ({x, y, width, height} - Object)
* func GetEnvironmentInfo : () return {x, y, width, height}
* func SetColor : (color - String)
* func GetColor : () return color
* func SetStrokeColor : (color - String)
* func GetStrokeColor : () return color
* func SetStrokeWidth : (Number)
* func GetStrokeWidth : () return Number
* func GetPosition : () return { x, y }


```javascript
const firefly = new RxFirefly.Firefly(window.innerWidth / 2, window.innerHeight / 2, 5 );
firefly.SetColor(`hsla(${Math.random() * 100}, 70%, 70%, 0.8)`);
firefly.SetEnvironmentInfo({
    x : 0, y : 0,
    width : window.innerWidth,
    height : window.innerHeight
});
```



### RxViscosityUtil
* Support Controller
