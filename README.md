## Particles.js - React Component

[![Particles][image]][hyperlink]

  [hyperlink]: https://rpj.bembi.org
  [image]: https://raw.githubusercontent.com/wufe/react-particles-js/master/img/particles.png (Particles)

Implementation in **Typescript** + **React** of [Particles.js](https://github.com/VincentGarreau/particles.js/) by [Vincent Garreau](https://github.com/VincentGarreau).

Checkout the [demo page](https://rpj.bembi.org).

---

## Installation

`npm install https://github.com/kdfwow64/react-particles-js-customization.git`

## How to use

### Code

Example:

```javascript
import Particles from 'react-particles-js';


##### Parameters

+ `shapes_count` (int; default false) - Count of Shapes
+ `circle_shapes` (object) - Shapes
+ `circle_shapes.radius` (int) - radius
+ `circle_shapes.direction` (1 or 2) - gradient direction
+ `circle_shapes.blur` (blur(0px)) - blur range
+ `circle_shapes.shadowBlur` (int) - ShadowBlur range
+ `circle_shapes.shadowColor` (color) - Shadow Color

---

---

#### Line link shadow

Adds blurred shadow to the lines of the canvas.

```js
import Particles from 'react-particles-js';
const particles_options = {
	"particles": {
		"number": {
			"value": 10,
			"density": {
				"enable": false
			}
		},
		"color":{
			"value":"#0c25d9"
		},
		"shape":{
			"type":"circle",
			"stroke":{
				"width":0,
				"color":"#000"
			},
			"polygon":{
				"nb_sides":6
			},
			"image":{
				"src":"img/github.svg",
				"width":50,
				"height":20}
		},
		"size": {
			"value": 100,
			"shapes_count": 5,
			"circle_shapes": [
				{
					"radius": 50,
					"direction": 1, //  x0:0% y0:100% x1:100% y1:0%
					"gradient": {
						'start': 'rgba(0,154,218,0.2)',
						'stop': 'rgba(10,79,213,0.2)'
					},
					"blur": "blur(0px)",
					"shadowBlur": 1,
					"shadowColor": "white"
				},
				{
					"radius": 100,
					"direction": 2, //  x0:0% y0:0% x1:100% y1:100%
					"gradient": {
						'start': 'rgba(255,45,80,0.2)',
						'stop': 'rgba(187,48,97,0.2)'
					},
					"blur": "blur(0px)",
					"shadowBlur": 1,
					"shadowColor": "white"
				},
				{
					"radius": 150,
					"direction": 1, //  x0:0% y0:0% x1:100% y1:100%
					"gradient": {
						'start': 'rgba(255,45,80,0.2)',
						'stop': 'rgba(187,48,255,0.2)'
					},
					"blur": "blur(0px)",
					"shadowBlur": 1,
					"shadowColor": "white"
				},
				{
					"radius": 200,
					"direction": 2, //  x0:0% y0:0% x1:100% y1:100%
					"gradient": {
						'start': 'rgba(255,45,80,0.2)',
						'stop': 'rgba(255,48,97,0.2)'
					},
					"blur": "blur(0px)",
					"shadowBlur": 5,
					"shadowColor": "white"
				},
				{
					"radius": 250,
					"direction": 1, //  x0:0% y0:0% x1:100% y1:100%
					"gradient": {
						'start': 'rgba(255,45,80,0.2)',
						'stop': 'rgba(187,48,255,0.2)'
					},
					"blur": "blur(0px)",
					"shadowBlur": 10,
					"shadowColor": "black"
				}
			],
			"random": true,
			"anim": {
				"speed": 1,
				"size_min": 100
			}
		},
		"line_linked": {
			"enable": false
		},
		"move": {
			"random": true,
			"speed": 0.2,
			"direction": "top",
			"out_mode": "out"
		}
	},
	"interactivity": {
		"events": {
			"onhover": {
				"enable": false,
				"mode": "bubble"
			},
			"onclick": {
				"enable": true,
				"mode": "push"
			}
		},
		"modes": {
			"bubble": {
				"distance": 300,
				"duration": 2,
				"size": 0,
				"opacity": 0
			},
			"repulse": {
				"distance": 400,
				"duration": 4
			},
			"push": {
				"particles_nb": 1
			},
		}
	}
}
class App extends Component{
  
    render(){
        return (
            <Particles 
              params={particles_options}
            />
        );
    };

}
```
