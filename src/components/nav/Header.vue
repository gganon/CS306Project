<template>
  <div id="header-container">
    <div id="nav-header-container">
      <div id="nav-header-container-left">
        <RouterLink to="/" @click="scrollToTop">Noxtoon</RouterLink>
      </div>

      <div id="nav-header-container-right">
        <RouterLink to="/about">ABOUT</RouterLink>
        <RouterLink to="/search">SEARCH TOONS</RouterLink>
      </div>
    </div>
  </div>
</template>

<script setup>
const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth"
  });
}
</script>

<style scoped>
#nav-header-container-right > a {
  width: 6em;
  text-align: center;
}

#nav-header-container-left > a {
  width: 6em;
  text-align: center;
  will-change: scroll-position;
}

a {
  height: 100%;
  border-radius: 1px;
  color: var(--nx-c-near-black);
}

a:hover {
  background-color: var(--nx-c-gray-hover);
  color: var(--nx-c-smoke)
}

#header-container {
  display: flex;
  flex-direction: column;
  background-color: var(--nx-c-orange);
  width: 100%;
  justify-content: center;
  z-index: 255;
  position: fixed;
}

#nav-header-container {
  display: flex;
}

#nav-header-container > div {
  display: flex;
  flex-grow: 1;
  column-gap: 1em;
}

#nav-header-container-right {
  height: inherit;
  justify-content: right;
}

#nav-header-container-left {
  height: inherit;
  justify-content: left;
}

#nav-header-container-left > a {
  margin-left: 2em;
  font-family: var(--nx-f-cheri);
  font-size: 150%;
  height: inherit;
}

#nav-header-container-right > a {
  font-family: var(--nx-f-cheri);
  font-size: 1.5em;
}

#nav-header-container-right > :last-child {
  margin-right: 2em;
  width: 7em;
}
</style>