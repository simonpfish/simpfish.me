<template lang="pug">
div#intro
  span#hello 
    h2 Hello, there!
  img(src="https://scontent-lht6-1.xx.fbcdn.net/v/t1.0-9/12717498_1016833525037503_5767685636819260516_n.jpg?_nc_cat=0&_nc_log=1&oh=8c03dc5743b21a51b9fec6b25b2f6dfc&oe=5C118315")#picture
  div#text-box
    p 
      :markdown-it
        I'm **Simon Posada Fishman**. I enjoy building things using code 👨‍💻 
        
        Currently finishing my Computer Science degree at [Pomona College](https://www.pomona.edu) 🎓

        I'm mostly interested in *web development*, *embedded systems* and *data analysis*. 

        We are what we ~~eat~~ read. Here's a list of things I enjoy consuming 🙃:
        
        Radiolab, Axios Login, Stratechery, The Download
</template>

<style>
#intro {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  height: 100vh;
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
}

#hello {
  font-weight: bold;
}
</style>
