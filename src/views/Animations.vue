<template>
  <div class="animations">
    <h1>Animations</h1>

    <div class="box2">
      <button class="header" @click="clickExpand">{{ expanded }}</button>
      <div class="content" :class="{ active: expanded }">
        <ul>
          <li>line</li>
          <li>line</li>
          <li>line</li>
          <li>line</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Animations',
  props: {
    msg: String
  },
  data() {
    return {
      expanded: false
    }
  },
  methods: {
    clickExpand() {
      this.expanded = !this.expanded
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.box2 {
  display: flex;
  flex-direction: column;
  width: 30em;
  margin: auto;

  .header {
    height: 2em;
    background: lightcoral;
    transform: scaleY(1);

    animation-name: expand;
    animation-duration: .5s;
  }
  .content {
    background: lightcyan;
    transform-origin: top;
    transform: scaleY(0);
    transition: transform 0.1s ease;

    ul {
      list-style: none;
      margin: 0;
      padding: 0;
    }
  }

  .active {
    transform: scaleY(1);
  }

  @keyframes expand {
    from {
      transform-origin: top;
      transform: scaleY(0)
    }
  }
}
</style>
