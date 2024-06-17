<script>

export default{
    data() {
        return{
            
        }
    }
}
</script>

<template>
    <section>
        <div class="loader">
      <p class="text">
      <span class="letter letter1">L</span>
      <span class="letter letter2">o</span>
      <span class="letter letter3">a</span>
      <span class="letter letter4">d</span>
      <span class="letter letter5">i</span>
      <span class="letter letter6">n</span>
      <span class="letter letter7">g</span>
      <span class="letter letter8">.</span>
      <span class="letter letter9">.</span>
      <span class="letter letter10">.</span>
      </p>
    </div>
    <div class="progress-loader">
        <div class="progress"></div>
    </div>
    </section>
</template>



<style lang="scss" scoped>

section{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.progress-loader {
  top: 30%;
  left: 50%;
  position: absolute;
  transform: translate(-50%, -50%);
  width: 550px;
  background: rgba(236, 236, 238, 0.253);
  height: 30px;
  border-radius: 7px;
}

.progress {
  width: 1px;
  height: 30px;
  border-radius: 7px;
  background: rgb(255, 255, 255);
  transition: 0.5s;
  animation: loading_44 6s cubic-bezier(.4,1.01,1,1) infinite;
}

@keyframes loading_44 {
  0% {
    width: 0%;
  }

  50% {
    width: 100%;
  }

  100% {
    width: 0%;
  }
}


/* Wave text loader made by: csozi | Website: english.csozi.hu*/

.text {
  color: white;
  font-weight: bolder;
}

@keyframes letter {
  0% {
    font-size: 30px;
  }

  50% {
    font-size: 40px;
  }

  100% {
    font-size: 30px;
  }
}

.letter {
  animation: letter 1s infinite;
}

.letter1 {
  animation-delay: 0s;
}

.letter2 {
  animation-delay: -0.9s;
}

.letter3 {
  animation-delay: -0.8s;
}

.letter4 {
  animation-delay: -0.7s;
}

.letter5 {
  animation-delay: -0.6s;
}

.letter6 {
  animation-delay: -0.5s;
}

.letter7 {
  animation-delay: -0.4s;
}

.letter8 {
  animation-delay: -0.3s;
}

.letter9 {
  animation-delay: -0.2s;
}

.letter10 {
  animation-delay: -0.1s;
}
</style>