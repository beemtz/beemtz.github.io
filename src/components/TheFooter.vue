<template>
  <footer class="footer has-text-centered">
    <p>made with vue, bulma, and <span>brains</span>.
    </p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'the-footer'
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/vars";

.footer {
  font-family: $marks;
  color: $pencil;
  background-color: $paper;
  padding: 48px;
  font-size: 1rem;
}

span {
  color: $ballpoint;
}
</style>
