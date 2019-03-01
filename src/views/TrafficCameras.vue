<template>
  <v-container grid-list-md text-xs-center>
    <v-layout row wrap>
      <v-flex xs12>
        <v-card dark color="primary">
          <v-card-text class="px-0 black toolbar">Sherman Traffic Cameras</v-card-text>
        </v-card>
      </v-flex>
      <v-flex
        <div>
          <img
            v-for="card in cards"
            :key="card.title"
            :class="{ full: fullWidthImage }"
            @click="fullWidthImage = !fullWidthImage"
            :src="card.src"
            alt=""
            xs3
          />
        </div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      cards: [
        { title: 'Camera 1', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 2', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 3', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 4', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 5', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 6', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 7', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 8', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 9', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 10', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 11', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 },
        { title: 'Camera 12', src: 'http://50.246.145.122:80/cgi-bin/faststream.jpg?stream=half&amp;fps=15&amp;rand=COUNTER', flex: 3 }
      ],
      'fullWidthImage': false
    })
  }
</script>

<style media="screen">
  .toolbar {
    font-size: 2em;
  }
  img {
    border: 4px solid white;
    width: 350px;
    height: 225px;
  }
  .full {
    z-index: 9999;
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
  }
  .images:hover {
    cursor: pointer;
  }
</style>
