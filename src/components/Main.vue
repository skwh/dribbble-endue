<template>
  <main>
    <div class="words large">
      <h1>Ideas
        <span class="out">
          <span class="in">
            inspire
          </span>
        </span>
        change
      </h1>
      <h3>Creative thinking inspires ideas</h3>
      <span class="bar"></span>
    </div>
    <blockquote>
        <p>
          Design is a way of life, a point of view. It involves the whole complex of visual communications: talent, creative ability, manual skill, and technical knowledge.
        </p>
      <cite>Paul Rand</cite>
    </blockquote>
    <div class="buttons">
      <large-button backgroundColor="#3D96FF">
        <logo-icon topColor="white" bottomColor="black"></logo-icon>
      </large-button>
      <large-button backgroundColor="rgba(0,0,0,0)" borderColor="rgba(255,255,255,0.5)">
        <material-icon name="play_arrow" size="32px"></material-icon>
      </large-button>
    </div>
  </main>
</template>

<script>
export default {
  name: 'endue-main'
}
</script>

<style lang="scss">
main {
  position: relative;
  margin-left: 280px;
  margin-top: 160px;
}

.words {
  position: relative;

  h1 {
    font-family: "Bodoni 72", serif;
    font-size: 6.5rem;
    margin-bottom: 4vh;

    span.out {
      display: inline-block;
      height: 1em;
      overflow: hidden;
      position: relative;
      width: 2.9em;
      transform: translateY(0.47em);
    }

    span.in {
      position: absolute;
      top: -0.4em;
    }
  }

  h3 {
    position: absolute;
    top: 5px;
    margin: 0;
    margin-left: 6.9vw;
    font-size: 2rem;
  }

  .bar {
    height: 3px;
    width: 85px;
    background-color: #FD455F;
    position: absolute;
    top: 13px;
  }
}

blockquote {
  margin: 0;
  width: 43%;
  line-height: 1.5rem;
  font-weight: normal;

  cite {
    font-style: normal;
    color: rgba(255, 255, 255, 0.5);

    &::before {
      content: "— ";
    }
  }
}

div.buttons {
  margin-top: 4vh;

  div.button-container {
    margin: 1vw;
  }
}

</style>
