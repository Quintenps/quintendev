<template>
  <section class="section">
    <div class="container">
      <div class="columns">
        <div class="column">
          <h1 class="title">Work</h1>
          <h2 class="subtitle">I'm always up for learning something new</h2>
        </div>
      </div>
      <div class="columns m-t-md">
        <div class="column">
          <h4>💼 Past experiences</h4>
          <div class="line-block"></div>
          <ul>
            <li>
              Magento developer at
              <a target="_blank" href="//itonomy.nl">Itonomy</a>
            </li>
            <li>
              PHP Developer at <a target="_blank" href="//devmob.com">DevMob</a>
            </li>
            <li>
              PHP Developer at
              <a target="_blank" href="//cargosnap.com">CargoSnap</a>
            </li>
            <li>
              Magento developer at
              <a target="_blank" href="//experius.nl">Experius</a>
            </li>
          </ul>
        </div>
        <div class="column">
          <h4>🔨 Stuff I work with</h4>
          <div class="line-block"></div>
          <ul>
            <li>C#</li>
            <li>PHP (Laravel)</li>
            <li>Python</li>
            <li>Vuejs / Nuxtjs</li>
            <li>Docker / Kubernetes</li>
          </ul>
        </div>
        <div class="column">
          <h4>💻 Computers</h4>
          <div class="line-block"></div>
          <ul>
            <li>
              Desktop:
              <a
                href="#"
                style="text-decoration:underline; cursor:pointer;"
                @click="
                  showModal = true
                  modalData = computerSpecs.computer
                "
                >Windows</a
              >
            </li>
            <li>Phone: Xiaomi mi 9t</li>
            <li>
              Homeserver:
              <a
                href="#"
                style="text-decoration:underline; cursor:pointer"
                @click="
                  showModal = true
                  modalData = computerSpecs.optiplex
                "
                >Optiplex 3050 Micro</a
              >
            </li>
            <li>
              Datacenter: KVM VPS @
              <a href="//ramnode.com" target="_blank">Ramnode</a>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div v-if="showModal" class="modal is-active">
      <div class="modal-background" @click="showModal = false"></div>
      <div class="modal-card">
        <header class="modal-card-head">
          <p class="modal-card-title">Specs</p>
        </header>
        <section class="modal-card-body">
          <ul>
            <li v-for="spec in modalData" :key="spec">
              {{ spec }}
            </li>
          </ul>
        </section>
        <footer class="modal-card-foot">
          <button class="button" @click="showModal = false">Close</button>
        </footer>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
      modalData: [],
      computerSpecs: {
        computer: [
          'CPU: Ryzen 2700x',
          'GPU: RTX 2060 (Gigabyte)',
          'RAM: G.Skill RGB 16 GB (2 x 8 GB) DDR4-3200',
          'MB: Aorus x470 Ultra',
          'PSU: Corsair RMx 750',
          'Case: NZXT H510',
          'Storage: NVME 500GB Samsung 960',
          'Etc: Dark rock 4 CPU Cooler, Noctua fans in case'
        ],
        optiplex: [
          'OS: Ubuntu 20.04.1 LTS',
          'CPU: Intel i5-7500T (4) @ 3.300GHz',
          'RAM: DDR4 2x 4gb'
        ]
      }
    }
  }
}
</script>
