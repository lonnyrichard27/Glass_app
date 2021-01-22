<template>
  <div class="container">
    <navbar />
    <div class="row">
      <div class="col-lg-2 col-md-2">
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
      <div class="col-lg-10 col-md-10">  
        <section class= "mt-5">
          <p class="text-muted">Step 4</p>
          <h2 class="">Add Cut-Out</h2>
          <p class="">Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus beatae numquam laudantium non illo odit quos tenetur doloribus laborum voluptatibus totam, aliquam, ipsum cumque quam blanditiis sunt, suscipit nobis praesentium?</p>
        </section>

        <!-- card stack -->
        <section class="container mt-5">
          <div class="row">
            <div class="col-lg-4 col-sm-12 col-md-6">
              <div class="card text-center border-dark">
                <div class="card-body my-5">
                  <img src="https://img.icons8.com/wired/64/000000/idea.png"/>
                  <h5>Branding</h5>
                </div>
              </div>
            </div>
            <div class="col-lg-4 col-sm-12 col-md-6">
              <div class="card text-center border-dark">
                <div class="card-body my-5">
                  <img src="https://img.icons8.com/wired/64/000000/idea.png"/>
                  <h5>Branding</h5>
                </div>
              </div>
            </div>
            <div class="col-lg-4 col-sm-12 col-md-6">
              <div class="card text-center border-dark">
                <div class="card-body my-5">
                  <img src="https://img.icons8.com/wired/64/000000/idea.png"/>
                  <h5>Branding</h5>
                </div>
              </div>
            </div>
          </div>
        </section>
        <!-- card stack ends -->

        <!-- button group -->
        <section class="d-flex mt-5 container">
          <button type="button" class="btn btn-success">Previous</button>
          <button type="button" class="btn btn-success ml-3">Next</button>
        </section>
        <!-- button group ends  -->
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
// import Timeline from '@/components/Timeline.vue'

export default {
  components: { Navbar },

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