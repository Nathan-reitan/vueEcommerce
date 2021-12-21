<template>
    <div>
        <div class="topRightDiamond"></div>
        <div class="topLeftDiamond"></div>
        <div class="botRightDiamond"></div>
        <div class="botLeftDiamond"></div>
        <div class="productRow" id="pelotonContainer" >
            <h1>Peloton</h1>
            <img src="../assets/peloton.png" id="peloton" alt="Peloton Bike" class="productContainer" @click="onClick"/>
            <p>Peloton is the top of the line for stationary bikes.  They've integrated online courses and ranking systems to keep work outs from home engaging and driven.</p>
        </div>
        <div class="productRow" id="mirrorContainer">
            <h1>Mirror</h1>
            <img src="../assets/mirror.png"  id="mirror" alt="Mirror" class="productContainer" @click="onClick" />
            <p>This isn't just a mirror. It's a cardio class, it's a yoga studio, it's a boxing ring, it's your new personal trainer, and it's so much more.</p>
        </div>
        <div class="productRow" id="rowerContainer">
            <h1>Hydrow Rower</h1>
            <img src="../assets/hydrowVert.png"  id="rower" alt="Hydrow Rower" class="productContainer" @click="onClick" />
            <p>This is more than just a workout! Be it the encouragement to keep going every time I row from the instructors, or that feeling of accomplishment after every row, this is an incredible piece of technology!</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Products',
  props: {
    
  },
  methods: {
    onClick(e){
        let product = e.target.id
        const nodes = document.getElementById(product+"Container").childNodes
        const details = {
            title: nodes[0].innerText,
            image: nodes[1].src,
            altText: nodes[1].alt,
            description: nodes[2].innerText
        }
      this.$emit('send-details', details)
    }
  }
}
</script>