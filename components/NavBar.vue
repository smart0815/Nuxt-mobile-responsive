<template>
  <nav :class="headerClassList" class="fixed w-full z-30 top-0 shadow-lg rounded-b-xl">
    <div class="navbar-top"></div>
    <div
      class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 pt-3 pb-2"
    >
      <div class="pl-4 flex items-center">
        <logo :isStickable="true" :isSticky="isSticky" />
      </div>
      <div class="block lg:hidden pr-4">
        <li>
          <a class="inline-block py-2 px-4 text-black font-bold no-underline btn-login" href="#"
            >Login</a
          >
        </li>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      scrollY: 0,
      isOpen: false,
    };
  },
  computed: {
    isSticky() {
      return this.scrollY > 10;
    },
    headerClassList() {
      return this.isSticky ? "bg-white shadow" : "";
    },
    navActionClassList() {
      return this.isSticky ? "gradient text-white" : "bg-white text-gray-800";
    },
    navContentClassList() {
      let classList = this.isSticky ? "bg-white" : "bg-gray-100";
      if (!this.isOpen) {
        classList += ` hidden`;
      }
      return classList;
    },
  },
  methods: {
    onClick() {
      this.isOpen = false;
    },
    onScroll() {
      this.scrollY = window.scrollY;
    },
    onToggleClick() {
      this.isOpen = !this.isOpen;
    },
  },
  mounted() {
    this.scrollY = window.scrollY;
    document.addEventListener("click", this.onClick);
    document.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    document.removeEventListener("click", this.onClick, true);
    document.removeEventListener("scroll", this.onScroll, true);
  },
};
</script>
<style lang="css" scoped>
.font-space {
  padding-top: 26px;
  padding-bottom: 22px;
}

.navbar-top {
  height: 5px;
  background: transparent linear-gradient(91deg, #319795 0%, #3182ce 100%) 0% 0% no-repeat
    padding-box;
}

.btn-login {
  font: normal normal 600 14px/17px Lato;
  letter-spacing: 0.84px;
  color: #319795;
}
</style>
