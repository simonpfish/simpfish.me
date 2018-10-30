<template lang="pug">
div
  particles-bg.bg   

  div#intro
    div#hello-typed
      h2 Hello, there! 
    div#hello
      |
    img(src="https://scontent-lht6-1.xx.fbcdn.net/v/t1.0-9/12717498_1016833525037503_5767685636819260516_n.jpg?_nc_cat=0&_nc_log=1&oh=8c03dc5743b21a51b9fec6b25b2f6dfc&oe=5C118315")#picture
    br
    div#text-box
      :markdown-it
        I'm **Simon Posada Fishman**. I enjoy making things 👨‍💻 
        
        Recently I've been doing a lot of *web development* and *data analysis*.

        We are what we ~~eat~~ read. Here's a list of things I enjoy consuming 🙃:
        
        [Radiolab](https://www.wnycstudios.org/shows/radiolab/), [Axios Login](https://www.axios.com/newsletters/axios-login), [Stratechery](https://stratechery.com/),  [The Download](https://www.technologyreview.com/the-download/)
      
        Computer Science at Pomona College 🎓 

        Feel free to connect with me!
      a(href='https://github.com/simpfish').icon-link
        fa(:icon="['fab', 'github']")
      a(href='https://twitter.com/simpfish').icon-link
        fa(:icon="['fab', 'twitter']") 
      a(href='https://www.facebook.com/spf.me').icon-link
        fa(:icon="['fab', 'facebook']")
    br
</template>

<script>
import Typed from "typed.js";
import ParticlesBg from "../components/ParticlesBg";

import { library } from "@fortawesome/fontawesome-svg-core";
import {
  faGithub,
  faTwitter,
  faFacebook
} from "@fortawesome/free-brands-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

library.add(faGithub, faTwitter, faFacebook);

export default {
  components: { ParticlesBg, fa: FontAwesomeIcon },
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
a:link {
  color: #aaa;
}

a:visited {
  color: #888;
}

a:hover {
  color: #333;
}

a:active {
  color: #333;
}

a:link {
  text-decoration: none;
}

.icon-link {
  margin: 0.5em;
  font-size: 1.3em;
}

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
  background-color: rgba(256, 256, 256, 0.7);
  box-shadow: 0 0 1em 1em rgba(256, 256, 256, 0.7);
  display: inline-block;
  padding: 0rem 1.5rem;
  font-size: 1.1rem;
  font-weight: 500;
  pointer-events: none;
  margin-top: -1rem;
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
  margin: 2rem 0rem;
  pointer-events: none;
}

@media only screen and (max-height: 600px) {
  #intro {
    justify-content: flex-start;
  }
}

@media only screen and (max-device-height: 700px) {
  #intro {
    justify-content: flex-start;
  }
}
</style>
