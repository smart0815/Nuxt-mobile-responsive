<template>
  <div class="relative">
    <section class="bg-white border-b rounded-t-xl">
      <div class="pt-6 pb-16 px-5">
        <button
          class="w-full text-sm text-white-800 font-bold rounded-2xl py-3 px-20 shadow-lg bg-primary"
        >
          Kostenlos Registrieren
        </button>
      </div>

      <div class="btn-group-over">
        <div
          class="inline-flex pt-6 pl-5"
          v-bind:class="{
            'overflow-hidden first-width': openTab === 1,
            'overflow-hidden left-1 second-width': openTab === 2,
            'left-2': openTab === 3,
          }"
          role="group"
        >
          <button
            class="bg-blue-500 text-sm text-white hover:bg-blue-400 rounded-l-lg py-3 px-8 mx-0 outline-none focus:shadow-outline"
            v-on:click="toggleTabs(1)"
            v-bind:class="{
              'btn btn-white': openTab !== 1,
              'btn btn-green': openTab === 1,
            }"
          >
            Arbeitnehmer
          </button>
          <button
            class="bg-blue-500 text-sm text-white hover:bg-blue-400 py-3 px-8 mx-0 outline-none focus:shadow-outline"
            v-on:click="toggleTabs(2)"
            v-bind:class="{
              'btn btn-white': openTab !== 2,
              'btn btn-green': openTab === 2,
            }"
          >
            Arbeitgeber
          </button>
          <button
            class="bg-blue-500 text-sm text-white hover:bg-blue-400 rounded-r-lg py-3 px-8 mx-0 outline-none focus:shadow-outline"
            v-on:click="toggleTabs(3)"
            v-bind:class="{
              'btn btn-white': openTab !== 3,
              'btn btn-green': openTab === 3,
            }"
          >
            Temporärbüro
          </button>
        </div>
      </div>

      <div class="relative w-full mt-16">
        <div class="tab-content tab-space">
          <div v-bind:class="{ hidden: openTab !== 1, block: openTab === 1 }">
            <div class="px-5 text-center pt-6 text-black lg-title">
              Drei einfache Schritte<br />
              zu deinem neuen Job
            </div>
            <div class="pl-5 pr-10 relative pb-24">
              <div class="flex justify-end">
                <img src="../assets/1.png?inline" alt slot="png" />
              </div>
              <div class="absolute bottom-0 left-0 pl-5 pr-10 flex items-end">
                <div class="big-number flex-shrink-0">1.</div>
                <div class="description ml-5 pb-5">Erstellen dein Lebenslauf</div>
              </div>
            </div>
            <div class="pl-8 pr-5 bg-section bg-space">
              <div class="flex items-end">
                <div class="big-number flex-shrink-0">2.</div>
                <div class="description ml-5 pb-5">Erstellen dein Lebenslauf</div>
              </div>
              <div class="flex justify-end pr-12 bg">
                <img src="../assets/2.png?inline" alt slot="png" />
              </div>
            </div>
            <div class="pl-12 pr-5 relative">
              <div class="flex items-center">
                <div class="big-number flex-shrink-0 z-10">3.</div>
                <div class="description ml-5 z-10">Erstellen dein Lebenslauf</div>
              </div>
              <div class="flex justify-end">
                <img class="z-10" src="../assets/3.png?inline" alt slot="png" />
              </div>
              <div class="absolute ellipse"></div>
            </div>
          </div>
          <div v-bind:class="{ hidden: openTab !== 2, block: openTab === 2 }">
            <div class="px-5 text-center pt-6 text-black lg-title">
              Drei einfache Schritte zu<br />
              deinem neuen Job
            </div>
            <div class="pl-5 pr-10 relative pb-24">
              <div class="flex justify-end">
                <img src="../assets/1.png?inline" alt slot="png" />
              </div>
              <div class="absolute bottom-0 left-0 pl-5 pr-10 flex items-end">
                <div class="big-number flex-shrink-0">1.</div>
                <div class="description ml-5 pb-5">Erstellen dein Lebenslauf</div>
              </div>
            </div>
            <div class="pl-8 pr-5 bg-section bg-space">
              <div class="flex items-end">
                <div class="big-number flex-shrink-0">2.</div>
                <div class="description ml-5 pb-5">Erstellen dein Lebenslauf</div>
              </div>
              <div class="flex justify-end pr-12">
                <img src="../assets/4.png?inline" alt slot="png" />
              </div>
            </div>
            <div class="pl-12 pr-5 relative">
              <div class="flex items-center">
                <div class="big-number flex-shrink-0 z-10">3.</div>
                <div class="description ml-5 z-10">Erstellen dein Lebenslauf</div>
              </div>
              <div class="flex justify-end">
                <img class="z-10" src="../assets/5.png?inline" alt slot="png" />
              </div>
              <div class="absolute ellipse"></div>
            </div>
          </div>
          <div v-bind:class="{ hidden: openTab !== 3, block: openTab === 3 }">
            <div class="px-5 text-center pt-6 text-black lg-title">
              Drei einfache Schritte zur<br />
              Vermittlung neuer Mitarbeiter
            </div>
            <div class="pl-5 pr-10 relative pb-24">
              <div class="flex justify-end">
                <img src="../assets/1.png?inline" alt slot="png" />
              </div>
              <div class="absolute bottom-0 left-0 pl-5 pr-10 flex items-end">
                <div class="big-number flex-shrink-0">1.</div>
                <div class="description ml-5 pb-5">Erstellen dein Lebenslauf</div>
              </div>
            </div>
            <div class="pl-8 pr-5 bg-section bg-space">
              <div class="flex items-end">
                <div class="big-number flex-shrink-0">2.</div>
                <div class="description ml-5 pb-5">Erstellen dein Lebenslauf</div>
              </div>
              <div class="flex justify-end pr-12">
                <img src="../assets/6.png?inline" alt slot="png" />
              </div>
            </div>
            <div class="pl-12 pr-5 relative">
              <div class="flex items-center">
                <div class="big-number flex-shrink-0 z-10">3.</div>
                <div class="description ml-5 z-10">Erstellen dein Lebenslauf</div>
              </div>
              <div class="flex justify-end">
                <img class="z-10" src="../assets/7.png?inline" alt slot="png" />
              </div>
              <div class="absolute ellipse"></div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  name: "pink-tabs",
  data() {
    return {
      openTab: 1,
    };
  },
  methods: {
    toggleTabs: function (tabNumber) {
      this.openTab = tabNumber;
    },
  },
};
</script>

