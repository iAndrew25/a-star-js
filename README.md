# A* algorithm in JS
Find the shortest path in a matrix.

### Usage
```javascript
const grid = [
	[🍀, 🌲, 🍀, 🍀, 🍀],
	[🍀, 🌲, 🌲, 🍀, 🍀],
	[🍀, 🍀, 🌊, 🍀, 🍀],
	[🍀, 🍀, 🌲, 🌲, 🍀],
	[🍀, 🍀, 🍀, 🍀, 🍀]
];

const legend = {
	🍀: {
		isWalkable: true,
		cost: 1
	},
	🌲: {
		isWalkable: false
	},
	🌊: {
		isWalkable: true,
		cost: 3
	}
};

// Creating the map
const map = aStar({
	grid,
	legend
});

// Getting the shortest path
const start = {
	x: 0,
	y: 0
};
const end = {
	x: 4,
	y: 4
};
const path = map(start, end);
// Output
// 
// [
//	Object { x: 1, y: 0, … },
​//	Object { x: 2, y: 0, … },
//	Object { x: 3, y: 0, … },
//	Object { x: 4, y: 0, … },
//	Object { x: 4, y: 1, … },
//	Object { x: 4, y: 2, … },
//	Object { x: 4, y: 3, … },
//	Object { x: 4, y: 4, … }
// ]

// 	Generated path
const gridWithPath = [
	[⚫️, 🌲, 🍀, 🍀, 🍀],
	[⚫️, 🌲, 🌲, 🍀, 🍀],
	[⚫️, 🍀, 🌊, 🍀, 🍀],
	[⚫️, 🍀, 🌲, 🌲, 🍀],
	[⚫️, ⚫️, ⚫️, ⚫️, ⚫️]
]	
```
