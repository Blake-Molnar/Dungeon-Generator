<script >
// import { RouterLink, RouterView } from 'vue-router' setup
// import HelloWorld from './components/HelloWorld.vue'


import { ref, onMounted } from 'vue'

export default {
  data() {
    return { 
      map : [
  ['w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','x','w',],
  ['w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w','w',],

],
    wall: 'wall',
    floor: 'floor',
    possibleDoorways: [],
    doorways: 3,
    roomDensity: 100,
    minHeight: 3,
    maxHeight: 10,
    minWidth: 3,
    maxWidth: 10
      }

  }, methods: {
     generateDungeon() {
  this.resetMap()
  this.generateRooms()
  this.corridorPlacable()

  this.placeDoors()
  this.removeDeadends()
  // this.resetMap()

},

 resetMap()
{
  for (let i = 1; i < this.map.length -1; i++) {
    for (let j = 1; j < this.map[0].length -1; j++) {
      this.map[i][j] = 'x'
    }
  }

  while(this.possibleDoorways.length > 0)
  {
    this.possibleDoorways.pop()
  }
  // this.map.forEach((ele, i) => this.map[i].forEach( (char, j) => this.map[i][j] = 'x'))
},

 generateRooms()
{
  for (let i= 0; i < this.roomDensity; i++)
	{
		const startingPoint = [
      Math.floor(Math.random() * this.map.length),
      Math.floor(Math.random() * this.map[0].length)
      ]
      let roomDoorways = []

        const height = (Math.floor(Math.random()  * (this.maxHeight - this.minHeight + 1) + this.minHeight )) + 2
        const width = (Math.floor(Math.random() * (this.maxWidth - this.minWidth + 1) + this.minWidth )) + 2

        if(height + startingPoint[0] > this.map.length -1 || width + startingPoint[1] > this.map[0].length -1 || startingPoint[0] < 3 || startingPoint[1] < 3)
        {
          continue;
        }


    if(this.map[startingPoint[0]][startingPoint[1]] !== 'o' && this.roomPlacable(startingPoint,height,width))
    {
        for (let i = startingPoint[0]; i < startingPoint[0] + height; i++) {
          for (let j = startingPoint[1]; j < startingPoint[1] + width; j++) {
            
            if(i == startingPoint[0] || i == startingPoint[0] + height -1 || j == startingPoint[1] || j == startingPoint[1] + width -1)
            {
              this.map[i][j] = 'w'
              roomDoorways.push([i,j])
            }
            else
            {
              this.map[i][j] = 'o'
            }
          }
        }
        // console.log(startingPoint, height, width)
    this.possibleDoorways.push(roomDoorways)

    }
	}
},

 roomPlacable(startingPoint,height,width)
{
  let isPlacable = true
  for (let i = startingPoint[0] -1; i < startingPoint[0] + height ; i++) {
    if(!isPlacable){break}
    for (let j = startingPoint[1] -1; j < startingPoint[1] + width ; j++) {

      if(this.map[i][j] == 'o')
      {
        isPlacable = false
        break
      }
    }
  }

  return isPlacable
},
  

  generateCorridors(firstX, firstY)
  {
    let corridorStack = [];
    this.map[firstX][firstY] = 'o'
    corridorStack.push([firstX,firstY])
    while(corridorStack.length > 0)
    {
      let currentPoint = corridorStack[corridorStack.length - 1]
      let unvisited = []

      let north = this.map[currentPoint[0] -1][currentPoint[1]] == 'x' ? 1 : 0;
      if(north == 1) {unvisited.push([currentPoint[0] -1,currentPoint[1]])}
      let east = this.map[currentPoint[0]][currentPoint[1]+1] == 'x' ? 1 : 0;
      if(east == 1) {unvisited.push([currentPoint[0],currentPoint[1]+1])}
      let south = this.map[currentPoint[0] +1][currentPoint[1]] == 'x' ? 1 : 0;
      if(south == 1) {unvisited.push([currentPoint[0] + 1,currentPoint[1]])}
      let west = this.map[currentPoint[0]][currentPoint[1]-1] == 'x' ? 1 : 0;
      if(west == 1) {unvisited.push([currentPoint[0],currentPoint[1] - 1])}
      // console.log("unvisited:" + unvisited)
      
      let sum = north + east + south + west
      if(sum > 0)
      {

        corridorStack.push(unvisited[Math.floor(Math.random() * sum)])
        currentPoint = corridorStack[corridorStack.length - 1]
        // console.log("push:"+ currentPoint)

        north = this.map[currentPoint[0] -1][currentPoint[1]] == 'o' ? 1 : 0;
        if(north == 1) {unvisited.push([currentPoint[0] -1,currentPoint[1]])}
        east = this.map[currentPoint[0]][currentPoint[1]+1] == 'o' ? 1 : 0;
        if(east == 1) {unvisited.push([currentPoint[0],currentPoint[1]+1])}
        south = this.map[currentPoint[0] +1][currentPoint[1]] == 'o' ? 1 : 0;
        if(south == 1) {unvisited.push([currentPoint[0] + 1,currentPoint[1]])}
        west = this.map[currentPoint[0]][currentPoint[1]-1] == 'o' ? 1 : 0;
        if(west == 1) {unvisited.push([currentPoint[0],currentPoint[1] - 1])}
        sum = north + east + south + west
        if(sum == 1)
        {
          this.map[currentPoint[0]][currentPoint[1]] = 'o'
        }
        else{
          this.map[currentPoint[0]][currentPoint[1]] = 'w'
          corridorStack.pop()
        }

      }else{
      // console.log("pop")

        corridorStack.pop()
      }
    }
  },

  corridorPlacable()
  {
    for (let i = 1; i < this.map.length -2; i++) {
      for (let j = 1; j < this.map[0].length -2; j++) {
        let north = this.map[i -1][j] == 'o' ? 1 : 0;
        let east = this.map[i][j +1] == 'o' ? 1 : 0;
        let south = this.map[i+1][j] == 'o' ? 1 : 0;
        let west = this.map[i ][j-1] == 'o' ? 1 : 0;
        let sum = north + east + south + west

        if(sum <= 1 && this.map[i][j] == 'x')
        {
          this.generateCorridors(i,j)
        }
      }
    }
  },

placeDoors()
{

  for (let i = 0; i < this.possibleDoorways.length; i++) {
    let doors = 0

    while( doors < this.doorways)
    {
      let doorway = this.possibleDoorways[i][Math.floor(Math.random() * this.possibleDoorways[i].length -1) + 1]

      let north = this.map[doorway[0] -1][doorway[1]] == 'o' ? 1 : 0;
      let east = this.map[doorway[0]][doorway[1] +1] == 'o' ? 1 : 0;
      let south = this.map[doorway[0]+1][doorway[1]] == 'o' ? 1 : 0;
      let west = this.map[doorway[0]][doorway[1]-1] == 'o' ? 1 : 0;
      let northDoor = this.map[doorway[0] -1][doorway[1]] == 'd' ? 1 : 0;
      let eastDoor = this.map[doorway[0]][doorway[1] +1] == 'd' ? 1 : 0;
      let southDoor = this.map[doorway[0]+1][doorway[1]] == 'd' ? 1 : 0;
      let westDoor = this.map[doorway[0]][doorway[1]-1] == 'd' ? 1 : 0;
      let doorCount = northDoor + eastDoor + southDoor + westDoor;

      // let sum = north + east + south + west
      if(doorCount == 0 && (north + south == 2 || east + west == 2))
      {
        this.map[doorway[0]][doorway[1]] = 'd'
        doors++
      }
    }
  }
},

  removeDeadends()
  {
    for (let i = 1; i < this.map.length -1; i++) {
        for (let j = 1; j < this.map[0].length -1; j++) {
          if(this.map[i][j] == 'o' || this.map[i][j] == 'd'){
            let floors = []
            let north = this.map[i -1][j] == 'w' ? 1 : 0;
            if(north == 0) {floors.push([i -1,j])}
            let east = this.map[i][j +1] == 'w' ? 1 : 0;
            if(east == 0) {floors.push([i,j +1])}
            let south = this.map[i+1][j] == 'w' ? 1 : 0;
            if(south == 0) {floors.push([i+1,j])}
            let west = this.map[i ][j-1] == 'w' ? 1 : 0;
            if(west == 0) {floors.push([i ,j-1])}

            let sum = north + east + south + west
            if(sum >= 3)
            {
              this.map[i][j] = 'w'
              i = 1
              j = 0
            }
          }
        }
      }
    }
}
}


