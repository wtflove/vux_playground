<template>
  <!-- <div class="loading-spinner" :style="spinnerStyle"> -->
  <div class="loading-spinner">
    <div class="spinner-inner">
      <div class="ferry">
        <div class="chimney"></div>
        <div class="waves"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  /* eslint-disable */
  name: 'LoadingSpinner'

  // props: {
  //   animationDuration: {
  //     type: Number,
  //     default: 1000
  //   },
  //   size: {
  //     type: Number,
  //     default: 60
  //   },
  //   color: {
  //     type: String,
  //     default: 'red'
  //   }
  // },

  // computed: {
  //   spinnerStyle() {
  //     return {
  //       height: `${this.size}px`,
  //       width: `${this.size}px`
  //     }
  //   },

  //   circleStyle() {
  //     return {
  //       color: this.color,
  //       fontSize: `${this.size * 0.24}px`
  //     }
  //   },

  //   lineStyle() {
  //     return {
  //       animationDuration: `${this.animationDuration}ms`,
  //       borderLeftWidth: `${this.size / 25}px`,
  //       borderTopWidth: `${this.size / 25}px`,
  //       borderLeftColor: this.color
  //     }
  //   }
  // }
}

</script>
<style scoped>
.loading-spinner,
.loading-spinner * {
  box-sizing: border-box;
}

.loading-spinner {
  height: 64px;
  width: 64px;
  overflow: hidden;
}

.loading-spinner .spinner-inner {
  position: relative;
  display: block;
  height: 100%;
  width: 100%;
}

.loading-spinner .ferry {
  position: absolute;
  top: 70%;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
  display: inline-block;
  width: 100%;
  height: 50%;
  border-radius: 3px 0 0 0;
  background-color: #2b2b2b;
  z-index: 1;
  -webkit-animation: bop 0.48s ease-in-out alternate infinite;
  animation: bop 0.48s ease-in-out alternate infinite;
  box-shadow: inset 0 -4px 0 0 #e74c3c, inset 0 12px 0 0 #2b2b2b, inset 0 14px 0 0 #f0cf3c;
  border-top: 4px solid #ecf0f1;
}

@-webkit-keyframes bop {
  to {
    -webkit-transform: translateY(-40%);
    transform: translateY(-40%);
  }
}

@keyframes bop {
  to {
    -webkit-transform: translateY(-40%);
    transform: translateY(-40%);
  }
}

.loading-spinner .ferry:after {
  content: "";
  position: absolute;
  top: -60%;
  right: 0;
  display: block;
  width: 70%;
  height: 60%;
  background-color: #ecf0f1;
  z-index: 1;
  border-radius: 3px 3px 0 0;
}

.loading-spinner .ferry:before {
  content: "";
  position: absolute;
  -webkit-transform: rotate(-25deg);
  transform: rotate(-25deg);
  top: -20%;
  left: -25%;
  width: 30%;
  height: 150%;
  background-color: white;
}

.spinner-inner .chimney {
  position: absolute;
  top: -120%;
  display: block;
  width: 27%;
  height: 73%;
  background-color: #f0cf3c;
  left: 50%;
  z-index: -1;
  -webkit-transform: rotate(8deg);
  transform: rotate(8deg);
  box-shadow: inset 0 3px 0 0 #2b2b2b;
}

.spinner-inner .waves {
  position: absolute;
  bottom: -150%;
  display: block;
  width: 156%;
  height: 200%;
  background-image: url("data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIj8+Cjxzdmcgd2lkdGg9IjE1NSIgaGVpZ2h0PSI4NSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KIDwhLS0gQ3JlYXRlZCB3aXRoIE1ldGhvZCBEcmF3IC0gaHR0cDovL2dpdGh1Yi5jb20vZHVvcGl4ZWwvTWV0aG9kLURyYXcvIC0tPgogPGc+CiAgPHRpdGxlPmJhY2tncm91bmQ8L3RpdGxlPgogIDxyZWN0IGZpbGw9Im5vbmUiIGlkPSJjYW52YXNfYmFja2dyb3VuZCIgaGVpZ2h0PSI4NyIgd2lkdGg9IjE1NyIgeT0iLTEiIHg9Ii0xIi8+CiAgPGcgZGlzcGxheT0ibm9uZSIgb3ZlcmZsb3c9InZpc2libGUiIHk9IjAiIHg9IjAiIGhlaWdodD0iMTAwJSIgd2lkdGg9IjEwMCUiIGlkPSJjYW52YXNHcmlkIj4KICAgPHJlY3QgZmlsbD0idXJsKCNncmlkcGF0dGVybikiIHN0cm9rZS13aWR0aD0iMCIgeT0iMCIgeD0iMCIgaGVpZ2h0PSIxMDAlIiB3aWR0aD0iMTAwJSIvPgogIDwvZz4KIDwvZz4KIDxnPgogIDx0aXRsZT5MYXllciAxPC90aXRsZT4KICA8ZyBpZD0ic3ZnXzkiPgogICA8ZWxsaXBzZSByeT0iMjYiIHJ4PSIyNiIgaWQ9InN2Z18xIiBjeT0iMzMuNSIgY3g9IjM0LjUiIHN0cm9rZS13aWR0aD0iMS41IiBmaWxsPSIjZmZmIi8+CiAgIDxlbGxpcHNlIHJ5PSIyNiIgcng9IjI2IiBpZD0ic3ZnXzMiIGN5PSIzMy41IiBjeD0iNjMuODY4NDkzIiBzdHJva2Utd2lkdGg9IjEuNSIgZmlsbD0iI2ZmZiIvPgogICA8ZWxsaXBzZSByeT0iMjYiIHJ4PSIyNiIgaWQ9InN2Z182IiBjeT0iMzMuNSIgY3g9IjkxLjcxODg4IiBzdHJva2Utd2lkdGg9IjEuNSIgZmlsbD0iI2ZmZiIvPgogICA8ZWxsaXBzZSByeT0iMjYiIHJ4PSIyNiIgaWQ9InN2Z183IiBjeT0iMzMuNSIgY3g9IjEyMS4wODczNzMiIHN0cm9rZS13aWR0aD0iMS41IiBmaWxsPSIjZmZmIi8+CiAgIDxyZWN0IGlkPSJzdmdfOCIgaGVpZ2h0PSI0NiIgd2lkdGg9IjE0MC4wMDAwMDYiIHk9IjMyLjUiIHg9IjcuNSIgc3Ryb2tlLXdpZHRoPSIxLjUiIGZpbGw9IiNmZmYiLz4KICA8L2c+CiA8L2c+Cjwvc3ZnPg==");
  background-size: 133% 144%;
  -webkit-animation: sail 4s linear infinite;
  animation: sail 4s linear infinite;
}

@-webkit-keyframes sail {
  to {
    background-position: 400px 0;
  }
}

@keyframes sail {
  to {
    background-position: 400px 0;
  }
}

</style>
