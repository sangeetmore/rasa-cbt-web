<template>
  <div id="features" color="#272822">
    <h1 class="section-title"><span class="primary-color">Features</span></h1>
    <br />

    <div class="container">
      <div class="card-outer-container ">

        <div :data-aos= 'obj.aos' data-aos-duration="800" class="card feature-card" style="width: 18rem; background-color: rgb(48, 90, 117); color: white" v-for="(obj, key) in cardJSON" :key="key">
          <div class="card-body">
            <i :class="obj.icon"/>
            <br />
            <h5 class="card-title"><em>{{obj.title}}</em></h5>
            <p class="card-text">
              {{obj.description}}
            </p>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
    name: "Features",
    data: () => ({
        cardJSON: [
            {
                aos: "fade-right",
                icon: "fa-3x fa fa-star-of-life mb-4",
                title: "Mental Health Support",
                description: "Our Chatbot understands you, and it's available 24/7, so you can access support whenever you need it, and it's completely confidential, so you can feel comfortable sharing your thoughts and feelings without fear of judgement."
            },
            {
                aos: "zoom-in",
                icon: "fa-3x fa fa-brain mb-4",
                title: "Human-like experience",
                description: "Our chatbot is built with advanced natural language processing capabilities, which means it can understand your concerns and respond in a compassionate and empathetic way."
            },
            {
                aos: "fade-left",
                icon: "fa-3x fa fa-gears mb-4",
                title: "Multiple Platform Integration",
                description: "Our Chatbot is integrated on multiple platforms, so you can access it wherever you want without downloading any app for it. We make sure it is environment flexible as help should be available wherever it is asked from."
            }
        ]
    }),
};
</script>

<style>
#features {
  overflow-x: hidden;
}
@media (max-width: 768px) {
    body{overflow-x: hidden}
}
</style>