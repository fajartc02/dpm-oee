<template>
  <div class="container-xxl" style="padding: 10px;height: 60vh;">
    <div class="row mb-4">
      <h1 class="header-line">Hyundai Line</h1>
    </div>
    <div class="flex-row d-flex justify-content-around mb-4">
      <div class="card dark border border-dark button right p-0 hw-200 border-3 rounded-3" typeof="button">
        <badge-error />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h2 class="text-light mc-text">T 1000</h2>
        </div>
      </div>
      <div class="card dark border border-dark button right p-0 hw-200 border-3 rounded-3" typeof="button">
        <BadgeTools />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h2 class="text-light mc-text">T 800</h2>
        </div>
      </div>
      <div class="card dark border border-dark button right p-0 hw-200 border-3 rounded-3" typeof="button">
        <BadgeRunning />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h2 class="text-light mc-text">T 600</h2>
        </div>
      </div>
      <div class="card dark border border-dark button right p-0 hw-200 border-3 rounded-3" typeof="button">
        <badge-idle />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h2 class="text-light mc-text">T 500</h2>
        </div>
      </div>
    </div>
    <div class="flex-row d-flex justify-content-around">
      <div class="card dark border border-dark button right p-0 hw-100 border-3 rounded-3" typeof="button">
        <BadgeRunning />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h4 class="text-light mc-text">Robot 1</h4>
        </div>
      </div>
      <div class="card dark border border-dark button right p-0 hw-100 border-3 rounded-3" typeof="button">
        <BadgeRunning />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h4 class="text-light mc-text">Robot 2</h4>
        </div>
      </div>
      <div class="card dark border border-dark button right p-0 hw-100 border-3 rounded-3" typeof="button">
        <BadgeRunning />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h4 class="text-light mc-text">Robot 3</h4>
        </div>
      </div>
      <div class="card dark border border-dark button right p-0 hw-100 border-3 rounded-3" typeof="button">
        <BadgeRunning />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h4 class="text-light mc-text">Robot 4</h4>
        </div>
      </div>
      <div class="card dark border border-dark button right p-0 hw-100 border-3 rounded-3" typeof="button">
        <BadgeRunning />
        <div class="card-body h-100 d-flex align-items-center justify-content-center rounded-3">
          <h4 class="text-light mc-text">Robot 5</h4>
        </div>
      </div>
    </div>
  </div>
  <div class="container" style="padding: 50px;height: 10vh;">
    <div class="row">
      <div class="col">
        <table class="table table-bordered">
          <tr>
            <td>
              <div class="card" typeof="button">
                <BadgeRunning />
              </div>
            </td>
            <td>
              Normal
            </td>
            <td>
              <div class="card" typeof="button">
                <BadgeError />
              </div>
            </td>
            <td>
              Error
            </td>
            <td>
              <div class="card" typeof="button">
                <BadgeIdle />
              </div>
            </td>
            <td>
              Idle
            </td>
            <td>
              <div class="card" typeof="button">
                <BadgeTools />
              </div>
            </td>
            <td>
              Change
            </td>
          </tr>
        </table>
      </div>
    </div>
  </div>
  <div class="container-xxl" style="padding: 50px;height: 20vh;">
    <div class="row">
      <div class="col">
        <div class="card border-dark">
          <div class="card-header border-dark">
            <h2>Clock</h2>
          </div>
          <div class="card-body">
            <h2>{{ clock }}</h2>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-dark">
          <div class="card-header border-dark">
            <h2>OEE</h2>
          </div>
          <div class="card-body">
            <h2>98.9%</h2>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-dark">
          <div class="card-header border-dark">
            <h2>Target</h2>
          </div>
          <div class="card-body">
            <h2>500</h2>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-dark">
          <div class="card-header border-dark">
            <h2>Plan</h2>
          </div>
          <div class="card-body">
            <h2>319</h2>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-dark">
          <div class="card-header border-dark">
            <h2>Actual</h2>
          </div>
          <div class="card-body">
            <h2>318</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BadgeError from '@/components/BadgeError.vue'
import BadgeTools from '@/components/BadgeTools.vue'
import BadgeRunning from '@/components/BadgeRunning.vue'
import BadgeIdle from '@/components/BadgeIdle.vue'
import moment from 'moment'
// @ is an alias to /src

export default {
  name: 'HomeView',
  data() {
    return {
      clock: moment().format('LTS'),
    }
  },
  components: {
    BadgeError,
    BadgeTools,
    BadgeRunning,
    BadgeIdle
  },
  mounted() {
    setInterval(() => {
      this.clock = moment().format('LTS')
    }, 1000)
  }
}
</script>

<style>
.header-line {
  font-family: 'Workbench', sans-serif;
}

.mc-text {
  font-family: 'Protest Riot', sans-serif;
}

.card.button {
  display: inline-block;
  padding: 0 2em;
  line-height: 2em;
  border-radius: 0.2em;
  text-decoration: none;
}

.right {
  float: right;
}

.dark {
  background: #555;
  color: #eee;
}

.border {
  box-shadow: inset 0.2em 0.2em 0.2em 0 rgba(255, 255, 255, 0.5), inset -0.2em -0.2em 0.2em 0 rgba(0, 0, 0, 0.5);
}

.hw-200 {
  height: 200px;
  width: 200px;
}

.hw-100 {
  height: 100px;
  width: 100px;
}

.hw-badge-50 {
  height: 50px;
  width: 50px;
}

.blink-warning {
  animation: blink-warning 1s linear infinite;
}

@keyframes blink-warning {
  0% {
    background-color: #eaf20e;
  }

  50% {
    background-color: #cad104;
  }

  100% {
    background-color: #c2c904;
  }
}

.blink-error {
  animation: blink-error 1s linear infinite;
}

@keyframes blink-error {
  0% {
    background-color: #fc6c6c;
  }

  50% {
    background-color: #fc3f3f;
  }

  100% {
    background-color: #fc0707;
  }
}

.blink-running {
  animation: blink-running 1s linear infinite;
}

@keyframes blink-running {
  0% {
    background-color: #24ff02;
  }

  50% {
    background-color: #20d604;
  }

  100% {
    background-color: #1bb503;
  }
}

.blink-idle {
  animation: blink-idle 1s linear infinite;
}

@keyframes blink-idle {
  0% {
    background-color: #b2b2b2;
  }

  50% {
    background-color: #9ca09b;
  }

  100% {
    background-color: #8e918e;
  }
}
</style>