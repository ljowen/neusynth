<script>
    let r = 50;
	let value = 0;
    let pos = {x: 0, y: 0};
	console.log("init");
	// function handleDrag(e) {
	//   count = Math.max(e.offsetX, e.offsetY);
	// }
    setInterval(() => {
        console.log('tick', pos);
        value += 10;
        // if(value > 2*Math.PI) {
        //     value = 0;
        // }
        pos = { y: r * Math.sin(value), x: r * Math.cos(value)}

    }, 100)
</script>

<style>
	button {
	  position: relative;
	  background: transparent;
	  border: none;	  
	  border-radius: 100px;
	  height: 100px;
	  width: 100px;
	  padding: 12px 12px;	  
	}
    svg {
        overflow: visible;
         position: absolute;
         top: 0;
         bottom: 0;
         left: 0;
         right: 0;         
    }
    .mark {        
        /* background: red; */
        /* border: 1px solid black; */
        width: 15px;
        height: 15px;
        position: absolute;        
    }
</style>

<button style="transform: rotate({value}deg);" class="raised" name="knob">
  <label for="knob"></label>
  <div style="top: 15px; left: 15px" class="pressed mark"></div>
  <!-- <svg>
    <line x1="{pos.x/1.25 + 50}" y1="{pos.y/1.25 + 50}" y2="{pos.y + 50}" x2="{pos.x + 50}" style="stroke:lime;stroke-width:4" />
  </svg> -->
</button>