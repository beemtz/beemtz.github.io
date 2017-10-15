<template>
  <footer class="footer">
    <div class="columns">
      <div class="column has-text-centered"><a href="https://twitter.com/thebeeletter" target="_blank"> <icon name="twitter" scale=">.1"></icon></a>
      <p>Rants</p>
      </div>
  <div class="column has-text-centered year">
    <span> © {{ new Date().getFullYear() }} </span>
    <p>Made by Bee, with help from the internet.</p>
  </div> 
       <div class="column has-text-centered"><a href="https://github.com/beemtz/fanzgrader" target="_blank"> <icon name="github" scale="1"></icon></a>
       <p>Repo</p>
       </div>
  </div>
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
  color: $paper;
  background-color: $ballpoint;
  padding: 48px;
  font-size: .8rem;
  line-height: 2rem
}

a, .year span {
  color: $paper;
  &:hover {
    color: $pencil;
  }
}
</style>