</script>

<template>
  <!-- <header> -->
    <!-- <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" /> -->

    <!-- <div class="wrapper">
      <HelloWorld msg="You did it!" />

       <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav> -->
    <!-- </div> --> 
  <!-- </header> -->
  <div>
    <label for="roomDensity">Room Density:</label>
    <input type="range" v-model.number="this.roomDensity" id="roomDensity" name="roomDensity" min="100" max="1000"/>

    <label for="minHeight">Room Minumum Height:</label>
    <input type="range" v-model.number="this.minHeight" id="minHeight" name="minHeight" min="1" max="10" oninput="num1.value = this.value"/>
    <output id="num1">3</output>

    <label for="maxHeight">Room Max Height:</label>
    <input type="range" v-model.number="this.maxHeight" id="maxHeight" name="maxHeight" min="1" max="10" oninput="num2.value = this.value"/>
    <output id="num2">10</output>

    <label for="minWidth">Room Minumum Width:</label>
    <input type="range" v-model.number="this.minWidth" id="minWidth" name="minWidth" min="1" max="10" oninput="num3.value = this.value"/>
    <output id="num3">3</output>

    <label for="maxWidth">Room Max Width:</label>
    <input type="range" v-model.number="this.maxWidth" id="maxWidth" name="maxWidth" min="1" max="10" oninput="num4.value = this.value"/>
    <output id="num4">10</output>

    <label for="doorways">Max Doorways:</label>
    <input type="range" v-model.number="this.doorways" id="doorways" name="doorways" min="1" max="10" oninput="num5.value = this.value"/>
    <output id="num5">3</output>
    <button @click="generateDungeon">Generate Dungeon</button>


  <tr>
    <td v-for="item in this.map">
      <span v-for="char in item">
      <span :class="[ 'tile', char == 'w' ? wall : '', char == 'o' ? floor : '', char == 'd'  ? 'door' : '']"></span>
      </span>
    </td>
  </tr>
</div>
  <!-- <RouterView /> -->
</template>

<style scoped>
  .tile{
  padding: 10px;
  display: flex;
  /* border: .5px dotted grey; */
  background-color: black;
  }
.wall{
  background-image: url(img/catacombs.png);

}
.floor{
  background-image: url(img/floor.png);
}
.door{
  background-image: url(img/open_door.png);
  background-size: cover;
}
header {
  line-height: 1.5;
  max-height: 100vh;
  display: block;
}
button{
  margin: 7%;
  flex-wrap: nowrap;
  width: 15%;
  height: auto;
  display: flex;

}

div
{
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

}
td{
  margin: 0;
  padding: 0;
  width: 100%;
  line-height: 0.5;
  display: flex;
  flex-direction: row;
}
tr{
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  width: auto;
  height: auto;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