<style lang="css" scoped>
.lg-title {
  font: normal normal 500 25px Lato;
  letter-spacing: 0px;
  color: #4a5568;
}

section {
  box-shadow: 0 -10px 15px -3px rgb(0 0 0 / 10%), 0 4px 6px -2px rgb(0 0 0 / 5%);
  position: absolute;
  top: -40px;
  left: 0;
  width: 100%;
}

.bg-space {
  padding-top: 40px;
  padding-bottom: 35px;
}

.bg-primary {
  background: transparent linear-gradient(95deg, #319795 0%, #3182ce 100%) 0% 0% no-repeat
    padding-box;
}

.bg-section {
  background: transparent linear-gradient(134deg, #e6fffa 0%, #ebf4ff 100%) 0% 0%
    no-repeat padding-box;
  background: url("../assets/bg-2.png") no-repeat;
}

.btn {
  border: 1px solid #cbd5e0;
}

.btn-green {
  background-color: #81e6d9;
}

.btn-white {
  background-color: #fff;
  color: #319795;
}

.big-number {
  font: normal normal normal 156px Lato, Regular;
  color: #718096;
  line-height: 1;
}

.description {
  font: normal normal normal 19px Lato;
  letter-spacing: 0.47px;
  color: #718096;
}

.focus\:shadow-outline:focus {
  box-shadow: none !important;
}

button:focus {
  outline: 0;
}

.ellipse {
  width: 304px;
  height: 303px;
  background: #f7fafc 0% 0% no-repeat padding-box;
  opacity: 1;
  top: -40px;
  left: -50px;
  border-radius: 50%;
  z-index: 0;
}

@media only screen and (max-width: 360px) {
  .left-1 {
    margin-left: -4.5rem;
  }

  .left-2 {
    margin-left: -9rem;
  }

  .first-width {
    width: 340px;
  }

  .second-width {
    width: 420px;
  }
}
</style>
