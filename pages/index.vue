<template lang="pug">
div#intro
  particles-bg.bg   

  div#hello-typed
    h2 Hello, there! 
  div#hello
  img(src="https://scontent-lht6-1.xx.fbcdn.net/v/t1.0-9/12717498_1016833525037503_5767685636819260516_n.jpg?_nc_cat=0&_nc_log=1&oh=8c03dc5743b21a51b9fec6b25b2f6dfc&oe=5C118315")#picture
  div#text-box
    :markdown-it
      I'm **Simon Posada Fishman**. I enjoy building things using code 👨‍💻 
      
      Currently finishing my Computer Science degree at [Pomona College](https://www.pomona.edu) 🎓

      I'm mostly interested in *web development*, *embedded systems* and *data analysis*. 

      We are what we ~~eat~~ read. Here's a list of things I enjoy consuming 🙃:
      
      Radiolab, Axios Login, Stratechery, The Download
</template>

<script>
import Typed from "typed.js";
import ParticlesBg from "../components/ParticlesBg";
export default {
  components: { ParticlesBg },
  mounted() {
    var typed = new Typed("#hello", {
      stringsElement: "#hello-typed",
      typeSpeed: 30,
      showCursor: false
    });
  }
};
</script>


<style>
#intro {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  height: 100vh;
}

#intro > * {
  z-index: 1;
}

#picture {
  align-self: center;
  max-width: 200px;
  max-height: 200px;
  border-radius: 50%;
}

#text-box {
  display: inline-block;
  padding: 0rem 2rem;
  font-size: 1.1rem;
  pointer-events: none;
}

#text-box > * {
  pointer-events: all;
}

#hello-typed {
  display: none;
}

#hello {
  height: 1.5rem;
  font-size: 1.5rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 2rem;
  pointer-events: none;
}
</style>
