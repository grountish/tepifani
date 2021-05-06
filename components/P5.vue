<template>
  
</template>

<script>
export default {
     async mounted() {
    if (process.browser) {
      const { default: P5 } = await import('p5')

      const sketch = (s) => {
        s.setup = () => {
          s.createCanvas(window.innerWidth -(window.innerWidth / 40) , window.innerHeight)
        }
        s.draw = () => {
          s.background(255, 9)
          s.fill(0)
          s.ellipse(s.random(s.mouseX * 4), s.random(s.mouseY * 4),0.7)
        }
      }
      // eslint-disable-next-line no-unused-vars
      const canvas = new P5(sketch, 'p5Canvas')
    }
  }
}
</script>

<style>
#defaultCanvas0 {
  position: absolute;
  z-index: -3;
  top: 0;
  left: 0;
}
</style>