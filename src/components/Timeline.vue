<template>
  <div>
    <div class="container">
      <ul class="list-timeline">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  components: {  },

}
</script>

<style scoped>
.list-timeline {
  font-family: helvetica;
  /* boring! */
  list-style: none;
  padding-left: 62px;
  counter-reset: timeline;
}

.list-timeline li {
  border-left: 1px solid #ccc;
  margin-left: -16px;
  margin: 0;
  padding: 40px 20px 40px 36px;
  position: relative;
}

.list-timeline li:before,
.list-timeline li:after {
  position: absolute;
  top: 0;
  bottom: 0;
  content: "";
}

.list-timeline li:before {
  height: 60px;
  width: 60px;
  background: #fff;
  left: -30px;
  border: 1px solid #ccc;
  border-radius: 100%;
  margin: auto;
}

.list-timeline li:after {
  height: 50px;
  width: 50px;
  left: -25px;
  margin: auto;
  border-radius: 100%;
  background: #ddd;
  counter-increment: timeline;
  content: counter(timeline);
  text-align: center;
  line-height: 50px;
  transform: scale(1);
  transform-origin: center center;
  box-shadow: 0 0 0 0px blue;
  transition: transform 0.2s ease-in-out, box-shadow 0.15s 0.2s ease-in-out;
}

/* .list-timeline li:hover:after {
  transform: scale(1.1);
  box-shadow: 0 0 0 4px blue;
} */
</style>