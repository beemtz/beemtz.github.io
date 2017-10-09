<template>
  <section class="hero">
    <div class="hero-body">
      <div class="container has-text-centered">
        <p class="title">
          Straight <span>A</span> Grade
        </p>
        <p class="subtitle">
          First Class Assessment
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'hero'
}
</script>

<style lang="scss" scoped>
@import "../assets/styles/vars";

.title {
  font-family: $marks;
  color: $ballpoint;
  font-size: 3rem;
}

span {
  color: $grade;
}

.subtitle {
  font-family: $sec;
  color: $pencil;
  line-height: 3rem;
}
</style>
